# Fortnite Community Shop Guide for Evoke OGFN

> **Tip:** You can find every cosmetic in [Fortnite.GG/cosmetics](https://fortnite.gg/cosmetics)

---

## 1. Requirements for Cosmetics

- **Version:** Must be from Chapter 1 Season 10 (Version 10.40) or earlier.
- **Cosmetic ID:** Must follow the correct format (see below).

---

## 2. Config File Structure

The item shop is defined using a JSON file. It contains slots for both daily and featured items.

**Basic JSON Structure:**

```json
{
    "//": "BR Item Shop Config",
    "daily1": {
        "itemGrants": [""],
        "name": "",
        "price": 0
    },
    "daily2": {
        "itemGrants": [""],
        "name": "",
        "price": 0
    },
    "daily3": {
        "itemGrants": [""],
        "name": "",
        "price": 0
    },
    "daily4": {
        "itemGrants": [""],
        "name": "",
        "price": 0
    },
    "daily5": {
        "itemGrants": [""],
        "name": "",
        "price": 0
    },
    "daily6": {
        "itemGrants": [""],
        "name": "",
        "price": 0
    },
    "featured1": {
        "itemGrants": [""],
        "name": "",
        "price": 0
    },
    "featured2": {
        "itemGrants": [""],
        "name": "",
        "price": 0
    }
  }
```

- **Daily Items:** `daily1` to `daily6`
- **Featured Items:** `featured1` to `featured6`
- **Name:** Just enter the name of the Cosmetic in English, otherwise your shop will not getting used!
- **itemGrants:** Cosmetic IDs for the item.
- **price:** The cost in V-Bucks.

---

## 3. Cosmetic ID Formatting

Each cosmetic has a unique ID. Format them as:

```
ItemType:CosmeticID
```

**Examples:**

- **Skin:** `"AthenaCharacter:CID_EVOKEOGFN"`
- **Emote:** `"AthenaDance:EID_Flare"`
- **Pickaxe:** `"AthenaPickaxe:Reaper"`
- **Backbling:** `"AthenaBackpack:BID_EVOKEOGFN"`
- **Glider:** `"AthenaGlider:Glider_StarSurfer"`
- **Wrap:** `"AthenaItemWrap:GalaxyWrap"`
- **Loading Screen:** `"AthenaLoadingScreen:LoadingScreen_Galactic"`
- **Skydiving Contrail:** `"AthenaSkyDiveContrail:Contrail_Rainbow"`

> **Important:** Always wrap Cosmetic IDs in double quotes.

---

## 4. Setting Up Your Item Shop

To add an item to your shop, fill in the slot with:
- **itemGrants:** The Cosmetic ID of the item.
- **Name:** The Cosmetic name in English.
- **price:** Its cost in V-Bucks.

**Example Config:**

```json
{
  "//": "BR Item Shop Config",
  "daily1": {"itemGrants": ["AthenaCharacter:Character_EVOKEOGFN"], "price": 1200},
  "daily2": {"itemGrants": ["AthenaPickaxe:Pickaxe_EVOKEOGFN"], "price": 800},
  "daily3": {"itemGrants": ["AthenaDance:Dance_Flare"], "price": 500},
  "daily4": {"itemGrants": ["AthenaItemWrap:Wrap_Galaxy"], "price": 300},
  "daily5": {"itemGrants": ["AthenaGlider:Glider_StarSurfer"], "price": 1500},
  "daily6": {"itemGrants": ["AthenaLoadingScreen:LoadingScreen_Galactic"], "price": 200},
  "featured1": {"itemGrants": ["AthenaCharacter:Character_Drift"], "price": 2000},
  "featured2": {"itemGrants": ["AthenaDance:Dance_DefaultDance"], "price": 200},
  "featured3": {"itemGrants": ["AthenaSkyDiveContrail:Contrail_Rainbow"], "price": 400},
  "featured4": {"itemGrants": ["AthenaItemWrap:Wrap_Camo"], "price": 600}
}
```

---

## 5. Common Mistakes to Avoid

- **No Quotes:** Always put cosmetic IDs in double quotes.
- **Comma Errors:** Write numbers without commas (e.g., use `1200` not `1,200`).
- **Wrong Versions:** Do not use cosmetics from after Chapter 1 Season 10.

---

## 6. Pro Tips

- **Use VS Code:** It highlights JSON errors and keeps formatting clean.
- **Validate with AI Tools:** Tools like ChatGPT can help check your JSON before testing.
