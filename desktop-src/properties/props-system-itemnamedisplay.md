---
description: Nome visualizzato nel formato \# &0034;più completo&\# 0034;.
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f34e21c0ded147789cadccc99aaf9b2a1910398430419edacc498214c6489d77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119598471"
---
# <a name="systemitemnamedisplay"></a>System.ItemNameDisplay

Nome visualizzato nel formato "più completo". Si tratta della rappresentazione univoca del nome dell'elemento più appropriato per gli utenti finali.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.ItemNameDisplay
   shellPKey = PKEY_ItemNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 10
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey.h.

Questo valore è l'individuazione di [System.ItemNamePrefix](./props-system-itemnameprefix.md) e [System.ItemName](./props-system-itemname.md).

Se l'elemento è un file, questa proprietà include il nome visualizzato, come illustrato in Esplora file. Esistono casi accettabili quando [viene specificato System.FileName,](./props-system-filename.md) ma il valore di questa proprietà è completamente diverso. I messaggi di posta elettronica sono un buon esempio. Se l'elemento è un messaggio di posta elettronica, il nome dell'elemento è in genere l'oggetto. In tal caso, il valore deve essere la concatenazione di [System.ItemNamePrefix](./props-system-itemnameprefix.md) e [System.ItemName](./props-system-itemname.md). Poiché il valore di System.ItemNamePrefix esclude gli spazi finali, la concatenazione deve includere uno spazio durante la generazione di [System.ItemNameDisplay.]() Si noti che questa proprietà non è garantita come univoca, ma è progettata per promuovere il candidato più probabile che può essere univoco e ha anche senso per gli utenti finali.

Ad esempio, per i documenti, è possibile usare [System.Title](./props-system-title.md) come [System.ItemNameDisplay,]()ma in pratica il titolo dei documenti potrebbe non essere utile o sufficientemente univoco per funzionare come unico System.ItemNameDisplay. Al contrario, [fornire System.FileName](./props-system-filename.md) come valore di System.ItemNameDisplay è una scelta migliore. In Windows Posta elettronica la posta elettronica viene archiviata nel file system come file con estensione eml. I valori System.FileName per tali file non sono di facile uso perché sono GUID. In questo esempio, l'innalzamento [di livello di System.Subject](./props-system-subject.md) come System.ItemNameDisplay ha più senso.

**Note sulla compatibilità:**

-   Implementazioni della cartella shell in Windows Vista: usare PKEY ItemNameDisplay per la colonna name quando si vuole che Windows Explorer chiami \_ [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN NORMAL) per ottenere il valore del \_ nome. Usare un'altra chiave PKEY, ad esempio PKEY ItemName, quando si vuole che Windows Explorer chiami l'archivio delle proprietà della cartella o \_ [**IShellFolder2::GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) per ottenere il valore del nome.
-   Implementazioni della cartella shell Windows XP: la prima colonna deve essere la colonna name e Windows Explorer chiama [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) per ottenere il valore del nome. Il valore PKEY/SCID non è importante.



| Tipo di elemento     | Esempio                   |
|---------------|---------------------------|
| File          | hello.txt                 |
| Message       | Re: Dove si trova la riunione? |
| Cartella del dispositivo | song.wma                  |
| Cartella        | Documenti                 |



 

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

 

 
