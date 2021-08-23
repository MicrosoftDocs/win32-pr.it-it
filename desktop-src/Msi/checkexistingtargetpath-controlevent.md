---
description: Questo evento notifica al programma di installazione che è necessario verificare che il percorso selezionato sia scrivibile. Se non è possibile scrivere il percorso, l'evento blocca altri ControlEvent associati al controllo.
ms.assetid: 4672e2e4-a789-4050-81b9-92ec491745ac
title: CheckExistingTargetPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d523d04eba4ede88ca1382c17c5d40d48dadadbc9520d766b5cfca2b26b77fb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520191"
---
# <a name="checkexistingtargetpath-controlevent"></a>CheckExistingTargetPath ControlEvent

Questo evento notifica al programma di installazione che è necessario verificare che il percorso selezionato sia scrivibile. Se non è possibile scrivere il percorso, l'evento blocca altri ControlEvent associati al controllo.

Questo evento può essere pubblicato da un [controllo PushButton o](pushbutton-control.md) [selectionTree.](selectiontree-control.md) Questo evento deve essere creato nella tabella [ControlEvent](controlevent-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia utente [*ridotta o*](r-gly.md) un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere [Livelli Interfaccia utente.](user-interface-levels.md)

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Nome della proprietà contenente il percorso. Se la proprietà è indiretta, il nome della proprietà è racchiuso tra parentesi quadre.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo PushButton](pushbutton-control.md) in una finestra di dialogo di esplorazione è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per controllare il percorso selezionato prima di tornare alla finestra di dialogo di selezione.

 

 



