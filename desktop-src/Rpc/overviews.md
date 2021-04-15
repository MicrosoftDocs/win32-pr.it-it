---
title: Cenni preliminari
description: Pagina di navigazione RPC (Remote Procedure Call) per le sezioni introduttive.
ms.assetid: 49dc35c3-efd7-45a2-bec0-cd68ac150754
keywords:
- RPC (Remote Procedure Call), descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea90c08dc075fdd90ae604b0d347ba6ac5baf9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331364"
---
# <a name="overviews"></a>Cenni preliminari

Questa parte della guida e del riferimento per programmatori RPC (Remote Procedure Call) è costituita da una sequenza di argomenti che consentono di comprendere la programmazione di applicazioni distribuite e RPC come segue:

-   Il [modello Microsoft RPC](microsoft-rpc-model.md) offre una panoramica del modello di programmazione client-server, gli standard per la programmazione di applicazioni distribuite e una descrizione del funzionamento di Microsoft RPC.
-   L' [installazione dell'ambiente di programmazione RPC](installing-the-rpc-programming-environment.md) indica come installare i file e gli strumenti necessari per lo sviluppo di applicazioni distribuite con Microsoft RPC.
-   La [compilazione di applicazioni RPC](building-rpc-applications.md) descrive il compilatore MIDL e l'ambiente necessario per la creazione di applicazioni distribuite con Microsoft RPC.
-   La [connessione tra il client e il server](connecting-the-client-and-the-server.md) fornisce una panoramica del processo di inizializzazione ed esecuzione di applicazioni distribuite.
-   [Viene fornita](tutorial.md) una panoramica dello sviluppo di un'applicazione distribuita di piccole dimensioni. Questo esempio illustra tutti i passaggi per lo sviluppo di un'applicazione distribuita, gli strumenti usati e i componenti che costituiscono i programmi eseguibili.
-   I [file IDL e ACF](the-idl-and-acf-files.md) descrivono i file IDL e ACF usati per specificare l'interfaccia per la chiamata di procedura remota e le opzioni del compilatore MIDL che controllano la modalità di elaborazione di questi file.
-   Le [funzionalità dei dati e del linguaggio](data-and-language-features.md) illustrano l'uso dei tipi di dati standard.
-   [Matrici e puntatori](arrays-and-pointers.md) spiegano come passare i puntatori alle matrici come parametri.
-   [Pipes](pipes.md) descrive come usare named pipe come meccanismo di trasporto per le chiamate di procedure remote.
-   [Binding e handle](binding-and-handles.md) descrive l'handle di associazione, ovvero la struttura dei dati che consente allo sviluppatore di associare l'applicazione chiamante alla procedura remota.
-   [Gestione della memoria](memory-management.md) offre suggerimenti su come gestire la memoria nel client e nel server durante l'esecuzione di chiamate a procedure remote.
-   I [servizi di serializzazione](serialization-services.md) descrivono i metodi per codificare o decodificare i dati.
-   [Sicurezza](security.md) vengono descritti i metodi per l'implementazione delle funzionalità di sicurezza nelle applicazioni distribuite.
-   L' [installazione e la configurazione di applicazioni RPC](installing-and-configuring-rpc-applications.md) illustra l'installazione di applicazioni client e server, descrive come configurare il provider di servizi dei nomi e il servizio di sicurezza. Questa sezione contiene anche informazioni sul trasporto di rete per RPC.
-   [RPC asincrone](asynchronous-rpc.md) presenta informazioni sulle estensioni asincrone Microsoft per la definizione RPC. Le chiamate asincrone a procedure remote vengono restituite immediatamente senza attendere l'output. Al termine dell'esecuzione della procedura remota sul server, trasferisce i dati restituiti al client.
-   [Accodamento messaggi RPC](rpc-message-queuing.md) descrive l'utilizzo del servizio di Accodamento messaggi (MSMQ), che consente agli utenti di comunicare tra reti e sistemi indipendentemente dallo stato corrente delle applicazioni e dei sistemi che comunicano.
-   Le [chiamate a procedure remote che utilizzano RPC su http](remote-procedure-calls-using-rpc-over-http.md) forniscono ai client RPC la possibilità di connettersi in modo sicuro tramite Internet ai programmi server RPC ed eseguire chiamate a procedure remote.
-   Il [bilanciamento del carico RPC](rpc-load-balancing.md) descrive la distribuzione di volumi elevati di RPC su traffico HTTP tra numerosi server RPC all'interno di una server farm.
-   [Esempi](examples.md) contiene una descrizione dei programmi RPC di esempio forniti con Microsoft Platform Software Developer ' s Kit.

 

 




