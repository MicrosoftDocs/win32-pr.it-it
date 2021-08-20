---
description: Valore di luminosità dell'immagine, in unità APEX, in genere compreso tra -99,99 e 99,99.
ms.assetid: 533f6934-dec8-455a-937c-d4e144be4335
title: System.Photo.Brightness
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d28d49464b5d5d081869e514a92fe892a95c1f5a2608412513a2a18b46a51f62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033349"
---
# <a name="systemphotobrightness"></a>System.Photo.Brightness

Valore di luminosità dell'immagine, in unità APEX, in genere compreso tra -99,99 e 99,99.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Photo.Brightness
   shellPKey = PKEY_Photo_Brightness
   formatID = 1A701BF6-478C-4361-83AB-3701BB053C58
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Double
      IsInnate = true
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey.h.

Vedere la specifica EXIF 2.2, allegato C, per un confronto tra [i numeri di System.Photo.Brightness]() e Foot-Lambert misurazioni. Questa proprietà viene calcolata da [System.Photo.BrightnessNumerator](./props-system-photo-brightnessnumerator.md) e [System.Photo.BrightnessDenominator](./props-system-photo-brightnessdenominator.md). Se il numeratore del valore registrato è FFFFFFFF. H, deve essere indicato "Sconosciuto".

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Exchangeable Image File Format per fotocamere digitali: Exif versione 2.2](https://www.exif.org/Exif2-2.PDF)
</dt> <dt>

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

 

 
