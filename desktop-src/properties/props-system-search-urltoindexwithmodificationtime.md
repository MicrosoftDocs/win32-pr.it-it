---
description: Questa proprietà corrisponde a System. search. UrlToIndex con la differenza che include l'ora dell'Ultima modifica apportata all'URL.
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: System. search. UrlToIndexWithModificationTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fcc83b9796ae2375f10235a08ba0db313fb1958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316879"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a>System. search. UrlToIndexWithModificationTime

Questa proprietà corrisponde a [**System. search. UrlToIndex**](props-system-search-urltoindex.md) con la differenza che include l'ora dell'Ultima modifica apportata all'URL. Si tratta di un'ottimizzazione per l'indicizzatore, in modo da non dover richiamarlo nel gestore di protocollo per richiedere queste informazioni per determinare se il contenuto deve essere indicizzato nuovamente.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.UrlToIndexWithModificationTime
   shellPKey = PKEY_Search_UrlToIndexWithModificationTime
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Any
```

## <a name="remarks"></a>Commenti

Questa proprietà [System. search. UrlToIndexWithModificationTime]() equivale alla proprietà [System. search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) , con la differenza che si passa anche l'ora dell'Ultima modifica del documento. Se l'ora dell'Ultima modifica corrisponde, l'indicizzatore presuppone che il documento sia già indicizzato e genera la notifica. Questa proprietà è un vettore con due elementi, un valore **VT \_ LPWSTR** che contiene l'URL e un valore di **\_ FILETIME VT** che contiene l'ora dell'Ultima modifica.

[System. search. UrlToIndexWithModificationTime]() è stato chiamato PID \_ gthr \_ DIRLINK \_ con \_ il tempo nelle versioni precedenti del sistema operativo Windows.

I valori PKEY sono definiti in Propkey. h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System. search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))
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

 

 
