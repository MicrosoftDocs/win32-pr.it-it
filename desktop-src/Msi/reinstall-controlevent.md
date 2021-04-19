---
description: Consente all'autore di avviare una reinstallazione di alcune o di tutte le funzionalità, mentre è in esecuzione la finestra di dialogo corrente.
ms.assetid: bc667f20-3abe-4ef3-b51e-dc74da63f651
title: Reinstallare ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d2adece3f89dbe57b77f2345d1714ece64b271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311700"
---
# <a name="reinstall-controlevent"></a>Reinstallare ControlEvent

Reinstallare ControlEventallows l'autore per avviare una reinstallazione di alcune o di tutte le funzionalità, mentre è in esecuzione la finestra di dialogo corrente.

Questo evento può essere pubblicato da un [controllo pulsante](pushbutton-control.md) o da un [controllo SelectionTree](selectiontree-control.md). Questo evento deve essere creato nella [tabella ControlEvent](controlevent-table.md)e richiede l'esecuzione dell'interfaccia utente a livello di [*interfaccia utente completo*](f-gly.md) . Questo evento non funziona con un'interfaccia utente [*ridotta*](r-gly.md) o un' [*interfaccia utente di base*](b-gly.md). Per ulteriori informazioni, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Stringa che rappresenta il nome della funzionalità o "ALL".

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Questo evento è associato a un controllo [pulsante](pushbutton-control.md) in una finestra di dialogo modale. Lo stesso controllo [pulsante](pushbutton-control.md) deve essere associato anche a un ControlEvent [REINSTALLMODE](reinstallmode-controlevent.md) .

 

 



