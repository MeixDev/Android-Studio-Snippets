# GetX Snippets
Compilation of useful Snippets for the [get](https://pub.dev/packages/get) package. Heavily inspired by the [getx-snippets](https://marketplace.visualstudio.com/items?itemName=get-snippets.get-snippets) VSCode extension.

---

## Snippets

---

### GetX.xml

#### getbinding

Creates a new Get Binding file.

```dart
import 'package:get/get.dart';

class $CLASS$Binding extends Bindings {
  @override
  void dependencies() {
    $END$
  }
}
```

#### getcontroller

Creates new GetXController.

```dart
import 'package:get/get.dart';

class $CLASS$Controller extends GetxController {
  static $CLASS$Controller to = Get.find();
  $END$
}
```

#### getfinal

Creates a new observable variable with a setter and a getter.

```dart
final _$NAME$ = ''.obs;
get $NAME$ => this._$NAME$.value;
set $NAME$(value) => this._$NAME$.value = value;
$END$
```

#### getfinalrx

Creates a new observable variable with a setter and a getter, with Rx clarity. Great for custom classes !

```dart
final Rx<$CLASS$> _$NAME$ = Rx<$CLASS$>($END$);
$CLASS$ get $NAME$ => this._$NAME$.value;
set $NAME$(value) => this._$NAME$.value = value;
```

#### getput

Shortcut for the Get.put() statement.

```dart
$CLASS$ $NAME$ = Get.put($CLASS$());
```

#### getfind

Shortcut for the Get.find() statement.

```dart
$CLASS$ $NAME$ = Get.find();
```

#### getlazyput

Shortcut for the Get.lazyPut() statement.

```dart
Get.lazyPut<$CLASS$>(() => $CLASS$());
```

#### getpagesroutes

Creates a new app_pages.dart file.

```dart
import 'package:get/get.dart';
part './app_routes.dart';

abstract class AppPages {
  static final pages = [
    GetPage(
      name: Routes.HOME,
      page: () => HomePage(),
    ),
    $END$
  ];
}
```

#### getroutes

Creates a new app_routes.dart static Strings class, part of app_pages.dart.

```dart
import 'package:get/get.dart';
part of './app_pages.dart';

abstract class Routes {
  static const INITIAL = '/';
  static const HOME = '/home';
  static const LOGIN = 'login';
  $END$
}
```

#### getpageroute

Adds an entry to the app_pages.dart file.

```dart
GetPage(
  name: Routes.$ROUTECONST$,
  page: () => $ROUTENAME$Page(),
),
```

#### getpageroutebind

Adds an entry to the app_pages.dart file, with a Binding.

```dart
GetPage(
  name: Routes.$ROUTECONST$,
  page: () => $ROUTENAME$Page(),
  binding: $ROUTENAME$Binding(),
),
```

#### getrxmodel

Creates a new RxModel with simple base parameters and from/toJson methods.

```dart
import 'package:get/get.dart';

class Rx$CLASS$Model {
  
  final id = 0.obs;
  final name = ''.obs;
}

class $CLASS$Model {
  $CLASS$Model({id, name});
  
  final rx = Rx$CLASS$Model();
  
  get id => rx.id.value;
  set id(value) => rx.id.value = value;

  get name => rx.name.value;
  set name(value) => rx.name.value = value;
  
  $CLASS$Model.fromJson(Map<String, dynamic> json) {
    this.id = json['id'];
    this.name = json['name'];
  }
  
  Map<String, dynamic> toJson() {
    final Map<String, dynamic> data = Map<String, dynamic>();
    data['id'] = this.id;
    data['name'] = this.name;
    return data;
  }
}
```

---

### surround.xml

Those templates are available through the Ctrl+Alt+T shortcut.

#### GB

Surrounds the selection with a GetBuilder.

```dart
GetBuilder<$CLASS$>(
  init: $CLASS$(),
  builder: (ctl) {
    return $SELECTION$$END$
  },
),
```

#### Mx

Surrounds the selection with a MixinBuilder.

```dart
MixinBuilder<$CLASS$>(
  init: $CLASS$(),
  builder: (ctl) {
    return $SELECTION$$END$
  },
),
```

#### Obx

Surrounds the selection with an Obx.

```dart
Obx(() => $SELECTION$),
```

#### X

Surrounds the selection with a GetX.

```dart
GetX<$CONTROLLER$>(
  builder: (ctl) {
    return $SELECTION$$END$
  },
),
```