---
description: 'Esistono due tipi distinti di applicazioni di rete socket: Server e Client.'
ms.assetid: 05e42384-1746-462d-82c7-8df848b4525e
title: Informazioni su server e client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e6d8016d1fc9c23b901a03a924cd0e3ade3982dc2e1bf0db277eac47170d89
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898641"
---
# <a name="about-servers-and-clients"></a>Informazioni su server e client

Esistono due tipi distinti di applicazioni di rete socket: Server e Client.

I server e i client hanno comportamenti diversi. Pertanto, il processo di creazione è diverso. Di seguito è riportato il modello generale per la creazione di un server TCP/IP di streaming e di un client.

## <a name="server"></a>Server

1.  Inizializzare Winsock.
2.  Creare un socket.
3.  Associare il socket.
4.  Restare in ascolto sul socket per un client.
5.  Accettare una connessione da un client.
6.  Ricevere e inviare dati.
7.  Eseguire la disconnessione.

## <a name="client"></a>Client

1.  Inizializzare Winsock.
2.  Creare un socket.
3.  Connessione al server.
4.  Inviare e ricevere dati.
5.  Eseguire la disconnessione.

> [!Note]  
> Alcuni passaggi sono gli stessi per un client e un server. Questi passaggi vengono implementati quasi esattamente allo stesso modo. Alcuni dei passaggi descritti in questa guida saranno specifici del tipo di applicazione da creare.

 

Primo passaggio: [Creazione di un'applicazione Winsock di base](creating-a-basic-winsock-application.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività iniziali con Winsock](getting-started-with-winsock.md)
</dt> </dl>

 

 



