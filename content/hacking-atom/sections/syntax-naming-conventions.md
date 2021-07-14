---
title: Syntax Naming Conventions
---

### Syntax Naming Conventions

Naming conventions ensure that every language is correctly highlighted by different themes. When creating a language grammar, use these conventions to decide which syntax classes correspond to your syntax nodes. When creating a syntax theme, use these conventions to decide which syntax classes correspond to your theme colors.

The syntax classes are organized into nested categories. In a language grammar, multiple nested classes can be applied to a syntax node by appending them with periods, as in `entity.function.call`. The order in which classes are appended does not affect the resulting highlighting. However, we recommended following their hierarchy to stay consistent.

Root classes, like `entity`, must not be appended to other root classes, unless explicitly allowed in this documentation. Main classes indicated in bold green, like `function`, must be used for coherent highlighting. Shared classes indicated in brackets, like `[call]`, can be appended when relevant. You may create additional classes if they clarify your grammar and do not introduce conflicts with existing classes.

#### List of Classes

<details>
  <summary>__`keyword`__ — A keyword.</summary>
  <ul>
    <li>__`[symbolic]`__ — A keyword with no alphabetic characters.
    </li>
    <li>__`control`__ — A control or structure keyword.
      <ul>
        <li>`condition` — A condition keyword.
          Examples: `if`, `else`, `elif`.
        </li>
        <li>`loop` — A loop keyword.
          Examples: `for`, `for`...`in`, `for`...`of`, `do`, `while`.
        </li>
        <li>`exception` — An exception keyword.
          Examples: `try`, `catch`, `finally`.
        </li>
        <li>`jump` — A keyword used to jump to/from a statement.
          Examples: `break`, `continue`, `pass`, `return`, `yield`, `throw`, `await`.
        </li>
        <li>`package` — A keyword for imports or exports.
          Examples: `import`, `from`, `include`, `export`, `require`.
        </li>
        <li>`directive` — An instruction given to the compiler.
          Examples: `#include`, `#define`, `#ifdef`, `using`, `package`, `use strict`.
        </li>
        <li>`evaluate` — A keyword used to evaluate an expression.
          Examples: `assert`, `with`...`as`.
        </li>
      </ul>
    </li>
    <li>__`storage`__ — A storage keyword.
      <ul>
        <li>`modifier` — A keyword to detail the behavior of an entity.
          Examples: `static`, `abstract`, `final`, `throws`, `get`, `extends`.
        </li>
        <li>`declaration` — A keyword to declare an entity.
          Examples: `let`, `const`, `func`, `def`, `class`, `enum`, `typedef`, `namespace`.
        </li>
      </ul>
    </li>
    <li>__`type`__ — A type keyword.
      Examples: `char`, `int`, `bool`, `void`.
      <ul>
        <li>`wildcard` — A wildcard keyword for an unknown type.
          Example: `?` in `List<?> list`.
        </li>
      </ul>
    </li>
    <li>__`operator`__ — An operator keyword. Includes overloaded operators.
      <ul>
        <li>`logical` — A logical operator.
          Examples: `and`, `not`, `or`, `!`, `&&`, `||`.
        </li>
        <li>`ternary` — A ternary condition operator.
          Examples: `?`, `:`.
        </li>
        <li>`assignment` `(compound)` — An assignment operator.
          Examples: `=`, `:=`, `+=`, `-=`, `*=`, `%=`.
        </li>
        <li>`comparison` — A comparison operator.
          Examples: `==`, `<`, `>`, `!=`, `in`, `instanceof`.
        </li>
        <li>`arithmetic` — An arithmetic operator.
          Examples: `+`, `-`, `/`, `*`, `@`, `++`, `--`.
        </li>
        <li>`pointer`  `(reference)` `(dereference)` — A pointer operator.
          Examples: `&`, `*`.
        </li>
        <li>`bitwise` — A bitwise operator.
          Examples: `<<`, `>>`, `|`, `&`, `^`, `~`.
        </li>
        <li>`instance` — A instance operator.
          Examples: `del`, `delete`, `new`, `typeof`.
        </li>
        <li>`composition` — A composition operator (Haskell).
          Example: `.`.
        </li>
        <li>`combinator` — A combinator operator (CSS).
          Examples: `>`, `+`, `~`, `&`.
        </li>
      </ul>
    </li>
    <li>__`function`__ — A function keyword.
      Example: `super`.
    </li>
    <li>__`variable`__ — A variable keyword.
      Examples: `this`, `self`, `@`.
    </li>
  </ul>
</details>
<details>
  <summary>__`entity`__ — An identifier.</summary>
  <ul>
    <li>`[parameter]` — A parameter in a definition or declaration.
      Examples: `fn myFunction(parameter: type) {}`, `class MyClass<parameter> {}`.
    </li>
    <li>`[argument]` — An argument in a call.
      Examples: `instance.method(argument)`, `new MyClass(argument)`.
    </li>
    <li>`[definition]` — An entity that is being defined or declared.
      Examples: `my_variable` in `let my_variable`, `myFunction` in `def myFunction()`.
    </li>
    <li>`[call]` — An entity that is being called.
      Examples: `myFunction` in `myFunction()`, `MyClass` in `new MyClass(argument)`.
    </li>
    <li>`[mutable]` — An entity whose properties or value can be changed.
      Examples: `var mutable`, `let mutable`.
    </li>
    <li>`[immutable]` — An entity whose properties or value cannot be changed.
      Examples: `const immutable`, `final immutable`.
    </li>
    <li>__`[support]`__ — A built-in/imported/conventional entity that can usually be redefined.
      Examples: `self`, `cls`, `arguments`, `iota`, `len`, `print`, `loop`, `int`, `bool`.
    </li>
    <li>__`variable`__ — A variable.
      <ul>
        <li>`member` — A member variable in an object.
          Examples: `{property: value}`, `object.attribute`.
        </li>
      </ul>
    </li>
    <li>__`function`__ — A function.
      <ul>
        <li>`cast` — A type casting function that is not a type itself.
          Examples: `as.matrix()`, `toInt()`.
        </li>
        <li>`method` `(constructor)`— A method in an object.
          Examples: `{method: (parameter) => value}`, `object.method()`.
        </li>
        <li>`lambda` — A lambda.
          Example: `lambda = ->() {}`.
        </li>
        <li>`infix` — A function used in infix notation.
          Example: ``1 `function` 2``.
        </li>
      </ul>
    </li>
    <li>__`operator`__ — An operator.
      <ul>
        <li>__`[symbolic]`__ — An operator with no alphabetic characters.
          Examples: `%>%`, `<+>`.
        </li>
      </ul>
    </li>
    <li>__`type`__ — A type.
      <ul>
        <li>`[cast]` — A type used for type casting, eventually in functional notation.
          Examples: `float(32)`, `int(3.2)`, `matrix()`.
        </li>
        <li>`[constructor]` — A type used as a constructor, eventually in functional notation.
          Examples: `new MyClass()`.
        </li>
        <li>__`fundamental`__ — A fundamental primitive or compound type.
          Examples: `char`, `int`, `bool`, `rune`, `list`, `map`, `tuple`.
        </li>
        <li>`class` — A class.
          Examples: `MyClass`, `String`, `List`.
          <ul>
            <li>`inherited` — An inherited class.
              Example: `class Child < Inherited`.
            </li>
            <li>`mixin` — A mixin class.
              Example: `module Mixin` (Ruby).
            </li>
            <li>`generic` — A generic class.
              Examples: `<T>`, `<E>`.
            </li>
            <li>`exception` — An exception.
              Example: `AssertionError`.
            </li>
            <li>`abstract` — An abstract class.
              Example: `abstract class Abstract` (Java)
            </li>
          </ul>
        </li>
        <li>`interface` — An interface.
          Example: `Vehicle` in `public interface Vehicle {}`.
        </li>
        <li>`enumeration` — An enumeration.
          Example: `Color` in `enum Color{red, green, blue}`.
        </li>
        <li>`structure` — A structure.
          Examples: `Address` in `type Address struct {}`.
        </li>
        <li>`union` — An union.
          Example: `IPv4` in `union IPv4 {}`.
        </li>
        <li>`alias` — An alias.
          Example: `Number` in `typedef int Number`.
        </li>
      </ul>
    </li>
    <li>`annotation` — An annotation.
      Examples: `@Override`, `@Deprecated` (Java), `[Obsolete]` (C#).
    </li>
    <li>`namespace` — A namespace.
      Examples: `namespace Namespace {}` (C++), `namespace::function()` (Rust).
    </li>
    <li>`package` — A package.
      Example: `from package import entity`.
    </li>
    <li>`label` — A statement label.
      Example: `goto label`.
    </li>
    <li>`option` — An option (Shell Script).
      Examples: `--name`, `-a`.
    </li>
    <li>__`tag`__ — A tag (HTML).
      Examples: `body`, `div`, `input`.
    </li>
    <li>__`attribute`__ `(id)` `(class)` — An attribute (HTML).
      Example: `<tag attribute=value>`.
    </li>
    <li>__`property`__ — A property (CSS).
      Example: `{property: value}`.
    </li>
    <li>__`selector`__ `(tag)` `(id)` `(class)` `(pseudo-)` `(attribute)` — A selector (CSS).
      Examples: `#id`, `.class`, `:hover`, `:not`, `::before`, `::after`, `[attribute]`.
    </li>
  </ul>
</details>
<details>
  <summary>__`string`__ — A string or part of a string.</summary>
  <ul>
    <li>`[argument]` — An argument in a call.
      Examples: `myFunction("string")`, `new MyClass('string')`.
    </li>
    <li>`[mutable]` — A mutable string. Specified when mutable and immutable coexist.
      Example: `'string'` (Ruby).
    </li>
    <li>`[immutable]` — An immutable string. Specified when mutable and immutable coexist.
      Example: `:immutable` (Ruby).
    </li>
    <li>`[key]` — A key in a key-value pair.
      Example: `{"key" => value}`.
    </li>
    <li>`[quoted]` — A quoted string.
      Examples: `"string"`, `'string'`, `$"template string"`, `/^regexp string$/`.
    </li>
    <li>`[unquoted]` — An unquoted string.
      Example: `'key': unquoted`.
    </li>
    <li>__`[part]`__ — A part of a string or regular expression.
      <ul>
        <li>`interpolation` — An interpolation in a string.
          Examples: `${variable}`, `{variable:<30}`.
        </li>
        <li>`placeholder` — A placeholder in a string.
          Examples: `%()d`, `{0:.2f}`, `%-#10x`, `\1`.
        </li>
        <li>`format` — A format specifier in a string.
          Examples: `<30`, `d`, `.2f`, `-#10x`.
        </li>
        <li>__`language`__ — A regular expression keyword.
          <ul>
            <li>__`[symbolic]`__ — A keyword with no alphabetic characters.
            </li>
            <li>`control` `(anchor)` `(boundary)` `(reference)` `(mode)` — A control token.
              Examples: `^`, `$`, `\b`, `\k`, `\1`, `i` in `(?i)`, `g` in `/^regexp$/g`.
            </li>
            <li>`operator` `(quantifier)` — A quantifier operator.
              Examples; `?`, `*`, `+`, `{1,2}`.
            </li>
          </ul>
        <li>__`variable`__ — A regular expression variable.
          Examples: `(?<variable>)`, `\k<variable>`.
        </li>
        <li>`group` — A regular expression group.
          Examples: `(capture)`, `(?:non-capture)`.
        </li>
        <li>`lookaround` — A regular expression lookaround.
          Example: `(?=lookahead)`.
        </li>
        <li>`set` — A regular expression set.
          Example: `[^A-Z]`.
        </li>
      </ul>
    <li>__`regexp`__ — A regular expression or part of a regular expression.
      Example: `/^regexp$/`.
    </li>
    <li>`template` — A template string.
      Examples: `$"string {interpolation}"`, `` `string ${interpolation}` ``.
    </li>
    <li>`heredoc` — A here document.
      Example: `<<EOF A multiline here document EOF`.
    </li>
  </ul>
</details>
<details>
  <summary>__`constant`__ — A literal other than a string.</summary>
  <ul>
    <li>`[argument]` — An argument in a call.
      Examples: `myFunction(constant)`, `float(constant)`.
    </li>
    <li>`[key]` — A key in a key-value pair.
      Example: `{key: value}`.
    </li>
    <li>`[quoted]` — A quoted constant.
      Example: `'a'`.
    </li>
    <li>`[unquoted]` — An unquoted constant.
      Example: `#color`.
    </li>
    <li>__`[support]`__ — A built-in or imported or conventional constant.
      Examples: `absolute`, `blue`, `screen`.
    </li>
    <li>__`[language]`__ — A literal keyword.
      <ul>
        <li>__`[symbolic]`__ — A keyword with no alphabetic characters.
          Example: `...` (Python).
        </li>
        <li>`boolean` — A boolean.
          Examples: `true`, `false`.
        </li>
        <li>`null` — A null value.
          Examples: `None`, `null`, `nil`.
        </li>
        <li>`undefined` — An undefined value.
          Example: `undefined`.
        </li>
        <li>`numeric` — A numeric word.
          Example: `Infinity`.
        </li>
      </ul>
    </li>
    <li>__`numeric`__ — A number.
      <ul>
        <li>`integer` — An integer.
          Example: `2`.
        </li>
        <li>`decimal` — A decimal number.
          Example: `.17`.
        </li>
        <li>`hexadecimal` — A hexadecimal number.
          Example: `0x29`.
        </li>
        <li>`unit` — A length unit (CSS).
          Examples: `%`, `px`, `pt`, `em`.
        </li>
        <li>`duration` — A duration (Lilypond).
          Examples: `8`, `2.`.
        </li>
      </ul>
    </li>
    <li>__`character`__ — A character.
      Example: `'a'`.
      <ul>
        <li>`[escape]` — An escape sequence.
          Examples: `\"`, `\\`, `\i`, `\?`, `\u2661`, `\n`, `\d`, `\W`.
        </li>
        <li>__`code`__ — A substitute for another character.
          Examples: `&lt;`, `\x2f`, `\n`.
          <ul>
            <li>`shorthand` — A shorthand for other characters (RegExp).
              Examples: `.`, `\d`, `\W`, `\s`.
            </li>
            <li>`range` — A range of characters (RegExp).
              Examples: `a-z`, `0-9`.
            </li>
            <li>`whitespace` — A whitespace character.
              Examples: `\t`, `\f`.
              <ul>
                <li>`newline` — A newline character.
                  Examples: `\n`, `\r`.
                </li>
              </ul>
            </li>
            <li>`unicode` — A unicode code point.
              Example: `\u2661`.
            </li>
            <li>`hexadecimal` — A hexadecimal code point.
              Example: `\x2f`.
            </li>
            <li>`octal` — An octal code point.
              Example: `\143`.
            </li>
          </ul>
        </li>
      </ul>
    </li>
    <li>`color` — A color (CSS).
      Examples: `crimson`, `#a35`.
    </li>
    <li>`font` — A font (CSS).
      Examples: `Helvetica`, `Times New Roman`.
    </li>
    <li>`style` — A style (CSS).
      Examples: `break-word`, `solid`, `absolute`.
    </li>
  </ul>
</details>
<details>
  <summary>__`text`__ — Plain text.</summary>
</details>
<details>
  <summary>__`markup`__ —  Stylized text.</summary>
  <ul>
    <li>`heading` — A heading.
      Example: `# Heading`.
    </li>
    <li>`list` — A list item.
      Examples: `1. item`, `- item`.
    </li>
    <li>`quote` — A quote.
      Example: `> quote`.
    </li>
    <li>`bold` — Bold text.
      Example: `**bold**`.
    </li>
    <li>`italic` — Italic text.
      Example: `*italic*`.
    </li>
    <li>`underline` — Underlined text.
      Example: `__underline__`.
    </li>
    <li>`strike` — Striked-through text.
      Example: `~~strike~~`.
    </li>
    <li>`raw` — Raw unformatted text or code.
       Example: `` `raw` ``.
    </li>
    <li>`link` — An url or path or reference.
      Examples: `url.com`, `(path)` in `[alt](path)`, `[reference]`.
    </li>
    <li>`alt` — Alternate text for a link.
      Examples: `[alt]`, `![alt]`.
    </li>
    <li>`critic` — A critic.
      <ul>
        <li>`inserted` — An insertion.
          Example: `{++ inserted ++}`.
        </li>
        <li>`deleted` — A deletion.
          Example: `{-- deleted --}`.
        </li>
        <li>`changed` — A modification.
          Example: `{~~ from ~> to ~~}`.
        </li>
        <li>`commented` — A comment.
          Example: `{>> commented <<}`.
        </li>
        <li>`highlighted` — A highlight.
          Example: `{== highlighted ==}`.
        </li>
      </ul>
    </li>
  </ul>
</details>
<details>
  <summary>__`comment`__ — A comment or part of a comment. Includes comments in strings.</summary>
  <ul>
    <li>__`part`__ — A part of a comment.
      <ul>
        <li>`caption` — A caption in a comment.
          Examples: `@param`, `<returns>`, `NOTE`, `TODO`, `FIXME`.
        </li>
        <li>`path` — A path in a comment.
          Example: `path/to/my-file`.
        </li>
        <li>`term` `(variable)` `(function)` `(operator)` `(type)` — A documented entity.
          Examples: `type` and `variable` in `@param {type} variable`.
        </li>
      </ul>
    </li>
    <li>`line` — A one-line comment.
      Example: `# comment`.
    </li>
    <li>`block` — A multi-line comment.
      Example: `/* ... */`.
    </li>
  </ul>
</details>
<details>
  <summary>__`punctuation`__ — A punctuation mark.</summary>
  <ul>
    <li>__`[string]`__ — Punctuation for a string or part of a string.
      Examples: `"`, `'`, `$"`.
      <ul>
        <li>__`[part]`__ — Punctuation for a part of a string or regular expression.
          <ul>
            <li>`interpolation` — Punctuation for an interpolation in a string.
              Examples: `#{`, `${`, `}`.
            </li>
            <li>`placeholder` — Punctuation for a placeholder in a string.
              Examples: `{`, `}`, `%`, `%(`, `)`.
            </li>
            <li>`format` — Punctuation for a format specifier in a string.
              Example: `:`.
            </li>
            <li>`group` — Punctuation for a group in a regular expression.
              Examples: `(?:`, `(`,  `(?P`, `)`.
            </li>
            <li>`lookaround` — Punctuation for a lookaround in a regular expression.
              Examples: `(?=`, `(?!`, `)`.
            </li>
            <li>`disjunction` — Punctuation for a disjunction in a regular expression.
              Example: `|`.
            </li>
            <li>`set` — Punctuation for a set in a regular expression.
              Examples: `[^`, `[`, `]`.
            </li>
            <li>`mode` — Punctuation for a mode specifier in a regular expression.
              Examples: `(?`, `)`.
            </li>
          </ul>
        </li>
        <li>__`regexp`__ — Punctuation for a regular expression or part of a regular expression.
          Examples: `r"`, `/`.
        </li>
      </ul>
    </li>
    <li>__`[constant]`__ — Punctuation for a literal other than a string.
      Example: `#`.
      <ul>
        <li>__`character`__ `(escape)` — Punctuation for a character.
          Examples: `'`, `\`.
        </li>
      </ul>
    </li>
    <li>__`[markup]`__ — Punctuation for text styling (Markdown).
      Examples: `_`, `*`, `~`, `#`, `-`. `1.`, `[`, `]`.
    </li>
    <li>__`[comment]`__ — Punctuation for a comment or part of a comment.
      Examples: `//`, `#`, `<!--`, `-->`.
      <ul>
        <li>__`part`__ — Punctuation for a part of a comment.
          <ul>
            <li>`caption` — Punctuation for a caption in a comment.
              Examples: `@`, `<`, `>`, `:`.
            </li>
            <li>`term` — Punctuation for a documented entity in a comment.
              Examples: `{` and `}` in `{type}`.
            </li>
          </ul>
        </li>
      </ul>
    </li>
    <li>__`definition`__ — Punctuation that defines tokens.
      <ul>
        <li>`collection` — Punctuation for a collection (array, set, map, etc.).
          Examples: `[`, `]`, `{`, `}`.
        </li>
        <li>`variable` — Punctuation for a variable.
          Example: `$`.
        </li>
        <li>`function` `(generator)` — Punctuation for a function.
          Examples: `` ` ``, `*`.
        </li>
        <li>`operator` — Punctuation for an operator.
          Examples: `(`, `)`, `%`.
        </li>
        <li>`annotation` — Punctuation for an annotation.
          Example: `@`.
        </li>
        <li>`directive` — Punctuation for a directive.
          Example: `#`.
        </li>
        <li>`package` `(wildcard)` — Punctuation for a package.
          Examples: `.`, `*`.
        </li>
        <li>`tag` — Punctuation for a tag (HTML).
          Examples: `<`, `/>`.
        </li>
        <li>`selector` `(wildcard)` — Punctuation for a selector (CSS).
          Examples: `*`, `.`, `#`, `:`, `::`, `[`, `]`.
        </li>
      </ul>
    </li>
    <li>__`alteration`__ — Punctuation that modifies tokens.
      <ul>
        <li>`variadic` — Punctuation for a variadic argument or parameter.
          Examples: `...`, `*`, `**`.
        </li>
        <li>`decorator` — Punctuation for a decorator.
          Example: `@`.
        </li>
      </ul>
    </li>
    <li>__`delimiter`__ — Punctuation that separates tokens by delimiting boundaries.
      <ul>
        <li>`statement` — Punctuation to delimit a statement.
          Examples: `{`, `}`, `:`, `;`.
        </li>
        <li>`expression` — Punctuation to delimit an expression.
          Examples: `(`, `)`.
        </li>
        <li>`arguments` — Punctuation to delimit arguments.
          Examples: `(`, `)`.
        </li>
        <li>`parameters` — Punctuation to delimit parameters.
          Examples: `(`, `)`.
        </li>
        <li>`body` — Punctuation to delimit a body (function, class, structure, etc.).
          Examples: `{`, `}`, `:`, `=>`.
        </li>
        <li>`embedded` — Punctuation to delimit embedded code.
          Examples: `~~~`, `<%=`, `%>`.
        </li>
        <li>`package` — Punctuation to delimit package imports or exports.
          Examples: `(` `)`, `{`, `}`.
        </li>
        <li>`type` — Punctuation to delimit the type of an entity.
          Examples: `<`, `>`, `:`, `->`.
        </li>
        <li>`argument` — Punctuation to delimit an argument.
          Example: `,`.
        </li>
        <li>`parameter` — Punctuation to delimit a parameter.
          Example: `,`.
        </li>
        <li>`item` — Punctuation to delimit an item in a collection.
          Example: `,`.
        </li>
        <li>`pair` — Punctuation to delimit a key's pair in a mapping.
          Examples: `:`, `=>`.
        </li>
        <li>`line` — Punctuation to delimit a line.
          Example: `\`.
        </li>
      </ul>
    </li>
    <li>__`accessor`__ — Punctuation to access contained entities.
      <ul>
        <li>`member` — Punctuation for member access.
          Examples: `.`, `->`.
        </li>
        <li>`scope` — Punctuation for scope resolution.
          Example: `::`.
        </li>
        <li>`subscript` — Punctuation to subscript a collection.
          Examples: `[`, `]`.
        </li>
      </ul>
    </li>
  </ul>
</details>
<details>
  <summary>`[invalid]` — An invalid token. Appendable to every class.</summary>
  <ul>
    <li>`deprecated` — A deprecated token which should no longer be used.
    </li>
    <li>`illegal` — An illegal token which doesn't belong there.
    </li>
  </ul>
</details>
<details>
  <summary>`meta` — A larger part of the document encompassing multiple tokens.</summary>
  <ul>
    <li>`function` — A function definition block.
    </li>
    <li>`class` — A class definition block.
    </li>
    <li>`embedded` — A language embedded in another.
    </li>
  </ul>
</details>
