[update-readmes]   Mode: rewrite — migrating to template structure...
# jardiff

[![Built with Ona](https://ona.com/build-with-ona.svg)](https://app.ona.com/#https://github.com/Interested-Deving-1896/jardiff)

<!-- AI:start:what-it-does -->
_Description pending._
<!-- AI:end:what-it-does -->

## Architecture

<!-- AI:start:architecture -->
_Architecture documentation pending._
<!-- AI:end:architecture -->

## Install

<!-- Add installation instructions here. This section is yours — the AI will not modify it. -->

```bash
git clone https://github.com/Interested-Deving-1896/jardiff.git
cd jardiff
```

## Usage


> [!CAUTION] 
> This tool needs a JDK11 to build and run. Example with `mise`
> ```shell
> $ mise exec java@corretto-11 -- java -jar jardiff-0.1.0-SNAPSHOT.jar
> ```

> [!TIP]
> The jar on the Github release is an executable jar, so you can run it directly with `./jardiff-0.1.0-SNAPSHOT.jar {left} {right}` after downloading it (`chmod`ing it executable as needed).

Build it `./gradlew build`, then run it:

```shell
$ jardiff --help
Usage: jardiff [-hVv] [--exit-code] [--class-text-producer=<tool>]
               [--color=<when>] [-c=<extension>[,<extension>...]]... [-e=<glob>
               [,<glob>...]]... [-i=<glob>[,<glob>...]]... [--status | --stat]
               <left> <right>
Compares two JAR files or directories and reports differences.
      <left>           The JAR file or directory to compare.
      <right>          The JAR file or directory to compare.
  -c, --class-exts, --coalesce-classe-exts=<extension>[,<extension>...]
                       Coalesce class files with the given extensions, in
                       addition to the usual 'class', i.e. makes classes
                       named 'Foo.class' and 'Foo.bin' aliased to the same
                       file same entry. Also this enables the file to be
                       compared on bytecode level Takes a comma separated
                       list, e.g. 'classdata' or 'raw,bin,clazz'.
      --class-text-producer=<tool>
                       Tool used to produce class text, possible values:
                       asm-textifier, class-file-version, class-outline
                       Default: 'asm-textifier'
      --color=<when>   Control when to use color output:
                       always, auto, never
                       Default: 'auto'
  -e, --exclude=<glob>[,<glob>...]
                       Glob exclude patterns (comma separated), e.g.
                       '**/raw*/**', or '**/*.bin'.
      --exit-code      Make jardiff exit with codes similar to diff(1).
                       That is, it exits with 1 if there were differences
                       and 0 means no differences.
  -h, --help           Show this help message and exit.
  -i, --include=<glob>[,<glob>...]
                       Glob include patterns (comma separated), e.g.
                       '**/raw*/**', or '**/*.bin'.
      --stat           Show statistics output (like 'git diff --stat').
                       Displays file-by-file statistics with
                         additions/deletions.
      --status         Show short status output (like 'git status --short').
                       Displays two-column XY status for each file.
  -v                   Specify multiple -v options to increase verbosity.
                       For example, '-v -v' or '-vv'.
  -V, --version        Print version information and exit.
```

> [!TIP]
> Use shell features, e.g. in Bash, ZSH instead of typing twice long folders use the [brace expansion](https://www.gnu.org/software/bash/manual/html_node/Brace-Expansion.html#Brace-Expansion-1) :
> ```shell
> $ java -jar jardiff-0.1.0-SNAPSHOT.jar /Users/brice.dutheil/path/to/repositories/project{-original,-with-changes}/submodule/submodule/submodule/build/classes/java/main
> ```


Also, you can run it from Gradle:

```shell
$ ./gradlew run --args="{left} {right}"
```

- `{left}` and `{right}` can be paths to JAR files or directories.
- The tool outputs a summary and detailed diff of all differing files.

## Configuration

<!-- Document configuration options here. This section is yours — the AI will not modify it. -->

## CI

<!-- AI:start:ci -->
_CI documentation pending._
<!-- AI:end:ci -->

## Mirror chain

<!-- AI:start:mirror-chain -->
This repo is maintained in [`Interested-Deving-1896/jardiff`](https://github.com/Interested-Deving-1896/jardiff) and mirrored through:

```
Interested-Deving-1896/jardiff  ──►  OpenOS-Project-OSP/jardiff  ──►  OpenOS-Project-Ecosystem-OOC/jardiff
```

Changes flow downstream automatically via the hourly mirror chain in
[`fork-sync-all`](https://github.com/Interested-Deving-1896/fork-sync-all).
Direct commits to OSP or OOC are detected and opened as PRs back to `Interested-Deving-1896`.
<!-- AI:end:mirror-chain -->

## Contributors

<!-- AI:start:contributors -->
_Contributors pending._
<!-- AI:end:contributors -->

## Origins

<!-- AI:start:origins -->
_Original project — no upstream fork._
<!-- AI:end:origins -->

## Resources

<!-- AI:start:resources -->
_No additional resource files found._
<!-- AI:end:resources -->

## License

<!-- AI:start:license -->
[MPL-2.0](https://github.com/Interested-Deving-1896/jardiff/blob/main/LICENSE) © 2026 [Interested-Deving-1896](https://github.com/Interested-Deving-1896)
<!-- AI:end:license -->
