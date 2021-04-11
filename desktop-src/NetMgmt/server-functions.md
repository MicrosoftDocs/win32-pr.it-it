---
title: Funzioni server (gestione della rete)
description: Le funzioni del server di gestione di rete eseguono attività amministrative su un server locale o remoto. Le funzioni server sono elencate di seguito.
ms.assetid: 43e1285b-8c86-4af4-9834-fcd5ee8aceb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43758fa822ce60d484418431941a386681bb77d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047764"
---
# <a name="server-functions-network-management"></a><span data-ttu-id="fb6d1-104">Funzioni server (gestione della rete)</span><span class="sxs-lookup"><span data-stu-id="fb6d1-104">Server Functions (Network Management)</span></span>

<span data-ttu-id="fb6d1-105">Le funzioni del server di gestione di rete eseguono attività amministrative su un server locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="fb6d1-105">The network management server functions perform administrative tasks on a local or remote server.</span></span> <span data-ttu-id="fb6d1-106">Le funzioni server sono elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="fb6d1-106">The server functions are listed following.</span></span>



| <span data-ttu-id="fb6d1-107">Funzione</span><span class="sxs-lookup"><span data-stu-id="fb6d1-107">Function</span></span>                                       | <span data-ttu-id="fb6d1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb6d1-108">Description</span></span>                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb6d1-109">**NetServerDiskEnum**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-109">**NetServerDiskEnum**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | <span data-ttu-id="fb6d1-110">Restituisce un elenco di unità disco locali in un server.</span><span class="sxs-lookup"><span data-stu-id="fb6d1-110">Returns a list of local disk drives on a server.</span></span>                                   |
| [<span data-ttu-id="fb6d1-111">**NetServerEnum**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-111">**NetServerEnum**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | <span data-ttu-id="fb6d1-112">Elenca tutti i server visibili di un tipo o di tipi specifici nel dominio specificato.</span><span class="sxs-lookup"><span data-stu-id="fb6d1-112">Lists all visible servers of a particular type (or types) in the specified domain.</span></span> |
| [<span data-ttu-id="fb6d1-113">**NetServerGetInfo**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-113">**NetServerGetInfo**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | <span data-ttu-id="fb6d1-114">Restituisce le informazioni di configurazione relative a un server specificato.</span><span class="sxs-lookup"><span data-stu-id="fb6d1-114">Returns configuration information about a specified server.</span></span>                        |
| [<span data-ttu-id="fb6d1-115">**NetServerSetInfo**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-115">**NetServerSetInfo**</span></span>](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | <span data-ttu-id="fb6d1-116">Imposta i parametri operativi per un server.</span><span class="sxs-lookup"><span data-stu-id="fb6d1-116">Sets the operating parameters for a server.</span></span>                                        |



 

<span data-ttu-id="fb6d1-117">Solo un utente o un'applicazione con appartenenza a un gruppo amministratore in un server locale o remoto può eseguire attività amministrative su tale server per controllare l'operazione del server, l'accesso degli utenti e la condivisione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="fb6d1-117">Only a user or application with admin group membership on a local or remote server can perform administrative tasks on that server to control the server's operation, user access, and resource sharing.</span></span> <span data-ttu-id="fb6d1-118">I parametri di basso livello che interessano l'operazione di un server possono essere esaminati e modificati chiamando le funzioni [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) e [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) .</span><span class="sxs-lookup"><span data-stu-id="fb6d1-118">The low-level parameters that affect a server's operation can be examined and modified by calling the [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo) and [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo) functions.</span></span> <span data-ttu-id="fb6d1-119">Questi parametri vengono definiti nel file di LANMAN.INI del server.</span><span class="sxs-lookup"><span data-stu-id="fb6d1-119">These parameters are defined in the server's LANMAN.INI file.</span></span>

<span data-ttu-id="fb6d1-120">La maggior parte delle funzioni del server di gestione di rete viene eseguita solo su un server remoto.</span><span class="sxs-lookup"><span data-stu-id="fb6d1-120">Most network management server functions execute only on a remote server.</span></span> <span data-ttu-id="fb6d1-121">La funzione [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) viene eseguita su una workstation locale o su un server remoto.</span><span class="sxs-lookup"><span data-stu-id="fb6d1-121">The [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum) function executes on either a local workstation or a remote server.</span></span> <span data-ttu-id="fb6d1-122">Se si tenta di eseguire altre funzioni server su una workstation locale, le funzioni restituiscono l'errore NERR \_ RemoteOnly.</span><span class="sxs-lookup"><span data-stu-id="fb6d1-122">If you attempt to execute other server functions on a local workstation, the functions return the error NERR\_RemoteOnly.</span></span>

<span data-ttu-id="fb6d1-123">Le informazioni specifiche del server sono disponibili ai livelli seguenti:</span><span class="sxs-lookup"><span data-stu-id="fb6d1-123">Server-specific information is available at the following levels:</span></span>

-   [<span data-ttu-id="fb6d1-124">**\_Informazioni SERVER \_ 100**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-124">**SERVER\_INFO\_100**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_100)
-   [<span data-ttu-id="fb6d1-125">**\_Informazioni SERVER \_ 101**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-125">**SERVER\_INFO\_101**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_101)
-   [<span data-ttu-id="fb6d1-126">**\_Informazioni SERVER \_ 102**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-126">**SERVER\_INFO\_102**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_102)
-   [<span data-ttu-id="fb6d1-127">**\_Informazioni SERVER \_ 402**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-127">**SERVER\_INFO\_402**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_402)
-   [<span data-ttu-id="fb6d1-128">**\_Informazioni SERVER \_ 403**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-128">**SERVER\_INFO\_403**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_403)
-   [<span data-ttu-id="fb6d1-129">**\_Informazioni SERVER \_ 1501**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-129">**SERVER\_INFO\_1501**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1501)
-   [<span data-ttu-id="fb6d1-130">**\_Informazioni SERVER \_ 1502**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-130">**SERVER\_INFO\_1502**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1502)
-   [<span data-ttu-id="fb6d1-131">**\_Informazioni SERVER \_ 1503**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-131">**SERVER\_INFO\_1503**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1503)
-   [<span data-ttu-id="fb6d1-132">**\_Informazioni SERVER \_ 1506**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-132">**SERVER\_INFO\_1506**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1506)
-   [<span data-ttu-id="fb6d1-133">**\_Informazioni SERVER \_ 1509**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-133">**SERVER\_INFO\_1509**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1509)
-   [<span data-ttu-id="fb6d1-134">**\_Informazioni SERVER \_ 1510**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-134">**SERVER\_INFO\_1510**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1510)
-   [<span data-ttu-id="fb6d1-135">**\_Informazioni SERVER \_ 1511**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-135">**SERVER\_INFO\_1511**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1511)
-   [<span data-ttu-id="fb6d1-136">**\_Informazioni SERVER \_ 1512**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-136">**SERVER\_INFO\_1512**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1512)
-   [<span data-ttu-id="fb6d1-137">**\_Informazioni SERVER \_ 1513**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-137">**SERVER\_INFO\_1513**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1513)
-   [<span data-ttu-id="fb6d1-138">**\_Informazioni SERVER \_ 1515**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-138">**SERVER\_INFO\_1515**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1515)
-   [<span data-ttu-id="fb6d1-139">**\_Informazioni SERVER \_ 1516**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-139">**SERVER\_INFO\_1516**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1516)
-   [<span data-ttu-id="fb6d1-140">**\_Informazioni SERVER \_ 1518**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-140">**SERVER\_INFO\_1518**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1518)
-   [<span data-ttu-id="fb6d1-141">**\_Informazioni SERVER \_ 1523**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-141">**SERVER\_INFO\_1523**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1523)
-   [<span data-ttu-id="fb6d1-142">**\_Informazioni SERVER \_ 1528**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-142">**SERVER\_INFO\_1528**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1528)
-   [<span data-ttu-id="fb6d1-143">**\_Informazioni SERVER \_ 1529**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-143">**SERVER\_INFO\_1529**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1529)
-   [<span data-ttu-id="fb6d1-144">**\_Informazioni SERVER \_ 1530**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-144">**SERVER\_INFO\_1530**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1530)
-   [<span data-ttu-id="fb6d1-145">**\_Informazioni SERVER \_ 1533**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-145">**SERVER\_INFO\_1533**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1533)
-   [<span data-ttu-id="fb6d1-146">**\_Informazioni SERVER \_ 1536**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-146">**SERVER\_INFO\_1536**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1536)
-   [<span data-ttu-id="fb6d1-147">**\_Informazioni SERVER \_ 1538**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-147">**SERVER\_INFO\_1538**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1538)
-   [<span data-ttu-id="fb6d1-148">**\_Informazioni SERVER \_ 1539**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-148">**SERVER\_INFO\_1539**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1539)
-   [<span data-ttu-id="fb6d1-149">**\_Informazioni SERVER \_ 1540**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-149">**SERVER\_INFO\_1540**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1540)
-   [<span data-ttu-id="fb6d1-150">**\_Informazioni SERVER \_ 1541**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-150">**SERVER\_INFO\_1541**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1541)
-   [<span data-ttu-id="fb6d1-151">**\_Informazioni SERVER \_ 1542**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-151">**SERVER\_INFO\_1542**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1542)
-   [<span data-ttu-id="fb6d1-152">**\_Informazioni SERVER \_ 1544**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-152">**SERVER\_INFO\_1544**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1544)
-   [<span data-ttu-id="fb6d1-153">**\_Informazioni SERVER \_ 1550**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-153">**SERVER\_INFO\_1550**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1550)
-   [<span data-ttu-id="fb6d1-154">**\_Informazioni SERVER \_ 1552**</span><span class="sxs-lookup"><span data-stu-id="fb6d1-154">**SERVER\_INFO\_1552**</span></span>](/windows/desktop/api/Lmserver/ns-lmserver-server_info_1552)

<span data-ttu-id="fb6d1-155">Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di Active Directory Service Interface (ADSI) per ottenere la stessa funzionalità che è possibile ottenere chiamando le funzioni del server di gestione di rete.</span><span class="sxs-lookup"><span data-stu-id="fb6d1-155">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management server functions.</span></span> <span data-ttu-id="fb6d1-156">Per ulteriori informazioni, vedere [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).</span><span class="sxs-lookup"><span data-stu-id="fb6d1-156">For more information, see [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).</span></span>

<span data-ttu-id="fb6d1-157">Per ulteriori informazioni, vedere le [funzioni di trasporto server e workstation](server-and-workstation-transport-functions.md).</span><span class="sxs-lookup"><span data-stu-id="fb6d1-157">For more information, see the [Server and Workstation Transport Functions](server-and-workstation-transport-functions.md).</span></span>

 

 
