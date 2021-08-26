---
description: Contiene informazioni di formattazione per le linee orizzontali utilizzate per la postazione in una nota journal.
ms.assetid: e3c9e7a8-8de6-4871-b386-2186883f2ee7
title: Elemento Horizontal
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aacadf35cca5e5f14f413ac857c4a6f3421d7ee8f5f2dc95d24cea9c7f0f6bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940642"
---
# <a name="horizontal-element"></a>Elemento Horizontal

Contiene informazioni di formattazione per le linee orizzontali utilizzate per la postazione in una nota journal.

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
<td>Necessario</td>
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
<td>Spaziatura tra questo elemento e gli elementi circostante.</td>
<td>Qualsiasi numero intero non negativo.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informazioni sull'elemento



|  Elemento     | valore                                                     |
|--------------|-------------------------------------------------------------------|
| Tipo di elemento | [**complexType HorizontalType**](horizontaltype-complex-type.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink                        |
| Nome schema  | Lettore journal                                                    |



 

 

 




