---
title: Linee guida per le applicazioni client/server
description: Le applicazioni client/server non devono presupporre che una connessione a un singolo computer sia equivalente a una singola sessione utente.
ms.assetid: 69822ef1-eca8-4302-b014-8e5894d52109
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d27f5bd024e2311307f39e4f86584747b59b874576e5cd5aa28e735b2945d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001619"
---
# <a name="clientserver-application-guidelines"></a>Linee guida per le applicazioni client/server

Le applicazioni client/server non devono presupporre che una connessione a un singolo computer sia equivalente a una singola sessione utente. Si tratta di un caso speciale del problema descritto in [Indirizzi IP e nomi di computer.](ip-addresses-and-computer-names.md)

Per identificare in modo univoco una connessione client/server, ogni modulo client deve usare un nome o un identificatore univoco. Le applicazioni possono usare oggetti denominati o pipe, socket o altri metodi IPC. Per altre informazioni, vedere [Spazi dei nomi degli oggetti kernel.](kernel-object-namespaces.md)

Per essere Servizi Desktop remoto, il modulo server in un'applicazione client/server deve essere in grado di gestire più client che si connettono dallo stesso computer. A tale scopo, il modulo server deve accettare connessioni client tramite un'interfaccia globale ben definita, ad esempio RPC o named pipe. Il server e il client devono negoziare un canale di comunicazione diverso per ogni sessione utente. Il client deve stabilire una connessione al server usando protocolli che supportano facilmente questo tipo di operazione, ad esempio TCP/IP, in cui è possibile utilizzare una connessione socket diversa per ogni applicazione client.

Il modulo client può chiamare la [**funzione ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) per recuperare l'identificatore della relativa Servizi Desktop remoto sessione. Il client usa quindi una forma di comunicazione interprocesso per passare il relativo identificatore di sessione al modulo server. I moduli client e server possono quindi usare l'identificatore di sessione per configurare un canale di comunicazione privato. Ad esempio, il modulo server può usare un identificatore di sessione per accedere agli oggetti nello spazio dei nomi della sessione per gli oggetti kernel.

Inoltre, il modulo server può usare l'identificatore di sessione in una [**chiamata WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) per recuperare informazioni aggiuntive sul client. Il modulo server può anche usare l'identificatore di sessione in una [**chiamata WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) per visualizzare un messaggio nel terminale client. Il modulo server può anche creare due eventi per monitorare la connessione client e la disconnessione da una sessione. A tale scopo, tuttavia, è necessario Desktop remoto server Host sessione Desktop remoto. Per altre informazioni, vedere [Monitoraggio delle connessioni di sessione e delle disconnessioni.](monitoring-session-connections-and-disconnections.md)

Le richieste di input dell'utente sono una potenziale fonte di problemi per le applicazioni client/server. Ad esempio, se un servizio chiama la funzione [**MessageBox,**](/windows/desktop/api/winuser/nf-winuser-messagebox) la finestra di messaggio viene visualizzata sul desktop del server Host sessione Desktop remoto, non sul desktop client. Per visualizzare un messaggio su un desktop client, il servizio può chiamare la [**funzione WtsSendMessage.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) In alternativa, il servizio può richiedere l'input dal modulo client e il modulo client può visualizzare l'interfaccia utente e inviare l'input risultante al servizio.

I processi generati da più sessioni possono inviare e ricevere dati l'uno dall'altro tramite l'uso di blocchi di memoria condivisa. Per altre informazioni, vedere [Creazione di memoria condivisa denominata.](/windows/desktop/Memory/creating-named-shared-memory) La memoria condivisa non può essere usata nelle condizioni seguenti:

-   I processi che usano il blocco di memoria condivisa sono stati generati da più sessioni.
-   Le sessioni condividono le stesse credenziali di autenticazione utente.

 

 