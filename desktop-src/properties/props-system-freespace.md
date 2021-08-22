---
description: Quantità di spazio disponibile in un volume, in byte.
ms.assetid: 84c85468-d3c2-49bf-b52b-bbd3d9ecb914
title: System.FreeSpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ba597cbea183cf1b7f1fde22cf07f9e159b520d9495d6e45004a17e3c38749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457821"
---
# <a name="systemfreespace"></a>System.FreeSpace

Quantità di spazio disponibile in un volume, in byte.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.FreeSpace
   shellPKey = PKEY_FreeSpace
   formatID = 9B174B35-40FF-11D2-A27E-00C04FC30871
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt64
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = Full
            minValue = 0
            setValue = 0
            text = Full
            defineToken = FREESPACE_FULL
            mnemonics = full
         enumRange
            name = Tiny
            minValue = 1
            setValue = 1
            text = Tiny (0 - 2 GB)
            defineToken = FREESPACE_TINY
            mnemonics = tiny
         enumRange
            name = Small
            minValue = 2147483649
            setValue = 2147483649
            text = Small (2 - 10 GB)
            defineToken = FREESPACE_SMALL
            mnemonics = small
         enumRange
            name = Medium
            minValue = 10737418241
            setValue = 10737418241
            text = Medium (10 - 40 GB)
            defineToken = FREESPACE_MEDIUM
            mnemonics = medium
         enumRange
            name = Large
            minValue = 42949672961
            setValue = 42949672961
            text = Large (40 - 80 GB)
            defineToken = FREESPACE_LARGE
            mnemonics = large
         enumRange
            name = Huge
            minValue = 85899345921
            setValue = 85899345921
            text = Huge (80 - 120 GB)
            defineToken = FREESPACE_HUGE
            mnemonics = huge
         enumRange
            name = Gigantic
            minValue = 137438953473
            setValue = 137438953473
            text = Gigantic (over 120 GB)
            defineToken = FREESPACE_GIGANTIC
            mnemonics = gigantic
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.FreeSpace
   shellPKey = PKEY_FreeSpace
   formatID = 9B174B35-40FF-11D2-A27E-00C04FC30871
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt64
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = Zero
            mnemonics = empty
         enumRange
            minValue = 1
            setValue = 1
            text = Tiny (0 - 2 GB)
            mnemonics = tiny
         enumRange
            minValue = 2147483649
            setValue = 2147483649
            text = Small (2 - 10 GB)
            mnemonics = small
         enumRange
            minValue = 10737418241
            setValue = 10737418241
            text = Medium (10 - 40 GB)
            mnemonics = medium
         enumRange
            minValue = 42949672961
            setValue = 42949672961
            text = Large (40 - 80 GB)
            mnemonics = large
         enumRange
            minValue = 85899345921
            setValue = 85899345921
            text = Huge (80 - 120 GB)
            mnemonics = huge
         enumRange
            minValue = 137438953473
            setValue = 137438953473
            text = Gigantic (over 120 GB)
            mnemonics = gigantic
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey.h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[Stringformat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[Datetimeformat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
