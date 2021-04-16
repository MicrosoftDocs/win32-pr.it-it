---
description: Emesso come TRUE da tutti gli elementi figlio di un contenitore, ad esempio un messaggio di posta elettronica o un file compresso con estensione zip, che genera System. search. IsClosedDirectory come TRUE. In questo modo si garantisce che gli elementi figlio siano inclusi nell'indice di ricerca.
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: System. search. IsFullyContained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1245f29a2940146a4e5d8f0a392210173be75e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530049"
---
# <a name="systemsearchisfullycontained"></a>System. search. IsFullyContained

Emesso come **true** da tutti gli elementi figlio di un contenitore, ad esempio un messaggio di posta elettronica o un file compresso con estensione zip, che genera [System. search. IsClosedDirectory](./props-system-search-iscloseddirectory.md) come **true**. In questo modo si garantisce che gli elementi figlio siano inclusi nell'indice di ricerca.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.IsFullyContained
   shellPKey = PKEY_Search_IsFullyContained
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 24
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey. h.

La proprietà [System. search. IsClosedDirectory](./props-system-search-iscloseddirectory.md) consente di ottimizzare le prestazioni dell'indicizzatore consentendo all'indicizzatore di ignorare l'enumerazione degli elementi figlio di un contenitore. Tuttavia, tali elementi figlio vengono contrassegnati dall'indicizzatore come non visitati e, in quanto tali, verranno eliminati dall'indice. Con l'emissione di [System. search. IsFullyContained]() come **true**, un elemento non viene eliminato dall'indice, sebbene non sia stato visitato.

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

 

 
