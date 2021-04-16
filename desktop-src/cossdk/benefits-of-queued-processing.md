---
description: Vantaggi dell'elaborazione in coda
ms.assetid: dc1fc03f-1e2c-481c-95a7-f8d7b1e06bb0
title: Vantaggi dell'elaborazione in coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0d2068d70ecf611ec334632c8b8f819319ef3
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "104559197"
---
# <a name="benefits-of-queued-processing"></a>Vantaggi dell'elaborazione in coda

Quando si progettano nuove applicazioni, gli sviluppatori devono considerare le implicazioni dei componenti di codifica per l'elaborazione in tempo reale (sincrona) rispetto all'elaborazione in coda (asincrona). La scelta dipende dai requisiti dell'applicazione specifica, come determinato dalla logica di business sottostante. Come linea guida, l'elaborazione in coda offre i vantaggi seguenti rispetto all'elaborazione in tempo reale:

-   Dipendenza ridotta dalla disponibilità di componenti
-   Durate del componente più breve
-   Produttività ininterrotta quando si usano applicazioni disconnesse
-   Affidabilità del messaggio
-   Pianificazione efficiente del server

## <a name="component-availability"></a>Disponibilità componenti

In un'applicazione di elaborazione in tempo reale, se solo un componente della transazione non è disponibile, probabilmente a causa di problemi di rete o di sovraccarico del server, l'intero processo è bloccato e non può essere completato. Al contrario, un'applicazione che utilizza il servizio componenti in coda COM+ separa la transazione in attività che devono essere completate ora e quelle che possono essere completate in un secondo momento. Ad esempio, i messaggi possono essere accodati per l'elaborazione successiva, in modo che il componente richiedente sia disponibile per altre attività.

## <a name="component-lifetimes"></a>Durate componenti

Un'applicazione che utilizza il servizio componenti in coda consente al componente server di funzionare indipendentemente dal client. Di conseguenza, i componenti del server possono essere completati più rapidamente. In un sistema in tempo reale, il componente server esiste dal momento in cui viene creato fino a quando l'oggetto non viene rilasciato. Il server attende che il client effettui le chiamate al metodo e che vengano restituiti i risultati, che nega il ciclo rapido di oggetti server e limita la scalabilità del server.

## <a name="disconnected-applications"></a>Applicazioni disconnesse

Il crescente utilizzo di laptop, notebook e computer Palm ha creato una necessità per le applicazioni che interessano saltuariamente client o utenti mobili. In un sistema in coda questi utenti possono continuare a lavorare in uno scenario disconnesso o quando non sono connessi al server e possono successivamente connettersi ai database o ai server per elaborare le richieste. Ad esempio, un venditore può prendere ordini dai clienti e successivamente connettersi al reparto spedizioni per elaborare tali ordini.

Se si dispone di un componente che può essere eseguito in modalità connessa o disconnessa, i messaggi vengono spostati in una direzione e raramente è necessario spostarsi avanti e indietro. Ad esempio, nello scenario di ordinamento, il componente Shipping riceve il messaggio e lo elabora. Potrebbe generare un altro componente per la fatturazione o il controllo. Il client eseguirà il commit prima che il server venga avviato. Il messaggio non viene inviato fino a quando non viene eseguito il commit dell'applicazione.

Nella figura seguente viene illustrato il flusso di informazioni in uno scenario disconnesso.

![Diagramma che mostra il flusso di informazioni tra il client e il server.](images/b1818188-0294-4bd8-8bbe-9fe8eea9e09a.png)

## <a name="message-reliability"></a>Affidabilità del messaggio

Accodamento messaggi è uno strumento potente che utilizza tecniche di database per proteggere i dati in modo affidabile. In caso di errore del server, Accodamento messaggi garantisce che venga eseguito il rollback delle transazioni in modo che i messaggi non vengano persi e che i dati non siano danneggiati.

## <a name="server-scheduling"></a>Pianificazione server

Un'applicazione che usa componenti in coda è adatta per l'esecuzione di componenti con spostamento temporale, che rinvia il lavoro non critico a un periodo di minore attività. Si tratta dello stesso concetto utile applicato all'elaborazione tradizionale in modalità batch. È possibile posticipare richieste simili per l'esecuzione contigua da parte del server piuttosto che richiedere al server di reagire immediatamente a una vasta gamma di richieste.

 

 



