---
description: Spazio di archiviazione totale libero sul dispositivo, come percentuale.
ms.assetid: ede845c6-abd8-4bb1-b0d8-c1f3facffa41
title: System. Devices. StorageFreeSpacePercent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df717e488d1fabac811a2629a75160a2e7f81df9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967348"
---
# <a name="systemdevicesstoragefreespacepercent"></a>System. Devices. StorageFreeSpacePercent

Spazio di archiviazione totale libero sul dispositivo, come percentuale.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Devices.StorageFreeSpacePercent
   shellPKey = PKEY_Devices_StorageFreeSpacePercent
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 14
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = StorageSpaceFull
            minValue = 0
            setValue = 0
            text = Storage space full
            defineToken = STORAGESPACE_FULL
         enumRange
            name = 5PercentFree
            minValue = 5
            setValue = 5
            text = 5% free space
            defineToken = STORAGESPACE_5_PERCENT
         enumRange
            name = 10PercentFree
            minValue = 10
            setValue = 10
            text = 10% free space
            defineToken = STORAGESPACE_10_PERCENT
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey. h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
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

 

 
