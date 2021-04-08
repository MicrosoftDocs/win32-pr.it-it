---
title: Utilizzo di MSMQ come trasporto RPC
description: Il sottosistema RPC supporta l'utilizzo di MSMQ come trasporto in modalità sincrona e asincrona.
ms.assetid: c3f96a91-b7bb-4c2a-8699-2100324af165
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a647fe4111e3ba4fc2ad0fe05fb7bcb48729a4c2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729298"
---
# <a name="using-msmq-as-an-rpc-transport"></a>Utilizzo di MSMQ come trasporto RPC

Il sottosistema RPC supporta l'utilizzo di MSMQ come trasporto in modalità sincrona e asincrona.

La modalità sincrona usa chiamate a procedure remote convenzionali. Queste chiamate utilizzano endpoint noti e il trasporto della coda di messaggi, [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq), come protocollo di trasporto. In modalità sincrona, le procedure remote possono disporre \[ [di parametri in](/windows/desktop/Midl/in) \] e \[ [out](/windows/desktop/Midl/out-idl) \] e possono utilizzare i servizi di sicurezza RPC standard. Il sottosistema RPC crea una coda di risposta per le chiamate remote contenenti parametri **\[ out \]** . La modalità sincrona è utile per le applicazioni in cui il client deve ricevere i dati dal server. La limitazione principale di questa modalità è che, come per le chiamate di procedure remote convenzionali, sia il client che il server devono essere in esecuzione e rimanere in esecuzione per la durata della chiamata.

La modalità asincrona consente alle applicazioni client di effettuare chiamate al server e di restituire immediatamente, indipendentemente dallo stato dell'applicazione server o del computer server. Rende inoltre disponibile un subset di funzionalità MSMQ per la gestione delle code di messaggi e del flusso di informazioni. La funzione [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) consente di controllare la qualità del servizio, la priorità delle chiamate, il journaling, la sicurezza e la durata della coda del processo server. La funzione [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) consente di specificare gli attributi della coda del processo server, ad esempio la persistenza della coda, l'autenticazione e la crittografia.

Il MSMQ asincrono viene implementato come per l'MSMQ sincrono. È necessario usare endpoint noti e definire il protocollo di trasporto come [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq). Nel file IDL applicare l'attributo [Message](/windows/desktop/Midl/message) alle funzioni che utilizzano l'Accodamento messaggi asincrono. Si noti che le funzioni di messaggio possono avere \[ \] solo parametri in.

 

 