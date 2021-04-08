---
description: Il programma di installazione usa l'evento TimeRemaining per pubblicare il tempo di permanenza approssimativo, in secondi, per la sequenza di avanzamento corrente.
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: ControlEvent TimeRemaining
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8978dfb7ed3be855921ad66af8554ea50972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058184"
---
# <a name="timeremaining-controlevent"></a>ControlEvent TimeRemaining

Il programma di installazione usa l'evento TimeRemaining per pubblicare il tempo di permanenza approssimativo, in secondi, per la sequenza di avanzamento corrente. Il tempo rimanente può essere visualizzato in una finestra di dialogo da un [controllo di testo](text-control.md) che sottoscrive questo ControlEvent. Questo evento deve essere creato nella [tabella EventMapping](eventmapping-table.md).

Questo ControlEvent può essere gestito da un'interfaccia utente eseguita nell'interfaccia utente di [*base*](b-gly.md), interfaccia utente [*ridotta*](r-gly.md)o livelli di [*interfaccia utente completi*](f-gly.md) . Per informazioni sui livelli dell'interfaccia utente, vedere [livelli di interfaccia utente](user-interface-levels.md).

## <a name="published-by"></a>Pubblicato da

Questo ControlEvent viene pubblicato dal programma di installazione.

## <a name="argument"></a>Argomento

Nessuna.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Nessuna.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo di testo](text-control.md) in una finestra di dialogo non modale sottoscrive questo evento tramite la [tabella EventMapping](eventmapping-table.md) e utilizza l' [attributo TimeRemaining](timeremaining-control-attribute.md) per visualizzare il tempo rimanente.

Lo stesso controllo di testo che sottoscrive TimeRemaining ControlEvent può inoltre sottoscrivere [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md). In questo caso, come la stringa di messaggio ScriptInProgress preliminare, viene sostituita dalla stringa "tempo rimanente: XX minuti".

 

 



