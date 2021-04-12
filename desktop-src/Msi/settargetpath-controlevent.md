---
description: L'evento SetTargetPath notifica al programma di installazione di controllare e impostare il percorso selezionato. Se il percorso non è valido per la scrittura in, il programma di installazione blocca ulteriori ControlEvents associate al controllo.
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: ControlEvent SetTargetPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36812d291ab4410b08c577e6d118c3ff9e5dc0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232437"
---
# <a name="settargetpath-controlevent"></a>ControlEvent SetTargetPath

L'evento SetTargetPath notifica al programma di installazione di controllare e impostare il percorso selezionato. Se il percorso non è valido per la scrittura in, il programma di installazione blocca ulteriori ControlEvents associate al controllo.

Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Nome della proprietà che contiene il percorso. Se la proprietà è indiretta, il nome della proprietà è racchiuso tra parentesi quadre.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Nessuna.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo di esplorazione è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per controllare il percorso selezionato prima di tornare alla finestra di dialogo di selezione.

## <a name="remarks"></a>Commenti

Non tentare di configurare il percorso di destinazione se i componenti che utilizzano tali percorsi sono già installati per l'utente corrente o per un altro utente. Controllare la proprietà [**ProductState**](productstate.md) prima di pubblicare il ControlEvent SetTargetPath per determinare se il prodotto contenente il componente è installato.

 

 



