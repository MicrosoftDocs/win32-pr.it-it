---
description: Esecuzione del codice di esempio completo dell'applicazione client e server TCP/IP.
ms.assetid: 617dfdf6-f7a7-4e72-8c77-8cfa3ab232e7
title: Esecuzione dell'esempio di codice client e server Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdb5a4b2385c9545410cfc29c913ea81660f6dc2810b92279fad22212781065c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132484"
---
# <a name="running-the-winsock-client-and-server-code-sample"></a>Esecuzione dell'esempio di codice client e server Winsock

Questa sezione contiene il codice sorgente completo per le applicazioni client e server TCP/IP:

-   [Completare il codice client Winsock](complete-client-code.md)
-   [Completare il codice del server Winsock](complete-server-code.md)

L'applicazione server deve essere avviata prima dell'avvio dell'applicazione client.

Per eseguire il server, compilare il codice sorgente completo del server ed eseguire il file eseguibile. L'applicazione server è in ascolto sulla porta TCP 27015 per la connessione di un client. Una volta che un client si connette, il server riceve i dati dal client e invia (invia) i dati ricevuti al client. Quando il client arresta la connessione, il server arresta il socket client, chiude il socket e termina.

Per eseguire il client, compilare il codice sorgente client completo ed eseguire il file eseguibile. L'applicazione client richiede che il nome del computer o dell'indirizzo IP del computer in cui è in esecuzione l'applicazione server sia passato come parametro della riga di comando quando viene eseguito il client. Se il client e il server vengono eseguiti nel computer di esempio, il client può essere avviato come segue:

**client localhost**

Il client tenta di connettersi al server sulla porta TCP 27015. Dopo la connessione, il client invia i dati al server e riceve tutti i dati inviati dal server. Il client chiude quindi il socket e termina.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con Winsock](getting-started-with-winsock.md)
</dt> </dl>

 

 



