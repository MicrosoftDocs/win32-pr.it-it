---
title: Qualità del servizio (RPC)
description: I programmi client possono utilizzare la funzione RpcBindingSetAuthInfoEx anziché la funzione RpcBindingSetAuthInfo per creare un'associazione autenticata.
ms.assetid: bc3d47ba-3c1b-4aba-8fe3-b4501a621931
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee93b1aa376c9d6f4e2b3eedab73c91471d42498
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103873194"
---
# <a name="quality-of-service-rpc"></a>Qualità del servizio (RPC)

I programmi client possono utilizzare la funzione [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) anziché la funzione [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) per creare un'associazione autenticata. In caso affermativo, passano un puntatore a una [**struttura \_ \_ QoS di sicurezza RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) come parametro finale di **RpcBindingSetAuthInfoEx**. Questa struttura contiene informazioni sulla qualità del servizio. I programmi client possono inoltre specificare il rilevamento delle identità e selezionare il tipo di rappresentazione.

Utilizzare il membro **capabilities** della struttura [**\_ \_ QoS di sicurezza RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) per impostare le parti dell'applicazione client/server autenticate. Se \_ \_ \_ \_ è selezionata l'impostazione predefinita funzionalità QoS C RPC, la libreria di runtime RPC autentica il client o il server in base all'impostazione predefinita per il provider di servizi condivisi. Per impostazione predefinita, il provider SSP del protocollo Kerberos autentica sia il client che il server. Il valore predefinito per tutti gli altri SSP forniti da Microsoft consiste nell'autenticare il client sul server, ma non nell'autenticare il server per il client.

Se il client e il server devono sempre eseguire l'autenticazione reciproca, impostare il membro delle **funzionalità** della struttura [**\_ \_ QoS di sicurezza RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) sulle \_ funzionalità di \_ \_ \_ autenticazione reciproca di QoS C \_ . Alcuni provider di sicurezza potrebbero non supportare l'autenticazione reciproca. Se \_ \_ \_ \_ \_ per tali provider di sicurezza viene specificata l'autenticazione reciproca delle funzionalità QoS C, viene restituito un errore quando viene effettuata una chiamata a una procedura remota. Quando si utilizza SSP SCHANNEL, è possibile impostare anche il membro delle **funzionalità** sulle \_ funzionalità QoS C di RPC \_ \_ \_ qualsiasi \_ autorità. Questa costante specifica che il provider di servizi condivisi deve convalidare la chiamata di procedura remota anche se l'autorità di certificazione che ha emesso il certificato di autenticazione del client non si trova nell'archivio certificati radice del provider di servizi condivisi. Per impostazione predefinita, il certificato viene rifiutato se il provider di servizi condivisi non riconosce l'autorità di certificazione. L'autorità di certificazione è una società o un'organizzazione indipendente, ad esempio VeriSign, che rilascia i certificati di autenticazione.

Le applicazioni possono inoltre impostare il rilevamento delle identità utilizzato dalla libreria di runtime RPC. I programmi usano in genere il [*Rilevamento statico delle identità*](s-glos.md). Con il rilevamento statico, le credenziali del client vengono impostate quando viene chiamata la funzione [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) . La libreria di runtime RPC usa quindi tali credenziali per tutte le chiamate RPC sull'associazione, indipendentemente dalle modifiche apportate all'identità del thread chiamante o del processo chiamante. Le applicazioni possono anche selezionare [*rilevamento identità dinamica*](d-glos.md). Il rilevamento dinamico delle identità indica alla libreria di runtime RPC di usare le credenziali del thread chiamante al momento di ogni chiamata, anziché l'handle di associazione. Il rilevamento delle identità predefinito è statico.

Se l'identità del client non verrà modificata, il rilevamento delle identità statiche può avere caratteristiche di prestazioni migliori e può salvare il tempo di esecuzione RPC dal controllo ogni volta che l'identità nel thread chiamante è uguale all'identità assegnata al sistema di sicurezza. Se l'identità del thread chiamante può variare tra le chiamate e il server deve riconoscere tali modifiche, è preferibile specificare il rilevamento dinamico delle identità, ovvero il tempo di esecuzione RPC in modo silenzioso ed efficiente, che tiene traccia dell'identità e, in caso di modifica dell'identità, gestisce la modifica per conto dell'utente.

> [!Note]  
> Per le chiamate **ncalrpc** , il rilevamento delle identità statica e dinamica hanno caratteristiche di prestazioni diverse e, a seconda delle circostanze, può essere più veloce.

 

Come parte della specifica QOS, il programma client può anche impostare il tipo di rappresentazione che un programma server può eseguire per suo conto. Per ulteriori informazioni, vedere [rappresentazione client](client-impersonation.md).

Il campo relativo al numero di versione della struttura [**\_ \_ QoS di sicurezza RPC**](/windows/desktop/api/Rpcdce/ns-rpcdce-rpc_security_qos) deve essere sempre impostato sulla \_ \_ versione QoS di sicurezza C \_ \_ .

 

 




