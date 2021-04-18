---
title: Contatori delle prestazioni dello scenario 3
description: I contatori delle prestazioni misurano quantità di informazioni o dati, in base al numero, alle dimensioni, alla durata e alla frequenza dei dati richiesti o ricevuti.
ms.assetid: 1b264144-7600-402e-86f8-674a2d02f9f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de90607cbda0542ee385b83f44bec878927d509f
ms.sourcegitcommit: fc3f2a28a55e590ac38846048f10b64ba527a98d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "106300682"
---
# <a name="scenario-3-performance-counters"></a>Scenario 3: contatori delle prestazioni

I contatori delle prestazioni misurano quantità di informazioni o dati, in base al numero, alle dimensioni, alla durata e alla frequenza dei dati richiesti o ricevuti. Non è previsto l'ottenimento di un elenco di dettagli da un contatore, ad esempio un elenco di messaggi di errore. Usare invece i contatori delle prestazioni per ottenere le quantità, ad esempio il numero di messaggi di errore dall'avvio o la frequenza con cui vengono generati i messaggi di errore.

## <a name="performance-counters-for-httpsys"></a>Contatori delle prestazioni per HTTP.sys

A partire da Windows Vista e Windows Server 2008, HTTP.sys dispone dei contatori delle metriche delle prestazioni seguenti per semplificare il monitoraggio, la diagnosi e la pianificazione della capacità per i server Web: il componente API server HTTP presenta i contatori delle prestazioni seguenti che consentono il monitoraggio, la diagnosi e la pianificazione della capacità per i server Web:

- Contatori servizio HTTP:
  - Numero di URI nella cache, aggiunti dall'avvio, eliminati dall'avvio e numero di scaricamenti della cache
  - Riscontri nella cache/secondo e mancati riscontri nella cache/secondo
- Gruppi di URL del servizio HTTP:
  - Velocità di invio dati, velocità di ricezione dati, byte trasferiti (inviati e ricevuti)
  - Numero massimo di connessioni, velocità dei tentativi di connessione, frequenza delle richieste GET e HEAD e numero totale di richieste
- Code di richieste del servizio HTTP:
  - Numero di richieste in coda, validità delle richieste meno recenti in coda (età dell'ultima richiesta nella coda)
  - Frequenza di arrivo delle richieste nella coda, frequenza di rifiuto, numero totale di richieste rifiutate, frequenza dei riscontri nella cache

**Accesso ai contatori delle prestazioni**

1.  Digitare **PerfMon** al prompt dei comandi per avviare la console di diagnostica delle prestazioni.
2.  Selezionare **Performance Monitor** nel controllo struttura ad albero, quindi aprire il **Aggiungi contatori** facendo clic su **+** .
3.  Da **Aggiungi contatori** selezionare dai tre set di contatori delle prestazioni **: servizio http**, **code di richieste del servizio http** o gruppi di URL del **servizio http**.
4.  Per visualizzare i contatori da insiemi di contatori di **richieste del servizio** http e gruppi di **URL del servizio http** , selezionare **istanza** /e, quindi fare clic su **Aggiungi** e infine su **OK**. Per visualizzare i contatori del servizio HTTP, selezionare l'insieme di contatori nel riquadro a sinistra e fare clic su **Aggiungi**.

> [!Note]  
> Per ogni computer esiste una sola istanza dei contatori dell'API server HTTP, poiché questi contatori rappresentano lo stato a livello di componente. Con le istanze dei contatori delle prestazioni del gruppo di URL, l'ID istanza (per il contatore delle prestazioni) corrisponderà all'ID gruppo URL. Per visualizzare l'ID gruppo URL, è possibile eseguire **netsh http show servicestate**. Con le istanze dei contatori delle prestazioni della coda di richieste, il nome dell'istanza corrisponde al nome della coda di richieste. Il nome della coda di richieste (se esistente) può essere visualizzato dallo stesso **netsh http show servicestate**. Tuttavia, alcune applicazioni server possono avere code di richiesta senza nome che non possono essere confrontate con un ID istanza del contatore delle prestazioni.

 

 

 




