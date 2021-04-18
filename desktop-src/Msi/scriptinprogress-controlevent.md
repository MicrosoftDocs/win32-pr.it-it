---
description: Il programma di installazione utilizza questo evento per visualizzare una stringa informativa durante la compilazione dello script di esecuzione dell'installazione.
ms.assetid: 088e91e0-734a-4f18-8ceb-cfa4f904f75c
title: ControlEvent ScriptInProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fdc9c0acec5979a835a6cd2a0ec09cc6f0c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312317"
---
# <a name="scriptinprogress-controlevent"></a>ControlEvent ScriptInProgress

Il programma di installazione utilizza questo evento per visualizzare una stringa informativa durante la compilazione dello script di esecuzione dell'installazione. La stringa informativa può essere visualizzata in una finestra di dialogo da un [controllo di testo](text-control.md) che sottoscrive questo ControlEvent. Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent può essere gestito da un'interfaccia utente eseguita nell'interfaccia utente di [*base*](b-gly.md), interfaccia utente [*ridotta*](r-gly.md)o livelli di [*interfaccia utente completi*](f-gly.md) . Per informazioni sui livelli dell'interfaccia utente, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Nessuna.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Un [controllo di testo](text-control.md) che sottoscrive ScriptInProgress visualizzerà la stringa di testo specificata nella [tabella UIText](uitext-table.md).

## <a name="typical-use"></a>Utilizzo tipico

Durante la compilazione dello script di esecuzione, il programma di installazione visualizza una ProgressBar che indica il tempo rimanente prima dell'inizio dell'esecuzione dello script. Al momento, l'autore del pacchetto può visualizzare un messaggio preliminare che illustra il ProgressBar. Per visualizzare un messaggio preliminare, includere un [controllo di testo](text-control.md) nella stessa finestra di dialogo non modale della ProgressBar. Consente di specificare che questo controllo di testo sottoscrive il ControlEvent ScriptInProgress tramite la [tabella EventMapping](eventmapping-table.md). Includere una voce nella [tabella UIText](uitext-table.md) con ScriptInProgress specificato nel campo chiave. Specificare il messaggio preliminare come stringa di testo nel campo di testo della tabella UIText. Quindi, durante la compilazione dello script, il programma di installazione visualizzerà questa stringa all'interno del controllo di testo. Il testo visualizzato scompare non appena la compilazione dello script è terminata.

Lo stesso controllo di testo che sottoscrive ScriptInProgress ControlEvent può inoltre sottoscrivere [TimeRemaining ControlEvent](timeremaining-controlevent.md). In questo caso, poiché il testo della stringa ScriptInProgress preliminare scompare, viene sostituito dalla stringa "tempo rimanente: XX minuti".

 

 



