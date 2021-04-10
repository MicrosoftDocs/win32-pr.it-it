---
description: "Prefisso di un elemento, utilizzato per i messaggi di posta elettronica in cui l'oggetto inizia con il prefisso &\\# 0034; Re: &\\# 0034;."
ms.assetid: 3c257edc-b7f7-498d-8347-0be4fca41023
title: System. ItemNamePrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf669dd867c8cf60046f226e33dae18f46060cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966882"
---
# <a name="systemitemnameprefix"></a>System. ItemNamePrefix

Prefisso di un elemento, utilizzato per i messaggi di posta elettronica in cui l'oggetto inizia con il prefisso "Re:".

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemNamePrefix
   shellPKey = PKEY_ItemNamePrefix
   formatID = D7313FF1-A77A-401C-8C99-3DBDD68ADD36
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey. h.

Se l'elemento è un file, il valore di questa proprietà è VT \_ Empty. Se l'elemento è un messaggio, il valore di questa proprietà corrisponde ai prefissi di inoltro o di risposta (inclusi i due punti di delimitazione, ma senza spazi vuoti) o VT \_ vuoti se non è presente alcun prefisso.

Valori di esempio



| System. ItemNamePrefix | System. ItemName  | System.ItemNameDisplay |
|-----------------------|------------------|------------------------|
| VT \_ vuoto             | "Giorno splendido"      | "Giorno splendido"            |
| "Re:"                 | "Giorno splendido"      | "Re: grande giorno"        |
| "FWD:"               | "Budget mensile" | "FWD: budget mensile"  |
| VT \_ vuoto             | accounts.xls     | accounts.xls           |



 

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

 

 
