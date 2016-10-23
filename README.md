Swift is fun.  Let's say hello to it.

    $ cat >hello.swift
    print("Hello, swift!")
    $ swift hello.swift
    Hello, swift!

The primary reference is the Swift ebook.  It is available as an
[epub][] file. It is recommended that you keep a text copy of that
book on your machine locally, so that you can use it as a man page and
quickly grep for stuff if you have doubts:

    curl -LO https://swift.org/documentation/TheSwiftProgrammingLanguage(Swift3).epub
    pandoc TheSwiftProgrammingLanguage\(Swift3\).epub -o swift3.txt -w plain

For naming conventions, go through the [Swift API design
guidelines][naming].

Apple's [Swift Blog][blog] is the new NSHipster.

Swift comes with five different "assertions"; see the first section
("API") of [Mike Ash's introduction][assertions].

[RxSwift][] is Swift port of Rx.  It unifies KVO observing,
notifications, async operations and streams under the same
abstraction.

## Coding Conventions

### Indentation

Use 4 spaces.

### No Boilerplate

The default Xcode Templates have auto-generated boilerplate at the top
of your source file; you can remove them with the following
[command][template-gist]:

    find -E $(xcode-select --print-path) -regex '.*___\.(c|h|m|swift)' -print0 | xargs -0 -n 1 sed -i '' '1,/^$/d'

You will have to run this each time you update Xcode.

[epub]: https://swift.org/documentation/TheSwiftProgrammingLanguage(Swift3).epub
[naming]: https://swift.org/documentation/#api-design-guidelines
[blog]: https://developer.apple.com/swift/blog/
[assertions]: https://www.mikeash.com/pyblog/friday-qa-2016-03-04-swift-asserts.html
[rxswift]: https://github.com/ReactiveX/RxSwift
[template-gist]: https://gist.github.com/mx4492/81da9f3c363bc1c44f4e
