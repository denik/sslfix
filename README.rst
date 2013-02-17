This is a fixed version of ssl package (http://pypi.python.org/pypi/ssl).

To install it, do

  pip install sslfix

Note, that the actually package installed is `ssl` and not `sslfix` (it's a drop-in replacement).

The fixes are:

- Remove installing tests system-wide (fixes "permission denied" error when installing into virtualenv).
- Add /usr/lib/i386-linux-gnu and /usr/lib/x86_64-linux-gnu to search path (fixes compilation on ubuntu 12.04).
- Do not use SSLv2_method if not present (fixes ImportError: ssl/_ssl2.so: undefined symbol: SSLv2_method).
