PDCurses
========

[Hamayama 氏](https://github.com/Hamayama) が https://github.com/Hamayama/PDCurses-win10-jp  にて  
 「PDCurses の Windows Console 用ポート (wincon) を、Windows 10 上での日本語表示が改善するように、改造」  
したモノを PDCurses v3.9 にマージしてみたものです。実験物。

Windowsの UTF-8 (CP65001) コンソールは Windows8 までは １エンコード文字が１表示文字になっていましたが、Windows10 からはいわゆる半角/全角文字の幅が反映されて互換がなくなったので、以前の挙動に寄せ、NCURSESでは入力できないキー等にも対応したモノのようです。

[PDCurses_win10_jp](https://github.com/tenk-a/PDCurses/tree/PDCurses_win10_jp)ブランチがマージ元で、[win10_jp](https://github.com/tenk-a/PDCurses/tree/win10_jp) ブランチが3.9へマージしてみたモノです。

makefile の修正が mingw 用のモノだけだったので、vc,watcom,bcc 用 makefile  も更新しています。

PDCurses の元々の README.md については下記に、  
PDCurses-win10-jp の README.md  は [win10_jp_files/README_PDCurses-win10-jp.md](win10_jp_files/README_PDCurses-win10-jp.md)  
に移しました。

単純に混ぜただけなので、不具合が増えているかもしれません。  
PDC_mouse_set()関数は衝突していましたが、PDCurses-win10-jp の処理のままなので…

[tenk*](https://github.com/tenk-a/)
※私がやった修正についても元のライセンスに同じです。

※ macやlinux の ncurses の挙動の兼ね合い等、これを反映するかどうかはケースバイケース。win10環境前提で作ったモノは逆におかしくなるが必然…

----------------------------------------------------------------------

PDCurses
========

Stable: [v3.9]  
Current: [See git repository][git]

PDCurses is a public domain curses library for [DOS], [OS/2], [Windows]
console, [X11] and [SDL], implementing most of the functions available in
[X/Open] and System V R4 curses, and supporting a variety of compilers for
these platforms. The X11 and SDL ports let you recompile existing
text-mode curses programs to produce GUI applications.

PDCurses is distributed mainly as source code, but some pre-compiled
libraries may be available.

The latest version can be found at:

   <https://pdcurses.org/>

For changes, see the [History] file. The main documentation is now in the
[docs] directory.


Mailing lists
-------------

There's a low-traffic mailing list for announcements and discussion. To
subscribe, email the [list server], with the first line of the body of
the message containing:

`subscribe pdcurses-l`

or you can read the mailing list [archive].


Other links
-----------

* [Docs][docs]
* [GitHub Page][git]
* [SourceForge Page]
* [X/Open] curses


Legal Stuff
-----------

The core package and most ports are in the public domain, but a few files
in the [demos] and [X11][xstatus] directories are subject to copyright
under licenses described there.

This software is provided AS IS with NO WARRANTY whatsoever.


Maintainer
----------

[William McBrine]


[v3.9]: https://github.com/wmcbrine/PDCurses/releases/tag/3.9
[git]: https://github.com/wmcbrine/PDCurses

[History]: docs/HISTORY.md
[docs]: docs/README.md

[list server]: mailto:majordomo@lightlink.com
[archive]: https://www.mail-archive.com/pdcurses-l@lightlink.com/

[SourceForge Page]: https://sourceforge.net/projects/pdcurses
[X/Open]: https://pubs.opengroup.org/onlinepubs/007908799/cursesix.html

[DOS]: dos/README.md
[OS/2]: os2/README.md
[SDL]: sdl2/README.md
[Windows]: wincon/README.md
[X11]: x11/README.md

[demos]: demos/README.md#distribution-status
[xstatus]: x11/README.md#distribution-status

[William McBrine]: https://wmcbrine.com/
