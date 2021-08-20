---
description: Generato da un filtro IFilter del contenitore per ogni URL figlio all'interno del contenitore. Gli elementi figlio vengono infine sottoposti a ricerca per indicizzazione dall'indicizzatore se sono all'interno dell'ambito.
ms.assetid: e864b3fa-6d43-40fe-9556-474953098947
title: System.Search.UrlToIndex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb964f146831561174f3713d5b827a2c736c59f93e034ac8494f86a0fc6584bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117864767"
---
# <a name="systemsearchurltoindex"></a>System.Search.UrlToIndex

Generato da un filtro [**IFilter del contenitore**](/windows/win32/api/filter/nn-filter-ifilter) per ogni URL figlio all'interno del contenitore. Gli elementi figlio vengono infine sottoposti a ricerca per indicizzazione dall'indicizzatore se sono all'interno dell'ambito.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.UrlToIndex
   shellPKey = PKEY_Search_UrlToIndex
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
```

## <a name="remarks"></a>Commenti

Questa proprietà contiene un URL e viene generata da un gestore di protocollo per ogni URL figlio o directoy nell'URL corrente. L'indicizzatore richiama il gestore di protocollo e chiede l'indicizzazione del documento. [System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) è stato chiamato PID \_ GTHR \_ DIRLINK nelle versioni precedenti del Windows operativo.

I valori PKEY sono definiti in Propkey.h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Search.UrlToIndexWithModificationTime](./props-system-search-urltoindexwithmodificationtime.md)
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

 

 
