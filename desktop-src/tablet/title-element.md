---
description: Contiene informazioni sul titolo relative alla nota Journal.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Elemento Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2362e286482b329c50788b8eae4b4a30cbd1a125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318685"
---
# <a name="title-element"></a>Elemento Title

Contiene informazioni sul titolo relative alla nota Journal.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementi padre

[**Cancelleria**](stationery-element.md)

## <a name="child-elements"></a>Elementi figlio

[**Elemento titlearea**](titlearea-element.md)

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
<th>Valori possibili</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Style</strong></td>
<td><strong>xs:string</strong></td>
<td>Necessario</td>
<td>Specifica il tipo di bordo che circonda il titolo della nota.</td>
<td><ul>
<li>nessuno</li>
<li>SolidSquare</li>
<li>OutlineSquare</li>
<li>SolidRoundRect</li>
<li>OutlineRoundRect</li>
<li>SolidRoundRectDottedBaseline</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>DateStyle</strong></td>
<td><strong>xs:string</strong></td>
<td>Necessario</td>
<td>Definisce se il titolo include o meno una data.</td>
<td><ul>
<li>nessuno</li>
<li>Short</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Colore</strong></td>
<td><a href="colortype-simple-type.md"><strong>SimpleType ColorType</strong></a></td>
<td>Facoltativo</td>
<td>Specifica il colore dello sfondo.</td>
<td>Vedere <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informazioni sull'elemento



|              |                                                         |
|--------------|---------------------------------------------------------|
| Tipo di elemento | ComplexType [**TitleType**](titletype-complex-type.md) |
| Spazio dei nomi    | urn: schemas-microsoft-com: TabletPC: RichInk              |
| Nome schema  | Lettore Journal                                          |



 

 

 



