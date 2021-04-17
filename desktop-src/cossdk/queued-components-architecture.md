---
description: Il servizio componenti in coda COM+ migliora il modello di programmazione COM fornendo un ambiente in cui un componente può essere richiamato in modalità sincrona (in tempo reale) o in modo asincrono (in coda).
ms.assetid: fd455679-b2b3-487f-8494-9ea296ce2c89
title: Architettura dei componenti in coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a2f6e1012bd3c11a27a44214ee28e84d5bd404
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104551694"
---
# <a name="queued-components-architecture"></a>Architettura dei componenti in coda

Il servizio componenti in coda COM+ migliora il modello di programmazione COM fornendo un ambiente in cui un componente può essere richiamato in modalità sincrona (in tempo reale) o in modo asincrono (in coda). Non è necessario che un componente sia in grado di essere utilizzato in un contesto in tempo reale o in coda.

Le applicazioni di messaggistica sono simili alle transazioni di posta elettronica tra i programmi. Il richiedente invia un messaggio al server. Quando il server riceve il messaggio, il messaggio viene elaborato. Analogamente alla posta elettronica, un sistema di messaggistica deve gestire i dettagli della rete e assicurarsi che il messaggio venga spostato dal client al server. Nel Framework dei componenti in coda, l'accodamento dei messaggi è responsabile di questa operazione.

Il servizio componenti in coda COM+ è costituito dalle parti seguenti:

-   Registratore (per il client o il lato di trasmissione)
-   Listener (per il server o il lato ricezione)
-   Player (per il server o il lato di ricezione)

![Diagramma che mostra il percorso dal client al server: client, registratore, coda, listener, lettore, server.](images/d732774b-1ca6-45ad-bce0-a95b0bfc3edb.png)

## <a name="the-recorder"></a>Registratore

In uno scenario tipico di componenti in coda, il client chiama un componente in coda. La chiamata viene effettuata al registratore dei componenti in coda, che lo inserisce come parte di un messaggio nel server e lo inserisce in una coda. Il registratore esegue il marshalling del contesto di sicurezza del client nel messaggio e registra tutte le chiamate al metodo del client. Nel ruolo di proxy per il componente server, il registratore seleziona le interfacce dalle interfacce di accodamento nel catalogo COM+.

Una rappresentazione della registrazione viene inviata a Accodamento messaggi come messaggio da inviare a un server. Quando il componente in coda presenta l'impostazione dell'attributo Transaction richiesta o supportata, Accodamento messaggi accetta il recapito del messaggio solo se il commit della transazione sul lato client e la coda di Accodamento messaggi sono transazionali, ovvero l'impostazione predefinita normalmente stabilita. Quando l'impostazione dell'attributo Transaction è richiesta New, Accodamento messaggi può accettare il messaggio anche se la transazione sul lato client viene interrotta. Per ulteriori informazioni sulle transazioni, vedere [Accodamento messaggi transazionale](transactional-message-queuing.md).

## <a name="the-listener"></a>Il listener

Il listener dei componenti in coda recupera il messaggio dalla coda e lo passa al lettore dei componenti in coda.

## <a name="the-player"></a>Il lettore

Il giocatore esegue l'unmarshalling del contesto di sicurezza del client sul lato server e quindi richiama il componente server e effettua le stesse chiamate al metodo. Le chiamate al metodo non vengono riprodotte dal lettore finché il componente client non viene completato e la transazione che ha registrato il metodo chiama commit.

## <a name="the-message-mover"></a>Mover del messaggio

Il motore messaggi in coda è un'utilità che sposta tutti i messaggi di Accodamento messaggi non riusciti da una coda a un'altra, in modo che possano essere ripetuti. L'utilità del Mover del messaggio è un oggetto di automazione che può essere richiamato con un VBScript. Per ulteriori informazioni, vedere [gestione degli errori](handling-errors-in-queued-components.md).

 

 



