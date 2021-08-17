---
description: Definisce le linee dei margini disegnate nella pagina.
ms.assetid: c3047706-affd-4feb-9d48-cfb4c7dd6fa0
title: Elemento Margin
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ff764585919ff144ebc25ac568caf1af74410a2f337beb03d5ce484f7d1abe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350441"
---
# <a name="margin-element"></a>Elemento Margin

Definisce le linee dei margini disegnate nella pagina.

## <a name="definition"></a>Definizione

``` syntax
<xs:complexType name="MarginType">
   <xs:attribute name="Style" use="required" type="LineLayoutStyleType" />
   <xs:attribute name="Color" type="ColorType" />
   <xs:attribute name="Type" type="MarginTypeType" />
   <xs:attribute name="Spacing" type="xs:positiveInteger" />
</xs:complexType>
```

## <a name="parent-elements"></a>Elementi padre

Nessuno.

## <a name="child-elements"></a>Elementi figlio

Nessuno..

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
<td><strong>Tipo</strong></td>
<td><a href="margintypetype-simple-type.md"><strong>SimpleType MarginTypeType</strong></a></td>
<td>Facoltativo</td>
<td>Indica il margine sinistro o destro.</td>
<td><ul>
<li>Sinistra</li>
<li>Destra</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Spaziatura</strong></td>
<td><strong>xs:nonNegativeInteger</strong></td>
<td>Facoltativo</td>
<td>Spaziatura tra il bordo della pagina e il margine.</td>
<td>Qualsiasi numero intero non negativo.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informazioni sull'elemento



|  Elemento     | valore                                                     |
|--------------|-----------------------------------------------------------|
| Tipo di elemento | [**complexType MarginType**](margintype-complex-type.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink                |
| Nome schema  | Lettore journal                                            |



 

 

 




