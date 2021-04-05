---
title: Funzionamento di RPC
description: Gli strumenti RPC lo rendono visibile agli utenti come se un client chiamasse direttamente una procedura che si trova in un programma server remoto.
ms.assetid: 265f31b8-9a41-4255-b070-fd50b00b935b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12832d0de4eb972bb1d9d51df0c871191d4d079a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711833"
---
# <a name="how-rpc-works"></a>Funzionamento di RPC

Gli strumenti RPC lo rendono visibile agli utenti come se un client chiamasse direttamente una procedura che si trova in un programma server remoto. Il client e il server dispongono ognuno dei propri spazi di indirizzi. ovvero ogni risorsa ha una propria risorsa di memoria allocata ai dati utilizzati dalla procedura. Nella figura seguente viene illustrata l'architettura RPC.

![architettura RPC](images/prog-a11.png)

Come illustrato nella figura, l'applicazione client chiama una procedura Stub locale anziché il codice effettivo che implementa la procedura. Gli stub vengono compilati e collegati con l'applicazione client. Anziché contenere il codice effettivo che implementa la procedura remota, il codice stub del client:

-   Recupera i parametri richiesti dallo spazio degli indirizzi del client.
-   Converte i parametri in base alle esigenze in un formato NDR standard per la trasmissione in rete.
-   Chiama le funzioni nella libreria di runtime del client RPC per inviare la richiesta e i relativi parametri al server.

Il server esegue i passaggi seguenti per chiamare la procedura remota.

1.  Le funzioni della libreria run-time RPC del server accettano la richiesta e chiamano la procedura stub del server.
2.  Lo stub del server recupera i parametri dal buffer di rete e li converte dal formato di trasmissione di rete al formato necessario per il server.
3.  Lo stub del server chiama la procedura effettiva nel server.

Viene quindi eseguita la procedura remota, probabilmente generando parametri di output e un valore restituito. Al termine della procedura remota, una sequenza simile di passaggi restituisce i dati al client.

1.  La procedura remota restituisce i dati allo stub del server.
2.  Lo stub del server converte i parametri di output nel formato necessario per la trasmissione in rete e li restituisce alle funzioni della libreria di run-time RPC.
3.  Le funzioni della libreria run-time RPC del server trasmettono i dati in rete al computer client.

Il client completa il processo accettando i dati in rete e restituendo la funzione chiamante.

1.  La libreria di runtime RPC client riceve i valori restituiti dalla procedura remota e li restituisce allo stub client.
2.  Lo stub client converte i dati dall'NDR nel formato utilizzato dal computer client. Lo stub scrive i dati nella memoria del client e restituisce il risultato al programma chiamante sul client.
3.  La procedura chiamante continua come se la procedura fosse stata chiamata nello stesso computer.

Le librerie di runtime sono disponibili in due parti: una libreria di importazione, collegata con l'applicazione e la libreria di runtime RPC, implementata come libreria di collegamento dinamico (DLL).

L'applicazione server contiene le chiamate alle funzioni della libreria di runtime del server che registrano l'interfaccia del server e consentono al server di accettare chiamate a procedure remote. L'applicazione server contiene anche le procedure remote specifiche dell'applicazione chiamate dalle applicazioni client.

 

 




