### 類型說明

```ts
/* Boolean */
let isDone: boolean = false;
```

```ts
/* Number 所有數字都是浮點數 */
let decLiteral: number = 6;
let hexLiteral: number = 0xf00d;
let binaryLiteral: number = 0b1010;
let octalLiteral: number = 0o744;
```

```ts
/* String */
let name: string = 'simen';
```

```ts
/* Array */
let list: number[] = [1 , 2 , 3];
// Array 泛型
let list: Array<number> = [1 , 2 , 3];
```

```ts
/* Tuple */
let x: [string , number];

x = ['hello' , 10]; //Ok
x = [10 , 'hello']; //Error
```

```ts
/* Enum : 此類為對javascript的補充 (從0開始) */
enum Color {Red=1, Green, Blue}
let c: Color = Color.Green;
```

```ts
/* Any 動態內容 不希望編譯 */
let notSure: any = 4;
notSure = true;
notSure = "something";
```

```ts
/* Void */
function test(): void {
    console.log('This function do not return anything');
}
```

```ts
/* Object */
declare function create(o: object | null):void;

create({ prop: 0 }); // Ok
create(null); // Ok

create('something') // Error
create(true) // Error
```

```ts
/* 自訂義類型 不編譯 */
let someValue: any = "this is a string";

let strLength: number = (<string>someValue).length;
```
```ts
/* 自訂義類型 不編譯 語法 */
let someValue: any = "this is a string";

let strLength: number = (someValue as string).length;

```