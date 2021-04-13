---
title: Errore di tabella dati ARIA
description: Errore di tabella dati ARIA
ms.assetid: 3D0448BB-50DC-4C85-93BD-D8E626475AB0
keywords:
- AriaDataTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286f88a0b3a0d962fd6ac45581f94bc351cb507
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104399844"
---
# <a name="aria-data-table-error"></a>Errore di tabella dati ARIA

## <a name="text"></a>Testo

La tabella contiene dati ma non ha un markup accessibile definito anche se **aria-label**, **aria-labelledby**, **titolo**, **didascalia** **o elementi** .

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica alle tabelle HTML con più di una cella. Questo errore non si applica alle tabelle con `role="presentation"` perché sono considerate tabelle di layout.

Questo errore indica che una tabella dati non ha un nome accessibile o informazioni di intestazione.

Per correggere l'errore, definire un nome accessibile usando il tag [**Caption**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) oppure gli attributi [**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)o [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) . Se nella tabella mancano informazioni di intestazione, utilizzare i tag [**thead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) per contrassegnare le celle di intestazione.

## <a name="example"></a>Esempio


```HTML
<!-- Data tables must contain an accessibile name and header information. -->
<table>
  <caption>ARIA Examples</caption>
  <thead>
    <tr>
      <th>Name</th>
      <th>Description</th>
      ...
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>Accessible tables</td>
      <td>This example illustrates how to make data tables accessible using ARIA</td>
      ...
    </tr>
  </tbody>
</table>
```



 

 




