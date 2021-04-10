---
description: Il controllo SelectionTree usa l'evento SelectionSize per pubblicare la dimensione dell'elemento evidenziato.
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: ControlEvent SelectionSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c11829661f0120fa5906a04f081e6c979b37180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231857"
---
# <a name="selectionsize-controlevent"></a>ControlEvent SelectionSize

Il [controllo SelectionTree](selectiontree-control.md) usa l'evento SelectionSize per pubblicare la dimensione dell'elemento evidenziato. Se è un elemento padre, viene pubblicato anche il numero di elementi figlio selezionati. La stringa è una delle stringhe **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos**, **SelParentCostPosNeg**, **SelParentCostNegPos** o **SelParentCostNegNeg** della [tabella UIText](uitext-table.md). Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

Questo evento può influire solo sui controlli che si trovano nella stessa finestra di dialogo del controllo SelectionTree.

## <a name="published-by"></a>Pubblicato da

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argomento

Nessuna.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Nessuna.

## <a name="typical-use"></a>Utilizzo tipico

Controllo di [testo](text-control.md) nella stessa finestra di dialogo modale del controllo SelectionTree tramite la [tabella EventMapping](eventmapping-table.md). Il controllo testo usa questo evento per visualizzare la dimensione dell'elemento evidenziato.

 

 



