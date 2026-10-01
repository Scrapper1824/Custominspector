# CustomInspectors (RML)

A ResoniteModLoader (RML) mod that lets you use custom inspector panels by saving them to your inventory and selecting **Set Inspector**. The `SceneInspector` component must be on the saved inspector's top-level slot. Wait for the item to finish syncing before favoriting it.

This repository contains the RML build of [art0007i/CustomInspectors](https://github.com/art0007i/CustomInspectors), adapted for the current Resonite .NET 10 runtime.

## Installation

1. Install [ResoniteModLoader](https://github.com/resonite-modding-group/ResoniteModLoader).
2. Download `CustomInspectors.dll` from this repository's Releases page and place it in Resonite's `rml_mods` folder.
3. Install the [RML `SpecialItemsLib.dll` 2.0.3](https://github.com/art0007i/SpecialItemsLib/releases/download/2.0.3/SpecialItemsLib.dll) in the same `rml_mods` folder. SpecialItemsLib 2.0.4 is a BepisLoader package, not the RML DLL.
4. Start Resonite, save an inspector with `SceneInspector` on its top-level slot, and wait for it to sync. Select it in inventory and use **Set Inspector**.

## Build

Requirements: .NET 10 SDK, Resonite's game references (provided by NuGet), and the RML `SpecialItemsLib.dll` 2.0.3 assembly reference.

Place `SpecialItemsLib.dll` in Resonite's `rml_mods` folder, then run:

```powershell
dotnet build Plugin/CustomInspectors.csproj -c Release -p:ResonitePath="C:/Program Files (x86)/Steam/steamapps/common/Resonite/"
```

The build output is `Plugin/bin/Release/net10.0/CustomInspectors.dll`.

## AI assistance disclosure

AI tools assisted with the RML port, project setup, documentation, and the prebuilt DLL. The resulting project was compiled against ResoniteModLoader 5.0.1 and the RML SpecialItemsLib 2.0.3 DLL. AI assistance does not change the original project's authorship: the upstream project is by art0007i. Review the source and test the mod in Resonite before using it.

## License

This project is distributed under the MIT No Attribution license. See [LICENSE](LICENSE).
