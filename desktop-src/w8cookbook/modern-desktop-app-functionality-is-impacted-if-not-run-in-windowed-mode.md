---
title: La funzionalità dell'app desktop è influenzata se non viene eseguita in modalità finestra
description: In Windows 10, le app Windows non sono più a schermo intero per impostazione predefinita, ma sono finestra e operazioni come la riduzione al minimo, il ripristino, l'ingrandimento, il ridimensionamento (e qualsiasi altra operazione che si è sempre potuto eseguire in qualsiasi altra finestra dell'applicazione Windows classica) è ora possibile.
ms.assetid: 435E85DA-008B-437E-92CB-AC105855760A
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 79b7db00eb2bab422adaa22d798c373ece7adf061faff43a67e13ee07528a2ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028819"
---
# <a name="desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode"></a>La funzionalità dell'app desktop è influenzata se non viene eseguita in modalità finestra

In Windows 10, le app Windows non sono più a schermo intero per impostazione predefinita, ma sono finestra e operazioni come la riduzione al minimo, il ripristino, l'ingrandimento, il ridimensionamento (e qualsiasi altra operazione che si è sempre potuto eseguire in qualsiasi altra finestra dell'applicazione Windows classica) è ora possibile.

## <a name="manifestations"></a>Manifestazioni

La modifica più evidente ora è che è possibile ridimensionare le dimensioni in base a dimensioni arbitrarie che non sono solo le dimensioni dello schermo o dell'altezza dello schermo. Un utente può ridimensionare continuamente la finestra dell'app in base alle proprie dimensioni (fino alle dimensioni minime della finestra dell'app). Questa operazione è diversa da Windows 8.0 o Windows 8.1, in cui l'azione di ridimensionamento di una finestra è un'azione discreta (gli utenti hanno ridimensionato un'anteprima della finestra, che ha quindi causato il ridimensionamento della finestra dopo che l'utente ha eseguito l'azione). Attualmente, invece, quando l'utente trascina la finestra nell'angolo inferiore (o in un'altra posizione del bordo), si tratta di un ridimensionamento continuo e l'app riceve messaggi di ridimensionamento in una riga, anziché modificare le dimensioni.

## <a name="mitigations"></a>Soluzioni di prevenzione

Per attenuare questo problema per Windows 8.0 e 8.1:

-   Se la funzionalità prevista all'interno della funzionalità dell'app è interrotta, la mitigazione dell'utente prevede di impostare l'app in modalità schermo intero (usando il pulsante "Vai a schermo intero" nell'angolo superiore destro della barra del titolo).
-   Se l'avvio dell'app non viene aperto come previsto, l'utente dovrebbe comunque essere in grado di passare alla modalità tablet per forzare l'avvio dell'app in modalità schermo intero senza l'intervento dell'utente.

Il modo migliore per gestire questo problema è modificare l'app in modo da tenere presente che può essere ridimensionata in base a posizioni/altezze non monitorate(ad esempio, non avere una tabella hardcoded di altezza/larghezza e aspettarsi solo tali valori o prevedere anche rapporti hardcoded). Gli sviluppatori di app devono aspettarsi che durante il ridimensionamento dell'app venga visualizzato un altro messaggio di ridimensionamento subito dopo il recapito del messaggio di ridimensionamento corrente. Di conseguenza, se l'app avvia animazioni durante il ridimensionamento, è possibile che l'app riceva un altro messaggio di ridimensionamento subito dopo (quindi è importante assicurarsi che questo tipo di situazione non causa l'arresto anomalo dell'app).

 

 




