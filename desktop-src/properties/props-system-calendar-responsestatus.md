---
description: Archivia lo stato delle risposte di un utente alle riunioni nel calendario.
ms.assetid: 5cbc0306-20c7-4f12-bb8b-3889b93dfd69
title: System. Calendar. ResponseStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7af8f69d177dba751ead02a0ee71f5ea4a42ae4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131095"
---
# <a name="systemcalendarresponsestatus"></a>System. Calendar. ResponseStatus

Archivia lo stato delle risposte di un utente alle riunioni nel calendario.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Calendar.ResponseStatus
   shellPKey = PKEY_Calendar_ResponseStatus
   formatID = 188C1F91-3C40-4132-9EC5-D8B03B72A8A2
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = None
            value = 0
            text = None
            defineToken = CALENDAR_RESPONSESTATUS_NONE
         enum
            name = Organized
            value = 1
            text = Organized
            defineToken = CALENDAR_RESPONSESTATUS_ORGANIZED
         enum
            name = Tentative
            value = 2
            text = Tentative
            defineToken = CALENDAR_RESPONSESTATUS_TENTATIVE
         enum
            name = Accepted
            value = 3
            text = Accepted
            defineToken = CALENDAR_RESPONSESTATUS_ACCEPTED
         enum
            name = Declined
            value = 4
            text = Declined
            defineToken = CALENDAR_RESPONSESTATUS_DECLINED
         enum
            name = NotResponded
            value = 5
            text = Not Responded
            defineToken = CALENDAR_RESPONSESTATUS_NOTRESPONDED
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Calendar.ResponseStatus
   shellPKey = PKEY_Calendar_ResponseStatus
   formatID = 188C1F91-3C40-4132-9EC5-D8B03B72A8A2
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = None
            defineName = CALENDAR_RESPONSESTATUS_NONE
         enum
            value = 1
            text = Organized
            defineName = CALENDAR_RESPONSESTATUS_ORGANIZED
         enum
            value = 2
            text = Tentative
            defineName = CALENDAR_RESPONSESTATUS_TENTATIVE
         enum
            value = 3
            text = Accepted
            defineName = CALENDAR_RESPONSESTATUS_ACCEPTED
         enum
            value = 4
            text = Declined
            defineName = CALENDAR_RESPONSESTATUS_DECLINED
         enum
            value = 5
            text = Not Responded
            defineName = CALENDAR_RESPONSESTATUS_NOTRESPONDED
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

 

 
