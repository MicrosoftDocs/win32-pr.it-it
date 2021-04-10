---
description: Il ControlEvent SpawnWaitDialog attiva la finestra di dialogo specificata dalla colonna Argument della tabella ControlEvent, se l'espressione nella colonna condizione restituisce FALSE.
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: ControlEvent SpawnWaitDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20059c936a8534d00799c93dfbe3408a19c6dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966786"
---
# <a name="spawnwaitdialog-controlevent"></a>ControlEvent SpawnWaitDialog

Il ControlEvent SpawnWaitDialog attiva la finestra di dialogo specificata dalla colonna Argument della [tabella ControlEvent](controlevent-table.md), se l'espressione nella colonna condizione restituisce false. La finestra di dialogo rimane attiva fino a quando l'espressione condizionale rimane FALSE e viene rimossa non appena la condizione restituisce TRUE.

Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Finestra di dialogo nella [tabella della finestra di dialogo](dialog-table.md).

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Nessuna.

## <a name="typical-use"></a>Utilizzo tipico

Il ControlEvent SpawnWaitDialog può essere usato per attendere il completamento di un'attività in background, che può essere testata usando un'espressione condizionale, ad esempio lo stato di una proprietà. Per un esempio relativo all'uso di SpawnWaitDialog ControlEvent, vedere la sezione [creazione di un condizionale "attendere..." MessageBox](authoring-a-conditional-please-wait-------message-box.md).

 

 



