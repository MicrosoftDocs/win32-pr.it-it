---
title: Cenni preliminari
description: Pagina di navigazione RPC (Remote Procedure Call) per le sezioni di panoramica.
ms.assetid: 49dc35c3-efd7-45a2-bec0-cd68ac150754
keywords:
- RPC Remote Procedure Call , descritto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97c7735976428ffc4128b0c6a566ac56228921a3bf1070eda69af1579d90b99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927560"
---
# <a name="overviews"></a>Cenni preliminari

Questa parte della Guida per programmatori RPC (Remote Procedure Call) è costituita da una sequenza di argomenti che consentono di comprendere la programmazione di applicazioni distribuite e RPC come indicato di seguito:

-   [Microsoft RPC Model offre](microsoft-rpc-model.md) una panoramica del modello di programmazione client-server, standard per la programmazione di applicazioni distribuite e una descrizione del funzionamento di Microsoft RPC.
-   [Installazione dell'ambiente di programmazione RPC](installing-the-rpc-programming-environment.md) indica come installare i file e gli strumenti necessari per sviluppare applicazioni distribuite con Microsoft RPC.
-   [Compilazione di applicazioni RPC](building-rpc-applications.md) descrive il compilatore MIDL e l'ambiente necessario per la compilazione di applicazioni distribuite con Microsoft RPC.
-   [La connessione del client e del server offre](connecting-the-client-and-the-server.md) una panoramica del processo di inizializzazione ed esecuzione di applicazioni distribuite.
-   [L'esercitazione](tutorial.md) offre una panoramica dello sviluppo di un'applicazione distribuita di piccole dimensioni. In questo esempio vengono illustrati tutti i passaggi per lo sviluppo di un'applicazione distribuita, gli strumenti utilizzati e i componenti che costituiscono i programmi eseguibili.
-   [File IDL](the-idl-and-acf-files.md) e ACF descrive i file IDL e ACF usati per specificare l'interfaccia per la chiamata di procedura remota e le opzioni del compilatore MIDL che controllano la modalità di elaborazione di questi file.
-   [Funzionalità dei dati e del linguaggio](data-and-language-features.md) illustrano l'uso di tipi di dati standard.
-   [Matrici e puntatori](arrays-and-pointers.md) spiega come passare puntatori di matrici come parametri.
-   [Pipes](pipes.md) descrive come utilizzare le named pipe come meccanismo di trasporto per le chiamate di procedura remota.
-   [Binding e Handle descrive](binding-and-handles.md) l'handle di associazione, ovvero la struttura dei dati che consente allo sviluppatore di associare l'applicazione chiamante alla procedura remota.
-   [Gestione memoria](memory-management.md) offre idee su come gestire la memoria nel client e nel server quando si eseguono chiamate di procedura remota.
-   [I servizi di](serialization-services.md) serializzazione descrivono i metodi per la codifica o la decodifica dei dati.
-   [Sicurezza](security.md) descrive i metodi per l'implementazione delle funzionalità di sicurezza nelle applicazioni distribuite.
-   [Installazione e configurazione di applicazioni RPC](installing-and-configuring-rpc-applications.md) illustra l'installazione delle applicazioni client e server e descrive come configurare il provider di servizi dei nomi e il servizio di sicurezza. Questa sezione contiene anche informazioni sul trasporto di rete per RPC.
-   [Rpc asincrono](asynchronous-rpc.md) presenta informazioni sulle estensioni asincrone Microsoft per la definizione RPC. Le chiamate asincrone di procedura remota restituiscono immediatamente un risultato senza attendere l'output. Al termine dell'esecuzione della procedura remota nel server, trasferisce i dati restituiti al client.
-   [Accodamento](rpc-message-queuing.md) messaggi RPC descrive l'utilizzo del servizio di accodamento messaggi (MSMQ), che consente agli utenti di comunicare tra reti e sistemi indipendentemente dallo stato corrente delle applicazioni e dei sistemi in comunicazione.
-   [Remote Procedure Calls Using RPC over HTTP (Chiamate](remote-procedure-calls-using-rpc-over-http.md) di procedura remota tramite RPC su HTTP) offre ai client RPC la possibilità di connettersi in modo sicuro tramite Internet ai programmi server RPC ed eseguire chiamate di procedura remota.
-   [Il bilanciamento del](rpc-load-balancing.md) carico RPC descrive la distribuzione di volumi elevati di traffico RPC su HTTP tra numerosi server RPC all'interno di un server farm.
-   [Esempi](examples.md) contiene una descrizione dei programmi RPC di esempio forniti con Microsoft Platform Software Developer's Kit.

 

 




