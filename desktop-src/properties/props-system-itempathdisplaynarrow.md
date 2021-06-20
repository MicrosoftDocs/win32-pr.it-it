---
description: Informazioni sulla proprietà System.ItemPathDisplayNarrow, che rappresenta il percorso di visualizzazione descrittivo dell'elemento.
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System.ItemPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84455a8b69ebf42cb91c191d1c275b70eeeb5ac
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403894"
---
# <a name="systemitempathdisplaynarrow"></a>System.ItemPathDisplayNarrow

Percorso di visualizzazione descrittivo dell'elemento.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemPathDisplayNarrow
   shellPKey = PKEY_ItemPathDisplayNarrow
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey.h.

Per ottimizzare una colonna di visualizzazione ridotta, il formato della stringa deve essere personalizzato in modo che il nome venga visualizzato per primo.

Se l'elemento è un file, il valore della proprietà esclude l'estensione di file, ma include i nomi localizzati, se presenti. Se l'elemento è un messaggio, il valore include [System.ItemNamePrefix.](./props-system-itemnameprefix.md) Per analizzare il percorso di un elemento, [usare System.ItemUrl](./props-system-itemurl.md) [o System.ParsingPath.](./props-system-parsingpath.md)

Valori di esempio



| Percorso                                   | ItemPathDisplayName                 |
|----------------------------------------|-------------------------------------|
| c: \\ barra mydir \\ \\hello.txt              | hello (c: \\ barra \\ mydir)              |
| \\\\condivisione \\ server \\ mydir \\goodnews.doc | goodnews \\ \\ (condivisione \\ server \\ mydir) |
| \\\\cartella \\ di condivisione \\ server              | folder \\ \\ (condivisione \\ server)          |
| c: \\ MyDir \\ MyFolder                    | Cartella (c: \\ mydir)                |
| /Mailbox Account/Inbox/'Re: Hello!'    | Re: Hello! (/Account cassetta postale/Posta in arrivo) |



 

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

 

 
