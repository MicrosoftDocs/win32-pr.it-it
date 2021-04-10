---
description: Nome descrittivo del tipo dell'elemento.
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System. ItemTypeText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699a953392054cb2344c5f3b3d652e64a9a2c1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227273"
---
# <a name="systemitemtypetext"></a>System. ItemTypeText

Nome descrittivo del tipo dell'elemento. Questo valore non può essere analizzato a livello di codice.

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

I valori PKEY sono definiti in Propkey. h.

Se [System. ItemType](./props-system-itemtype.md) è VT \_ vuoto, anche il valore di questa proprietà è VT \_ Empty. Se l'elemento è un file, il valore di questa proprietà è uguale a quello di se il valore System. ItemType del file è stato passato a [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).

Questa proprietà non deve essere confusa con [System. Kind](./props-system-kind.md), che è un nome di tipo di alto livello descrittivo. Per un file di documento con estensione doc, ad esempio, le varie proprietà sono illustrate di seguito:



| Proprietà                                               | Valore                   |
|--------------------------------------------------------|-------------------------|
| [System. Kind](./props-system-kind.md)                 | Documento                |
| [System. ItemType](./props-system-itemtype.md)         | doc                    |
| [System. ItemTypeText]() | Documento di Microsoft Word |



 

Valori di esempio



| Percorso                                   | ItemTypeText            |
|----------------------------------------|-------------------------|
| c: \\ \\hello.txt della barra mydir \\              | File di testo               |
| \\\\\\condivisione server \\ mydir \\goodnews.doc | Documento di Microsoft Word |
| \\\\\\cartella condivisione \\ Server              | Cartella di file             |
| c: \\ mydir \\ cartella                    | Cartella di file             |
| /Mailbox account/Inbox/' re: Hello!'    | Messaggio di posta elettronica di Outlook  |



 

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

 

 
