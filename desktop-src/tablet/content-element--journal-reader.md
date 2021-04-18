---
description: Contiene il contenuto di una pagina journal.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Content (elemento) [Reader Journal]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b5a7c9631cd69d38b8db54e2a2f8e69636f7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314930"
---
# <a name="content-element-journal-reader"></a>\[Lettore Journal elemento contenuto\]

Contiene il contenuto di una pagina journal.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementi padre

[**JournalPage**](journalpage-element.md)

## <a name="child-elements"></a>Elementi figlio

[**Nodo del gruppo**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**Disegno**](drawing-element.md)

[**Text**](text-element.md)

[**Immagine**](image-element.md)

[**Contrassegno**](flag-element.md)

## <a name="attributes"></a>Attributi



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Type</th>
<th>Obbligatoria</th>
<th>Descrizione</th>
<th>PossibleValues</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Tipo</strong></td>
<td><a href="contenttype-complex-type.md"><strong>ComplexType ContentType</strong></a></td>
<td>Necessario</td>
<td>Se il tipo è &quot; inerte &quot; , il contenuto non può essere modificato.<br/></td>
<td><ul>
<li>Normale</li>
<li>Inerte</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informazioni sull'elemento



|              |                                                             |
|--------------|-------------------------------------------------------------|
| Tipo di elemento | ComplexType [**ContentType**](contenttype-complex-type.md) |
| Spazio dei nomi    | urn: schemas-microsoft-com: TabletPC: RichInk                  |
| Nome schema  | Lettore Journal                                              |



 

 

 




