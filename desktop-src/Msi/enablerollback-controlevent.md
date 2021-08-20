---
description: Questo ControlEvent può essere usato per attivare o disattivare le funzionalità di rollback del programma di installazione.
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: EnableRollback ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3b0cd93a65a9402c915606585f3eb1cd43c058847e2907b1134e1c84982b76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143112"
---
# <a name="enablerollback-controlevent"></a>EnableRollback ControlEvent

Questo ControlEvent può essere usato per attivare o disattivare le funzionalità di rollback del programma di installazione.

Questo evento può essere pubblicato da un [controllo PushButton o](pushbutton-control.md) [selectionTree.](selectiontree-control.md) Questo evento deve essere creato nella tabella [ControlEvent](controlevent-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia utente [*ridotta o*](r-gly.md) un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere [Livelli Interfaccia utente.](user-interface-levels.md)

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

False disattiva le funzionalità di rollback del programma di installazione. True attiva le funzionalità di rollback del programma di installazione.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Può essere usato per disattivare le funzionalità di rollback se il programma di installazione rileva che lo spazio su disco disponibile non è sufficiente per completare l'installazione. In questo caso, è necessario usare ControlEvent con le proprietà [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)e [**PROMPTROLLBACKCOST.**](promptrollbackcost.md)

 

 



