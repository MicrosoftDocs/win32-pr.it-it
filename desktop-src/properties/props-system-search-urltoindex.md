---
description: Emesso da un IFilter del contenitore per ogni URL figlio all'interno del contenitore. Gli elementi figlio vengono infine sottoposti a ricerca per indicizzazione dall'indicizzatore se sono inclusi nell'ambito.
ms.assetid: e864b3fa-6d43-40fe-9556-474953098947
title: System. search. UrlToIndex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4832279237cb7a3659b37d6502bd853caff113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313473"
---
# <a name="systemsearchurltoindex"></a>System. search. UrlToIndex

Emesso da un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) del contenitore per ogni URL figlio all'interno del contenitore. Gli elementi figlio vengono infine sottoposti a ricerca per indicizzazione dall'indicizzatore se sono inclusi nell'ambito.

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

Questa proprietà contiene un URL e viene emessa da un gestore di protocollo per ogni URL figlio o directory nell'URL corrente. L'indicizzatore richiama il gestore di protocollo e richiede che il documento venga indicizzato. [System. search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) è stato chiamato PID \_ gthr \_ DIRLINK nelle versioni precedenti del sistema operativo Windows.

I valori PKEY sono definiti in Propkey. h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. search. UrlToIndexWithModificationTime](./props-system-search-urltoindexwithmodificationtime.md)
</dt> <dt>

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

 

 
