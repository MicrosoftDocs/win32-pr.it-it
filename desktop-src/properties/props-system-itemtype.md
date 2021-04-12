---
description: Tipo canonico dell'elemento.
ms.assetid: 530ba98a-09fd-438b-8872-9eee47f0cf54
title: System. ItemType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0159a12e1cc3c6d85e461461cad20334a641fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233580"
---
# <a name="systemitemtype"></a>System. ItemType

Tipo canonico dell'elemento.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemType
   shellPKey = PKEY_ItemType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 11
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey. h.

Il valore di System. ItemType deve essere analizzato a livello di codice e può essere uno dei seguenti:

-   Estensione di file che punta a un valore ProgID ( \_ radice delle classi HKEY) che \_ \\ <ProgID> contiene il nome visualizzato per il tipo.
-   Valore ProgID (classi HKEY \_ \_ RROOT \\ <ProgID> ), contenente il nome visualizzato per il tipo.

L'elemento FriendlyTypeName di un ProgID deve essere una versione localizzata del nome dell'applicazione ( @winword.dll ,-42), mentre il valore predefinito della chiave ProgID è un nome non localizzato (Word.Document. 12).

Se non è presente alcun tipo canonico, il valore è VT \_ vuoto. Se l'elemento è un file ([System. FileName](./props-system-filename.md) non è un VT \_ vuoto), il valore corrisponde a [System. FileExtension](./props-system-fileextension.md). Utilizzare [System. ItemTypeText](./props-system-itemtypetext.md) quando si desidera visualizzare il tipo agli utenti finali in una vista.

> [!Note]  
> Se l'elemento è un file, il passaggio del valore [System. ItemType]() a [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) restituisce lo stesso valore di [System. ItemTypeText](./props-system-itemtypetext.md).

 

Valori di esempio



| Percorso                                   | ItemType         |
|----------------------------------------|------------------|
| c: \\ \\hello.txt della barra mydir \\              | .txt             |
| \\\\\\condivisione server \\ mydir \\goodnews.doc | doc             |
| \\\\\\cartella condivisione \\ Server              | Directory        |
| c: \\ mydir \\ cartella                    | Directory        |
| \[desktop\]                            | Cartella           |
| /Mailbox account/Inbox/' re: Hello!'    | MAPI/IPM. Messaggio |



 

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
</dt> <dt>

[Identificatori a livello di codice](../shell/fa-progids.md)
</dt> </dl>

 

 
