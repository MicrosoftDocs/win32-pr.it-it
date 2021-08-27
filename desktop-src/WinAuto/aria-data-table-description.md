---
title: Avviso della tabella dati ARIA
description: Avviso della tabella dati ARIA
ms.assetid: 3CFCF248-6A66-4140-B3E7-133E3809B287
keywords:
- AriaDataTableWarningId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16fb9e8e97336199b5b133dc59ef7c5f0900f7bdeb0c7a8d8098a51707b107f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122391"
---
# <a name="aria-data-table-warning"></a>Avviso della tabella dati ARIA

## <a name="text"></a>Testo

La tabella contiene dati, ma non include un riepilogo né un attributo **aria-describedby** valido.

## <a name="type"></a>Tipo

Avviso

## <a name="description"></a>Descrizione

Questo avviso si applica alle tabelle HTML con più di una cella. Non si applica alle tabelle con `role="presentation"` poiché sono considerate tabelle di layout.

Questo avviso indica che la tabella è identificata come tabella di dati, ma non ha una descrizione accessibile definita.

> [!Note]  
> Non tutte le tabelle dati devono avere una descrizione accessibile. È consigliabile definire una descrizione accessibile se gli utenti necessitano di altre informazioni per comprendere la struttura e il contenuto della tabella dati.

 

Per risolvere questo avviso, definire una descrizione accessibile da una tabella usando l'attributo summary o **l'attributo aria-describedby.**

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



 

 




