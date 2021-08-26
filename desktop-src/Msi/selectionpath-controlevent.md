---
description: Il controllo SelectionTree usa l'evento SelectionPath per pubblicare il percorso per l'elemento evidenziato.
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: SelectionPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f45dfcb017c18b026f03bf9fa9b89d7be33db49bafc3dd9f899846cbada1047
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040441"
---
# <a name="selectionpath-controlevent"></a>SelectionPath ControlEvent

Il [controllo SelectionTree usa](selectiontree-control.md) l'evento SelectionPath per pubblicare il percorso per l'elemento evidenziato. Se l'elemento è selezionato per l'esecuzione dall'origine, questo è il percorso dell'origine. Se l'elemento è selezionato come assente, la stringa è la stringa **AbsentPath** della [tabella UIText](uitext-table.md). Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia [*utente ridotta*](r-gly.md) o un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere [Livelli Interfaccia utente.](user-interface-levels.md)

Questo evento può influire solo sui controlli che si trovano nella stessa finestra di dialogo del controllo SelectionTree.

## <a name="published-by"></a>Pubblicato da

[SelectionTree](selectiontree-control.md)

## <a name="argument"></a>Argomento

Nessuno.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Nessuno.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo Text](text-control.md) nella stessa finestra di dialogo modale di SelectionTree deve sottoscrivere l'evento tramite la tabella [EventMapping](eventmapping-table.md). Il controllo Text visualizza il percorso dell'elemento evidenziato.

 

 



