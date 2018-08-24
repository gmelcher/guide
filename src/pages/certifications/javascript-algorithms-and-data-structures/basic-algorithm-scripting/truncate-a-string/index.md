---
title: Truncate a String
---
![:triangular_flag_on_post:](https://forum.freecodecamp.com/images/emoji/emoji_one/triangular_flag_on_post.png?v=3 ":triangular_flag_on_post:") Remember to use <a>**`Read-Search-Ask`**</a> if you get stuck. Try to pair program ![:busts_in_silhouette:](https://forum.freecodecamp.com/images/emoji/emoji_one/busts_in_silhouette.png?v=3 ":busts_in_silhouette:") and write your own code ![:pencil:](https://forum.freecodecamp.com/images/emoji/emoji_one/pencil.png?v=3 ":pencil:")

### ![:checkered_flag:](https://forum.freecodecamp.com/images/emoji/emoji_one/checkered_flag.png?v=3 ":checkered_flag:") Problem Explanation:

We need to reduce the length of the string or **truncate** it if it is longer than the maximum length specified and add `...` to the end. If it is not longer than the maximum length specified we return the original string without modification.

#### Relevant Links

*   <a href='https://github.com/FreeCodeCamp/FreeCodeCamp/wiki/JS-String-Prototype-Slice' target='_blank' rel='nofollow'>String.prototype.slice()</a>

## ![:speech_balloon:](https://forum.freecodecamp.com/images/emoji/emoji_one/speech_balloon.png?v=3 ":speech_balloon:") Hint: 1

Strings are immutable in JavaScript so we will need a new variable to store the truncated string.

> _try to solve the problem now_

## ![:speech_balloon:](https://forum.freecodecamp.com/images/emoji/emoji_one/speech_balloon.png?v=3 ":speech_balloon:") Hint: 2

You will need to use the slice() method and specify where to start and where to stop.

> _try to solve the problem now_

## Spoiler Alert!

![warning sign](//discourse-user-assets.s3.amazonaws.com/original/2X/2/2d6c412a50797771301e7ceabd554cef4edcd74d.gif)

**Solution ahead!**

## ![:beginner:](https://forum.freecodecamp.com/images/emoji/emoji_one/beginner.png?v=3 ":beginner:") Basic Code Solution:

    function truncateString(str, num) {
      // Clear out that junk in your trunk
      if (str.length > num) {
        return str.slice(0, num) + '...';
      } else {
        return str;
      }

    }

![:rocket:](https://forum.freecodecamp.com/images/emoji/emoji_one/rocket.png?v=3 ":rocket:") <a href='https://repl.it/CLjU/55' target='_blank' rel='nofollow'>Run Code</a>

### Code Explanation:

*   First we start off with an `if` statement to decide which of two actions to take.
*   If the given string length is greater than the maximum length specified as`num`, we return a slice of our string starting at character 0, and ending at `num`. We then append `...` to the end of the string.
*   If our string length is less than `num`, it does not need truncation or added elipses. Therefore, we can simply return the original string.

## ![:rotating_light:](https://forum.freecodecamp.com/images/emoji/emoji_one/rotating_light.png?v=3 ":rotating_light:") Advanced Code Solution:

    function truncateString(str, num) {
        return ((str.length <= num) ? str : str.slice(0, num) + '...');
    }

![:rocket:](https://forum.freecodecamp.com/images/emoji/emoji_one/rocket.png?v=3 ":rocket:") <a href='https://repl.it/CLjU/54' target='_blank' rel='nofollow'>Run Code</a>

### Code Explanation:

*   Using the ternary operator simplifies the code to a single return and creates a compact yet eminently understandable result.

    condition ? value if true: valueif false 

*   First we use the conditional test to see if the length of the full string passed in as the first argument fits within the size limit passed in as the second argument. 

    (str.length <= num)
    
*   If the condition is true we return the string passed in `str` as the `value if true`. 

*   If the condition is false, we move to the `value if false`, where we will return a "slice" of the string. The slice method extracts a section of a string and returns a new string. We pass 0 to start our slice at the beginning of the string and `num` as the endpoint.  Finally, the `...` is appended to complete the requirement for truncated strings.

    str.slice(0, num) + '...';
     

#### Relevant Links

*   <a href='https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Conditional_Operator' target='_blank' rel='nofollow'>Conditional (ternary) Operator</a>
*   <a href='https://github.com/FreeCodeCamp/FreeCodeCamp/wiki/JS-String-Prototype-Slice' target='_blank' rel='nofollow'>String.prototype.slice()</a>

## ![:clipboard:](https://forum.freecodecamp.com/images/emoji/emoji_one/clipboard.png?v=3 ":clipboard:") NOTES FOR CONTRIBUTIONS:

*   ![:warning:](https://forum.freecodecamp.com/images/emoji/emoji_one/warning.png?v=3 ":warning:") **DO NOT** add solutions that are similar to any existing solutions. If you think it is **_similar but better_**, then try to merge (or replace) the existing similar solution.
*   Add an explanation of your solution.
*   Categorize the solution in one of the following categories — **Basic**, **Intermediate** and **Advanced**. ![:traffic_light:](https://forum.freecodecamp.com/images/emoji/emoji_one/traffic_light.png?v=3 ":traffic_light:")
*   Please add your username only if you have added any **relevant main contents**. (![:warning:](https://forum.freecodecamp.com/images/emoji/emoji_one/warning.png?v=3 ":warning:") **_DO NOT_** _remove any existing usernames_)

> See ![:point_right:](https://forum.freecodecamp.com/images/emoji/emoji_one/point_right.png?v=3 ":point_right:") <a href='http://forum.freecodecamp.com/t/algorithm-article-template/14272' target='_blank' rel='nofollow'>**`Wiki Challenge Solution Template`**</a> for reference.
