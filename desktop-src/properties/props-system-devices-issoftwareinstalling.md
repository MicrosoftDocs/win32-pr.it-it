---
description: Se VARIANT \_ TRUE, il programma di installazione del dispositivo sta attualmente installando il software.
ms.assetid: 7C62C1E3-D3F3-49ce-A19D-B3A1C14E24D6
title: System.Devices.IsSoftwareInstalling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 603e011e525e5d56dfe524c7875d87f77d639167190d6671e679feda4312d29c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117866709"
---
# <a name="systemdevicesissoftwareinstalling"></a>System.Devices.IsSoftwareInstalling

Se VARIANT \_ TRUE, il programma di installazione del dispositivo sta attualmente installando il software.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.Devices.IsSoftwareInstalling
   shellPKey = PKEY_Devices_IsSoftwareInstalling
   formatID = 83DA6326-97A6-4088-9453-A1923F573B29
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = SoftwareInstalling
            value = #TRUE#
            text = Device setup in progress
            defineToken = ISSOFTWAREINSTALLING_INSTALLING
```

## <a name="windows-7"></a>Windows 7

```
propertyDescription
   name = System.Devices.IsSoftwareInstalling
   shellPKey = PKEY_Devices_IsSoftwareInstalling
   formatID = 83DA6326-97A6-4088-9453-A1923F573B29
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = SoftwareInstalling
            value = #TRUE#
            text = Software is installing for this device
            defineToken = ISSOFTWAREINSTALLING_INSTALLING
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

 

 
