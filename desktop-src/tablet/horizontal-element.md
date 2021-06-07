---
description: Contiene informazioni di formattazione per le linee orizzontali utilizzate per gli elementi decorativi in una nota del journal.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Elemento Horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de08008d0243d27f8a8c5f64d6aeac5ddbcc1c
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432378"
---
# <a name="horizontal-element"></a>Elemento Horizontal

Contiene informazioni di formattazione per le linee orizzontali utilizzate per gli elementi decorativi in una nota del journal.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Horizontal" type="HorizontalType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementi padre

[**LineLayout**](linelayout-element.md)

## <a name="child-elements"></a>Elementi figlio

Nessuno.

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
<td><a href="linelayoutstyletype-simple-type.md"><strong>SimpleType LineLayoutStyleType</strong></a></td>
<td>Obbligatoria</td>
<td>Specifica il tipo di linea da disegnare.</td>
<td><ul>
<li>Nessuno</li>
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
<td><a href="colortype-simple-type.md"><strong>SimpleType ColorType</strong></a></td>
<td>Facoltativo</td>
<td>Colore dell'elemento.</td>
<td>Valore RGB esadecimale. Corrisponde all'espressione regolare seguente: #[0-9a-zA-Z] {6} . Ad esempio, #4a79B5.<br/></td>
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



|  Elemento     | valore                                                     |
|--------------|-------------------------------------------------------------------|
| Tipo di elemento | [**ComplexType HorizontalType**](horizontaltype-complex-type.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink                        |
| Nome schema  | Lettore journal                                                    |



 

 

 




