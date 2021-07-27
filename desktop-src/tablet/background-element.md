---
description: Contiene lo sfondo per un elemento JournalDocument o JournalPage.
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Elemento Background
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46388d56c04fc24ecd578788eecf9926ef01a301
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436586"
---
# <a name="background-element"></a>Elemento Background

Contiene lo sfondo per un [**elemento JournalDocument**](journaldocument-element.md) o [**JournalPage.**](journalpage-element.md)

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a>Elementi padre

[**Cancelleria**](stationery-element.md)

## <a name="child-elements"></a>Elementi figlio

[**Immagine**](image-element.md)

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
<td>Obbligatoria</td>
<td>Specifica lo stile dello sfondo.</td>
<td><ul>
<li>Nessuno</li>
<li>Tinta unita</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Colore</strong></td>
<td><a href="colortype-simple-type.md"><strong>SimpleType ColorType</strong></a></td>
<td>Facoltativo</td>
<td>Specifica il colore dello sfondo.</td>
<td>Vedere <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType.</td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informazioni sull'elemento



|                  | Valore                                                             |
|------------------|-------------------------------------------------------------------|
| **Tipo di elemento** | [**ComplexType BackgroundType**](backgroundtype-complex-type.md) |
| **Namespace**    | urn:schemas-microsoft-com:tabletpc:richink                        |
| **Nome schema**  | Lettore di journal                                                    |



 

 

 



