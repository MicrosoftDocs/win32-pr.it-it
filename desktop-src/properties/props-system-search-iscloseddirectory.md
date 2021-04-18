---
description: Generato come TRUE da un elemento contenitore per indicare che i relativi elementi figlio non devono essere enumerati da un indicizzatore se l'elemento contenitore non è stato modificato dopo l'ultima ricerca per indicizzazione di verifica indicizzazione.
ms.assetid: 8bb487b9-4a51-4a6b-939e-946a8aad85de
title: System. search. IsClosedDirectory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea97aeb8d0192eea7d71ca65fd0ec109780702f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316881"
---
# <a name="systemsearchiscloseddirectory"></a>System. search. IsClosedDirectory

Generato come **true** da un elemento contenitore per indicare che i relativi elementi figlio non devono essere enumerati da un indicizzatore se l'elemento contenitore non è stato modificato dopo l'ultima ricerca per indicizzazione di verifica indicizzazione. Ciò contribuisce all'ottimizzazione delle prestazioni dell'indicizzatore. In questi casi di contenitori (ad esempio un messaggio di posta elettronica con allegati o un file compresso con estensione zip), gli elementi figlio sono inseparabili dal relativo elemento padre. Ad esempio, se la proprietà [System. DateModified](./props-system-datemodified.md) di un elemento contenuto cambia, il valore System. DateModified del contenitore viene modificato in modo che corrisponda. Inoltre, se un elemento padre viene eliminato, vengono eliminati anche tutti gli elementi figlio. Se pertanto il contenitore non è stato modificato, l'indicizzatore sa che non è stato modificato alcun elemento al suo interno e non è necessario aprire il contenitore per esaminare il contenuto singolarmente.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.IsClosedDirectory
   shellPKey = PKEY_Search_IsClosedDirectory
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey. h.

> [!IMPORTANT]
> Se un elemento genera **true** per questa proprietà, ognuno dei relativi elementi figlio deve creare la proprietà [System. search. IsFullyContained](./props-system-search-isfullycontained.md) su **true** per impedire che tali elementi vengano eliminati dall'indice.

 

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

 

 
