---
description: Il controllo SelectionTree usa l'evento SelectionNoItems per eliminare il testo della descrizione dell'elemento obsoleto o per disabilitare i pulsanti che sono diventati inutili. Questo evento deve essere creato nella tabella EventMapping.
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: SelectionNoItems ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17220849c6bf50a28a0a0596bcd347e2f0a4c5af77cb53c9d9fa0041ced59abe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040461"
---
# <a name="selectionnoitems-controlevent"></a>SelectionNoItems ControlEvent

Il [controllo SelectionTree usa l'evento](selectiontree-control.md) SelectionNoItems per eliminare il testo della descrizione dell'elemento obsoleto o per disabilitare i pulsanti che sono diventati inutili. Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia utente [*ridotta o*](r-gly.md) un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere [Livelli Interfaccia utente.](user-interface-levels.md)

Questo evento può interessare solo i controlli che si trovano nella stessa finestra di dialogo del controllo SelectionTree.

## <a name="published-by"></a>Pubblicato da

[Controllo SelectionTree](selectiontree-control.md) se la selezione non ha nodi.

## <a name="argument"></a>Argomento

Nessuno.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Elimina il testo di descrizione dell'elemento obsoleto o disabilita i pulsanti obsoleti.

## <a name="typical-use"></a>Utilizzo tipico

Può essere usato per disabilitare i pulsanti Avanti, Reimposta e DiskCost nella finestra di dialogo di selezione quando una selezione non ha nodi e questi pulsanti diventano inutili. [](selection-dialog.md)

 

 



