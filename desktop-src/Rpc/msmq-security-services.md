---
title: Servizi di sicurezza MSMQ
description: I messaggi RPC sincroni possono utilizzare le funzionalità di sicurezza disponibili in fase di esecuzione RPC. Per ulteriori informazioni, vedere sicurezza.
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd2e12cd9f32a571088de769adb079327caab9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118095"
---
# <a name="msmq-security-services"></a>Servizi di sicurezza MSMQ

I messaggi RPC sincroni possono utilizzare le funzionalità di sicurezza disponibili in fase di esecuzione RPC. Per ulteriori informazioni, vedere [sicurezza](security.md) .

Le chiamate asincrone al \[ [messaggio](/windows/desktop/Midl/message) \] non possono utilizzare la sicurezza RPC perché non esiste un handshake tra client e server. Infatti, il server potrebbe non essere ancora in esecuzione al momento della chiamata. Per accedere ai servizi di sicurezza forniti da servizi di Accodamento messaggi (MSMQ), l'applicazione client deve chiamare [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) per controllare il livello di autenticazione e privacy per le chiamate al server.

L'applicazione server può chiamare [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) dall'interno di una chiamata di procedura remota per determinare il livello di sicurezza per la chiamata. La tabella seguente illustra il mapping tra le costanti di sicurezza RPC e la sicurezza MSMQ.



| Livello di sicurezza RPC                | Descrizione                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| \_livello di autenticazione \_ RPC \_ None           | La chiamata non è autenticata o crittografata.                                                |
| \_ \_ integrità PKT a livello di autenticazione \_ RPC \_ | La chiamata viene autenticata utilizzando la sicurezza MSMQ.                                             |
| \_ \_ privacy PKT a livello di autenticazione \_ RPC \_   | La chiamata viene autenticata e crittografata mentre viene spostata tra la coda del client e del server. |



 

Il server è anche in grado di forzare l'autenticazione e la crittografia delle chiamate chiamando [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) e impostando il livello di autenticazione RPC c mq, l'integrità PKT e i flag di privacy del livello auth c mq di RPC \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ nella struttura dei [**\_ criteri RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) .

 

 