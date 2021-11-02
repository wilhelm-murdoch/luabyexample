---
order: 1000 
icon: code
label: Hello, world!
---

Our first program will print the classic "Hello, world!" message. Here’s the full source code:

```lua
print('Hello, world!')
```

Save this to your local file system and assign `hello-world.lua` as the name. You can execute this program with the following command:

```bash
$ lua hello-world.lua
Hello, world!
```

The `*.lua` file extension isn't really necessary as the interpreter will assume its contents contain valid Lua code.

If you wish to run this program without explicitly-feeding it into the interpreter, you can make it an executable. Here are the updated contents of the program:

```lua
#!/usr/bin/env lua

print('Hello, world!')
```

The shebang at the top of the file tells your operating system to execute this program as Lua by running it through the specified interpreter. Give the file executable permissions and you can run it directly. If you add the executable file's base directory to your OS' `$PATH`, you will be able to execute it anywhere within your file system without the `./` prefix.

```bash
$ chmod a+x hello-world
$ ./hello-world
Hello, world!
```

Running the Lua interpreter in interactive mode allows you to execute arbitrary code in a REPL.

```bash
$ lua
Lua 5.4.3  Copyright (C) 1994-2021 Lua.org, PUC-Rio
> print('Hello, world!')
Hello, world!
```

Finally, you can execute arbitrary cold by pass it directly into the interpreter via the command line:

```bash
$ lua -e "print('Hello, world!')"
Hello, world!
```