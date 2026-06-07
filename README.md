# BongoCat Click Multiplier

A simple change for Bongo Cat that multiplies your score.

## Requirements

- dnSpy
- Bongo Cat

## Installation

1. Open dnSpy

2. Drag and drop `BongoCat_Data/Managed/Assembly-CSharp.dll` into dnSpy

3. Press `Ctrl + Shift + K` to open Search Assemblies

4. Search for `BongoCat.Pets`

5. On the right side you will see `BongoCat.Pets` — click on it

6. Press `Ctrl + F` to find `AddPet`

7. Right-click on `AddPet` → Edit Method (C#) and replace with:

```csharp
public void AddPet(int value)
{
    if (!this._init) return;
    this._currentGained += value * 10;
    this._currentAchievement += value * 10;
    this.UpdateStats();
}
```

Change `10` to any multiplier you want:
- `10` → x10 per keypress
- `100` → x100 per keypress
- `1000` → x1000 per keypress

8. Click Compile

9. Go to File → Save Module

10. Launch the game — done!

## Uninstalling

Verify game files on Steam to restore the original DLL:

```
Steam → Bongo Cat → Properties → Local Files → Verify integrity of game files
```

## Notes

- Stats are saved to Steam — changes are permanent
- <img width="1404" height="551" alt="image" src="https://github.com/user-attachments/assets/451a60f4-786e-4bd0-b58b-00cbdbfc4cd4" />

