---
title: Uso di MSMQ come trasporto RPC
description: Il sottosistema RPC supporta l'uso di MSMQ come trasporto in modalità sincrona e asincrona.
ms.assetid: c3f96a91-b7bb-4c2a-8699-2100324af165
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab18f4476815929e8a7e6fb4e4a1eef0a4e4e34754ac134f023c8551899e0138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010679"
---
# <a name="using-msmq-as-an-rpc-transport"></a>Uso di MSMQ come trasporto RPC

Il sottosistema RPC supporta l'uso di MSMQ come trasporto in modalità sincrona e asincrona.

La modalità sincrona usa chiamate di procedura remota convenzionali. Queste chiamate usano endpoint noti e il trasporto della coda di messaggi, [ncadg \_ mq,](/windows/desktop/Midl/ncadg-mq)come protocollo di trasporto. In modalità sincrona, le procedure remote possono avere parametri in e out e \[ [](/windows/desktop/Midl/in) \] possono usare i servizi \[ [](/windows/desktop/Midl/out-idl) \] di sicurezza RPC standard. Il sottosistema RPC crea una coda di risposta per le chiamate remote contenenti **\[ parametri out. \]** La modalità sincrona è utile per le applicazioni in cui il client deve ricevere dati dal server. La limitazione principale di questa modalità è che, come per le chiamate di procedura remota convenzionali, sia il client che il server devono essere in esecuzione e rimanere in esecuzione per tutta la durata della chiamata.

La modalità asincrona consente alle applicazioni client di effettuare chiamate al server e di restituire immediatamente, indipendentemente dallo stato dell'applicazione server o del computer server. Rende inoltre disponibile un subset di funzionalità MSMQ per la gestione delle code di messaggi e del flusso delle informazioni. La [**funzione RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) consente di controllare la qualità del servizio, la priorità delle chiamate, l'inserimento nel journal, la sicurezza e la durata della coda del processo server. La [**funzione RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) consente di specificare gli attributi della coda del processo server, ad esempio la persistenza della coda, l'autenticazione e la crittografia.

Si implementa MSMQ asincrono come si farebbe con MSMQ sincrono. È necessario usare endpoint noti e definire il protocollo di trasporto come [ncadg \_ mq.](/windows/desktop/Midl/ncadg-mq) Nel file IDL applicare l'attributo [message](/windows/desktop/Midl/message) alle funzioni che usano l'accodamento messaggi asincrono. Si noti che le funzioni di messaggio possono avere \[ solo \] parametri .

 

 