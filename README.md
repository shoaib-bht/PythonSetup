# Assignment A2: Setup Python &nbsp; (10 Pts)

## 1.) Challenge: Terminal

### Command Results:
Find the command results of this task:
```sh
> cd                    # change to HOME-directory
> pwd                   # print path to working directory
> ls -la                # show content of HOME-directory
> whoami                # show user identity
> cat .profile              # file may not exist
> cat .bashrc               # for Mac, use .zshrc
> echo $PATH            # show PATH variable
```

in this file [1. Challenge - Terminal](./1.%20Challenge%20-%20Terminal.txt)


### Differences between `.profile` and `.bashrc` (macOS: `.zshrc`)

1. **Purpose**  
   `.profile` is sourced by *login shells* and runs once when you start a session (for example, when logging in via Terminal or SSH).  
   `.bashrc` or `.zshrc` is used by *interactive non-login shells* and runs every time a new terminal tab or window opens.

2. **When `.profile` runs**  
   It’s executed only once at login and is typically used to set environment variables such as `PATH`, `JAVA_HOME`, or other session-level settings.  
   On macOS with Zsh, the equivalent file is `~/.zprofile`.

3. **When `.bashrc` (or `.zshrc`) runs**  
   It’s executed for each new interactive shell session and is mainly used for things like aliases, shell prompts, and custom functions.

4. **Typical usage**  
   `.profile` handles environment setup for the session, while `.bashrc` or `.zshrc` manages interactive preferences.  
   Many users source `.bashrc` or `.zshrc` inside `.profile` to ensure a consistent environment across all shells.

## 2.) Challenge: Python3

```sh
shoaibkhan@Shoaibs-MacBook-Air ~ % python3 --version
Python 3.14.0
```

## 3.) Challenge: pip

```sh
shoaibkhan@Shoaibs-MacBook-Air ~ % pip3 --version
pip 25.2 from /opt/homebrew/lib/python3.14/site-packages/pip (python 3.14)
```

## 4.) Challenge: Test Python

Start Python in the terminal and execute commands:

```sh
shoaibkhan@Shoaibs-MacBook-Air ~ % python3
Python 3.14.0 (main, Oct  7 2025, 09:34:52) [Clang 17.0.0 (clang-1700.0.13.3)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> print('Hello World')
Hello World
>>> help('modules')

Please wait a moment while I gather a list of all available modules...

test_sqlite3: testing with SQLite version 3.50.4
__future__          _sre                enum                readline
__hello__           _ssl                errno               reprlib
__phello__          _stat               faulthandler        resource
_abc                _statistics         fcntl               rlcompleter
_aix_support        _string             filecmp             runpy
_android_support    _strptime           fileinput           sched
_apple_support      _struct             fnmatch             secrets
_ast                _suggestions        fractions           select
_ast_unparse        _symtable           ftplib              selectors
_asyncio            _sysconfig          functools           shelve
_bisect             _sysconfigdata__darwin_darwin gc                  shlex
_blake2             _testbuffer         genericpath         shutil
_bz2                _testcapi           getopt              signal
_codecs             _testclinic         getpass             site
_codecs_cn          _testclinic_limited gettext             sitecustomize
_codecs_hk          _testimportmultiple glob                smtplib
_codecs_iso2022     _testinternalcapi   graphlib            socket
_codecs_jp          _testlimitedcapi    grp                 socketserver
_codecs_kr          _testmultiphase     gzip                sqlite3
_codecs_tw          _testsinglephase    hashlib             sre_compile
_collections        _thread             heapq               sre_constants
_collections_abc    _threading_local    hmac                sre_parse
_colorize           _tokenize           html                ssl
_compat_pickle      _tracemalloc        http                stat
_contextvars        _types              idlelib             statistics
_csv                _typing             imaplib             string
_ctypes             _uuid               importlib           stringprep
_ctypes_test        _warnings           inspect             struct
_curses             _weakref            io                  subprocess
_curses_panel       _weakrefset         ipaddress           symtable
_datetime           _xxtestfuzz         itertools           sys
_dbm                _zoneinfo           json                sysconfig
_decimal            _zstd               keyword             syslog
_elementtree        abc                 linecache           tabnanny
_functools          annotationlib       locale              tarfile
_hashlib            antigravity         logging             tempfile
_heapq              argparse            lzma                termios
_hmac               array               mailbox             test
_imp                ast                 marshal             textwrap
_interpchannels     asyncio             math                this
_interpqueues       atexit              mimetypes           threading
_interpreters       base64              mmap                time
_io                 bdb                 modulefinder        timeit
_ios_support        binascii            multiprocessing     tkinter
_json               bisect              netrc               token
_locale             builtins            ntpath              tokenize
_lsprof             bz2                 nturl2path          tomllib
_lzma               cProfile            numbers             trace
_markupbase         calendar            opcode              traceback
_md5                cmath               operator            tracemalloc
_multibytecodec     cmd                 optparse            tty
_multiprocessing    code                os                  turtle
_opcode             codecs              pathlib             turtledemo
_opcode_metadata    codeop              pdb                 types
_operator           collections         pickle              typing
_osx_support        colorsys            pickletools         unicodedata
_pickle             compileall          pip                 unittest
_posixshmem         compression         pkgutil             urllib
_posixsubprocess    concurrent          platform            uuid
_py_abc             configparser        plistlib            venv
_py_warnings        contextlib          poplib              warnings
_pydatetime         contextvars         posix               wave
_pydecimal          copy                posixpath           weakref
_pyio               copyreg             pprint              webbrowser
_pylong             csv                 profile             wheel
_pyrepl             ctypes              pstats              wsgiref
_queue              curses              pty                 xml
_random             dataclasses         pwd                 xmlrpc
_remote_debugging   datetime            py_compile          xxlimited
_scproxy            dbm                 pyclbr              xxlimited_35
_sha1               decimal             pydoc               xxsubtype
_sha2               difflib             pydoc_data          zipapp
_sha3               dis                 pyexpat             zipfile
_signal             doctest             queue               zipimport
_sitebuiltins       email               quopri              zlib
_socket             encodings           random              zoneinfo
_sqlite3            ensurepip           re                  

Enter any module name to get more help.  Or, type "modules spam" to search
for modules whose name or summary contain the string "spam".

>>> 2+3*4
14
>>> x = 2+3*4
>>> x
14
```

Running the file [print_sys.py](./print_sys.py):

```sh
shoaibkhan@Shoaibs-MacBook-Air SetupPython % ls 
1. Challenge - Terminal.txt    print_sys.py
shoaibkhan@Shoaibs-MacBook-Air SetupPython % python3 print_sys.py       
Python impl:    CPython
Python version: Darwin Kernel Version 24.6.0: Mon Jul 14 11:30:51 PDT 2025; root:xnu-11417.140.69~1/RELEASE_ARM64_T8112
Python machine: arm64
Python system:  Darwin
Python version: 3.14.0
```


