# Android-Studio-Snippets
Compilation of Snippets that can be imported in Android Studio, or any IntelliJ editor really.

As of now, as I almost exclusively work with Flutter on Android Studio, all the available snippets are for Flutter & in Dart.

## Usage

• Clone this repo
• For each category you want to install, copy the XML files to a same `templates` folder, then zip that folder along with installed.txt and the IntelliJ IDEA Global Settings.
• Then, you can import your new snippets through `File > Import Settings`.

**CAUTION** : Importing Live Templates will erase all your already saved Live Templates. Backup'em up before importing the new ones !

**SPECIAL CASE** : If you have multiple XML files with the same name, such as `surround.xml`, you'll need to manually edit them to create a single file. Basically copy everything inside the `<templateSet>` tag into a single file. It is sometimes necessary since the IDE uses some groups as special Live Templates : The `surround` group for example is the list of snippets you can call when you use Ctrl+Alt+T on a line or a selection to surround it with brackets, parenthesis, or more exotic stuff.

---

## Documentation

Refer to the README.md available in each category subfolder.

## Categories

---

#### [GetX](https://github.com/MeixDev/Android-Studio-Snippets/tree/master/getx)
Snippets and Surround shortcuts useful for Flutter's GetX package.
