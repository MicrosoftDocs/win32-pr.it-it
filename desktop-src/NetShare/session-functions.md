---
description: Informazioni su funzioni di sessione nella gestione della condivisione di rete. Queste funzioni controllano le sessioni di rete stabilite tra workstation e server.
ms.assetid: 931455e3-1301-4a68-93c3-2674b3d4c491
title: Funzioni di sessione (Gestione condivisione di rete)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdde451eb2942171569b24c36aae5d5742208e5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409724"
---
# <a name="session-functions-network-share-management"></a><span data-ttu-id="823b9-104">Funzioni di sessione (Gestione condivisione di rete)</span><span class="sxs-lookup"><span data-stu-id="823b9-104">Session Functions (Network Share Management)</span></span>

<span data-ttu-id="823b9-105">Le funzioni della sessione di gestione di rete controllano le sessioni di rete stabilite tra workstation e server.</span><span class="sxs-lookup"><span data-stu-id="823b9-105">The network management session functions control network sessions established between workstations and servers.</span></span> <span data-ttu-id="823b9-106">Le funzioni richiedono l'avvio del servizio server nel server.</span><span class="sxs-lookup"><span data-stu-id="823b9-106">The functions require that the server service be started on the server.</span></span>

<span data-ttu-id="823b9-107">Le funzioni di sessione sono elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="823b9-107">The session functions are listed following.</span></span>



| <span data-ttu-id="823b9-108">Funzione</span><span class="sxs-lookup"><span data-stu-id="823b9-108">Function</span></span>                                       | <span data-ttu-id="823b9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="823b9-109">Description</span></span>                                                                                       |
|------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="823b9-110">**NetSessionDel**</span><span class="sxs-lookup"><span data-stu-id="823b9-110">**NetSessionDel**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)         | <span data-ttu-id="823b9-111">Elimina le connessioni correnti tra una workstation e un server. termina la sessione di rete.</span><span class="sxs-lookup"><span data-stu-id="823b9-111">Deletes the current connections between a workstation and server; terminates the network session.</span></span> |
| [<span data-ttu-id="823b9-112">**Enumerazione NetSessionEnum**</span><span class="sxs-lookup"><span data-stu-id="823b9-112">**NetSessionEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessionenum)       | <span data-ttu-id="823b9-113">Restituisce informazioni su tutte le sessioni correnti stabilite per un server.</span><span class="sxs-lookup"><span data-stu-id="823b9-113">Returns information about all current sessions established for a server.</span></span>                          |
| [<span data-ttu-id="823b9-114">**NetSessionGetInfo**</span><span class="sxs-lookup"><span data-stu-id="823b9-114">**NetSessionGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsessiongetinfo) | <span data-ttu-id="823b9-115">Restituisce informazioni su una sessione specifica.</span><span class="sxs-lookup"><span data-stu-id="823b9-115">Returns information about a particular session.</span></span>                                                   |



 

<span data-ttu-id="823b9-116">Una *sessione* è un collegamento tra una workstation e un server.</span><span class="sxs-lookup"><span data-stu-id="823b9-116">A *session* is a link between a workstation and a server.</span></span> <span data-ttu-id="823b9-117">Una sessione viene stabilita la prima volta che una workstation effettua una connessione a una risorsa condivisa nel server.</span><span class="sxs-lookup"><span data-stu-id="823b9-117">A session is established the first time a workstation makes a connection to a shared resource on the server.</span></span> <span data-ttu-id="823b9-118">Fino al termine della sessione, tutte le altre connessioni tra la workstation e il server fanno parte della stessa sessione.</span><span class="sxs-lookup"><span data-stu-id="823b9-118">Until the session ends, all further connections between the workstation and the server are part of the same session.</span></span> <span data-ttu-id="823b9-119">Per terminare una sessione, un'applicazione sul server finale di una connessione chiama la [**funzione NetSessionDel.**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)</span><span class="sxs-lookup"><span data-stu-id="823b9-119">To end a session, an application on the server end of a connection calls the [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) function.</span></span>

<span data-ttu-id="823b9-120">Le funzioni della sessione di gestione di rete gestiscono le informazioni in base all'utente con il *parametro username.*</span><span class="sxs-lookup"><span data-stu-id="823b9-120">The network management session functions manage information on a per-user basis with the *username* parameter.</span></span> <span data-ttu-id="823b9-121">Poiché possono essere presenti più utenti per sessione, questo parametro è necessario per accedere alle informazioni specifiche dell'utente per la sessione.</span><span class="sxs-lookup"><span data-stu-id="823b9-121">Because there can be multiple users per session, this parameter is necessary to access the user-specific information for the session.</span></span>

<span data-ttu-id="823b9-122">Le funzioni di sessione sono disponibili a cinque livelli di informazioni:</span><span class="sxs-lookup"><span data-stu-id="823b9-122">Session functions are available at five information levels:</span></span>

<dl>

[<span data-ttu-id="823b9-123">**INFORMAZIONI \_ SESSIONE \_ 0**</span><span class="sxs-lookup"><span data-stu-id="823b9-123">**SESSION\_INFO\_0**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_0)  
[<span data-ttu-id="823b9-124">**INFORMAZIONI \_ SESSIONE \_ 1**</span><span class="sxs-lookup"><span data-stu-id="823b9-124">**SESSION\_INFO\_1**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_1)  
[<span data-ttu-id="823b9-125">**INFORMAZIONI \_ SESSIONE \_ 2**</span><span class="sxs-lookup"><span data-stu-id="823b9-125">**SESSION\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_2)  
[<span data-ttu-id="823b9-126">**INFORMAZIONI \_ SESSIONE \_ 10**</span><span class="sxs-lookup"><span data-stu-id="823b9-126">**SESSION\_INFO\_10**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_10)  
[<span data-ttu-id="823b9-127">**INFORMAZIONI \_ SESSIONE \_ 502**</span><span class="sxs-lookup"><span data-stu-id="823b9-127">**SESSION\_INFO\_502**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-session_info_502)  
</dl>

<span data-ttu-id="823b9-128">Se si programma per Active Directory, è possibile chiamare determinati metodi ADSI (Active Directory Service Interface) per ottenere le stesse funzionalità che è possibile ottenere chiamando le funzioni della sessione di gestione di rete.</span><span class="sxs-lookup"><span data-stu-id="823b9-128">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management session functions.</span></span> <span data-ttu-id="823b9-129">Per altre informazioni, vedere [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) e [**IADsFileServiceOperations.**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)</span><span class="sxs-lookup"><span data-stu-id="823b9-129">For more information, see [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) and [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).</span></span>

 

 
