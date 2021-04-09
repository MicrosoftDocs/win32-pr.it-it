---
description: Questo evento notifica al programma di installazione di eseguire la transizione di una finestra di dialogo modale a un'altra finestra di dialogo. Il programma di installazione rimuove la finestra di dialogo presente e ne crea una nuova con il nome indicato nell'argomento.
ms.assetid: bd1aa465-55a0-4983-8c71-7e7075ee9dfb
title: ControlEvent NewDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 439c459bc5bfe061cc7f888d9c0a3374afa9098b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130674"
---
# <a name="newdialog-controlevent"></a>ControlEvent NewDialog

Questo evento notifica al programma di installazione di eseguire la transizione di una finestra di dialogo modale a un'altra finestra di dialogo. Il programma di installazione rimuove la finestra di dialogo presente e ne crea una nuova con il nome indicato nell'argomento.

Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md)o da un [controllo SelectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Stringa che rappresenta il nome della nuova finestra di dialogo.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per segnalare una transizione alla finestra di dialogo successiva o precedente della stessa sequenza della procedura guidata.

 

 



