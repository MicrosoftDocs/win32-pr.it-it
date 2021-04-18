---
description: La finestra di dialogo viene reimpostata. In altre parole, tutti i controlli della finestra di dialogo vengono chiamati per annullare le modifiche apportate alle proprietà. Questo evento Reimposta tutti i valori della proprietà quando è stata creata la finestra di dialogo.
ms.assetid: 6449abb8-54cb-4400-9eb2-b7e7f1564747
title: Reimposta ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889f1b0f984f14b7522707db4ffbd958bff9c32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313794"
---
# <a name="reset-controlevent"></a>Reimposta ControlEvent

La finestra di dialogo viene reimpostata. In altre parole, tutti i controlli della finestra di dialogo vengono chiamati per annullare le modifiche apportate alle proprietà. Questo evento Reimposta tutti i valori della proprietà quando è stata creata la finestra di dialogo.

Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

Un caso, che dovrebbe verificarsi raramente in pratica, non viene gestito correttamente da questo ControlEvent. Se sono presenti due o più controlli nella stessa finestra di dialogo collegati indirettamente alla stessa proprietà e almeno uno di essi ha iniziato a disporre di un'altra proprietà, il valore di questa proprietà verrà a volte reimpostato sul secondo valore.

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Nessuna.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Nessuna.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale viene utilizzato per reimpostare tutti i valori nella finestra di dialogo e per annullare tutte le modifiche nella pagina.

 

 



