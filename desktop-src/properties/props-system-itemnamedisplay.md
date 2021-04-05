---
description: Nome visualizzato nel form &\# 0034; più completo&\# 0034;.
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf735935ee7971acad7d11ee91636e18a6542252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753111"
---
# <a name="systemitemnamedisplay"></a>System.ItemNameDisplay

Nome visualizzato nel form "più completo". Si tratta della rappresentazione univoca del nome dell'elemento più appropriato per gli utenti finali.

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

I valori PKEY sono definiti in Propkey. h.

Questo valore è concatentation di [System. ItemNamePrefix](./props-system-itemnameprefix.md) e [System. ItemName](./props-system-itemname.md).

Se l'elemento è un file, questa proprietà include il nome visualizzato, come illustrato in Esplora file. Esistono casi accettabili quando [System. FileName](./props-system-filename.md) viene specificato, ma il valore di questa proprietà è completamente diverso. I messaggi di posta elettronica rappresentano un valido esempio. Se l'elemento è un messaggio di posta elettronica, il nome dell'elemento corrisponde in genere al soggetto. In tal caso, il valore deve essere la concatenazione di [System. ItemNamePrefix](./props-system-itemnameprefix.md) e [System. ItemName](./props-system-itemname.md). Poiché il valore di System. ItemNamePrefix esclude tutti gli spazi finali, la concatenazione deve includere uno spazio durante la generazione di [System. ItemNameDisplay](). Si noti che questa proprietà non è necessariamente univoca, ma è progettata per promuovere la candidatura più probabile che può essere univoca e anche sensata per gli utenti finali.

Per i documenti, ad esempio, è possibile usare [System. title](./props-system-title.md) come [System. ItemNameDisplay](), ma in pratica il titolo dei documenti potrebbe non essere utile o sufficientemente univoco per funzionare come unico System. ItemNameDisplay. È invece preferibile fornire [System. FileName](./props-system-filename.md) come valore di System. ItemNameDisplay. In Windows Mail, i messaggi di posta elettronica vengono archiviati nel file system file con estensione eml. I valori System. FileName per questi file non sono intuitivi perché sono GUID. In questo esempio la promozione di [System. Subject](./props-system-subject.md) come System. ItemNameDisplay risulta più sensata.

**Note sulla compatibilità:**

-   Implementazioni di cartelle della shell in Windows Vista: usare PKEY \_ ItemNameDisplay per la colonna Name quando si desidera che Esplora risorse chiami [**IShellFolder:: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN \_ Normal) per ottenere il valore del nome. Utilizzare un altro PKEY, ad esempio PKEY \_ itemName, quando si desidera che Esplora risorse chiami l'archivio delle proprietà della cartella o [**IShellFolder2:: GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) per ottenere il valore del nome.
-   Implementazioni di cartelle della shell in Windows XP: la prima colonna deve essere la colonna Name e Esplora risorse chiama [**IShellFolder:: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) per ottenere il valore del nome. PKEY/SCID non è rilevante.



| Tipo di elemento     | Esempio                   |
|---------------|---------------------------|
| File          | hello.txt                 |
| Message       | Re: dove si trova la riunione? |
| Cartella del dispositivo | Song. WMA                  |
| Cartella        | Documenti                 |



 

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

 

 
