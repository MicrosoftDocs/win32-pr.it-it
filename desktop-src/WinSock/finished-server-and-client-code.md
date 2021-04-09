---
description: Esecuzione del codice di esempio completo dell'applicazione server e client TCP/IP.
ms.assetid: 617dfdf6-f7a7-4e72-8c77-8cfa3ab232e7
title: Esecuzione dell'esempio di codice server e client Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b3588af6bac668f0b7c785bafe2f69de4ef2b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966681"
---
# <a name="running-the-winsock-client-and-server-code-sample"></a>Esecuzione dell'esempio di codice server e client Winsock

Questa sezione contiene il codice sorgente completo per le applicazioni client e server TCP/IP:

-   [Codice client Winsock completo](complete-client-code.md)
-   [Codice server Winsock completo](complete-server-code.md)

Prima di avviare l'applicazione client, è necessario avviare l'applicazione server.

Per eseguire il server, compilare il codice sorgente completo del server ed eseguire il file eseguibile. L'applicazione server è in ascolto sulla porta TCP 27015 per la connessione di un client. Una volta che un client si connette, il server riceve i dati dal client e restituisce i dati restituiti al client. Quando il client arresta la connessione, il server arresta il socket client, chiude il socket e viene chiuso.

Per eseguire il client, compilare il codice sorgente completo del client ed eseguire il file eseguibile. L'applicazione client richiede che il nome del computer o dell'indirizzo IP del computer in cui è in esecuzione l'applicazione server venga passato come parametro della riga di comando quando viene eseguito il client. Se il client e il server vengono eseguiti nel computer di esempio, è possibile avviare il client come indicato di seguito:

**localhost client**

Il client tenta di connettersi al server sulla porta TCP 27015. Una volta che il client si connette, il client invia i dati al server e riceve tutti i dati inviati dal server. Il client chiude quindi il socket e viene chiuso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con Winsock](getting-started-with-winsock.md)
</dt> </dl>

 

 



