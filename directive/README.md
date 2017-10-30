 The interpolation is controlled by specifiers inspired by printf which have a number of formats:

- `%%	insert a %`
- `%p	insert the port number of the virtual host`
- `%N.M	insert (part of) the name`


N and M are used to specify substrings of the name. 
N selects from the dot-separated components of the name, and M selects characters within whatever N has selected. 
M is optional and defaults to zero if it isn't present; the dot must be present if and only if M is present. The interpretation is as follows:

- `0	the whole name`
- `1	the first part`
- `2	the second part`
- `1	the last part`
- `-2	the penultimate part`
- `2+	the second and all subsequent parts`
- `-2+	the penultimate and all preceding parts`
- `1+ and -1+	the same as 0`

