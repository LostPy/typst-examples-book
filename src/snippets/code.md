# Code formatting

## Inline highlighting

```typ
#let r = raw.with(lang: "r")

This can then be used like: #r("x <- c(10, 42)")
```

## Tab size

```````typ
#set raw(tab-size: 8)
```tsv
Year	Month	Day
2000	2	3
2001	2	1
2002	3	10
```
```````

## Theme

See [reference](https://typst.app/docs/reference/text/raw/#parameters-theme)

## Enable ligatures for code

```typ
#show raw: set text(ligatures: true, font: "Cascadia Code")

Then the code becomes `x <- a`
```

## Customize background

To write code in customisable block, use a show rule:


``````typ
#show raw.where(block: true): it => block(
  radius: 1em,
  fill: luma(240),
  stroke: 1pt,
  width: 100%,
  inset: 1em,
  it
)

```rust
fn main() {
  println!("Hello World!");
}
```
``````

## Advanced formatting

See [packages](../packages/code.md) section.
