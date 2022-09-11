# Digests in raku

This is a [raku](https://raku.org/) module implementing some digest algorithms
in pure raku (no parrot or nqp:: code).

The `Digest` module also exports a subroutine `blob-to-hex` to turn a blob into
a hexadecimal string representation.

## Synopsis

    use Digest::SHA;
    say sha1     "hello";
    say sha256   "Привет"; 
    say sha3_256 "bonjour";
    
    use Digest::RIPEMD;
    say rmd160 "bye";

## Features

Currently implemented:

* Digest
  - md5
  - blob-to-hex
* Digest::SHA :
  - sha1
  - sha256
  - sha512
  - SHA-3 (direct translation from [this python implementation](https://github.com/XKCP/XKCP/blob/master/Standalone/CompactFIPS202/Python/CompactFIPS202.py))
* Digest::RIPEMD :
  - rmd160

## Disclaimer

PERFORMANCE WARNING: currently, execution is much slower than with most other programming languages.

## License

This work is published under the terms of the artistic license, as rakudo is.
See LICENSE file.

