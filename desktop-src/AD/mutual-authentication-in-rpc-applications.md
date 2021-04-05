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
# <a name="mutual-authentication-in-rpc-applications"></a><span data-ttu-id="02be5-105">Autenticazione reciproca nelle applicazioni RPC</span><span class="sxs-lookup"><span data-stu-id="02be5-105">Mutual Authentication in RPC Applications</span></span>

<span data-ttu-id="02be5-106">I servizi RPC possono usare i punti di connessione del servizio per la pubblicazione oppure possono usare le API RpcNs (RPC Name Service).</span><span class="sxs-lookup"><span data-stu-id="02be5-106">RPC services can use service connection points to publish themselves, or they can use the RPC name service (RpcNs) APIs.</span></span> <span data-ttu-id="02be5-107">In questo argomento viene illustrato come eseguire l'autenticazione reciproca con un servizio RPC che pubblica se stesso utilizzando le API del servizio del nome RPC (RpcNs).</span><span class="sxs-lookup"><span data-stu-id="02be5-107">This topic discusses how to perform mutual authentication with an RPC service that publishes itself using the RPC name service (RpcNs) APIs.</span></span>

<span data-ttu-id="02be5-108">**Per registrare un nome SPN nella directory**</span><span class="sxs-lookup"><span data-stu-id="02be5-108">**To register an SPN in the directory**</span></span>

1.  <span data-ttu-id="02be5-109">Chiamare la funzione [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) per comporre un nome dell'entità servizio (SPN) per il servizio.</span><span class="sxs-lookup"><span data-stu-id="02be5-109">Call the [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) function to compose a service principal name (SPN) for the service.</span></span>
2.  <span data-ttu-id="02be5-110">Chiamare la funzione [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) per registrare il nome SPN nell'account del servizio o nel computer in cui viene eseguito il servizio.</span><span class="sxs-lookup"><span data-stu-id="02be5-110">Call the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function to register the SPN on the service account or computer account in whose context the service will run.</span></span>

<span data-ttu-id="02be5-111">**Per registrare un servizio con il servizio di denominazione RPC**</span><span class="sxs-lookup"><span data-stu-id="02be5-111">**To register a service with the RPC naming service**</span></span>

1.  <span data-ttu-id="02be5-112">Verificare che i nomi SPN appropriati siano registrati nell'account con cui è in esecuzione il servizio.</span><span class="sxs-lookup"><span data-stu-id="02be5-112">Verify that the appropriate SPNs are registered on the account under which the service is running.</span></span> <span data-ttu-id="02be5-113">Per altre informazioni, vedere [attività di manutenzione degli account di accesso](logon-account-maintenance-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="02be5-113">For more information, see [Logon Account Maintenance Tasks](logon-account-maintenance-tasks.md).</span></span>
2.  <span data-ttu-id="02be5-114">Chiamare la funzione [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) per registrare il nome SPN del servizio con il servizio di autenticazione RPC e specificare la **\_ \_ \_ \_ negoziazione GSS C AuthN** come servizio di autenticazione da usare.</span><span class="sxs-lookup"><span data-stu-id="02be5-114">Call the [**RpcServerRegisterAuthInfo**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterauthinfo) function to register the service SPN with the RPC authentication service, and specify **RPC\_C\_AUTHN\_GSS\_NEGOTIATE** as the authentication service to use.</span></span>

<span data-ttu-id="02be5-115">Per ulteriori informazioni sull'esecuzione dell'autenticazione reciproca in un servizio RPC, vedere [scrittura di un server SSPI autenticato](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).</span><span class="sxs-lookup"><span data-stu-id="02be5-115">For more information about performing mutual authentication in an RPC service, see [Writing an Authenticated SSPI Server](/windows/desktop/Rpc/writing-an-authenticated-sspi-server).</span></span>

<span data-ttu-id="02be5-116">**Per autenticare il servizio dal client**</span><span class="sxs-lookup"><span data-stu-id="02be5-116">**To authenticate the service from the client**</span></span>

1.  <span data-ttu-id="02be5-117">Estrarre il nome host dall'associazione RPC.</span><span class="sxs-lookup"><span data-stu-id="02be5-117">Extract the host name from the RPC Binding.</span></span>
2.  <span data-ttu-id="02be5-118">Comporre il nome SPN per il servizio chiamando la funzione [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) con la classe del servizio, il nome host DNS e il nome del servizio; si tratta del nome distinto del punto di connessione nel caso di RpcNs.</span><span class="sxs-lookup"><span data-stu-id="02be5-118">Compose the SPN for the service by calling the [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) function with the service class, the DNS host name, and the service name; that is the distinguished name of the connection point in the case of RpcNs.</span></span>

    <span data-ttu-id="02be5-119">Per ulteriori informazioni sulla composizione di un nome SPN per un servizio RpcNs, vedere [composizione di nomi SPN per un servizio RpcNs](composing-spns-for-an-rpcns-service.md).</span><span class="sxs-lookup"><span data-stu-id="02be5-119">For more information about composing an SPN for an RpcNs service, see [Composing SPNs for an RpcNs Service](composing-spns-for-an-rpcns-service.md).</span></span>

3.  <span data-ttu-id="02be5-120">Configurare una struttura [**\_ \_ QoS di sicurezza RPC**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) per richiedere l'autenticazione reciproca.</span><span class="sxs-lookup"><span data-stu-id="02be5-120">Set up an [**RPC\_SECURITY\_QOS**](/windows/desktop/api/rpcdce/ns-rpcdce-rpc_security_qos) structure to request mutual authentication.</span></span>
4.  <span data-ttu-id="02be5-121">Chiamare la funzione [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) per impostare i dati di autenticazione per l'associazione RPC.</span><span class="sxs-lookup"><span data-stu-id="02be5-121">Call the [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) function to set the authentication data for the RPC binding.</span></span> <span data-ttu-id="02be5-122">Per assicurarsi che le comunicazioni non siano state manomesse, il client deve richiedere almeno l' **\_ \_ \_ \_ \_ integrità PKT del livello auth C di RPC** .</span><span class="sxs-lookup"><span data-stu-id="02be5-122">The client must request at least **RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY** to ensure that communications have not been tampered.</span></span> <span data-ttu-id="02be5-123">Per una maggiore sicurezza, il client deve specificare il **\_ livello di \_ autenticazione \_ \_ PKT \_ di RPC C** per la crittografia della richiesta.</span><span class="sxs-lookup"><span data-stu-id="02be5-123">For increased security, the client should specify **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** to request encryption.</span></span>
5.  <span data-ttu-id="02be5-124">Eseguire la chiamata RPC.</span><span class="sxs-lookup"><span data-stu-id="02be5-124">Perform the RPC call.</span></span>

<span data-ttu-id="02be5-125">Per ulteriori informazioni sull'esecuzione dell'autenticazione reciproca in un client RPC, vedere [scrittura di un client SSPI autenticato](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).</span><span class="sxs-lookup"><span data-stu-id="02be5-125">For more information about performing mutual authentication in an RPC client, see [Writing an Authenticated SSPI Client](/windows/desktop/Rpc/writing-an-authenticated-sspi-client).</span></span>

<span data-ttu-id="02be5-126">**Per autenticare il client dal servizio**</span><span class="sxs-lookup"><span data-stu-id="02be5-126">**To authenticate the client from the service**</span></span>

1.  <span data-ttu-id="02be5-127">Chiamare la funzione [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) per verificare i parametri di autenticazione specificati dal client.</span><span class="sxs-lookup"><span data-stu-id="02be5-127">Call the [**RpcBindingInqAuthClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqauthclient) function to verify the authentication parameters specified by the client.</span></span> <span data-ttu-id="02be5-128">Se il client non ha richiesto il livello di autenticazione desiderato, rifiutare la chiamata.</span><span class="sxs-lookup"><span data-stu-id="02be5-128">If the client has not requested the desired level of authentication, reject the call.</span></span> <span data-ttu-id="02be5-129">Tenere presente che un servizio RPC deve verificare il livello di autenticazione, il servizio di autenticazione e l'identità del client a ogni chiamata per assicurarsi che il client sia stato autenticato correttamente.</span><span class="sxs-lookup"><span data-stu-id="02be5-129">Be aware that an RPC service must verify the authentication level, authentication service, and client identity on every call to ensure that the client has been properly authenticated.</span></span>
2.  <span data-ttu-id="02be5-130">Chiamare la funzione [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) per rappresentare il client.</span><span class="sxs-lookup"><span data-stu-id="02be5-130">Call the [**RpcImpersonateClient**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcimpersonateclient) function to impersonate the client.</span></span>
3.  <span data-ttu-id="02be5-131">Eseguire l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="02be5-131">Perform the requested operation.</span></span>
4.  <span data-ttu-id="02be5-132">Chiamare la funzione [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) per ripristinare il contesto di sicurezza del servizio.</span><span class="sxs-lookup"><span data-stu-id="02be5-132">Call the [**RpcRevertToSelf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcreverttoself) function to revert to the service security context.</span></span>

<span data-ttu-id="02be5-133">Per ulteriori informazioni sulla rappresentazione client RPC, vedere [rappresentazione client](/windows/desktop/Rpc/client-impersonation).</span><span class="sxs-lookup"><span data-stu-id="02be5-133">For more information about RPC client impersonation, see [Client Impersonation](/windows/desktop/Rpc/client-impersonation).</span></span>

<span data-ttu-id="02be5-134">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="02be5-134">For more information, see:</span></span>

-   [<span data-ttu-id="02be5-135">Pubblicazione con il servizio nome RPC (RpcNs)</span><span class="sxs-lookup"><span data-stu-id="02be5-135">Publishing with the RPC Name Service (RpcNs)</span></span>](publishing-with-the-rpc-name-service-rpcns.md)
-   [<span data-ttu-id="02be5-136">Concetti di base sulla sicurezza RPC</span><span class="sxs-lookup"><span data-stu-id="02be5-136">RPC Security Essentials</span></span>](/windows/desktop/Rpc/rpc-security-essentials)

 

 