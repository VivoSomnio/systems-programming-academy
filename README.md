# Systems Programming Academy

Welcome! The Systems Programming Academy (SPA) teaches you to build real
systems software, one small runnable program at a time. Each lesson teaches one
idea and shows it in six languages side by side: C, C++, C#, Go, Python and
TypeScript. Optional EXTENDED companion lessons show the same idea in Assembly
(Windows and Linux), Rust, Erlang and Solidity.

Volume 1, *Foundations of Systems Programming*, starts with setting up your
tools and the language basics, then moves through files, databases, CRUD
applications, REST APIs, networking and web applications. Everything builds
toward one small but complete platform: a notes application with file import
and export, MySQL storage, search, a REST API, a simple web page, validation,
error handling, logging and a Git history.

## Get the lessons

You do **not** need a GitHub account to read this page or to download the
lessons. Anyone can view and download this repository. You will create a GitHub
account later in the course, when you publish your own work.

There are two ways to get the lessons. Way 1, Git, is recommended; Way 2 needs no tools.

### Way 1: Git (recommended; one command gets every update)

Git copies the whole repository to your computer and can fetch new and
corrected lessons later with one command. Lesson 1.9 teaches Git properly; the
steps below are all you need for now.

**Step 1: install Git (once).** Open **PowerShell** (press the Windows key, type
`PowerShell`, and press Enter) and run:

```
winget install --id Git.Git --exact --source winget
```

The first time you use winget, it may ask whether you agree to the source
agreements terms. Type `Y` and press Enter. If PowerShell says `winget` is not
recognized, open the **Microsoft Store**, search for **App Installer**, click
**Get** or **Update**, then close PowerShell, open a new one, and run the
command again.

Or, if you prefer: download the 64-bit "Git for Windows" installer from
https://git-scm.com/install/windows and run it. Keep the default answer on
every page.

When the install finishes, **close PowerShell and open a new one**, so it can
find the `git` command. Check that it works:

```
git --version
```

It prints a version such as `git version 2.55.0.windows.1`. Any version from
2.55 on is fine.

**Step 2: choose where the lessons go.** A new PowerShell (or Git Bash) window
starts in your home folder, `C:\Users\<your name>`, which both call `~`. To keep
the lessons in your Documents folder instead, run this (it works the same in
PowerShell and Git Bash):

```
cd ~/Documents
pwd
```

`pwd` prints the folder you are in. It should end in `Documents`. If it does
not, the clone in the next step lands somewhere else.

**Step 3: copy the lessons to your computer.** Run:

```
git clone https://github.com/VivoSomnio/systems-programming-academy.git
```

Git creates a folder named `systems-programming-academy` inside the folder you
were in. With the commands above, that is
`C:\Users\<your name>\Documents\systems-programming-academy`. No account or
password is needed.

**Step 4: open the folder.** Run (Git Bash or PowerShell):

```
cd systems-programming-academy
explorer .
```

File Explorer opens the folder. Open `Volume 1` and then a chapter.

**Getting updates later.** Open PowerShell or Git Bash, go back into the folder, and run
`git pull`:

```
cd ~/Documents/systems-programming-academy
git pull
```

It downloads every new and corrected lesson.

**Keep your own work somewhere else.** Do not save files or type your programs
inside `systems-programming-academy`. Treat it as a read-only library. If you
change files there, `git pull` may refuse to update them. The course keeps your
own programs in a separate folder, `C:\Users\<your name>\spa`, which Chapter 1 creates and
Lesson 1.9 turns into your own Git repository.

### Way 2: download a zip (quickest, no tools needed)

1. Open the **Releases** page:
   https://github.com/VivoSomnio/systems-programming-academy/releases
2. Under the newest release, click the `.zip` file (for example
   `SPA_Volume1_Chapter1.zip`) to download it. Your browser saves it to your
   **Downloads** folder.
3. Open File Explorer, go to **Downloads**, right-click the zip, and choose
   **Extract All...**. Pick a folder you will find again, for example your
   **Documents** folder, and click **Extract**.
4. Open the new folder, then `Volume 1`, then the chapter you want.

When a new release appears with more chapters, download its zip the same way.
The new zip holds every published lesson, so it replaces the old one.

## Open the lessons

The lessons are Word documents (`.docx`). Open them with any of these:

- **Microsoft Word**, if you have it.
- **LibreOffice Writer**, free, from https://www.libreoffice.org.
- **Word for the web**, free with a Microsoft account, at https://www.office.com.

## Where to start

Start with **Chapter 01 - Development Environment**, Lesson 1.1, and work in
order. Each lesson assumes the ones before it, and Chapter 1 installs every tool
the rest of the course uses.

## Folder layout

```
Volume 1/
  Chapter 01 - Development Environment/
  Chapter 02 - Language Fundamentals/
  ...
```

Each chapter folder holds its lesson documents (`.docx`, opens in Microsoft Word
or LibreOffice). File names keep the lesson number, so they sort in order, for
example `SPA_Vol1_Ch5_Lesson5_1_Create_Records.docx`. A name with an `a` after
the number, or `EXTENDED` in it, is the optional companion lesson. Project
documents close each chapter.

## Published chapters

<!-- published-chapters:begin -->
- `Volume 1/Chapter 01 - Development Environment` (14 lessons)
- `Volume 1/Chapter 02 - Language Fundamentals` (34 lessons, 4 projects)
- `Volume 1/Chapter 03 - File Handling` (38 lessons, 4 projects)
- `Volume 1/Chapter 04 - Databases` (30 lessons, 2 projects)
<!-- published-chapters:end -->

## Type the code, never copy it

There is no code folder here, on purpose. Every program is printed in full in
its lesson. Type it yourself, line by line. Typing is how your hands and eyes
learn the syntax, and the mistakes you make and fix while typing teach as much
as the lesson does. Each lesson shows the exact output to expect, so you can
check your work.

## Tools you need

Chapter 1 walks you through installing and checking each one:

- **C and C++:** GCC (`gcc` and `g++`), from MSYS2 UCRT64 on Windows
- **C#:** the .NET SDK
- **Go:** the Go toolchain
- **Python:** Python 3
- **TypeScript:** Node.js and the TypeScript compiler (`tsc`)
- **Git**, for getting updates and, later, for your own projects

Lesson 4.0 adds MySQL Server with the `mysql` command-line client, and each
language's MySQL connector, installed inside the lesson project. On Windows the
C++ connector also needs the Visual Studio Build Tools (Lesson 4.0 explains why).

The EXTENDED lessons use NASM (with WSL Ubuntu for Linux Assembly), Rust,
Erlang/OTP, and the Solidity compiler with Foundry. They are optional.

## Windows first

Every lesson's Windows commands have been run and checked. Linux and macOS
command blocks are printed in the lessons too, but they have not been verified
yet. If one does not work for you, the Windows steps show what it is meant to do.

## Your own secrets

Nothing secret ships in this repository. When a lesson needs a database
password, a certificate or an API key, it shows you how to create your own and
keep it out of your source code (for example in an environment variable such as
`SPA_DB_PASSWORD`). Never commit your secrets to Git.

## License

The lessons are licensed under CC BY-NC-SA 4.0 (see `LICENSE`). The code
printed in the lessons is also available under the MIT License (see
`LICENSE-CODE`), so you may use what you type in your own work.

Copyright (c) 2026 Scott Jarboe.
