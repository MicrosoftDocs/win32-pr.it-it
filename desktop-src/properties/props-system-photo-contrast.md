---
description: Indica la direzione di elaborazione del contrasto applicata dalla fotocamera quando è stata scattata l'immagine. &\#0034;0&\# 0034; indica &\# 0034; Normale&\# 0034;; &\# 0034;1&\# 0034; indica &\# 0034; Soft&\# 0034;; &\# 0034;2&\# 0034; indica &\# 0034; Hard&\# 0034;.
ms.assetid: 32f89149-b90d-4fe9-9d1a-b8bb966d62fe
title: System.Photo.Contrast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 847eadd54e82ebed60f947b5aac994ad8e2e69c44d82246c8e65ccb70adf0675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118230371"
---
# <a name="systemphotocontrast"></a>System.Photo.Contrast

Indica la direzione di elaborazione del contrasto applicata dalla fotocamera quando è stata scattata l'immagine. "0" indica "Normal"; "1" indica "Soft"; "2" indica "Hard".

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Photo.Contrast
   shellPKey = PKEY_Photo_Contrast
   formatID = 2A785BA9-8D23-4DED-82E6-60A350C86A10
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Normal
            value = 0
            text = Normal
            defineToken = PHOTO_CONTRAST_NORMAL
         enum
            name = Soft
            value = 1
            text = Soft
            defineToken = PHOTO_CONTRAST_SOFT
         enum
            name = Hard
            value = 2
            text = Hard
            defineToken = PHOTO_CONTRAST_HARD
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Photo.Contrast
   shellPKey = PKEY_Photo_Contrast
   formatID = 2A785BA9-8D23-4DED-82E6-60A350C86A10
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Normal
            defineName = PHOTO_CONTRAST_NORMAL
         enum
            value = 1
            text = Soft
            defineName = PHOTO_CONTRAST_SOFT
         enum
            value = 2
            text = Hard
            defineName = PHOTO_CONTRAST_HARD
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

 

 
