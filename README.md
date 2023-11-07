# Artifact for pythoneda-shared-artifact/application

Artifact space for <https://github.com/pythoneda-shared-artifact/application>.

## How to declare it in your flake

Check the latest tag of the artifact repository: [https://github.com/pythoneda-shared-artifact/application-artifact/tags](https://github.com/pythoneda-shared-artifact/application-artifact/tags) and use it instead of the `[version]` placeholder below.

```nix
{
  description = "[..]";
  inputs = rec {
    [..]
    pythoneda-shared-artifact-application = {
      [optional follows]
      url =
        "github:pythoneda-shared-artifact/application-artifact/[version]?dir=application";
    };
  };
  outputs = [..]
};
```

Should you use another PythonEDA modules, you might want to pin those also used by this project. The same applies to [nixpkgs](https://github.com/nixos/nixpkgs "nixpkgs") and [flake-utils](https://github.com/numtide/flake-utils "flake-utils").

Use the specific package depending on your system (one of `flake-utils.lib.defaultSystems`) and Python version:

- `#packages.[system].pythoneda-shared-artifact-application-python38` 
- `#packages.[system].pythoneda-shared-artifact-application-python39` 
- `#packages.[system].pythoneda-shared-artifact-application-python310` 
- `#packages.[system].pythoneda-shared-artifact-application-python311` 

The Nix flake is under the 
[infrastructure](https://github.com/pythoneda-shared-artifact/application-artifact/tree/main/application "application") folder.
