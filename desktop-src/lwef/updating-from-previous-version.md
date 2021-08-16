---
title: Aggiornamento dalla versione precedente
description: Aggiornamento dalla versione precedente
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de894f220db7ee09847a8fa767e1f99c38cee8014cb86b65c1251e0579eaabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745724"
---
# <a name="updating-from-previous-version"></a>Aggiornamento dalla versione precedente

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Le applicazioni compilate e compilate con la versione 1.5 precedente di Microsoft Agent devono essere eseguite senza modifiche nella nuova versione 2.0. La [**proprietà Connected**](connected-property.md) non può più essere impostata su **False.** Alcune proprietà dell'oggetto SpeechInput che sono state sostituite esistono ancora, ma non attivano più alcun valore e il server non genera più gli eventi [**Restart**](https://www.bing.com/search?q=**Restart**) e [**Shutdown.**](https://www.bing.com/search?q=**Shutdown**)

Tuttavia, se si aggiornano le applicazioni per l'uso del controllo Agent 2.0, potrebbe essere necessario modificare il codice. Se è stata installata la versione 2.0 di Microsoft Agent e si carica un progetto Visual Basic che usa la versione precedente del controllo Agent, Visual Basic include un'opzione che visualizza automaticamente un messaggio che indica che è stata rilevata una nuova versione del controllo. Per garantire il corretto funzionamento dell'applicazione, scegliere sempre di usare la versione successiva.

Per altri linguaggi di programmazione , ad esempio Microsoft Office 97 VBA, per aggiornare il controllo potrebbe essere necessario prima rimuovere il controllo Agent 1.5 e salvare il codice. Chiudere quindi l'ambiente di programmazione, riavviare l'ambiente di programmazione, ricaricare il codice e inserire il nuovo controllo. Evitare di modificare un'applicazione abilitata per Agent 2.0 nella stessa istanza dell'ambiente di programmazione in cui si sta modificando un'applicazione abilitata per Agent 1.5. Alcuni ambienti di programmazione potrebbero non gestire le differenze tra le due versioni dei controlli.

Dovrebbe essere possibile disinstallare la versione di Agent 1.5 nel sistema dopo l'installazione di Agent 2.0. Tuttavia, se Agent 1.5 è installato nella versione 2.0, potrebbe essere necessario reinstallare la versione 2.0.

 

 




