---
description: Il programma di installazione usa questo evento per visualizzare una stringa in formato informativo durante la compilazione dello script di esecuzione dell'installazione.
ms.assetid: 088e91e0-734a-4f18-8ceb-cfa4f904f75c
title: ScriptInProgress ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b2e92baf6f1ad3fd4a7ffb714aede88dc90d664564dd5d18f4c97e4d3bdc8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041421"
---
# <a name="scriptinprogress-controlevent"></a>ScriptInProgress ControlEvent

Il programma di installazione usa questo evento per visualizzare una stringa in formato informativo durante la compilazione dello script di esecuzione dell'installazione. La stringa informativo può essere visualizzata in una finestra di dialogo da un [controllo di](text-control.md) testo che sottoscrive questo ControlEvent. Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent può essere gestito da un'interfaccia utente eseguita a livello di interfaccia utente di [*base,*](b-gly.md)interfaccia [*utente*](r-gly.md)ridotta [*o interfaccia utente*](f-gly.md) completa. Per informazioni sui livelli dell'interfaccia utente, [vedere Interfaccia utente Livelli.](user-interface-levels.md)

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Nessuno.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Un [controllo Text](text-control.md) che sottoscrive ScriptInProgress visualizza la stringa di testo specificata nella tabella [UIText](uitext-table.md).

## <a name="typical-use"></a>Utilizzo tipico

Durante la compilazione dello script di esecuzione, il programma di installazione visualizza un controllo ProgressBar che indica il tempo rimanente prima dell'inizio dell'esecuzione dello script. L'autore del pacchetto può visualizzare un messaggio preliminare in questo momento che spiega ProgressBar. Per visualizzare un messaggio preliminare, includere un [controllo Text](text-control.md) nella stessa finestra di dialogo non modabile di ProgressBar. Specificare che questo controllo Text sottoscrive ScriptInProgress ControlEvent tramite [la tabella EventMapping](eventmapping-table.md). Includere una voce nella [tabella UIText con](uitext-table.md) ScriptInProgress specificato nel campo Chiave. Specificare il messaggio preliminare come stringa di testo nel campo Testo della tabella UIText. Durante la compilazione dello script, il programma di installazione visualizza quindi questa stringa all'interno del controllo di testo. Il testo visualizzato scompare non appena la compilazione dello script è terminata.

Lo stesso controllo di testo che sottoscrive ScriptInProgress ControlEvent può anche sottoscrivere [TimeRemaining ControlEvent](timeremaining-controlevent.md). In questo caso, quando il testo della stringa Preliminare ScriptInProgress scompare, viene sostituito dalla stringa "Time Remaining: xx minutes".

 

 



