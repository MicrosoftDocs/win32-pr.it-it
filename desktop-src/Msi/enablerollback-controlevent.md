---
description: Questo ControlEvent può essere usato per attivare o disattivare le funzionalità di rollback del programma di installazione.
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: ControlEvent EnableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc651ef90b46c87431453f50c7ee5a28953e4d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309486"
---
# <a name="enablerollback-controlevent"></a>ControlEvent EnableRollback

Questo ControlEvent può essere usato per attivare o disattivare le funzionalità di rollback del programma di installazione.

Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

False disattiva le funzionalità di rollback del programma di installazione. True attiva le funzionalità di rollback del programma di installazione.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Può essere usato per disattivare le funzionalità di rollback se il programma di installazione rileva che lo spazio disponibile su disco è insufficiente per completare l'installazione. In questo caso, ControlEvent deve essere usato con le proprietà [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)e [**PROMPTROLLBACKCOST**](promptrollbackcost.md) .

 

 



