#TextInput Single Line Input & Multi Line Input

TextInput is a UI component that is often used in games. TextInput is used whenever input is needed. Let's first look at the API of TextInput.

All API parameters in laya.ui.textInput:

![1](img/1.png)</br>

Here we set up one-line input and multi-line input of text. One-line input can only be entered in one line, and multi-line input can be entered in the next line if the previous line is not full by return.


```typescript

module laya {
    import Input = Laya.Input;
    import Stage = Laya.Stage;
    import Browser = Laya.Browser;
    import WebGL = Laya.WebGL;
    export class HelloLayabox {
 
      constructor() {
            // 不支持WebGL时自动切换至Canvas
            Laya.init(Browser.clientWidth, Browser.clientHeight, WebGL);
 
            Laya.stage.alignV = Stage.ALIGN_MIDDLE;
            Laya.stage.alignH = Stage.ALIGN_CENTER;

            Laya.stage.scaleMode = "showall";
            Laya.stage.bgColor = "#232628";

            this.createSingleInput();
            this.createMultiInput();
        }

       private createSingleInput(): void {
            var inputText: Input = new Input();

            inputText.size(350, 100);
            inputText.x = Laya.stage.width - inputText.width >> 1;
            inputText.y = (Laya.stage.height - inputText.height >> 1) - 100;

            // 移动端输入提示符
            inputText.prompt = "Type some word...";
 
            // 设置字体样式
            inputText.bold = true;
            inputText.bgColor = "#666666";
            inputText.color = "#ffffff";
            inputText.fontSize = 20;
            Laya.stage.addChild(inputText);
        }
        private createMultiInput(): void {
            var inputText: Input = new Input();

            // 移动端输入提示符
            inputText.prompt = "Type some word...";
            //多行输入
            inputText.multiline = true;
            inputText.wordWrap = true;

            inputText.size(350, 100);
            inputText.x = Laya.stage.width - inputText.width >> 1;
            inputText.y = (Laya.stage.height - inputText.height >> 1) +100;
            inputText.padding = [2, 2, 2, 2];

            inputText.bgColor = "#666666";
            inputText.color = "#ffffff";
            inputText.fontSize = 20;

            Laya.stage.addChild(inputText);
        }
    }
}
new laya.HelloLayabox();
```


Operation results:

![2](img/2.png)</br>

