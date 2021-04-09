---
title: Pubblicazione di un servizio
description: I servizi si annunciano usando oggetti archiviati in Active Directory Domain Services.
ms.assetid: 69e9256f-40ee-4aed-8213-1bbda0e508af
ms.tgt_platform: multiple
keywords:
- ANNUNCIO pubblicazione servizio
- Active Directory, utilizzo di, pubblicazione del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9437d9f4aa5184c53f2962d7b2640e933107501f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044092"
---
# <a name="service-publication"></a><span data-ttu-id="e27fe-105">Pubblicazione di un servizio</span><span class="sxs-lookup"><span data-stu-id="e27fe-105">Service Publication</span></span>

<span data-ttu-id="e27fe-106">I servizi si annunciano usando oggetti archiviati in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="e27fe-106">Services advertise themselves using objects stored in Active Directory Domain Services.</span></span> <span data-ttu-id="e27fe-107">Questa operazione è nota come *pubblicazione del servizio*.</span><span class="sxs-lookup"><span data-stu-id="e27fe-107">This is known as *service publication*.</span></span> <span data-ttu-id="e27fe-108">I client eseguono una query sulla directory per individuare i servizi.</span><span class="sxs-lookup"><span data-stu-id="e27fe-108">Clients query the directory to locate services.</span></span> <span data-ttu-id="e27fe-109">Questa operazione è denominata *Rendezvous del servizio client*.</span><span class="sxs-lookup"><span data-stu-id="e27fe-109">This is called *client-service rendezvous*.</span></span> <span data-ttu-id="e27fe-110">In questa sezione vengono illustrati i tipi di oggetti directory utilizzati per la pubblicazione del servizio e viene illustrata la relativa modalità di utilizzo per gli Rendezvous del servizio client.</span><span class="sxs-lookup"><span data-stu-id="e27fe-110">This section discusses the types of directory objects used for service publication and explains how they are used for client-service rendezvous.</span></span>

<span data-ttu-id="e27fe-111">In questa sezione vengono illustrati gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="e27fe-111">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="e27fe-112">Panoramica della pubblicazione del servizio</span><span class="sxs-lookup"><span data-stu-id="e27fe-112">An overview of service publication</span></span>](about-service-publication.md)
-   [<span data-ttu-id="e27fe-113">Problemi di sicurezza per la pubblicazione del servizio</span><span class="sxs-lookup"><span data-stu-id="e27fe-113">Security issues for service publication</span></span>](security-issues-for-service-publication.md)
-   [<span data-ttu-id="e27fe-114">Oggetti punto di connessione</span><span class="sxs-lookup"><span data-stu-id="e27fe-114">Connection point objects</span></span>](connection-points.md)
-   [<span data-ttu-id="e27fe-115">Pubblicazione con i punti di connessione del servizio (convergenza)</span><span class="sxs-lookup"><span data-stu-id="e27fe-115">Publishing with service connection points (SCPs)</span></span>](publishing-with-service-connection-points.md)
-   [<span data-ttu-id="e27fe-116">Informazioni da archiviare in un punto di connessione del servizio</span><span class="sxs-lookup"><span data-stu-id="e27fe-116">What information to store in a service connection point</span></span>](service-connection-point-properties.md)
-   [<span data-ttu-id="e27fe-117">Dove creare un punto di connessione del servizio</span><span class="sxs-lookup"><span data-stu-id="e27fe-117">Where to create a service connection point</span></span>](where-to-create-a-service-connection-point.md)
-   [<span data-ttu-id="e27fe-118">Come pubblicare servizi replicabili, basati su host e database usando i punti di connessione del servizio</span><span class="sxs-lookup"><span data-stu-id="e27fe-118">How to publish replicable, host-based, and database services using service connection points</span></span>](service-connection-points-for-replicated-host-based-and-database-services.md)
-   [<span data-ttu-id="e27fe-119">Creazione e gestione di un punto di connessione del servizio</span><span class="sxs-lookup"><span data-stu-id="e27fe-119">Creating and maintaining a service connection point</span></span>](creating-and-maintaining-a-service-connection-point.md)
-   [<span data-ttu-id="e27fe-120">Come un client esegue una query per un SCP e lo usa per eseguire il binding a un'istanza del servizio</span><span class="sxs-lookup"><span data-stu-id="e27fe-120">How a client queries for an SCP and uses it to bind to a service instance</span></span>](how-clients-find-and-use-a-service-connection-point.md)
-   [<span data-ttu-id="e27fe-121">Uso delle API RpcNs (RPC Name Service) per pubblicare un servizio RPC</span><span class="sxs-lookup"><span data-stu-id="e27fe-121">Using the RPC name service (RpcNs) APIs to publish an RPC service</span></span>](publishing-with-the-rpc-name-service-rpcns.md)
-   [<span data-ttu-id="e27fe-122">Registrazione e risoluzione di Windows Sockets (RnR) per pubblicare un servizio Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="e27fe-122">Windows Sockets registration and resolution (RnR) to publish a Windows Sockets service</span></span>](publishing-with-windows-sockets-registration-and-resolution.md)
-   [<span data-ttu-id="e27fe-123">Pubblicazione di servizi basati su COM nell'archivio di classi COM+</span><span class="sxs-lookup"><span data-stu-id="e27fe-123">Publication of COM-based services in the COM+ class store</span></span>](publishing-com-services.md)

<span data-ttu-id="e27fe-124">Per ulteriori informazioni sul modo in cui i servizi e i client si autenticano [reciprocamente, vedere l'autenticazione reciproca tramite Kerberos](mutual-authentication-using-kerberos.md).</span><span class="sxs-lookup"><span data-stu-id="e27fe-124">For more information about how services and clients authenticate each other, see [Mutual Authentication Using Kerberos](mutual-authentication-using-kerberos.md).</span></span> <span data-ttu-id="e27fe-125">Per ulteriori informazioni sui contesti di sicurezza del servizio e gli account di accesso, vedere [account di accesso al servizio](service-logon-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="e27fe-125">For more information about service security contexts and logon accounts, see [Service Logon Accounts](service-logon-accounts.md).</span></span>

 

 




