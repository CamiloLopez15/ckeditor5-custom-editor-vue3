# CKEditor Vue 3 complete custom build

This is a project which uses a custom build of CKEditor, this build has the vast majority of free plugins already installed and the toolbar already organized, it was created with the intention that you only install the package and pass it as an editor to the CKEditor package.

This editor uses the Spanish Colombia language by default, if you want to use another language, you would just have to create a [new custom build](https://ckeditor.com/docs/ckeditor5/latest/installation/getting-started/quick-start-other.html), upload it to npm (there are other options to use CKEditor locally) and instead of installing this package you install yours, they are practically the same steps, it's really easy!!!

## Sources

-   [CKEditor](https://ckeditor.com)
-   [CKEditor Vue 3](https://ckeditor.com/docs/ckeditor5/latest/installation/integrations/vuejs-v3.html)

## Deployment

To be able to run the project it is the same as if you were using a normal editor or the default CKEditor.

Follow the next steps:

-   Install the following dependencies
    ```bash
    npm install --save @ckeditor/ckeditor5-vue
    ```
-   Go to your main.js or main.ts file and add the following line, this is to instantiate the component so you can use the component globally.

    ```js
    import CKEditor from "@ckeditor/ckeditor5-vue";
    ```

    ```js
    Vue.createApp({
        /* options */
    })
        .use(CKEditor)
        .mount(/* DOM element */);
    ```

    [But if you want to do it only in a single component, you can follow CKEditor's guide.](https://ckeditor.com/docs/ckeditor5/latest/installation/integrations/vuejs-v3.html#using-the-component-locally)

-   Install the CKEditor Vue 3 complete custom build package or yours.
    ```bash
    npm i @camilo__lp/custom-editor-vue3
    ```
-   Go to the component where you want to use the custom editor and do the following:
    ```html
    <script setup>
        import { ref } from "vue";
        import { Editor } from "@camilo__lp/custom-editor-vue3"; // Or yours
        const editorSettings = {
            //settings
        };
        const body = ref("");
    </script>
    <template>
        <ckeditor :editor="Editor" v-model="body" :config="editorSettings">
        </ckeditor>
    </template>
    ```
-   Enjoy your editor

## Support

-   This editor is using version 41.3.1 in dependencies and in the editor itself
-   This editor uses the Spanish Colombia language by default
