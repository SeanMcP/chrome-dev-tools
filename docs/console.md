# Console

## Commands
- `clear()` or `Command + K` - Clears console
- `copy(myData)` - Copies data to clipboard
- `Shift + Enter` - New line

## Multi-line blocks

The console will try to detect when you want to write multi-line code blocks, but it is prone to mistakes. To avoid interpretive mistakes, use the `Shift + Enter` command to manually create a new line or use braces to scope your block:

```js
{
  let greeting = 'Hello there!';
  console.log(greeting);
}
```

When starting a block with an open brace, the console will let you use return as expected until the block is closed.

## Assert

Throws a red error block in console if first argument evaluates **false**.

```js
function greaterThan(a, b) {
    console.assert(a > b, {
        'message': `${a} is not greater than ${b}`
    });
}
greaterThan(5, 6);
```

Asserts are useful if there is certain information that you expect to be true.

## History

`$_` accesses the previous value in the console.

## Group

You can group similar logs into a HTML `<details>`-like panel using `console.group`: 

```js
function nameGroup(obj) {
    console.group('Name');
    console.log('first:', obj.first);
    console.log('last:', obj.last);
    console.groupEnd();
}
nameGroup({ first: 'Sean', last: 'McPherson' });
```

This groups can be nested within one another.

## Logs

- `console.log` - Standard log
- `console.info` - Previously displayed an info icon; now functions like log
- `console.warn` - Yellow banner with warning icon
- `console.error` - Red banner with error icon
- `console.trace` - Logs the call stack

### Change style

You can change the style of a log by tagging it with `%c` and providing a CSS-string argument:

```
console.log('%cBig, blue, and highlighted', 'color: blue; font-size: 5rem; background: yellow')
```

Add multiple `%c`s and CSS arguments:

```
console.log('%cBig, %cblue, and %chighlighted', 'font-weight: bold', 'color: blue', 'background: yellow');
```

The console is your oyster.

## Time

1. `console.time('total')` - Initiates a time measurement
2. `// Execute some time-consuming code`
3. `console.timeEnd('total')` - Ends time measurement

Logs the amount of time it takes to run a block of code in milliseconds.

## Dollar shortcuts

On sites that **do not use jQuery**, you can use `$` to perform some quick functions:

- `$` - `document.querySelector`
- `$$` - `document.querySelectorAll`
- `$_` - Previously returned value
- `$0` - Selects currently inspected element
- `$1`-`$3` - Selects previously inspected element
