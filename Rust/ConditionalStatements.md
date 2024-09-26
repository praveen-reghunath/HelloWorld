# if else
Sample
```
if n > 0 { print!("Positive"); }
```

- The condition must be of boolean type. ( ie ``if 4 { print!("four"); }`` will not work )
- It is not required to enclose the condition in brackets.
- After the condition a block is required.


```
let n = 0;

if n > 0 {
  print!("Positive");
}
else if n == 0 {
  print!("zero");
}
else {
  print!("Negative");
}
```
