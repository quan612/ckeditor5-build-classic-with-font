# CKEditor 5 classic editor build with Font feature

Due to issue mentioned in https://github.com/ckeditor/ckeditor5/issues/2072

The build version cannot be imported directly into React project, so the source must be published to git and then we manually install into the React project.

This project is a fork from [CKEditor 5 Classic Editor Build](https://github.com/ckeditor/ckeditor5-build-classic). 

## Added plugins:

+FontFamily from '@ckeditor/ckeditor5-font/src/fontfamily';

+FontSize from '@ckeditor/ckeditor5-font/src/fontsize';

+FontColor from '@ckeditor/ckeditor5-font/src/fontcolor';

+FontBackGroundColor from '@ckeditor/ckeditor5-font/src/fontbackgroundcolor';

## Install:
```bash
npm install --save https://github.com/quan612/ckeditor5-build-classic-with-font
```

## Usage:
```bash
import CKEditor from "@ckeditor/ckeditor5-react";
import ClassicEditor from "@ckeditor5-build-classic-with-font/ckeditor5-build-classic";

<CKEditor
             editor={ClassicEditor}
             data={state.description}
                      
             onInit={editor => {
                // You can store the "editor" and use when it is needed.
                console.log("Editor is ready to use!", editor);
             }}
             onChange={(event, editor) => {
                const data = editor.getData();
                console.log({ event, editor, data });
             }}
/>
```

![CKEditor with Font](https://github.com/quan612/ckeditor5-build-classic-with-font/blob/master/CKEditor.PNG)
