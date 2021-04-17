---
title: Linee guida per applicazioni client/server
description: Le applicazioni client/server non devono presupporre che una connessione a computer singolo sia equivalente a una singola sessione utente.
ms.assetid: 69822ef1-eca8-4302-b014-8e5894d52109
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0c1a71256f3ab469bfeb1c08b2d096b56ac1b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299864"
---
# <a name="clientserver-application-guidelines"></a>Linee guida per applicazioni client/server

Le applicazioni client/server non devono presupporre che una connessione a computer singolo sia equivalente a una singola sessione utente. Si tratta di un caso speciale del problema descritto in [indirizzi IP e nomi di computer](ip-addresses-and-computer-names.md).

Per identificare in modo univoco una connessione client/server, ogni modulo client deve usare un nome o un identificatore univoco. Le applicazioni possono usare oggetti denominati o pipe, socket o altri metodi IPC. Per altre informazioni, vedere [spazi dei nomi degli oggetti kernel](kernel-object-namespaces.md).

Per essere Servizi Desktop remoto compatibile, il modulo server in un'applicazione client/server deve essere in grado di gestire più client che si connettono dallo stesso computer. A tale scopo, è necessario che il modulo server accetti le connessioni client tramite un'interfaccia globale ben definita, ad esempio RPC o Named Pipes. Il server e il client devono negoziare un canale di comunicazione diverso per ogni sessione utente. Il client deve stabilire una connessione al server utilizzando protocolli che supportano facilmente questo tipo di operazione, ad esempio TCP/IP, in cui è possibile utilizzare una connessione socket diversa per ogni applicazione client.

Il modulo client può chiamare la funzione [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) per recuperare l'identificatore della sessione di Servizi Desktop remoto. Il client usa quindi una forma di comunicazione interprocesso per passare il relativo identificatore di sessione al modulo server. I moduli client e server possono quindi utilizzare l'identificatore di sessione per configurare un canale di comunicazione privato. Ad esempio, il modulo server può usare un identificatore di sessione per accedere agli oggetti nello spazio dei nomi della sessione per gli oggetti kernel.

Il modulo server può inoltre usare l'identificatore di sessione in una chiamata [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) per recuperare informazioni aggiuntive sul client. Il modulo server può anche usare l'identificatore di sessione in una chiamata [**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) per visualizzare un messaggio nel terminale client. Il modulo server può inoltre creare due eventi per monitorare la connessione e la disconnessione del client da una sessione. Per eseguire questa operazione, tuttavia, deve essere registrato nel server host sessione Desktop remoto (host sessione Desktop remoto). Per ulteriori informazioni, vedere [monitoraggio delle connessioni di sessione e disconnessione](monitoring-session-connections-and-disconnections.md).

Le richieste di input dell'utente costituiscono una potenziale fonte di problemi per le applicazioni client/server. Se, ad esempio, un servizio chiama la funzione [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) , la finestra di messaggio viene visualizzata sul desktop del server Host sessione Desktop remoto e non sul desktop client. Per visualizzare un messaggio su un desktop client, il servizio può chiamare la funzione [**WtsSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) . In alternativa, il servizio può richiedere l'input dal modulo client e il modulo client può visualizzare l'interfaccia utente e inviare di nuovo l'input risultante al servizio.

I processi generati da più sessioni possono inviare e ricevere dati tra loro tramite l'utilizzo di blocchi di memoria condivisi. Per ulteriori informazioni, vedere [creazione di una memoria condivisa denominata](/windows/desktop/Memory/creating-named-shared-memory). La memoria condivisa non può essere utilizzata nelle condizioni seguenti:

-   I processi che utilizzano il blocco di memoria condivisa sono stati generati da più sessioni.
-   Le sessioni condividono le stesse credenziali di autenticazione utente.

 

 