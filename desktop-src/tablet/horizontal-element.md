---
description: Contiene informazioni sulla formattazione per le linee orizzontali utilizzate per la cancelleria in una nota di Journal.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Elemento Horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e380ca35f86ce1012084d31de732cd66c79363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751895"
---
# <a name="horizontal-element"></a>Elemento Horizontal

Contiene informazioni sulla formattazione per le linee orizzontali utilizzate per la cancelleria in una nota di Journal.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementi padre

[**LineLayout**](linelayout-element.md)

## <a name="child-elements"></a>Elementi figlio

Nessuna.

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
<td>SimpleType <a href="linelayoutstyletype-simple-type.md"><strong>LineLayoutStyleType</strong></a></td>
<td>Necessario</td>
<td>Specifica il tipo di linea da disegnare.</td>
<td><ul>
<li>nessuno</li>
<li>Tinta unita</li>
<li>Trattino</li>
<li>Punto</li>
<li>DashDot</li>
<li>DashDotDot</li>
<li>Double</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Colore</strong></td>
<td>SimpleType <a href="colortype-simple-type.md"><strong>ColorType</strong></a></td>
<td>Facoltativo</td>
<td>Colore dell'elemento.</td>
<td>Valore RGB esadecimale. Corrisponde all'espressione regolare seguente: # [0-9a-zA-Z] {6} . Ad esempio, #4a79B5.<br/></td>
</tr>
<tr class="odd">
<td><strong>SpacingBefore</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Facoltativo</td>
<td>Spaziatura prima dell'elemento.</td>
<td>Qualsiasi numero intero non negativo.</td>
</tr>
<tr class="even">
<td><strong>SpacingBetween</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Facoltativo</td>
<td>Spaziatura tra questo elemento e gli elementi circostanti.</td>
<td>Qualsiasi numero intero non negativo.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informazioni sull'elemento



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| Tipo di elemento | [**ComplexType HorizontalType**](horizontaltype-complex-type.md) |
| Spazio dei nomi    | urn: schemas-microsoft-com: TabletPC: RichInk                        |
| Nome schema  | Lettore Journal                                                    |



 

 

 




