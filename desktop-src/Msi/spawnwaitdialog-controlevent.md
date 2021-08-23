---
description: SpawnWaitDialog ControlEvent attiva la finestra di dialogo specificata dalla colonna Argomento della tabella ControlEvent, se l'espressione nella colonna Condizione restituisce FALSE.
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: SpawnWaitDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffeddfcb46f67d292de81a5a8195ba17c2a63b305be229ae96b2133448d41f00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628011"
---
# <a name="spawnwaitdialog-controlevent"></a>SpawnWaitDialog ControlEvent

SpawnWaitDialog ControlEvent attiva la finestra di dialogo specificata dalla colonna Argomento della tabella [ControlEvent](controlevent-table.md)se l'espressione nella colonna Condizione restituisce FALSE. La finestra di dialogo rimane aperta fino a quando l'espressione condizionale rimane FALSE e viene rimossa non appena la condizione restituisce TRUE.

Questo evento può essere pubblicato da un [controllo PushButton o](pushbutton-control.md) [selectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia [*utente ridotta*](r-gly.md) o un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere [Livelli Interfaccia utente.](user-interface-levels.md)

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Finestra di dialogo nella [tabella Finestra di dialogo](dialog-table.md).

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Nessuno.

## <a name="typical-use"></a>Utilizzo tipico

SpawnWaitDialog ControlEvent può essere usato per attendere il completamento di qualsiasi attività in background di cui è possibile testare il completamento usando un'espressione condizionale, ad esempio lo stato di una proprietà. Per un esempio di uso di SpawnWaitDialog ControlEvent, vedere la sezione Creazione di un oggetto [condizionale "Please wait . ." Finestra di messaggio](authoring-a-conditional-please-wait-------message-box.md).

 

 



