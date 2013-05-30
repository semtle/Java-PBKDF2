# Java-PBKDF2

Small and free (as in LGPL) Java implementation of [RFC 2898](http://www.faqs.org/rfcs/rfc2898.html) / PKCS#5 by Matthias Gärtner. 

I am not the original author of this library. I'm merely making this repository for my and others convenience.

## Dependencies
None

## Importing into Eclipse
1. git clone https://github.com/NakedFerret/Java-PBKDF2.git
2. File -> Import... -> General -> Existing Projects into Workspace

## Building with Ant
Ant build script is not included. If you would like it [open an issue](https://github.com/NakedFerret/Java-PBKDF2/issues/new).

## How to use
Encrypt the password Using PBKDF2 into binary:

    PBKDF2Parameters p = new PBKDF2Parameters( "HmacSHA1", "UTF-8", "salt".getBytes(), iterations );
    PBKDF2Engine e = new PBKDF2Engine(p);
    e.deriveKey( "password", 20 );

Display the password as hex:

    BinTools.bin2hex( e.deriveKey( "password", 20 )

## Where to send praise
I'm not sure...

Here's the [original page](http://www.rtner.de/software/PBKDF2.html) for the library

## License

[LGPL](http://www.gnu.org/licenses/old-licenses/lgpl-2.1.html)
