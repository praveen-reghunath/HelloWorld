# looping expressions

### Infinite loop

```
loop { println!("I loop for ever."); }
```

### Break loop

```
loop {
        println!("I live.");
        break;
    }
```

### While loop

```
let mut i = 0;

while i < 10 {
    println!("hello");
    i = i + 1;
}
```

### while let form

```
let mut x = vec![1, 2, 3];

while let Some(y) = x.pop() {
    println!("y = {}", y);
}

while let _ = 5 {
    println!("Irrefutable patterns are always true");
    break;
}
```

### for loop

```
let v = &["apples", "cake", "coffee"];

for text in v {
    println!("I like {}.", text);
}
```

```
let mut sum = 0;
for n in 1..11 {
    sum += n;
}
```

### Loop labels

```
'a: loop {
    'a: loop {
        break 'a;
    }
    print!("outer loop");
    break 'a;
}
```

## break expression

```
'outer: loop {
    while true {
        break 'outer;
    }
}
```

```
let result = 'block: {
    do_thing();
    if condition_not_met() {
        break 'block 1;
    }
    do_next_thing();
    if condition_not_met() {
        break 'block 2;
    }
    do_last_thing();
    3
};
```

## continue expressions

```
let mut sum = 0;

for n in 1..11 {
    sum += n;

    if n == 2 {
        continue;
    }

    if n == 4 {
        continue;
    }
}

println!("{}" , sum);

```
