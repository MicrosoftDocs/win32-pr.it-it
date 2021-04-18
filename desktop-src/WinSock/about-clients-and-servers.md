---
description: 'Esistono due tipi distinti di applicazioni di rete socket: server e client.'
ms.assetid: 05e42384-1746-462d-82c7-8df848b4525e
title: Informazioni su server e client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a951d23ba1c6ad4f0f5ffd1f674b056a36c3f8dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307059"
---
# <a name="about-servers-and-clients"></a>Informazioni su server e client

Esistono due tipi distinti di applicazioni di rete socket: server e client.

I server e i client hanno comportamenti diversi; Pertanto, il processo di creazione di tali elementi è diverso. Di seguito è riportato il modello generale per la creazione di un client e un server TCP/IP di streaming.

## <a name="server"></a>Server

1.  Inizializzare Winsock.
2.  Creare un socket.
3.  Associare il socket.
4.  Ascolto sul socket per un client.
5.  Accettare una connessione da un client.
6.  Ricevere e inviare dati.
7.  Eseguire la disconnessione.

## <a name="client"></a>Client

1.  Inizializzare Winsock.
2.  Creare un socket.
3.  Connettersi al server.
4.  Inviare e ricevere dati.
5.  Eseguire la disconnessione.

> [!Note]  
> Alcuni passaggi sono gli stessi per un client e un server. Questi passaggi vengono implementati quasi esattamente allo stesso modo. Alcuni dei passaggi di questa guida saranno specifici del tipo di applicazione da creare.

 

Primo passaggio: [creazione di un'applicazione Winsock di base](creating-a-basic-winsock-application.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con Winsock](getting-started-with-winsock.md)
</dt> </dl>

 

 



