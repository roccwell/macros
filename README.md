# macrosr

## 实现：一个简单的声明宏并理解其代码结构，和编译过程。

## 创建一个声明宏，名为 greet，并在 main 函数中使用它。

```rust
// 定义一个名为 'greet' 的声明宏
macro_rules! greet {
    ($name:expr) => {
        println!("Hello, {}.", $name);
    };
}

fn main() {
    // 将展开为 println!("Hello, Rust.);
    greet!("Rust");
}

```

> 编译时，编译器遇到 `greet("Rust")` 宏调用，它会应用宏展开规则，匹配宏定义中的模式，并生成相应的代码。
