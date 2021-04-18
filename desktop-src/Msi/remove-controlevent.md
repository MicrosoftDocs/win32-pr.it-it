---
description: Il programma di installazione riceve una notifica tramite questo evento quando una funzionalità o tutte le funzionalità sono selezionate per la rimozione mantenendo la finestra di dialogo corrente.
ms.assetid: dabe44f7-97dd-4037-80e5-f289bab6d4b3
title: Rimuovere ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f214330fc16704fd4eef50bc8c75fc10fc2823d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312323"
---
# <a name="remove-controlevent"></a>Rimuovere ControlEvent

Il programma di installazione riceve una notifica tramite questo evento quando una funzionalità o tutte le funzionalità sono selezionate per la rimozione mantenendo la finestra di dialogo corrente.

Questo evento può essere pubblicato tramite un controllo [pulsante](pushbutton-control.md), un [controllo CheckBox](checkbox-control.md)o un [controllo SelectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md).

Questo ControlEvent richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funzionerà con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Stringa che rappresenta il nome della funzionalità o "ALL".

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="action-by-publisher-when-subscriber-activated"></a>Azione per autore quando il Sottoscrittore è attivato

Il programma di installazione mantiene la finestra di dialogo in esecuzione e invia una notifica al programma di installazione.

## <a name="typical-use"></a>Utilizzo tipico

Controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale associata a questo evento.

 

 



