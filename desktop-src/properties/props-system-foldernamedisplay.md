---
description: Questa proprietà è simile a System. ItemNameDisplay, con la differenza che è impostata solo per le cartelle, per i file sarà vuota.
ms.assetid: 4517a4bf-3cc1-4835-b21b-03de5b33db0c
title: System. FolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60922054e80a6589bcb04c3962a4527ee62eaf7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313961"
---
# <a name="systemfoldernamedisplay"></a>System. FolderNameDisplay

Questa proprietà è simile a System. ItemNameDisplay, con la differenza che è impostata solo per le cartelle, per i file sarà vuota. Questa operazione è utile per separare i file e le cartelle utilizzando come prima chiave di ordinamento. Quando System. ItemDate viene usato come seconda chiave di ordinamento, produce i risultati con le cartelle prima ordinate in base al nome, quindi i file ordinati per data.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1

```
propertyDescription
   name = System.FolderNameDisplay
   shellPKey = PKEY_FolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 25
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey. h.

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

 

 
