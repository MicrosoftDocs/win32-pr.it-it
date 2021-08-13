---
description: Il servizio componenti in coda COM+ migliora il modello di programmazione COM fornendo un ambiente in cui un componente può essere richiamato in modo sincrono (in tempo reale) o asincrono (in coda).
ms.assetid: fd455679-b2b3-487f-8494-9ea296ce2c89
title: Architettura dei componenti in coda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93914fd82a14c73b134098a759c8d61e324b6cda65d03de23f9c3ea2fcfb53f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117916207"
---
# <a name="queued-components-architecture"></a>Architettura dei componenti in coda

Il servizio componenti in coda COM+ migliora il modello di programmazione COM fornendo un ambiente in cui un componente può essere richiamato in modo sincrono (in tempo reale) o asincrono (in coda). Un componente non deve essere a conoscenza del fatto che viene utilizzato in tempo reale o in un contesto in coda.

Le applicazioni di messaggistica sono come le transazioni di posta elettronica tra programmi. Il richiedente invia un messaggio al server. Quando il server vi arriva, il messaggio viene elaborato. Analogamente alla posta elettronica, un sistema di messaggistica deve gestire i dettagli della rete e assicurarsi che il messaggio passi dal client al server. Nel framework dei componenti in coda, Accodamento messaggi è responsabile di questa operazione.

Il servizio componenti in coda COM+ è costituito dalle parti seguenti:

-   Registratore (per il lato client o di invio)
-   Listener (per il lato server o di ricezione)
-   Lettore (per il lato server o di ricezione)

![Diagramma che mostra il percorso dal client al server: client, registratore, coda, listener, lettore, server.](images/d732774b-1ca6-45ad-bce0-a95b0bfc3edb.png)

## <a name="the-recorder"></a>Registratore

In un tipico scenario di componenti in coda, il client chiama un componente in coda. La chiamata viene effettuata al registratore di componenti in coda, che lo inserisce in un pacchetto come parte di un messaggio al server e lo inserisce in una coda. Il registratore effettua il marshalling del contesto di sicurezza del client nel messaggio e registra tutte le chiamate al metodo del client. Nel ruolo di proxy per il componente server, il registratore seleziona le interfacce dalle interfacce di cui è possibile eseguire query nel catalogo COM+.

Una rappresentazione della registrazione viene inviata ad Accodamento messaggi come messaggio da inviare a un server. Quando l'attributo della transazione del componente in coda è impostato su Richiesto o Supportato, Accodamento messaggi accetta il recapito del messaggio solo se viene eseguito il commit della transazione sul lato client e la coda di Accodamento messaggi è transazionale, ovvero l'impostazione predefinita normalmente stabilita. Quando l'impostazione dell'attributo della transazione è Requires New, Accodamento messaggi può accettare il messaggio anche se la transazione sul lato client viene interrotta. Per altre informazioni sulle transazioni, vedere [Transactional Message Queuing](transactional-message-queuing.md).

## <a name="the-listener"></a>The Listener

Il listener dei componenti in coda recupera il messaggio dalla coda e lo passa al lettore dei componenti in coda.

## <a name="the-player"></a>Lettore

Il lettore esegue l'unmarshaling del contesto di sicurezza del client sul lato server, quindi richiama il componente server ed esegue le stesse chiamate al metodo. Le chiamate al metodo non vengono riprodotte dal lettore fino al completamento del componente client e del commit della transazione che ha registrato il metodo.

## <a name="the-message-mover"></a>Spostamento dei messaggi

Lo spostamento messaggi dei componenti in coda è un'utilità che sposta tutti i messaggi di Accodamento messaggi non riusciti da una coda a un'altra in modo che possano essere ritentati. L'utilità di spostamento dei messaggi è un oggetto di automazione che può essere richiamato con vbscript. Per altre informazioni, vedere [Gestione degli errori.](handling-errors-in-queued-components.md)

 

 



