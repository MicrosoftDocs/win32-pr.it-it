---
description: Il controllo SelectionTree usa l'evento SelectionSize per pubblicare le dimensioni dell'elemento evidenziato.
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: SelectionSize ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c8733c0155adc085343c0a5db1a42e3aa219719babb5b342781c5bb9923ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040361"
---
# <a name="selectionsize-controlevent"></a>SelectionSize ControlEvent

Il [controllo SelectionTree usa](selectiontree-control.md) l'evento SelectionSize per pubblicare le dimensioni dell'elemento evidenziato. Se si tratta di un elemento padre, viene pubblicato anche il numero di elementi figlio selezionati. La stringa è una delle stringhe **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos**, **SelParentCostPosNeg**, **SelParentCostNegPos** o **SelParentCostNegNegNeg** della tabella [UIText](uitext-table.md). Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia utente [*ridotta o*](r-gly.md) un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere [Livelli Interfaccia utente.](user-interface-levels.md)

Questo evento può interessare solo i controlli che si trovano nella stessa finestra di dialogo del controllo SelectionTree.

## <a name="published-by"></a>Pubblicato da

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argomento

Nessuno.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Nessuno.

## <a name="typical-use"></a>Utilizzo tipico

Controllo [Text](text-control.md) nella stessa finestra di dialogo modale del controllo SelectionTree tramite la [tabella EventMapping](eventmapping-table.md). Il controllo Text usa questo evento per visualizzare le dimensioni dell'elemento evidenziato.

 

 



