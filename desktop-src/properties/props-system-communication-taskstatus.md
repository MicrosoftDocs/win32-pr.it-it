---
description: Indica lo stato corrente dell'attività.
ms.assetid: 76bb9bb7-3383-4e5a-ae75-a11c40f318e2
title: System.Communication.TaskStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982f0b1be8b4cd284f50d0132d9fda02fc434a226fba61fc8cc83ca046cd7f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970730"
---
# <a name="systemcommunicationtaskstatus"></a>System.Communication.TaskStatus

Indica lo stato corrente dell'attività.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Communication.TaskStatus
   shellPKey = PKEY_Communication_TaskStatus
   formatID = BE1A72C6-9A1D-46B7-AFE7-AFAF8CEF4999
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotStarted
            value = 0
            text = Not Started
            defineToken = TASKSTATUS_NOTSTARTED
         enum
            name = InProgress
            value = 1
            text = In Progress
            defineToken = TASKSTATUS_INPROGRESS
         enum
            name = Complete
            value = 2
            text = Complete
            defineToken = TASKSTATUS_COMPLETE
         enum
            name = Waiting
            value = 3
            text = Waiting
            defineToken = TASKSTATUS_WAITING
         enum
            name = Deferred
            value = 4
            text = Deferred
            defineToken = TASKSTATUS_DEFERRED
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Communication.TaskStatus
   shellPKey = PKEY_Communication_TaskStatus
   formatID = BE1A72C6-9A1D-46B7-AFE7-AFAF8CEF4999
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
            text = Not Started
            defineName = TASKSTATUS_NOTSTARTED
         enum
            value = 1
            text = In Progress
            defineName = TASKSTATUS_INPROGRESS
         enum
            value = 2
            text = Complete
            defineName = TASKSTATUS_COMPLETE
         enum
            value = 3
            text = Waiting
            defineName = TASKSTATUS_WAITING
         enum
            value = 4
            text = Deferred
            defineName = TASKSTATUS_DEFERRED
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

 

 
