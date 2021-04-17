---
description: Sono disponibili diversi modi per gestire l'invio di messaggi SOAP ricevuti al servizio appropriato. I due meccanismi più semplici sono la distribuzione a livello di trasporto, l'indirizzo e l'invio dell'azione.
ms.assetid: 988dc505-5d1f-46df-9340-107483bb9581
title: Invio di messaggi SOAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a60e896557a64b840ec890ddc5c5d2e2cf8295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529382"
---
# <a name="dispatching-soap-messages"></a>Invio di messaggi SOAP

Sono disponibili diversi modi per gestire l'invio di messaggi SOAP ricevuti al servizio appropriato. I due meccanismi più semplici sono la distribuzione a livello di trasporto, l'indirizzo e l'invio dell'azione.

## <a name="transport-level-dispatch"></a>Dispatch a livello di trasporto

Con la distribuzione a livello di trasporto, il server HTTP sottostante (ad esempio l' [API HTTP](/windows/desktop/Http/http-api-start-page)) viene usato per gestire il routing delle richieste al dispositivo e ai relativi servizi. Il server fornisce un URL diverso per ogni servizio e per il dispositivo e i sink diversi sono registrati per ogni URL. In questo modo è possibile progettare il codice in modo che ogni servizio sia isolato dall'altro, in esecuzione come componenti distinti all'interno dello stesso processo o in esecuzione come processi distinti.

La distribuzione a livello di trasporto presenta alcuni vantaggi. I messaggi possono essere inviati al componente appropriato senza prima analizzare la busta SOAP o il corpo del messaggio. Inoltre, è possibile riutilizzare il meccanismo esistente per il routing dei messaggi forniti dalla maggior parte delle implementazioni del server HTTP, il che significa che il codice di invio personalizzato non è necessario. Isola inoltre il codice di elaborazione SOAP tra i servizi, che fornisce un livello di sicurezza, poiché i servizi sicuri evitano che i messaggi viaggino attraverso codice comune.

## <a name="address-and-action-dispatch"></a>Indirizzo e invio di azioni

L'invio di indirizzi e azioni si basa sulle intestazioni SOAP per determinare il servizio appropriato a cui viene inviato il messaggio. Questo modello può inoltre utilizzare informazioni aggiuntive, ad esempio parametri di riferimento, per facilitare l'invio.

Questo modello incoraggia il riutilizzo del codice in uno stack di messaggistica a più livelli, poiché tutto il codice fino al processore SOAP è condiviso da tutti i servizi. Inoltre, non sono necessari indirizzi di trasporto distinti per i servizi, il che significa che gli indirizzi UUID possono essere utilizzati per gli endpoint di servizio. La distribuzione degli indirizzi e delle azioni converte inoltre più direttamente in un modello di programmazione. Gli sviluppatori possono collegare servizi e dispositivi a un singolo componente che gestisce il routing, anziché dover associare un livello HTTP o creare componenti distinti per ogni servizio.

 

 
