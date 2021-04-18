---
title: Aggiornamento dalla versione precedente
description: Aggiornamento dalla versione precedente
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7860e2cf49fbe21c2522226ec61ab57c93d9df27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297867"
---
# <a name="updating-from-previous-version"></a>Aggiornamento dalla versione precedente

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Le applicazioni compilate e compilate con la versione 1,5 precedente di Microsoft Agent devono essere eseguite senza modifiche nella nuova versione 2,0. La proprietà [**connessa**](connected-property.md) non può più essere impostata su **false**; alcune proprietà dell'oggetto SpeechInput che sono state sostituite sono ancora disponibili, ma non trasformano più alcun valore e il server non genera più gli eventi di [**riavvio**](https://www.bing.com/search?q=**Restart**) e [**arresto**](https://www.bing.com/search?q=**Shutdown**) .

Tuttavia, se si aggiornano le applicazioni per l'utilizzo del controllo Agent 2,0, potrebbe essere necessario modificare il codice. Se è stata installata la versione 2,0 di Microsoft Agent e si carica un progetto Visual Basic usare la versione precedente del controllo agente, Visual Basic include un'opzione che visualizzerà automaticamente un messaggio che indica che è stata rilevata una nuova versione del controllo. Per assicurare il corretto funzionamento dell'applicazione, scegliere sempre di usare la versione più recente.

Per gli altri linguaggi di programmazione (ad esempio Microsoft Office 97 VBA), per aggiornare il controllo, potrebbe essere necessario rimuovere prima il controllo agente 1,5 e salvare il codice. Quindi, chiudere l'ambiente di programmazione, riavviare l'ambiente di programmazione, ricaricare il codice e inserire il nuovo controllo. Evitare di modificare un'applicazione abilitata per Agent 2,0 nella stessa istanza dell'ambiente di programmazione in cui si sta modificando un'applicazione abilitata per Agent 1,5. Alcuni ambienti di programmazione potrebbero non gestire le differenze tra le due versioni dei controlli.

Al termine dell'installazione dell'agente 2,0, dovrebbe essere possibile disinstallare la versione 1,5 dell'agente nel sistema. Tuttavia, se l'agente 1,5 viene installato sulla versione 2,0, potrebbe essere necessario reinstallare 2,0.

 

 




