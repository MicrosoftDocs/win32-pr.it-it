---
description: Identifica l'estensione di file dell'elemento basato su file, incluso il punto iniziali.
ms.assetid: b72c695e-bdbd-471d-b902-9e30a62facd4
title: System. FileExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8792a3965c394a1944985515df527e41e3a159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311400"
---
# <a name="systemfileextension"></a>System. FileExtension

Identifica l'estensione di file dell'elemento basato su file, incluso il punto iniziali. Questa proprietà è derivata da System. FileName. Se System. FileName non ha un'estensione di file o è un VT \_ vuoto, il valore di questa proprietà deve essere VT \_ vuoto.

Per ottenere il tipo di qualsiasi elemento (incluso un elemento che non è un file), usare System. ItemType.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.FileExtension
   shellPKey = PKEY_FileExtension
   formatID = E4F10A3C-49E6-405D-8288-A23BD4EEAA6C
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey. h.

Se [System. FileName](./props-system-filename.md) è VT \_ vuoto, anche questa proprietà deve essere vuota. In caso contrario, questa proprietà deve essere derivata in modo appropriato dall'origine dati da System. FileName. Se System. FileName non include un'estensione di file, [System. FileExtension]() deve essere un VT \_ vuoto. Per ottenere il tipo di qualsiasi elemento (incluso un elemento che non è un file), usare [System. ItemType](./props-system-itemtype.md).

Esempi di proprietà di estensione di file e percorso. 

| Percorso                               | Estensione nome del file |
|------------------------------------|----------------|
| c: \\ file \\ personali \\hello.txt     | .txt           |
| \\\\\\condivisione server \\ mydir \\news.doc | doc           |
| \\\\\\numbers.xls condivisione \\ Server     | xls           |
| \\\\\\cartella condivisione \\ Server          | VT \_ vuoto      |
| c: \\ Stuff \\ cartella                | VT \_ vuoto      |
| \[desktop\]                        | VT \_ vuoto      |



 

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

 

 
