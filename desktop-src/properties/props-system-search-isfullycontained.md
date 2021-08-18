---
description: Generato come TRUE da tutti gli elementi figlio di un contenitore (ad esempio un messaggio di posta elettronica o un file compresso con estensione .zip) che genera System.Search.IsClosedDirectory come TRUE. Ciò garantisce che gli elementi figlio siano inclusi nell'indice di ricerca.
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: System.Search.IsFullyContained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce7f325be26abdb81dcb51da7018f6da786e6ec5f3a31111e4ae3823acf8c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117864990"
---
# <a name="systemsearchisfullycontained"></a>System.Search.IsFullyContained

Generato come **TRUE** da tutti gli elementi figlio di un contenitore (ad esempio un messaggio di posta elettronica o un file compresso con estensione .zip) che genera [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) **come TRUE**. Ciò garantisce che gli elementi figlio siano inclusi nell'indice di ricerca.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.IsFullyContained
   shellPKey = PKEY_Search_IsFullyContained
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 24
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey.h.

La [proprietà System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) consente di ottimizzare le prestazioni dell'indicizzatore consentendo all'indicizzatore di ignorare l'enumerazione degli elementi figlio di un contenitore. Tali elementi figlio, tuttavia, sono contrassegnati dall'indicizzatore come non visitati e di conseguenza verranno eliminati dall'indice. [Emettendo System.Search.IsFullyContained]() **come TRUE,** un elemento non viene eliminato dall'indice nonostante non sia stato visitato.

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

 

 
