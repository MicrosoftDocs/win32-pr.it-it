---
description: Nome descrittivo del tipo dell'elemento.
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System.ItemTypeText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f145aa2491f3352c4691be95c0e8ae16a75e8e0880732904e983fbf02c167dbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553751"
---
# <a name="systemitemtypetext"></a>System.ItemTypeText

Nome descrittivo del tipo dell'elemento. Questo valore non deve essere analizzato a livello di codice.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemTypeText
   shellPKey = PKEY_ItemTypeText
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 4
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey.h.

Se [System.ItemType](./props-system-itemtype.md) è VT EMPTY, anche il \_ valore di questa proprietà è VT \_ EMPTY. Se l'elemento è un file, il valore di questa proprietà è lo stesso di quello passato dal valore System.ItemType del file a [**PSFormatForDisplay.**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay)

Questa proprietà non deve essere confusa [con System.Kind,](./props-system-kind.md)che è un nome di tipo di alto livello e descrittivo. Ad esempio, per un .doc file di documento, le varie proprietà sono come illustrato di seguito:



| Proprietà                                               | Valore                   |
|--------------------------------------------------------|-------------------------|
| [System.Kind](./props-system-kind.md)                 | Documento                |
| [System.ItemType](./props-system-itemtype.md)         | doc                    |
| [System.ItemTypeText]() | Microsoft Word Documento |



 

Valori di esempio



| Percorso                                   | ItemTypeText            |
|----------------------------------------|-------------------------|
| c: \\ barra mydir \\ \\hello.txt              | File di testo               |
| \\\\condivisione \\ server \\ mydir \\goodnews.doc | Microsoft Word Documento |
| \\\\cartella \\ di condivisione \\ server              | Cartella file             |
| c: \\ MyDir \\ MyFolder                    | Cartella file             |
| /Mailbox Account/Inbox/'Re: Hello!'    | Outlook Messaggio di posta elettronica  |



 

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

 

 
