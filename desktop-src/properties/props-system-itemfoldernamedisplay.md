---
description: Nome visualizzato descrittivo della cartella padre di un elemento.
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System. ItemFolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d637412b02345b52fee2e1c13e8f499314af4c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232500"
---
# <a name="systemitemfoldernamedisplay"></a>System. ItemFolderNameDisplay

Nome visualizzato descrittivo della cartella padre di un elemento.

Questa operazione deriva da [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md). Se la proprietà è VT \_ vuota, anche questa proprietà deve essere.

Se la cartella è una cartella di file, il valore verrà localizzato se è disponibile un nome localizzato.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemFolderNameDisplay
   shellPKey = PKEY_ItemFolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey. h.

Se [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) è un VT \_ vuoto, anche questa proprietà deve essere vuota. In caso contrario, deve essere derivato in modo appropriato dall'origine dati da System. ItemFolderPathDisplay.

Esempi:



| Percorso specificato                             | Nome visualizzato cartella |
|----------------------------------------|---------------------|
| c: \\ MyFile \\ testo \\hello.txt           | Testo                |
| \\\\\\condivisione server \\ mydir \\goodnews.doc | mydir               |
| \\\\\\numbers.xls condivisione \\ Server         | condividi               |
| c: \\ cartelle \\ cartella                  | Cartelle             |
| /Mailbox account/Inbox/' re: Hello!'    | Posta in arrivo               |



 

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

 

 
