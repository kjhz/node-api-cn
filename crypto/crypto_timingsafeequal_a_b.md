<!-- YAML
added: v6.6.0
-->
- `a` {Buffer | TypedArray | DataView}
- `b` {Buffer | TypedArray | DataView}
- Returns: {boolean}

This function is based on a constant-time algorithm.
Returns true if `a` is equal to `b`, without leaking timing information that
would allow an attacker to guess one of the values. This is suitable for
comparing HMAC digests or secret values like authentication cookies or


`a` and `b` must both be `Buffer`s, `TypedArray`s, or `DataView`s, and they
must have the same length.

Use of `crypto.timingSafeEqual` does not guarantee that the *surrounding* code
is timing-safe. Care should be taken to ensure that the surrounding code does
not introduce timing vulnerabilities.

