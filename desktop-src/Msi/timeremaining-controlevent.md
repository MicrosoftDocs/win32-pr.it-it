---
description: Il programma di installazione usa l'evento TimeRemaining per pubblicare il tempo approssimativo rimanente, in secondi, per la sequenza di avanzamento corrente.
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: TimeRemaining ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fa29184c489e3d3a0b0f71d0dcd01297aa5359b25b3c463d3ccd3def6991257
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810711"
---
# <a name="timeremaining-controlevent"></a>TimeRemaining ControlEvent

Il programma di installazione usa l'evento TimeRemaining per pubblicare il tempo approssimativo rimanente, in secondi, per la sequenza di avanzamento corrente. Il tempo rimanente può essere visualizzato in una finestra di dialogo da un [controllo di](text-control.md) testo che sottoscrive questo ControlEvent. Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent può essere gestito da un'interfaccia utente eseguita a livello di interfaccia utente di [*base,*](b-gly.md) [*interfaccia utente*](r-gly.md)ridotta o [*interfaccia utente*](f-gly.md) completa. Per informazioni sui livelli dell'interfaccia utente, [Interfaccia utente livelli.](user-interface-levels.md)

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Nessuno.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Nessuno.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo Testo](text-control.md) in una finestra di dialogo non modali sottoscrive questo evento tramite la tabella [EventMapping](eventmapping-table.md) e usa l'attributo [TimeRemaining](timeremaining-control-attribute.md) per visualizzare il tempo rimanente.

Lo stesso controllo di testo che sottoscrive TimeRemaining ControlEvent può anche sottoscrivere [ScriptInProgress ControlEvent.](scriptinprogress-controlevent.md) In questo caso, come stringa di messaggio ScriptInProgress preliminare, viene sostituita dalla stringa "Time Remaining: xx minutes".

 

 



