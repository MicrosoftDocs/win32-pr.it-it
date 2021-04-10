---
description: 'Stato di un flag. Values: (0 = None 1 = white 2 = Red).'
ms.assetid: 0485deab-2408-4147-acaa-cb09e9e0032a
title: System. FlagStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57dde42493f2d450854c3f53de5ecab26394f0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227296"
---
# <a name="systemflagstatus"></a>System. FlagStatus

Stato di un flag. Values: (0 = None 1 = white 2 = Red).

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.FlagStatus
   shellPKey = PKEY_FlagStatus
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Int32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotFlagged
            value = 0
            text = Not flagged
            defineToken = FLAGSTATUS_NOTFLAGGED
            mnemonics = Unflagged
         enum
            name = Completed
            value = 1
            text = Completed
            defineToken = FLAGSTATUS_COMPLETED
         enum
            name = FollowUp
            value = 2
            text = Follow Up
            defineToken = FLAGSTATUS_FOLLOWUP
            mnemonics = Followup Flag|followup|follow
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.FlagStatus
   shellPKey = PKEY_FlagStatus
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 12
   SearchInfo
      IsColumn = true
   typeInfo
      type = Int32
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Not flagged
            defineName = FLAGSTATUS_NOTFLAGGED
            mnemonics = Unflagged
         enum
            value = 1
            text = Completed
            defineName = FLAGSTATUS_COMPLETED
         enum
            value = 2
            text = Follow Up
            defineName = FLAGSTATUS_FOLLOWUP
            mnemonics = Followup Flag|followup|follow
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

 

 
