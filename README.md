## dargon2_interface

# NOTE: Archive

This repository has been archived. Don't worry, `dargon2_flutter` is still in development with full support! I've just moved this repository and all dargon2 components into a single `dargon2` repository: https://github.com/tmthecoder/dargon2

---

This library generally should not be used in most contexts

This library only provides an interface to implement a dargon2-compatible argon2 hash binding.

This library is used by `dargon2_core` and `dargon2_flutter_web` to maintain cross-platform hashing functionality.

## Usage

A simple usage example:

```dart
import 'package:dargon2_interface/dargon2_interface.dart';

void main() {
  // Create an instance of TestDArgon2
  var dargon2 = TestDArgon2();
}

class TestDArgon2 extends DArgon2 {
  @override
  Future<DArgon2Result> hashPasswordBytes(List<int> password, {required Salt salt, int iterations = 32, int memory = 256, int parallelism = 2, int length = 32, Argon2Type type = Argon2Type.i, Argon2Version version = Argon2Version.V13}) {
    // Create an implementation for hashing passwords with the given parameters
    throw UnimplementedError();
  }

  @override
  Future<bool> verifyHashBytes(List<int> password, List<int> encodedHash, {Argon2Type type = Argon2Type.i}) {
    // Create an implementation for verifying passwords with the given parameters
    throw UnimplementedError();
  }
}
```

## Features and bugs

Please file feature requests and bugs at the [issue tracker].

[issue tracker]: https://github.com/tmthecoder/dargon2_interface/issues

## Licensing

- dargon2_core is Licensed under the [MIT License]
- The C implementation of [Argon2] is licensed under a dual [Apache and CC0 License]

[MIT License]: https://github.com/tmthecoder/dargon2_interface/blob/main/LICENSE

[Argon2]: https://github.com/P-H-C/phc-winner-argon2

[Apache and CC0 License]: https://github.com/P-H-C/phc-winner-argon2/blob/master/LICENSE
