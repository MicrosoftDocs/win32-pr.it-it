---
title: Autenticazione reciproca nelle applicazioni RPC
description: I servizi RPC possono usare i punti di connessione del servizio per la pubblicazione oppure possono usare le API RpcNs (RPC Name Service).
ms.assetid: 9f575aef-0a4b-4e1b-8ea9-5f40e6c3d9c7
ms.tgt_platform: multiple
keywords:
- Autenticazione reciproca nelle applicazioni RPC AD
- Active Directory, utilizzo di, autenticazione reciproca, RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05a8591056293c916205b5b600c1b1a061d169f0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872286"
---
# <a name="mutual-authentication-in-rpc-applications"></a>Autenticazione reciproca nelle applicazioni RPC

I servizi RPC possono usare i punti di connessione del servizio per la pubblicazione oppure possono usare le API RpcNs (RPC Name Service). In questo argomento viene illustrato come eseguire l'autenticazione reciproca con un servizio RPC che pubblica se stesso utilizzando le API del servizio del nome RPC (RpcNs).

**Per registrare un nome SPN nella directory**

1.  Chiamare la funzione [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) per comporre un nome dell'entità servizio (SPN) per il servizio.
2.  Chiamare la funzione [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) per registrare il nome SPN nell'account del servizio o nel computer in cui viene eseguito il servizio.

**Per registrare un servizio con il servizio di denominazione RPC**

1.  Verificare che i nomi SPN appropriati siano registrati nell'account con cui è in esecuzione il servizio. Per altre informazioni, vedere [attività di manutenzione degli account di accesso](logon-account-maintenance-tasks.md).
2.  Chiamare la funzione [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) per registrare il nome SPN del servizio con il servizio di autenticazione RPC e specificare la **\_ \_ \_ \_ negoziazione GSS C AuthN** come servizio di autenticazione da usare.

Per ulteriori informazioni sull'esecuzione dell'autenticazione reciproca in un servizio RPC, vedere [scrittura di un server SSPI autenticato](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).

**Per autenticare il servizio dal client**

1.  Estrarre il nome host dall'associazione RPC.
2.  Comporre il nome SPN per il servizio chiamando la funzione [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) con la classe del servizio, il nome host DNS e il nome del servizio; si tratta del nome distinto del punto di connessione nel caso di RpcNs.

    Per ulteriori informazioni sulla composizione di un nome SPN per un servizio RpcNs, vedere [composizione di nomi SPN per un servizio RpcNs](composing-spns-for-an-rpcns-service.md).

3.  Configurare una struttura [**\_ \_ QoS di sicurezza RPC**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) per richiedere l'autenticazione reciproca.
4.  Chiamare la funzione [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) per impostare i dati di autenticazione per l'associazione RPC. Per assicurarsi che le comunicazioni non siano state manomesse, il client deve richiedere almeno l' **\_ \_ \_ \_ \_ integrità PKT del livello auth C di RPC** . Per una maggiore sicurezza, il client deve specificare il **\_ livello di \_ autenticazione \_ \_ PKT \_ di RPC C** per la crittografia della richiesta.
5.  Eseguire la chiamata RPC.

Per ulteriori informazioni sull'esecuzione dell'autenticazione reciproca in un client RPC, vedere [scrittura di un client SSPI autenticato](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).

**Per autenticare il client dal servizio**

1.  Chiamare la funzione [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) per verificare i parametri di autenticazione specificati dal client. Se il client non ha richiesto il livello di autenticazione desiderato, rifiutare la chiamata. Tenere presente che un servizio RPC deve verificare il livello di autenticazione, il servizio di autenticazione e l'identità del client a ogni chiamata per assicurarsi che il client sia stato autenticato correttamente.
2.  Chiamare la funzione [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) per rappresentare il client.
3.  Eseguire l'operazione richiesta.
4.  Chiamare la funzione [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) per ripristinare il contesto di sicurezza del servizio.

Per ulteriori informazioni sulla rappresentazione client RPC, vedere [rappresentazione client](/windows/desktop/Rpc/client-impersonation).

Per altre informazioni, vedere:

-   [Pubblicazione con il servizio nome RPC (RpcNs)](publishing-with-the-rpc-name-service-rpcns.md)
-   [Concetti di base sulla sicurezza RPC](/windows/desktop/Rpc/rpc-security-essentials)

 

 