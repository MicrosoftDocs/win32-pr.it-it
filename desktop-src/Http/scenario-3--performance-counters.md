---
title: Contatori delle prestazioni dello scenario 3
description: I contatori delle prestazioni misurano le quantità di informazioni o dati, in base al numero, alle dimensioni, alla durata e alla frequenza dei dati richiesti o ricevuti.
ms.assetid: 1b264144-7600-402e-86f8-674a2d02f9f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92afacf959c72735adea25c3ace60c8ae032da66394dda6731fdab913407e21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950720"
---
# <a name="scenario-3-performance-counters"></a>Scenario 3: Contatori delle prestazioni

I contatori delle prestazioni misurano le quantità di informazioni o dati, in base al numero, alle dimensioni, alla durata e alla frequenza dei dati richiesti o ricevuti. Non è consigliabile ottenere un elenco di dettagli da un contatore, ad esempio un elenco di messaggi di errore. Usare invece i contatori delle prestazioni per ottenere quantità, ad esempio il numero di messaggi di errore dall'avvio o la frequenza con cui vengono generati i messaggi di errore.

## <a name="performance-counters-for-httpsys"></a>Contatori delle prestazioni per HTTP.sys

A partire da Windows Vista e Windows Server 2008, HTTP.sys include i contatori delle metriche delle prestazioni seguenti che consentono di monitorare, diagnosticare e pianificare la capacità per i server Web: il componente API Server HTTP include i contatori delle prestazioni seguenti per facilitare il monitoraggio, la diagnosi e la pianificazione della capacità per i server Web:

- Contatori del servizio HTTP:
  - Numero di URI nella cache, aggiunti dall'avvio, eliminati dall'avvio e numero di scaricamenti della cache
  - Riscontri nella cache al secondo e mancati riscontri nella cache al secondo
- Gruppi di URL del servizio HTTP:
  - Velocità di invio dei dati, velocità di ricezione dei dati, byte trasferiti (inviati e ricevuti)
  - Numero massimo di connessioni, frequenza dei tentativi di connessione, frequenza per le richieste GET e HEAD e numero totale di richieste
- Code di richieste del servizio HTTP:
  - Numero di richieste in coda, durata delle richieste meno recenti nella coda (età dell'ultima richiesta nella coda)
  - Frequenza di arrivo delle richieste nella coda, frequenza di rifiuto, numero totale di richieste rifiutate, frequenza di riscontri nella cache

**Accesso ai contatori delle prestazioni**

1.  Digitare **perfmon al** prompt dei comandi per avviare la console di diagnostica delle prestazioni.
2.  Selezionare **Monitor prestazioni** nel controllo struttura ad albero e quindi aprire **Aggiungi contatori** facendo clic su **+** .
3.  In **Aggiungi contatori selezionare** uno dei tre insiemi di contatori delle prestazioni: Servizio **HTTP**, Code richieste servizio **HTTP** o Gruppi URL **servizio HTTP**.
4.  Per visualizzare i contatori dagli insiemi di contatori Code  richieste servizio **HTTP** e Gruppi di URL del servizio **HTTP,** selezionare le istanze e fare clic su Aggiungi **e** quindi fare clic su **OK.** Per visualizzare i contatori del servizio HTTP, selezionare l'insieme di contatori nel riquadro sinistro e fare clic su **Aggiungi**.

> [!Note]  
> Esiste una sola istanza dei contatori DELL'API del server HTTP per computer, poiché questi contatori rappresentano lo stato a livello di componente. Con le istanze dei contatori delle prestazioni del gruppo di URL, l'ID istanza (per il contatore delle prestazioni) corrisponderà all'ID del gruppo di URL. L'ID del gruppo di URL può essere visualizzato eseguendo **netsh http show servicestate**. Con le istanze dei contatori delle prestazioni delle code di richiesta, il nome dell'istanza corrisponde al nome della coda di richiesta. Il nome della coda di richieste (se esistente) può essere visualizzato dallo stesso **netsh http show servicestate**. Tuttavia, alcune applicazioni server potrebbero avere code di richieste senza nome che non possono essere abbinate a un ID istanza del contatore delle prestazioni.

 

 

 




