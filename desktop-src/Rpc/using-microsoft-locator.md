---
title: Uso di Microsoft Locator
description: Microsoft Locator è il servizio dei nomi predefinito. La libreria di runtime RPC la utilizza per trovare i programmi server nei sistemi host server.
ms.assetid: 8481de50-4e72-432d-aef7-524f18f5c9c4
keywords:
- RPC (Remote Procedure Call), attività, utilizzo di Microsoft Locator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 236dce18b9286150581af925935222f3c9b3f862
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856137"
---
# <a name="using-microsoft-locator"></a><span data-ttu-id="d3c19-105">Uso di Microsoft Locator</span><span class="sxs-lookup"><span data-stu-id="d3c19-105">Using Microsoft Locator</span></span>

<span data-ttu-id="d3c19-106">Microsoft Locator è il servizio dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="d3c19-106">Microsoft Locator is the default name service.</span></span> <span data-ttu-id="d3c19-107">La libreria di runtime RPC la utilizza per trovare i programmi server nei sistemi host server.</span><span class="sxs-lookup"><span data-stu-id="d3c19-107">The RPC run-time library uses it to find server programs on server host systems.</span></span>

<span data-ttu-id="d3c19-108">**Nota**    Microsoft RPC Locator non è supportato in Windows Vista e nei sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="d3c19-108">**Note**  Microsoft RPC locator is not supported in Windows Vista and later operating systems.</span></span>

<span data-ttu-id="d3c19-109">Prima di Windows 2000, Microsoft Locator non forniva voci del servizio di nome permanenti.</span><span class="sxs-lookup"><span data-stu-id="d3c19-109">Prior to Windows 2000, Microsoft Locator did not provide persistent name service entries.</span></span> <span data-ttu-id="d3c19-110">Tutte le voci nel servizio nome sono state archiviate in una cache in memoria sul computer host del programma server.</span><span class="sxs-lookup"><span data-stu-id="d3c19-110">All entries in the name service were stored in a memory cache on the server program's host computer.</span></span> <span data-ttu-id="d3c19-111">Il localizzatore ha utilizzato un meccanismo di trasmissione per individuare il percorso dei server richiesti dai client.</span><span class="sxs-lookup"><span data-stu-id="d3c19-111">The locator used a broadcast mechanism to discover the location of servers as requested by clients.</span></span> <span data-ttu-id="d3c19-112">Ogni volta che il sistema host si arresta, tutte le voci del servizio nome andranno perse.</span><span class="sxs-lookup"><span data-stu-id="d3c19-112">Whenever the host system shut down, all name service entries were lost.</span></span>

<span data-ttu-id="d3c19-113">A partire dal rilascio di Windows 2000, Microsoft Locator supporta ora le voci del servizio nome permanente.</span><span class="sxs-lookup"><span data-stu-id="d3c19-113">Beginning with the release of Windows 2000, Microsoft Locator now supports persistent name service entries.</span></span> <span data-ttu-id="d3c19-114">A tale scopo, il sistema usa un servizio di directory distribuito per archiviare le voci del servizio del nome.</span><span class="sxs-lookup"><span data-stu-id="d3c19-114">To accomplish this, the system employs a distributed directory service to store name service entries.</span></span> <span data-ttu-id="d3c19-115">Questo meccanismo presenta diversi vantaggi:</span><span class="sxs-lookup"><span data-stu-id="d3c19-115">This mechanism has several advantages:</span></span>

-   <span data-ttu-id="d3c19-116">**Persistenza.**</span><span class="sxs-lookup"><span data-stu-id="d3c19-116">**Persistence.**</span></span> <span data-ttu-id="d3c19-117">I programmi server non sono più necessari per esportare le informazioni di binding nel servizio nome ogni volta che vengono avviate.</span><span class="sxs-lookup"><span data-stu-id="d3c19-117">Server programs are no longer required to export their binding information to the name service each time they start up.</span></span> <span data-ttu-id="d3c19-118">Il servizio nome Archivia ora le informazioni finché il programma server nell'amministratore di rete non lo rimuove in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="d3c19-118">The name service now stores the information until the server program on the network administrator explicitly removes it.</span></span>
-   <span data-ttu-id="d3c19-119">**Efficienza.**</span><span class="sxs-lookup"><span data-stu-id="d3c19-119">**Efficiency.**</span></span> <span data-ttu-id="d3c19-120">Eliminando la maggior parte delle trasmissioni per le voci del servizio nomi, il localizzatore riduce il traffico di rete.</span><span class="sxs-lookup"><span data-stu-id="d3c19-120">By eliminating the majority of broadcasting for name service entries, the locator reduces network traffic.</span></span> <span data-ttu-id="d3c19-121">Trova anche le voci del servizio nome più rapidamente.</span><span class="sxs-lookup"><span data-stu-id="d3c19-121">It also finds name service entries more rapidly.</span></span>
-   <span data-ttu-id="d3c19-122">**Interoperabilità tra domini.**</span><span class="sxs-lookup"><span data-stu-id="d3c19-122">**Cross-Domain Interoperability.**</span></span> <span data-ttu-id="d3c19-123">I client sono ora in grado di effettuare richieste di servizio con nome tra più domini.</span><span class="sxs-lookup"><span data-stu-id="d3c19-123">Clients are now able to make name service requests across multiple domains.</span></span>

<span data-ttu-id="d3c19-124">Le versioni correnti di Microsoft Locator sono compatibili con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="d3c19-124">Current versions of Microsoft Locator are backward compatible.</span></span> <span data-ttu-id="d3c19-125">Ad esempio, un sistema host server che esegue il localizzatore fornito con Windows 2000 può funzionare correttamente in una rete che contiene i sistemi host server che eseguono il localizzatore fornito con Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="d3c19-125">For instance, a server host system running the locator that ships with Windows 2000 can operate correctly on a network that contains server host systems running the locator that ships with Windows NT 4.0.</span></span>

<span data-ttu-id="d3c19-126">Con il rilascio di Windows 2000, Microsoft Locator ora supporta le voci del servizio di denominazione per i gruppi di utenti.</span><span class="sxs-lookup"><span data-stu-id="d3c19-126">With the release of Windows 2000, Microsoft Locator now supports name service entries for groups of users.</span></span> <span data-ttu-id="d3c19-127">Offre inoltre la possibilità di creare profili utente.</span><span class="sxs-lookup"><span data-stu-id="d3c19-127">It also provides the ability for you to create user profiles.</span></span>

<span data-ttu-id="d3c19-128">Inoltre, la versione corrente di Microsoft Locator supporta l'utilizzo degli elenchi di controllo di accesso nelle voci del servizio di denominazione.</span><span class="sxs-lookup"><span data-stu-id="d3c19-128">In addition, the current version of Microsoft Locator supports the use of Access Control Lists in name service entries.</span></span> <span data-ttu-id="d3c19-129">Questa funzionalità migliora la sicurezza della rete.</span><span class="sxs-lookup"><span data-stu-id="d3c19-129">This ability enhances the security of the network.</span></span>

<span data-ttu-id="d3c19-130">Il supporto Plug and Play è ora incluso in Microsoft Locator.</span><span class="sxs-lookup"><span data-stu-id="d3c19-130">Plug and Play support is now included in Microsoft Locator.</span></span> <span data-ttu-id="d3c19-131">Pertanto, può gestire in modo trasparente Plug and Play eventi come le modifiche al dominio.</span><span class="sxs-lookup"><span data-stu-id="d3c19-131">Therefore, it can transparently handle Plug and Play events such as domain changes.</span></span> <span data-ttu-id="d3c19-132">Per ulteriori informazioni, vedere [**RpcNsBindingExportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) e [**RpcNsBindingUnexportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa).</span><span class="sxs-lookup"><span data-stu-id="d3c19-132">For more information, see [**RpcNsBindingExportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexportpnpa) and [**RpcNsBindingUnexportPnP**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingunexportpnpa).</span></span>

 

 




