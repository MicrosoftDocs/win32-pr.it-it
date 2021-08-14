---
title: Autenticazione reciproca nelle applicazioni RPC
description: I servizi RPC possono usare i punti di connessione del servizio per pubblicare se stessi oppure le API RPC Name Service (RpcNs).
ms.assetid: 9f575aef-0a4b-4e1b-8ea9-5f40e6c3d9c7
ms.tgt_platform: multiple
keywords:
- Autenticazione reciproca nelle applicazioni RPC AD
- Active Directory, uso, autenticazione reciproca, RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c7d5ea3632d08671861b72267419efd54c1a6a89770fbde72543596b29fa8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186056"
---
# <a name="mutual-authentication-in-rpc-applications"></a>Autenticazione reciproca nelle applicazioni RPC

I servizi RPC possono usare i punti di connessione del servizio per pubblicare se stessi oppure le API RPC Name Service (RpcNs). In questo argomento viene illustrato come eseguire l'autenticazione reciproca con un servizio RPC che si pubblica usando le API RPC Name Service (RpcNs).

**Per registrare un nome SPN nella directory**

1.  Chiamare la [**funzione DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) per comporre un nome dell'entità servizio (SPN) per il servizio.
2.  Chiamare la [**funzione DsWriteAccountSpn per**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) registrare il nome SPN nell'account del servizio o nell'account computer nel cui contesto verrà eseguito il servizio.

**Per registrare un servizio con il servizio di denominazione RPC**

1.  Verificare che i nomi SPN appropriati siano registrati nell'account con cui è in esecuzione il servizio. Per altre informazioni, vedere [Attività di manutenzione dell'account di accesso.](logon-account-maintenance-tasks.md)
2.  Chiamare la [**funzione RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) per registrare il nome SPN del servizio con il servizio di autenticazione RPC e specificare **RPC C \_ \_ AUTHN \_ GSS \_ NEGOTIATE** come servizio di autenticazione da usare.

Per altre informazioni sull'esecuzione dell'autenticazione reciproca in un servizio RPC, vedere Scrittura di [un server SSPI autenticato.](/windows/desktop/Rpc/writing-an-authenticated-sspi-server)

**Per autenticare il servizio dal client**

1.  Estrarre il nome host dall'associazione RPC.
2.  Comporre il nome SPN per il servizio chiamando la funzione [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) con la classe del servizio, il nome host DNS e il nome del servizio; che è il nome distinto del punto di connessione nel caso di RPCN.

    Per altre informazioni sulla composizione di un nome SPN per un servizio RpcNs, vedere Composizione di nomi [SPN per un servizio RpcNs.](composing-spns-for-an-rpcns-service.md)

3.  Configurare una struttura [**\_ \_ QOS di sicurezza RPC**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) per richiedere l'autenticazione reciproca.
4.  Chiamare la [**funzione RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) per impostare i dati di autenticazione per l'associazione RPC. Il client deve richiedere almeno **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ INTEGRITY** per garantire che le comunicazioni non siano state manomissionate. Per una maggiore sicurezza, il client deve specificare **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** per richiedere la crittografia.
5.  Eseguire la chiamata RPC.

Per altre informazioni sull'esecuzione dell'autenticazione reciproca in un client RPC, vedere Scrittura di [un client SSPI autenticato.](/windows/desktop/Rpc/writing-an-authenticated-sspi-client)

**Per autenticare il client dal servizio**

1.  Chiamare la [**funzione RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) per verificare i parametri di autenticazione specificati dal client. Se il client non ha richiesto il livello di autenticazione desiderato, rifiutare la chiamata. Tenere presente che un servizio RPC deve verificare il livello di autenticazione, il servizio di autenticazione e l'identità client in ogni chiamata per garantire che il client sia stato autenticato correttamente.
2.  Chiamare la [**funzione RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) per rappresentare il client.
3.  Eseguire l'operazione richiesta.
4.  Chiamare la [**funzione RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) per ripristinare il contesto di sicurezza del servizio.

Per altre informazioni sulla rappresentazione del client RPC, vedere [Rappresentazione client.](/windows/desktop/Rpc/client-impersonation)

Per altre informazioni, vedere:

-   [Pubblicazione con RPC Name Service (RpcNs)](publishing-with-the-rpc-name-service-rpcns.md)
-   [Informazioni di base sulla sicurezza RPC](/windows/desktop/Rpc/rpc-security-essentials)

 

 