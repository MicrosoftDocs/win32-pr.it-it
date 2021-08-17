---
description: Indica se il dispositivo è in roaming.
ms.assetid: d2382e96-7ca4-42e4-8e5b-89f1da736904
title: System.Devices.Roaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2f13e9de3eb6c4b1d71bcfc0ac541ea5311cdf7160c3f18c0711aa3f76993ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119097200"
---
# <a name="systemdevicesroaming"></a>System.Devices.Roaming

Indica se il dispositivo è in roaming.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Devices.Roaming
   shellPKey = PKEY_Devices_Roaming
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = NotRoaming
            minValue = 0
            setValue = 0
            text = Not roaming
            defineToken = ROAMING_NOT_ROAMING
         enumRange
            name = Roaming
            minValue = 1
            setValue = 1
            text = Roaming
            defineToken = ROAMING_ROAMING
         enumRange
            name = UnknownStatus
            minValue = 2
            setValue = 2
            text = Unknown roaming status
            defineToken = ROAMING_UNKNOWN_STATUS
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey.h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[proprietàDescrizione](./propdesc-schema-propertydescription.md)
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

[DrawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
