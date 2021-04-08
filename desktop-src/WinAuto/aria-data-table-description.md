---
title: Avviso tabella dati ARIA
description: Avviso tabella dati ARIA
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- AriaDataTableWarningId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dcd77983092983649d8bcd41357afb4756120e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045236"
---
# <a name="aria-data-table-warning"></a>Avviso tabella dati ARIA

## <a name="text"></a>Testo

La tabella contiene dati ma non include alcun Riepilogo né un attributo **aria-describedby** valido.

## <a name="type"></a>Tipo

Avviso

## <a name="description"></a>Descrizione

Questo avviso si applica alle tabelle HTML con più di una cella. Non si applica alle tabelle con `role="presentation"` poiché queste sono considerate tabelle di layout.

Questo avviso indica che la tabella è stata identificata come tabella dati, ma non è stata definita una descrizione accessibile.

> [!Note]  
> Non è necessario che tutte le tabelle dati dispongano di una descrizione accessibile. È necessario definire una descrizione accessibile se gli utenti necessitano di ulteriori informazioni per comprendere la struttura e il contenuto della tabella di dati.

 

Per risolvere il problema, definire una descrizione accessibile per la tabella usando l'attributo summary o l'attributo **aria-describedby** .

## <a name="example"></a>Esempio


```HTML
<!-- Define a table description by using the summary attribute. -->
<table summary="The first column contains the list of examples. In the second column ...">
...
</table>

<!-- Define a table description using the aria-describedby attribute. -->
<p id="tableHeader" >The first column contains the list of examples. In the second column ...</p>
<table aria-describedby="tableHeader" >
...
</table>
```



 

 




