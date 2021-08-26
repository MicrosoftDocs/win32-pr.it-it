---
title: Servizi di sicurezza MSMQ
description: I messaggi RPC sincroni possono usare qualsiasi funzionalità di sicurezza disponibile in fase di esecuzione RPC. Per altri dettagli, vedere Sicurezza.
ms.assetid: 0f4d45c4-7457-4449-8736-e141a95f6930
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f142d83c003f1293556786167222a4e9e88d3912786aa328319efa7fb0ea345d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019651"
---
# <a name="msmq-security-services"></a>Servizi di sicurezza MSMQ

I messaggi RPC sincroni possono usare qualsiasi funzionalità di sicurezza disponibile in fase di esecuzione RPC. Per [altri dettagli,](security.md) vedere Sicurezza.

Le chiamate di messaggi asincrone non possono usare la sicurezza RPC perché non è presente \[ [](/windows/desktop/Midl/message) \] alcun handshake tra client e server. In realtà, il server potrebbe non essere in esecuzione al momento della chiamata. Per accedere ai servizi di sicurezza forniti da Message Queuing Services (MSMQ), l'applicazione client deve chiamare [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) per controllare il livello di autenticazione e la privacy per le chiamate al server.

L'applicazione server può chiamare [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) dall'interno di una chiamata di procedura remota per determinare il livello di sicurezza per tale chiamata. Il mapping tra le costanti di sicurezza RPC e la sicurezza MSMQ è illustrato nella tabella seguente.



| Livello di sicurezza RPC                | Descrizione                                                                                |
|-----------------------------------|--------------------------------------------------------------------------------------------|
| LIVELLO \_ RPC AUTHN \_ \_ NONE           | La chiamata non è autenticata o crittografata.                                                |
| INTEGRITÀ \_ PKT A \_ LIVELLO DI \_ AUTENTICAZIONE \_ RPC | La chiamata viene autenticata usando la sicurezza MSMQ.                                             |
| PRIVACY \_ \_ PKT A LIVELLO \_ DI AUTENTICAZIONE \_ RPC   | La chiamata viene autenticata e crittografata durante il viaggio tra la coda client e server. |



 

Il server può anche forzare l'autenticazione e la crittografia delle chiamate chiamando [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) e impostando i flag RPC \_ \_ C \_ MQ AUTHN \_ LEVEL \_ NONE, RPC \_ C \_ MQ \_ AUTHN LEVEL PKT INTEGRITY e \_ RPC C \_ \_ \_ \_ MQ \_ AUTHN \_ LEVEL PKT \_ \_ PRIVACY [**\_**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_policy) nella struttura RPC POLICY.

 

 