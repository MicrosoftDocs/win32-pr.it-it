---
description: Nome visualizzato descrittivo della cartella padre di un elemento.
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System.ItemFolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c8e8ca12af7c7665a2fd4b64f2911a1e6dbc99805cf4355ea1bb1ceec764c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119945171"
---
# <a name="systemitemfoldernamedisplay"></a>System.ItemFolderNameDisplay

Nome visualizzato descrittivo della cartella padre di un elemento.

Deriva da [System.ItemFolderPathDisplay.](./props-system-itemfolderpathdisplay.md) Se la proprietà è VT \_ EMPTY, anche questa proprietà deve essere .

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

I valori PKEY sono definiti in Propkey.h.

Se [System.ItemFolderPathDisplay è](./props-system-itemfolderpathdisplay.md) VT \_ EMPTY, anche questa proprietà deve essere vuota. In caso contrario, deve essere derivato in modo appropriato dall'origine dati da System.ItemFolderPathDisplay.

Esempi:



| Percorso specificato                             | Nome visualizzato cartella |
|----------------------------------------|---------------------|
| c: \\ MyFiles \\ Text \\hello.txt           | Testo                |
| \\\\condivisione \\ server \\ mydir \\goodnews.doc | mydir               |
| \\\\condivisione \\ \\ servernumbers.xls         | condividi               |
| c: \\ Cartelle \\ Cartella                  | Cartelle             |
| /Mailbox Account/Inbox/'Re: Hello!'    | Posta in arrivo               |



 

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

 

 
