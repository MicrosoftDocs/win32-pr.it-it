---
title: Errore della tabella dati ARIA
description: Errore della tabella dati ARIA
ms.assetid: 3D0448BB-50DC-4C85-93BD-D8E626475AB0
keywords:
- AriaDataTableErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 025443ab452ff0103c8808c27dce834a03cb8c96e0d9106a7abb4409b64a0697
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133974"
---
# <a name="aria-data-table-error"></a>Errore della tabella dati ARIA

## <a name="text"></a>Testo

La tabella contiene dati, ma non dispone di markup accessibile definito anche se **aria-label**, **aria-labelledby,** **title,** **caption** o **th** elementi.

## <a name="type"></a>Tipo

Errore

## <a name="description"></a>Descrizione

Questo errore si applica alle tabelle HTML con più di una cella. Questo errore non si applica alle tabelle con `role="presentation"` perché sono considerate tabelle di layout.

Questo errore indica che una tabella dati non dispone di un nome o di un'intestazione accessibile.

Per correggere l'errore, definire un nome accessibile usando il tag [**CAPTION**](https://developer.mozilla.org/docs/Web/HTML/Element/caption) o gli attributi [**aria-labelledby,**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) [**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)o [**title.**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) Se nella tabella mancano informazioni di intestazione, usare [**i tag THead**](https://developer.mozilla.org/docs/Web/HTML/Element/thead) per contrassegnare le celle di intestazione.

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



 

 




