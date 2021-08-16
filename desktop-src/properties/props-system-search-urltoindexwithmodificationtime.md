---
description: Questa proprietà è uguale a System.Search.UrlToIndex, ad eccezione del fatto che include l'ora dell'ultima modifica dell'URL.
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: System.Search.UrlToIndexWithModificationTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7869005084379db1bdf288c6237a420666634c349eee47ca7942af2bb271a39d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118464771"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a>System.Search.UrlToIndexWithModificationTime

Questa proprietà è uguale a [**System.Search.UrlToIndex,**](props-system-search-urltoindex.md) ad eccezione del fatto che include l'ora dell'ultima modifica dell'URL. Si tratta di un'ottimizzazione per l'indicizzatore in modo che non sia necessario richiamare il gestore di protocollo per richiedere queste informazioni per determinare se il contenuto deve essere indicizzato nuovamente.

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

Questa [proprietà System.Search.UrlToIndexWithModificationTime]() corrisponde alla proprietà [System.Search.UrlToIndex,](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) ad eccezione del fatto che si passa anche l'ora dell'ultima modifica del documento. Se l'ora dell'ultima modifica corrisponde, l'indicizzatore presuppone che il documento sia già indicizzato e genera la notifica. Questa proprietà è un vettore con due elementi, un valore **\_ LPWSTR VT** che contiene l'URL e un valore **\_ FILETIME VT** che contiene l'ora dell'ultima modifica.

[System.Search.UrlToIndexWithModificationTime]() è stato chiamato PID \_ GTHR DIRLINK WITH TIME nelle versioni precedenti \_ \_ del Windows \_ operativo.

I valori PKEY sono definiti in Propkey.h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))
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

 

 
