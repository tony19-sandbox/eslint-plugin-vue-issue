# eslint-plugin-vue-issue

> Demonstrates a linter bug using `vue/script-indent`

## Steps to reproduce

 1. Generate a Vue CLI project with `vue create`, and pick the default setup at the prompt.

 2. In `package.json > eslintConfig > rules`, add the following rule to ignore nested arrays/objects, excluding top level from the exported object in `.vue`:

        "vue/script-indent": [
          "error",
          2,
          {
            "ignores": [
              "[value.type='ObjectExpression']:not(:matches(ExportDefaultDeclaration, [left.property.name='exports']) > * > [value.type='ObjectExpression'])",
              "[value.type='ArrayExpression']"
            ]
          }
        ]

 2. In `App.vue`, add the following unindented code:

        methods: {
        foo() {
        const x = {
        a: [],
        b: 1,
        c: {},
        d: 2
        }
        console.log(x)
        }
        }

 3. Run the linter with `npm run lint` or `yarn lint`.

 4. Observe the method we added in `App.vue` is now:

          methods: {
            foo() {
              const x = {
        a: [],
        b: 1,             // <-- FIXME: should be indented
        c: {},
        d: 2              // <-- FIXME: should be indented
              }
              console.log(x)
            }
          }
