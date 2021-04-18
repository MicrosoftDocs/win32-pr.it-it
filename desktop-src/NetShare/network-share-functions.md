---
description: Le funzioni di condivisione di rete controllano le risorse condivise. Una risorsa condivisa è una risorsa locale in un server (ad esempio, una directory del disco, un dispositivo di stampa o named pipe) a cui possono accedere utenti e applicazioni nella rete.
ms.assetid: 14886bb0-e597-4728-a64f-bc16e82874da
title: Funzioni di condivisione di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 640dc877c9b482cb8ebdcef0d36e6dff562fcd8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310780"
---
# <a name="network-share-functions"></a><span data-ttu-id="5886c-104">Funzioni di condivisione di rete</span><span class="sxs-lookup"><span data-stu-id="5886c-104">Network Share Functions</span></span>

<span data-ttu-id="5886c-105">Le funzioni di condivisione di rete controllano le risorse condivise.</span><span class="sxs-lookup"><span data-stu-id="5886c-105">The network share functions control shared resources.</span></span> <span data-ttu-id="5886c-106">Una risorsa condivisa è una risorsa locale in un server (ad esempio, una directory del disco, un dispositivo di stampa o named pipe) a cui possono accedere utenti e applicazioni nella rete.</span><span class="sxs-lookup"><span data-stu-id="5886c-106">A shared resource is a local resource on a server (for example, a disk directory, print device, or named pipe) that can be accessed by users and applications on the network.</span></span>

<span data-ttu-id="5886c-107">Le funzioni di condivisione sono elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="5886c-107">The share functions are listed following.</span></span>



| <span data-ttu-id="5886c-108">Funzione</span><span class="sxs-lookup"><span data-stu-id="5886c-108">Function</span></span>                                   | <span data-ttu-id="5886c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5886c-109">Description</span></span>                                                          |
|--------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="5886c-110">**Funzione NetShareAdd**</span><span class="sxs-lookup"><span data-stu-id="5886c-110">**NetShareAdd**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd)         | <span data-ttu-id="5886c-111">Condivide una risorsa in un server.</span><span class="sxs-lookup"><span data-stu-id="5886c-111">Shares a resource on a server.</span></span>                                       |
| [<span data-ttu-id="5886c-112">**NetShareCheck**</span><span class="sxs-lookup"><span data-stu-id="5886c-112">**NetShareCheck**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharecheck)     | <span data-ttu-id="5886c-113">Esegue una query sull'eventuale condivisione di un dispositivo da parte di un server.</span><span class="sxs-lookup"><span data-stu-id="5886c-113">Queries whether a server is sharing a device.</span></span>                        |
| [<span data-ttu-id="5886c-114">**NetShareDel**</span><span class="sxs-lookup"><span data-stu-id="5886c-114">**NetShareDel**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharedel)         | <span data-ttu-id="5886c-115">Elimina un nome di condivisione dall'elenco di risorse condivise di un server.</span><span class="sxs-lookup"><span data-stu-id="5886c-115">Deletes a share name from a server's list of shared resources.</span></span>       |
| [<span data-ttu-id="5886c-116">**NetShareEnum**</span><span class="sxs-lookup"><span data-stu-id="5886c-116">**NetShareEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netshareenum)       | <span data-ttu-id="5886c-117">Recupera le informazioni sulla condivisione di ogni risorsa condivisa in un server.</span><span class="sxs-lookup"><span data-stu-id="5886c-117">Retrieves share information about each shared resource on a server.</span></span>  |
| [<span data-ttu-id="5886c-118">**NetShareGetInfo**</span><span class="sxs-lookup"><span data-stu-id="5886c-118">**NetShareGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharegetinfo) | <span data-ttu-id="5886c-119">Recupera le informazioni su una risorsa condivisa specificata in un server.</span><span class="sxs-lookup"><span data-stu-id="5886c-119">Retrieves information about a specified shared resource on a server.</span></span> |
| [<span data-ttu-id="5886c-120">**NetShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="5886c-120">**NetShareSetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo) | <span data-ttu-id="5886c-121">Imposta i parametri di una risorsa condivisa.</span><span class="sxs-lookup"><span data-stu-id="5886c-121">Sets a shared resource's parameters.</span></span>                                 |



 

<span data-ttu-id="5886c-122">La funzione [**funzione NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) consente a un utente o a un'applicazione di condividere una risorsa di un tipo specifico usando il nome di condivisione specificato.</span><span class="sxs-lookup"><span data-stu-id="5886c-122">The [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) function allows a user or application to share a resource of a specific type using the specified share name.</span></span> <span data-ttu-id="5886c-123">La funzione **funzione NetShareAdd** richiede il nome della condivisione e il nome del dispositivo locale per condividere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5886c-123">The **NetShareAdd** function requires the share name and local device name to share the resource.</span></span> <span data-ttu-id="5886c-124">Per accedere alla risorsa, è necessario che un utente o un'applicazione disponga di un account nel server.</span><span class="sxs-lookup"><span data-stu-id="5886c-124">A user or application must have an account on the server to access the resource.</span></span>

<span data-ttu-id="5886c-125">È anche possibile specificare un descrittore di sicurezza da associare a una condivisione.</span><span class="sxs-lookup"><span data-stu-id="5886c-125">You can also specify a security descriptor to be associated with a share.</span></span> <span data-ttu-id="5886c-126">I descrittori di sicurezza specificano quali utenti possono accedere ai file attraverso la condivisione e con quale tipo di accesso.</span><span class="sxs-lookup"><span data-stu-id="5886c-126">Security descriptors specify which users are allowed to access files through the share, and with what type of access.</span></span> <span data-ttu-id="5886c-127">Specificare un [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) con il livello di informazioni [**share \_ info \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502) quando si chiama [**funzione NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) o [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo).</span><span class="sxs-lookup"><span data-stu-id="5886c-127">Specify a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) with the [**SHARE\_INFO\_502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502) information level when calling [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) or [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo).</span></span> <span data-ttu-id="5886c-128">**NetShareSetInfo** supporta il livello di informazioni [**condivisione \_ informazioni \_ 1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) .</span><span class="sxs-lookup"><span data-stu-id="5886c-128">**NetShareSetInfo** supports the [**SHARE\_INFO\_1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) information level.</span></span> <span data-ttu-id="5886c-129">Per ulteriori informazioni sui descrittori di sicurezza, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="5886c-129">For more information about security descriptors, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="5886c-130">Le funzioni di gestione della rete utilizzano i nomi di condivisione speciali seguenti per la comunicazione interprocesso (IPC) e l'amministrazione remota del server:</span><span class="sxs-lookup"><span data-stu-id="5886c-130">The network management functions use the following special share names for interprocess communication (IPC) and remote administration of the server:</span></span>

-   <span data-ttu-id="5886c-131">IPC $, riservata per la comunicazione interprocesso</span><span class="sxs-lookup"><span data-stu-id="5886c-131">IPC$, reserved for interprocess communication</span></span>
-   <span data-ttu-id="5886c-132">ADMIN $, riservato per l'amministrazione remota</span><span class="sxs-lookup"><span data-stu-id="5886c-132">ADMIN$, reserved for remote administration</span></span>
-   <span data-ttu-id="5886c-133">Un $, B $, C $ (e altri nomi di disco locale seguiti da un simbolo di dollaro) assegnati a dispositivi disco locali</span><span class="sxs-lookup"><span data-stu-id="5886c-133">A$, B$, C$ (and other local disk names followed by a dollar sign), assigned to local disk devices</span></span>

<span data-ttu-id="5886c-134">Per elencare tutte le connessioni effettuate a una risorsa condivisa in un server o per elencare tutte le connessioni stabilite da un determinato computer, chiamare la funzione [**NetConnectionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) .</span><span class="sxs-lookup"><span data-stu-id="5886c-134">To list all connections made to a shared resource on a server, or to list all connections established from a particular computer, call the [**NetConnectionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) function.</span></span> <span data-ttu-id="5886c-135">È possibile chiamare **NetConnectionEnum** con le informazioni di [**connessione \_ \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0) e i livelli di informazioni di [**connessione \_ \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1) .</span><span class="sxs-lookup"><span data-stu-id="5886c-135">You can call **NetConnectionEnum** at the [**CONNECTION\_INFO\_0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0) and [**CONNECTION\_INFO\_1**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1) information levels.</span></span>

<span data-ttu-id="5886c-136">Le funzioni di condivisione sono disponibili ai livelli di informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5886c-136">Share functions are available at the following information levels:</span></span>

<dl>

[<span data-ttu-id="5886c-137">**Informazioni sulla condivisione \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="5886c-137">**SHARE\_INFO\_0**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_0)  
[<span data-ttu-id="5886c-138">**Condividi \_ informazioni \_ 1**</span><span class="sxs-lookup"><span data-stu-id="5886c-138">**SHARE\_INFO\_1**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1)  
[<span data-ttu-id="5886c-139">**Condividi \_ informazioni \_ 2**</span><span class="sxs-lookup"><span data-stu-id="5886c-139">**SHARE\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_2)  
[<span data-ttu-id="5886c-140">**Condividi \_ informazioni \_ 501**</span><span class="sxs-lookup"><span data-stu-id="5886c-140">**SHARE\_INFO\_501**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_501)  
[<span data-ttu-id="5886c-141">**Condividi \_ informazioni \_ 502**</span><span class="sxs-lookup"><span data-stu-id="5886c-141">**SHARE\_INFO\_502**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502)  
[<span data-ttu-id="5886c-142">**Condividi \_ informazioni \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="5886c-142">**SHARE\_INFO\_1005**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1005)  
</dl>

<span data-ttu-id="5886c-143">I livelli di informazioni seguenti sono validi solo per [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo):</span><span class="sxs-lookup"><span data-stu-id="5886c-143">The following information levels are valid only for [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo):</span></span>

<dl>

[<span data-ttu-id="5886c-144">**Condividi \_ informazioni \_ 1004**</span><span class="sxs-lookup"><span data-stu-id="5886c-144">**SHARE\_INFO\_1004**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1004)  
[<span data-ttu-id="5886c-145">**Condividi \_ informazioni \_ 1006**</span><span class="sxs-lookup"><span data-stu-id="5886c-145">**SHARE\_INFO\_1006**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1006)  
[<span data-ttu-id="5886c-146">**Condividi \_ informazioni \_ 1501**</span><span class="sxs-lookup"><span data-stu-id="5886c-146">**SHARE\_INFO\_1501**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501)  
</dl>

<span data-ttu-id="5886c-147">Se si sta programmando per Active Directory, è possibile chiamare determinati metodi di Active Directory Service Interface (ADSI) per ottenere la stessa funzionalità che è possibile ottenere chiamando le funzioni di condivisione di gestione della rete.</span><span class="sxs-lookup"><span data-stu-id="5886c-147">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management share functions.</span></span> <span data-ttu-id="5886c-148">Per ulteriori informazioni, vedere [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).</span><span class="sxs-lookup"><span data-stu-id="5886c-148">For more information, see [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).</span></span>

 

 
