---
description: Contiene il contenuto di una pagina Journal.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Content - elemento [Lettore journal]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fec59601a91d63b09c703557b7c6cd28fd11620
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432153"
---
# <a name="content-element-journal-reader"></a>Lettore journal \[ dell'elemento Content\]

Contiene il contenuto di una pagina Journal.

## <a name="definition"></a>Definizione

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Elementi padre

[**JournalPage**](journalpage-element.md)

## <a name="child-elements"></a>Elementi figlio

[**GroupNode**](groupnode-element.md)

[**Paragraph**](paragraph-element.md)

[**Disegno**](drawing-element.md)

[**Text**](text-element.md)

[**Immagine**](image-element.md)

[**Bandiera**](flag-element.md)

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
<td><strong>Tipo</strong></td>
<td><a href="contenttype-complex-type.md"><strong>complexType ContentType</strong></a></td>
<td>Obbligatoria</td>
<td>Se il tipo è &quot; &quot; Inert, il contenuto non può essere modificato.<br/></td>
<td><ul>
<li>Normale</li>
<li>Inerte</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a>Informazioni sull'elemento



|  Elemento     | valore                                                     |
|--------------|-------------------------------------------------------------|
| Tipo di elemento | [**complexType ContentType**](contenttype-complex-type.md) |
| Spazio dei nomi    | urn:schemas-microsoft-com:tabletpc:richink                  |
| Nome schema  | Lettore journal                                              |



 

 

 




