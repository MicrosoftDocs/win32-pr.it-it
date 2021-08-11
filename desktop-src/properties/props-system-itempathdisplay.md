---
description: Informazioni sulla proprietà System.ItemPathDisplay, che rappresenta il percorso di visualizzazione descrittivo dell'elemento.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System.ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88a58d48740c6f7a2f9db0e496a951105c176ca7eba3dd205c2971188af7fd55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118231664"
---
# <a name="systemitempathdisplay"></a>System.ItemPathDisplay

Percorso di visualizzazione descrittivo dell'elemento.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemPathDisplay
   shellPKey = PKEY_ItemPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 7
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey.h.

Se l'elemento è un file o una cartella, questa proprietà include l'estensione in tutti i casi e viene localizzata se è disponibile un nome localizzato. Per altri elementi, si tratta dell'equivalente descrittivo, presupponendo che l'elemento esista nell'archiviazione gerarchica.

A [differenza di System.ItemUrl,](./props-system-itemurl.md)questo valore della proprietà non include lo schema URL. Per analizzare il percorso di un elemento, usare System.ItemUrl [o System.ParsingPath.](./props-system-parsingpath.md) Per fare riferimento agli elementi dello spazio dei nomi della shell usando le API shell, usare System.ParsingPath.

Valori di esempio



| Path                                   | ItemPathDisplay                        |
|----------------------------------------|----------------------------------------|
| c: \\ barra mydir \\ \\hello.txt              | c: \\ barra mydir \\ \\hello.txt              |
| \\\\condivisione \\ server \\ mydir \\goodnews.doc | \\\\condivisione \\ server \\ mydir \\goodnews.doc |
| \\\\condivisione \\ server \\numbers.xls         | \\\\condivisione \\ server \\numbers.xls         |
| c: \\ mydir \\ MyFolder                    | c: \\ mydir \\ MyFolder                    |
| /Mailbox Account/Inbox/'Re: Hello!'    | /Mailbox Account/Inbox/'Re: Hello!'    |



 

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

 

 
