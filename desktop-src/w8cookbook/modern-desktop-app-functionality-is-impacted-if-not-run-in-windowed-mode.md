---
title: La funzionalità dell'app desktop è interessata se non viene eseguita in modalità finestra
description: In Windows 10, le app di Windows non sono più a schermo intero per impostazione predefinita, ma sono a finestra e le operazioni come la riduzione, il ripristino, l'ottimizzazione, il ridimensionamento e qualsiasi altra operazione che è sempre stato possibile eseguire in qualsiasi altra finestra dell'applicazione Windows classica sono ora possibili.
ms.assetid: 435E85DA-008B-437E-92CB-AC105855760A
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aae44fda5847e5b86616b40ab1bf4ab8cbd206b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396547"
---
# <a name="desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode"></a>La funzionalità dell'app desktop è interessata se non viene eseguita in modalità finestra

In Windows 10, le app di Windows non sono più a schermo intero per impostazione predefinita, ma sono a finestra e le operazioni come la riduzione, il ripristino, l'ottimizzazione, il ridimensionamento e qualsiasi altra operazione che è sempre stato possibile eseguire in qualsiasi altra finestra dell'applicazione Windows classica sono ora possibili.

## <a name="manifestations"></a>Manifestazioni

La modifica più evidente ora è che è possibile ottenere dimensioni arbitrarie che non sono solo le dimensioni della schermata o dell'altezza dello schermo. Un utente può ridimensionare continuamente la finestra dell'app a piacimento (fino alla dimensione minima della finestra dell'app). Questo comportamento è diverso da Windows 8,0 o Windows 8.1, in cui l'azione di ridimensionamento di una finestra era un'azione discreta (gli utenti ridimensionavano un'anteprima della finestra, causando il ridimensionamento della finestra dopo che l'utente ha eseguito il commit dell'azione). Attualmente, invece, quando l'utente trascina la finestra dall'angolo inferiore (o da un'altra posizione del bordo), si tratta di un ridimensionamento continuo e l'app riceve i messaggi di ridimensionamento in una riga, anziché la modifica delle dimensioni.

## <a name="mitigations"></a>Soluzioni di prevenzione

Per attenuare questo problema per le app di Windows 8,0 e 8,1:

-   Se la funzionalità prevista all'interno della funzionalità dell'app è interruppe, la mitigazione dell'utente consiste nell'inserire l'app in modalità schermo intero (usando il pulsante "Vai a schermo intero" nell'angolo superiore destro della barra del titolo).
-   Se l'avvio dell'app è influenzato dal fatto che non si apre come previsto, l'utente deve comunque essere in grado di passare alla modalità tablet per forzare l'avvio dell'app in modalità schermo intero senza l'intervento dell'utente.

Il modo migliore per gestire questa situazione consiste nel modificare l'app in modo che sia consapevole del fatto che può essere ridimensionata in posizioni/altezze di dimensioni non monitorate (ovvero non avere una tabella hardcoded di altezza/larghezza e prevedere solo i rapporti hardcoded). Gli sviluppatori di app dovrebbero prevedere che, durante il ridimensionamento dell'app, un altro messaggio di ridimensionamento possa essere eseguito subito dopo il recapito del messaggio di ridimensionamento. di conseguenza, se l'app avvia animazioni durante il ridimensionamento, è possibile che l'app riceva un altro messaggio di ridimensionamento subito dopo, quindi è importante assicurarsi che questo tipo di situazione non provochi l'arresto anomalo dell'

 

 




