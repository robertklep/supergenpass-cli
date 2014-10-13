## supergenpass-cli

This is a simple CLI script that wraps [supergenpass-lib](https://github.com/chriszarate/supergenpass-lib) to facilitate generating unique per-domain passwords.

### Usage:

```
$ supergenpass -h

Usage: supergenpass <uri> [options]

uri     URI to generate a password for.

Options:
   -s SECRET, --secret SECRET                A secret password to be appended to the master password before generating the password.  []
   -l LENGTH, --length LENGTH                Length of the generated password. Valid lengths are integers between 4 and 24 inclusive.  [20]
   -m, --md5                                 Use MD5 method instead of SHA512.  [false]
   -r, --remove-subdomains                   Remove subdomains from the hostname before generating the password?  [true]
   -m PASSWORD, --master-password PASSWORD   Master password to use. BE CAREFUL WITH THIS OPTION!
   -v, --verify                              Verify master password (only when prompted).  [true]

If no master password is provided with -m/--master-password
or $SGP_MASTER_PASSWORD, you will be prompted for one.

The -s/--secret option could be used to encode a username into
the generated password, so you can register multiple usernames
with one website and get a unique password for each.
```

