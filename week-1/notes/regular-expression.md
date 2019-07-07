# Reguler Expressions

Regular expressions (regex) is a **formal language** for specifying text strings.

## Disjunction

- Letters inside **square brackets** []

| Pattern      | Matches              |
| :----------- | :------------------- |
| [wW]oodchuck | Woodchuck, woodchuck |

- Letters **range** using **dash** “-”

| Pattern | Matches              | Results                                    |
| ------- | -------------------- | ------------------------------------------ |
| [A-Z]   | An upper case letter | **<u>D</u>**renched Blossoms               |
| [a-z]   | A lower case letter  | **<u>m</u>**y beans were important         |
| [0-9]   | A single digit       | Chapter **<u>1</u>**: Down the Rabbit Hole |

## Negation in Disjunction

| Pattern | Matches                  |
| ------- | ------------------------ |
| [^A-Z]  | Not an upper case letter |
| [^Ss]   | Neither ’S’ nor ’s’      |
| [^e ^]  | neither ‘e’ nor ^        |
| a^b     | The pattern ‘a carat b’  |

## More on Disjunction

- The pip ‘|’ for disjunction act as **or**

| Pattern                    | Matches            |
| -------------------------- | ------------------ |
| groundhog\|woodchuck       | groundhogwoodchuck |
| yours\|mine                | yoursmine          |
| a\|b\|c                    | =[abc]             |
| [gG]roundhog\|[Ww]oodchuck |                    |

## ? * + .

| Pattern | Matches                                  | Examples                                          |
| ------- | ---------------------------------------- | ------------------------------------------------- |
| colou?r | Optional previous char                   | <u>color</u> <u>colour</u>                        |
| oo*h!   | 0 or more of previous char               | <u>oh!</u> <u>ooh!</u> <u>oooh!</u> <u>ooooh!</u> |
| o+h     | 1 or more of previous char               | <u>oh!</u> <u>ooh!</u> <u>oooh!</u> <u>ooooh!</u> |
| baa+    | contain ‘ba’ and char 1 or more ‘a’ char | <u>baa</u> <u>baaa</u> <u>baaaa</u> <u>baaaaa</u> |
| beg.n   | Any character (except new line char)     | <u>begin</u> <u>begun</u> <u>beg1n</u>            |

## Anchors ^ ?

| Pattern    | Matches                               |
| ---------- | ------------------------------------- |
| ^[A-Z]     | Starts with capital letter            |
| ^[^A-Za-z] | Starts with characters except letters |
| \.$        | Ends with ‘.’                         |
| .$         | Ends with any character               |



## Errors

In NLP, most of the time errors occur in two types, which are **False Positives (Type I)** and **False Negative (Type II)**.

- **False Positive** means we match (other action) strings that **should not have matched**
- **False Negative** means we don’t match (other action) strings that **should have matched**

Reducing those error involves:

- Increasing **accuracy/precision** (minimizing FP)
- Increasing **coverage/recall** (minimizing FN)



## So...

- Regex is mostly used as the first tools for any text processing
- But for many hard task, **machine learning classifier** is still preferred
- Regex is used as **features** in the classifiers



