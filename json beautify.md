1.  安装包 "ang-jsoneditor": "^1.10.5",
2.  引入文件 import { NgJsonEditorModule } from 'ang-jsoneditor' 
3.  使用组件  <json-editor #editor style="height:100%" [options]="editorOptions" [(data)]="responseData" (change)="getData($event)"></json-editor>
4.  配置 options  

5.  ```
6.  this.editorOptions = new JsonEditorOptions();
    //set only one mode
    this.editorOptions.mode = 'text';
    ```

7. 获取数据 this.editor.get();
8. 组件
      @ViewChild(JsonEditorComponent, { static: false })
        editor: JsonEditorComponent;