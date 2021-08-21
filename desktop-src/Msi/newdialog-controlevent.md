---
description: Questo evento notifica al programma di installazione di eseguire la transizione di una finestra di dialogo modale a un'altra finestra di dialogo. Il programma di installazione rimuove la finestra di dialogo presente e ne crea una nuova con il nome indicato nell'argomento .
ms.assetid: bd1aa465-55a0-4983-8c71-7e7075ee9dfb
title: NewDialog ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed643272bf5cb329e04dc73426d5448ad71cca781bd129992e29f03b02b9dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519721"
---
# <a name="newdialog-controlevent"></a>NewDialog ControlEvent

Questo evento notifica al programma di installazione di eseguire la transizione di una finestra di dialogo modale a un'altra finestra di dialogo. Il programma di installazione rimuove la finestra di dialogo presente e ne crea una nuova con il nome indicato nell'argomento .

Questo evento può essere pubblicato da un [controllo PushButton o](pushbutton-control.md) [selectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede che l'interfaccia utente sia eseguita a livello [*completo dell'interfaccia*](f-gly.md) utente. Questo evento non funzionerà con un'interfaccia [*utente ridotta*](r-gly.md) o un'interfaccia utente [*di base.*](b-gly.md) Per informazioni, vedere [Livelli Interfaccia utente.](user-interface-levels.md)

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Stringa che rappresenta il nome della nuova finestra di dialogo.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo PushButton](pushbutton-control.md) in una finestra di dialogo modale è associato a questo evento nella tabella [ControlEvent](controlevent-table.md) per segnalare una transizione alla finestra di dialogo successiva o precedente della stessa sequenza della procedura guidata.

 

 



