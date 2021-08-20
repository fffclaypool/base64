## Base64
### Conversion Algorithm

1. Define the string to be converted.

```
abcde
```

2. Converts to binary numbers based on the ASCII code table

```
01100001 01100010 01100011 01100100 01100101
```

<img width="766" alt="スクリーンショット 2021-08-20 22 39 34" src="https://user-images.githubusercontent.com/43327056/130242177-2aea773c-44de-418a-b22e-6815a5c27696.png">

3. Divide it into 6 bits each

```
011000 010110 001001 100011 011001 000110 0101
```

4. Add 0 so that the last group is 6 bits

```
011000 010110 001001 100011 011001 000110 010100
```

5. Convert to characters based on the base64 conversion table

```
Y W J j Z G U
```

<img width="469" alt="スクリーンショット 2021-08-20 22 40 10" src="https://user-images.githubusercontent.com/43327056/130242201-09a6edf7-291e-4116-a194-f89b2c321d50.png">

6. Combine them into four letters each

```
YWJj ZGU
```

7. If the last group is less than 4 characters, add `=` for the number of them

```
YWJj ZGU=
```

8. Concatenating the groups into a single string completes the base64 string

```
YWJjZGU=
```
