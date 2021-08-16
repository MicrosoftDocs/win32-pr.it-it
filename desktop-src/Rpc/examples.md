---
title: Esempi (RPC)
description: Esempi che illustrano i concetti di chiamata a procedura remota (RPC).
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- RPC remote procedure call , esempi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e75dca3866e325a4f10eb446d209b834b62ff0407e7edd19f92ec70ac700df85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930050"
---
# <a name="examples-rpc"></a>Esempi (RPC)

Platform Software Development Kit (SDK) include esempi che illustrano un'ampia gamma di concetti rpc (Remote Procedure Call), come indicato di seguito:

-   ASYNCRPC illustra la struttura di un'applicazione RPC che usa chiamate di procedura remota asincrone. Illustra anche vari metodi di notifica del completamento della chiamata.
-   CLUUID illustra l'uso dell'UUID dell'oggetto client per consentire a un client di selezionare tra più implementazioni di una procedura remota.
-   La directory DATA contiene quattro programmi: DUNION illustra unioni discriminate (non incapsulate). INOUT illustra [ \[ nei \] ](../midl/in.md)parametri , [ \[ out; \] ](../midl/out-idl.md) REPAS dimostra che [rappresenta \_ come](/windows/desktop/Midl/represent-as) attributo. XMIT illustra [l'attributo transmit \_ as.](/windows/desktop/Midl/transmit-as)
-   DYNEPT illustra un'applicazione client che gestisce la connessione al server tramite endpoint dinamici.
-   La directory FILEREP contiene quattro esempi che illustrano come gli sviluppatori possono scrivere un semplice servizio di replica file, un servizio di replica di file multi-utente, un servizio che supporta le funzionalità di sicurezza e un servizio che usa pipe asincrone RPC.
-   La directory HANDLES contiene tre programmi, AUTO, CXHNDL, USRDEF, che illustrano rispettivamente l'handle [automatico, \_ ](/windows/desktop/Midl/auto-handle)l'handle di contesto e gli handle \[ \_ \] generici (definiti dall'utente).
-   HELLO è un'implementazione client/server di "Hello, world".
-   La directory PICKLE contiene due programmi: PICKLP illustra la serializzazione delle procedure dei dati. PICKLT illustra la serializzazione del tipo di dati; entrambi i programmi usano [ \[ gli attributi di \] ](../midl/encode.md) codifica e [ \[ decodifica. \] ](../midl/decode.md)
-   PIPES illustra l'uso del costruttore di tipo pipe.
-   RPCSVC illustra l'implementazione di un servizio con RPC.
-   STROUT illustra come allocare memoria in un server per un oggetto bidimensionale (una matrice di puntatori) e passarla di nuovo al client come \[ parametro out \] -only. Il client libera quindi la memoria. Questa tecnica consente lo stub di chiamare il server senza sapere in anticipo la quantità di dati che verranno restituiti.

    Questo programma consente anche all'utente di compilare per UNICODE o ANSI.

Tutti i file di origine e i makefile per questi programmi si trovano in Platform SDK.

Per lo sviluppo di applicazioni RPC di base ed esempi più semplici, vedere gli [argomenti dell'esercitazione.](tutorial.md)

 

 
