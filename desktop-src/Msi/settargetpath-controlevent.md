---
description: L'evento SetTargetPath notifica al programma di installazione di controllare e impostare il percorso selezionato. Se il percorso non è valido per la scrittura, il programma di installazione blocca altri ControlEvent associati al controllo.
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: SetTargetPath ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e49e9447d7d2e67dce85e7d60638c18a949ecbc87800d12a60bc94d971cb30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625071"
---
# <a name="settargetpath-controlevent"></a>SetTargetPath ControlEvent

L'evento SetTargetPath notifica al programma di installazione di controllare e impostare il percorso selezionato. Se il percorso non è valido per la scrittura, il programma di installazione blocca altri ControlEvent associati al controllo.

Questo evento può essere pubblicato da un [controllo PushButton o](pushbutton-control.md) [selectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia [*utente ridotta*](r-gly.md) o un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere [Livelli Interfaccia utente.](user-interface-levels.md)

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Nome della proprietà contenente il percorso. Se la proprietà è indiretta, il nome della proprietà è racchiuso tra parentesi quadre.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Nessuno.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo PushButton](pushbutton-control.md) in una finestra di dialogo di esplorazione è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per controllare il percorso selezionato prima di tornare alla finestra di dialogo di selezione.

## <a name="remarks"></a>Commenti

Non tentare di configurare il percorso di destinazione se i componenti che usano tali percorsi sono già installati per l'utente corrente o per un utente diverso. Controllare la [**proprietà ProductState**](productstate.md) prima di pubblicare SetTargetPath ControlEvent per determinare se il prodotto contenente il componente è installato.

 

 



