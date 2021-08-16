---
description: Vantaggi dell'elaborazione in coda
ms.assetid: dc1fc03f-1e2c-481c-95a7-f8d7b1e06bb0
title: Vantaggi dell'elaborazione in coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02c41d902d9e72af40b70ccc95efe33e2857c8ef07953c70ef1fc0879ba676ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308786"
---
# <a name="benefits-of-queued-processing"></a>Vantaggi dell'elaborazione in coda

Quando si progettano nuove applicazioni, gli sviluppatori devono considerare le implicazioni dei componenti di codifica per l'elaborazione in tempo reale (sincrona) e l'elaborazione in coda (asincrona). La scelta dipende dai requisiti dell'applicazione specifica, come determinato dalla logica di business sottostante. Come linea guida, l'elaborazione in coda offre i vantaggi seguenti rispetto all'elaborazione in tempo reale:

-   Riduzione della dipendenza dalla disponibilità dei componenti
-   Durate dei componenti più brevi
-   Produttività ininterrotta quando si usano applicazioni disconnesse
-   Affidabilità dei messaggi
-   Pianificazione efficiente dei server

## <a name="component-availability"></a>Disponibilità dei componenti

In un'applicazione di elaborazione in tempo reale, se un solo componente della transazione non è disponibile, ad esempio a causa di un sovraccarico del server o di problemi di rete, l'intero processo viene bloccato e non può essere completato. Al contrario, un'applicazione che usa il servizio componenti in coda COM+ separa la transazione in attività che devono essere completate ora e quelle che possono essere completate in un secondo momento. Ad esempio, i messaggi possono essere accodati per un'elaborazione successiva in modo che il componente richiedente sia gratuito per altre attività.

## <a name="component-lifetimes"></a>Durate dei componenti

Un'applicazione che usa il servizio componenti in coda consente al componente server di operare indipendentemente dal client. Di conseguenza, i componenti server possono essere completati più rapidamente. In un sistema in tempo reale, il componente server esiste dal momento in cui viene creato fino al rilascio dell'oggetto. Il server attende che il client esere chiamate al metodo e che i risultati siano restituiti, il che nega il ciclo rapido degli oggetti server e limita la scalabilità del server.

## <a name="disconnected-applications"></a>Applicazioni disconnesse

L'uso crescente di portatili, notebook e computer palm ha creato la necessità di applicazioni che servono client occasionalmente disconnessi o utenti mobili. In un sistema in coda, questi utenti possono continuare a lavorare in uno scenario disconnesso o quando non sono connessi al server e in un secondo momento possono connettersi ai database o ai server per elaborare le richieste. Ad esempio, un venditore può prendere ordini dai clienti e successivamente connettersi al reparto spedizioni per elaborare tali ordini.

Se si dispone di un componente che può essere eseguito connesso o disconnesso, i messaggi viaggiano in una direzione e raramente è necessario tornare indietro. Ad esempio, nello scenario di assunzione degli ordini, il componente di spedizione riceve il messaggio ed elabora il messaggio. Può generare un altro componente per la fatturazione o il controllo. Il commit del client viene eseguito prima dell'avvio del server. Il messaggio non viene inviato fino al commit dell'applicazione.

La figura seguente mostra il flusso di informazioni in uno scenario disconnesso.

![Diagramma che mostra il flusso di informazioni tra il client e il server.](images/b1818188-0294-4bd8-8bbe-9fe8eea9e09a.png)

## <a name="message-reliability"></a>Affidabilità dei messaggi

Accodamento messaggi è uno strumento potente che usa tecniche di database per proteggere i dati in modo affidabile. In caso di errore del server, Accodamento messaggi garantisce il rollback delle transazioni in modo che i messaggi non andranno persi e i dati non siano danneggiati.

## <a name="server-scheduling"></a>Pianificazione del server

Un'applicazione che usa componenti in coda è adatta per l'esecuzione di componenti spostati nel tempo, che rinvia il lavoro non critico a un periodo di minore attività. Si tratta dello stesso concetto utile applicato all'elaborazione in modalità batch tradizionale. Richieste simili possono essere posticipate per l'esecuzione contigua dal server anziché richiedere al server di reagire immediatamente a un'ampia gamma di richieste.

 

 



