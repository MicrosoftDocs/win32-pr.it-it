---
description: Informazioni sulla proprietà System.ItemFolderPathDisplay, che rappresenta il percorso di visualizzazione descrittivo della cartella padre di un elemento.
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System.ItemFolderPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8fd2288f12073fe8e36707bf49aca2bc5e000d0bbe25d95fba0736b4e77af44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822341"
---
# <a name="systemitemfolderpathdisplay"></a>System.ItemFolderPathDisplay

Percorso di visualizzazione descrittivo della cartella padre di un elemento.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemFolderPathDisplay
   shellPKey = PKEY_ItemFolderPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 6
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey.h.

Se [System.ItemPathDisplay è](./props-system-itempathdisplay.md) VT \_ EMPTY, anche questa proprietà deve essere vuota. In caso contrario, deve essere derivato in modo appropriato dall'origine dati da System.ItemPathDisplay.

Valori di esempio



| Percorso                                   | ItemFolderPathDisplay    |
|----------------------------------------|--------------------------|
| c: \\ file \\ personali \\hello.txt         | c: \\ file \\ personali      |
| \\\\condivisione \\ server \\ mydir \\goodnews.doc | \\\\condivisione \\ server \\ mydir |
| \\\\condivisione \\ \\ servernumbers.xls         | \\\\condivisione \\ server        |
| c: \\ food \\ MyFolder                     | c: \\ food                 |
| /Mailbox Account/Inbox/'Re: Hello!'    | /Account cassetta postale/Posta in arrivo   |



 

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

 

 
