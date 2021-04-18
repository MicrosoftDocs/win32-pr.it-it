---
title: Esempi (RPC)
description: Esempi che illustrano i concetti di RPC (Remote Procedure Call).
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- RPC remote procedure call, esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a814d78afbfc7fefa979c890cbbb8c3d4ce0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300730"
---
# <a name="examples-rpc"></a>Esempi (RPC)

Il Software Development Kit (SDK) della piattaforma include esempi che illustrano una varietà di concetti di Remote Procedure Call (RPC), come indicato di seguito:

-   ASYNCRPC illustra la struttura di un'applicazione RPC che utilizza chiamate asincrone a procedure remote. Vengono inoltre illustrati i vari metodi di notifica del completamento della chiamata.
-   CLUUID illustra l'uso dell'UUID dell'oggetto client per consentire a un client di effettuare la selezione da più implementazioni di una procedura remota.
-   La directory dei dati contiene quattro programmi: DUNION illustra le unioni discriminate (non incapsulate); Inout illustra [ \[ in \] ](../midl/in.md), parametri [ \[ out \] ](../midl/out-idl.md) ; REPAS dimostra [che rappresenta \_ come](/windows/desktop/Midl/represent-as) attributo. XMIT illustra l'attributo [trasmissione \_ As](/windows/desktop/Midl/transmit-as) .
-   DYNEPT illustra un'applicazione client che gestisce la connessione al server tramite endpoint dinamici.
-   La directory FILEREP contiene quattro esempi che illustrano come gli sviluppatori possono scrivere un semplice servizio Replica file, un servizio Replica file multiutente, un servizio che supporta le funzionalità di sicurezza e un servizio che utilizza pipe asincrone RPC.
-   GESTISCE la directory contiene tre programmi, AUTO, CXHNDL, USRDEF, che illustrano rispettivamente handle [automatico \_ ](/windows/desktop/Midl/auto-handle), \[ handle di contesto \_ \] e handle generici (definiti dall'utente).
-   HELLo è un'implementazione client/server di "Hello, World".
-   La directory Pickle contiene due programmi: PICKLP illustra la serializzazione delle procedure dati; La serializzazione del tipo di dati viene illustrata in pickle entrambi i programmi utilizzano gli attributi [ \[ Encode \] ](../midl/encode.md) e [ \[ Decode \] ](../midl/decode.md) .
-   PIPEs illustra l'uso del costruttore di tipo pipe.
-   RPCSVC illustra l'implementazione di un servizio con RPC.
-   STROUT illustra come allocare memoria in un server per un oggetto bidimensionale, ovvero una matrice di puntatori, e come passarlo di nuovo al client come \[ \] parametro out-only. Il client libera quindi la memoria. Questa tecnica consente allo stub di chiamare il server senza conoscere in anticipo la quantità di dati che verranno restituiti.

    Questo programma consente inoltre all'utente di compilare per UNICODE o ANSI.

Tutti i file di origine e i makefile per questi programmi si trovano in Platform SDK.

Per lo sviluppo di applicazioni RPC di base e per esempi più semplici, vedere gli argomenti dell' [esercitazione](tutorial.md) .

 

 
