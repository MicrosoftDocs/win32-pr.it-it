---
description: Nome del file, inclusa l'estensione.
ms.assetid: 40940026-6c67-4196-aff6-5f846dc94f27
title: System. FileName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8f535eff4625178b3c32a04ea6d325505266a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311398"
---
# <a name="systemfilename"></a>System. FileName

Nome del file, inclusa l'estensione. System. FileExtension deriva da questa proprietà.

È possibile che l'elemento non esista in un file System (ovvero, potrebbe non essere aperto con CreateFile). Tuttavia, se l'elemento è rappresentato come un file e il nome segue la sintassi standard di denominazione dei file Win32, l'origine dati deve emettere questa proprietà. Se l'elemento non è un file, l'origine dati deve emettere questa proprietà come VT \_ Empty.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = 0-9
         enumRange
            minValue = A
            setValue = A
            text = A-H
         enumRange
            minValue = I
            setValue = I
            text = I-P
         enumRange
            minValue = Q
            setValue = Q
            text = Q-Z
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey. h.

L'elemento potrebbe non esistere in un file System (ovvero, potrebbe non essere aperto utilizzando CreateFile), ma se l'elemento è rappresentato come file dal senso logico e il nome segue la sintassi standard per la denominazione dei file Win32, l'origine dati deve emettere questa proprietà. Se un elemento non è un file, il valore di questa proprietà è VT \_ Empty. Vedere System. ItemNameDisplay. Ha lo stesso valore di System. ParsingName per gli elementi forniti dalla cartella di file della shell.

Nella tabella seguente sono elencati esempi di valori di proprietà Path e FileName:



| Percorso                               | Valore della proprietà |
|------------------------------------|----------------|
| c: \\ file \\ personali \\hello.txt     | hello.txt      |
| \\\\\\condivisione server \\ mydir \\news.doc | news.doc       |
| \\\\\\numbers.xls condivisione \\ Server     | numbers.xls    |
| c: \\ Stuff \\ cartella                | MyFolder       |
| \[Messaggio di posta elettronica\]                  | VT \_ vuoto      |
| \[Song. WMA sul dispositivo portatile\]    | Song. WMA       |



 

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

 

 
