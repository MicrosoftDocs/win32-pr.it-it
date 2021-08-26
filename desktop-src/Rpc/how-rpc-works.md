---
title: Funzionamento di RPC
description: Gli strumenti RPC lo fanno sembrare agli utenti come se un client chiama direttamente una procedura che si trova in un programma server remoto.
ms.assetid: 265f31b8-9a41-4255-b070-fd50b00b935b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd7a3adf59e848d962d4765a0feee16eb1fa84842c2a1ddd34ed82ecf95a8e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020856"
---
# <a name="how-rpc-works"></a>Funzionamento di RPC

Gli strumenti RPC lo fanno sembrare agli utenti come se un client chiama direttamente una procedura che si trova in un programma server remoto. Il client e il server hanno ognuno i propri spazi di indirizzi. in altri, ognuno ha una propria risorsa di memoria allocata ai dati usati dalla procedura. La figura seguente illustra l'architettura RPC.

![Architettura rpc](images/prog-a11.png)

Come illustrato nella figura, l'applicazione client chiama una routine stub locale anziché il codice effettivo che implementa la procedura. Gli stub vengono compilati e collegati all'applicazione client. Anziché contenere il codice effettivo che implementa la procedura remota, il codice stub del client:

-   Recupera i parametri obbligatori dallo spazio degli indirizzi del client.
-   Converte i parametri in base alle esigenze in un formato NDR standard per la trasmissione in rete.
-   Chiama le funzioni nella libreria di runtime del client RPC per inviare la richiesta e i relativi parametri al server.

Il server esegue i passaggi seguenti per chiamare la procedura remota.

1.  Le funzioni della libreria di runtime RPC del server accettano la richiesta e chiamano la procedura stub del server.
2.  Lo stub del server recupera i parametri dal buffer di rete e li converte dal formato di trasmissione di rete nel formato necessario per il server.
3.  Lo stub del server chiama la procedura effettiva nel server.

Viene quindi eseguita la procedura remota, generando eventualmente parametri di output e un valore restituito. Al termine della procedura remota, una sequenza di passaggi simile restituisce i dati al client.

1.  La procedura remota restituisce i dati al server stub.
2.  Lo stub del server converte i parametri di output nel formato richiesto per la trasmissione in rete e li restituisce alle funzioni della libreria di runtime RPC.
3.  Le funzioni della libreria di runtime RPC del server trasmettono i dati in rete al computer client.

Il client completa il processo accettando i dati in rete e restituirlo alla funzione chiamante.

1.  La libreria di runtime RPC client riceve i valori restituiti dalla procedura remota e li restituisce al client stub.
2.  Lo stub client converte i dati dal relativo rapporto di mancato recapito al formato usato dal computer client. Lo stub scrive i dati nella memoria del client e restituisce il risultato al programma chiamante nel client.
3.  La routine chiamante continua come se la procedura fosse stata chiamata nello stesso computer.

Le librerie di runtime vengono fornite in due parti: una libreria di importazione collegata all'applicazione e la libreria di runtime RPC, implementata come libreria a collegamento dinamico (DLL).

L'applicazione server contiene chiamate alle funzioni della libreria di runtime del server che registrano l'interfaccia del server e consentono al server di accettare chiamate di procedura remota. L'applicazione server contiene anche le procedure remote specifiche dell'applicazione chiamate dalle applicazioni client.

 

 




