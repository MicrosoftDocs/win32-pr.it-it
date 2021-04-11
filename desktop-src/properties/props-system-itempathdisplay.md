---
description: Percorso di visualizzazione intuitivo per l'elemento.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System. ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb76a4218e7e7580ec70cb57dd16c635ca024ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131574"
---
# <a name="systemitempathdisplay"></a>System. ItemPathDisplay

Percorso di visualizzazione intuitivo per l'elemento.

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

I valori PKEY sono definiti in Propkey. h.

Se l'elemento è un file o una cartella, questa proprietà include l'estensione in tutti i casi ed è localizzata se è disponibile un nome localizzato. Per gli altri elementi, questo è l'equivalente intuitivo, supponendo che l'elemento esista nell'archivio gerarchico.

Diversamente da [System. ItemUrl](./props-system-itemurl.md), il valore di questa proprietà non include lo schema URL. Per analizzare un percorso di elemento, usare System. ItemUrl o [System. ParsingPath](./props-system-parsingpath.md). Per fare riferimento agli elementi dello spazio dei nomi della shell usando le API della shell, usare System. ParsingPath.

Valori di esempio



| Percorso                                   | ItemPathDisplay                        |
|----------------------------------------|----------------------------------------|
| c: \\ \\hello.txt della barra mydir \\              | c: \\ \\hello.txt della barra mydir \\              |
| \\\\\\condivisione server \\ mydir \\goodnews.doc | \\\\\\condivisione server \\ mydir \\goodnews.doc |
| \\\\\\numbers.xls condivisione \\ Server         | \\\\\\numbers.xls condivisione \\ Server         |
| c: \\ mydir \\ cartella                    | c: \\ mydir \\ cartella                    |
| /Mailbox account/Inbox/' re: Hello!'    | /Mailbox account/Inbox/' re: Hello!'    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

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

 

 
