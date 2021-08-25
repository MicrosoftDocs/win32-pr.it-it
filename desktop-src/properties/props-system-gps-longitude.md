---
description: Indica la longitudine.
ms.assetid: ef28141f-1b63-4694-b6df-fcc11ce7e50b
title: System.GPS.Longitude
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12d65c2776c3740360c4cb298048621a877d58999eaddd6e219c682e5a0c9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010341"
---
# <a name="systemgpslongitude"></a>System.GPS.Longitude

Indica la longitudine. Si tratta di una matrice di tre valori, come indicato di seguito: Indice 0 è il gradi, indice 1 è il minuto, indice 2 è il secondo. Ognuno viene calcolato dai valori in PKEY \_ GPS \_ LongitudeNumerator e PKEY \_ GPS \_ LongitudeDenominator.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.GPS.Longitude
   shellPKey = PKEY_GPS_Longitude
   formatID = C4C4DBB2-B593-466B-BBDA-D03D27D5E43A
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="windows-7-windows-vista"></a>Windows 7, Windows Vista

```
propertyDescription
   name = System.GPS.Longitude
   shellPKey = PKEY_GPS_Longitude
   formatID = C4C4DBB2-B593-466B-BBDA-D03D27D5E43A
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Double
      IsInnate = true
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey.h.

È stato aggiunto il requisito di un riferimento a una stringa indiretta specifico per l'attributo `label` **di labelInfo** per Windows Vista con Service Pack 1 (SP1).

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

 

 
