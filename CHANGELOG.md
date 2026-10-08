# Changelog

## [1.0.0] - 2026-10-08

First release as a standalone UPM package (previously shipped inside BillGameCore).

- Namespace `BillGameCore.BillFav` → `BillFav`; assembly `BillGameCore.BillFav` → `BillFav`.
- Menu moved from `BillGameCore/BillFav…` to `Tools/Bill/BillFav…`.
- Default data asset path is now `Assets/Settings/Editor/BillFavData.asset` (an existing `BillFavData`
  anywhere in the project is still found and used).
- Removed unused fields and variables that produced compiler warnings.
