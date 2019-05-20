# unicode-decode
Convert unicode text (binary) to \uHHHH or \UHHHHHHHH style escape sequence

## usage
```bash
$ cat thinking_face.txt
thinking_face = 考え中🤔
$ udecode thinking_face.txt
thinking_face = \u8003\u3048\u4e2d\U0001f914
```

Output is compatible with bash `echo` format.

```bash
$ echo -e $(udecode thinking_face.txt)
thinking_face = 考え中🤔
```

## Requirements
- Bash 4.x or later (not tested)

## References
- RFC3629
