---
title: Informazioni sull'amministrazione del servizio di accesso remoto
description: I sistemi operativi Windows 2000 e versioni successive forniscono un set di funzioni per l'amministrazione delle autorizzazioni e delle porte utente nei server RAS.
ms.assetid: 95c6dceb-e3a9-421e-b43f-88b18b9e64ff
keywords:
- Servizio Routing e accesso remoto RRAS, amministrazione RAS
- Servizio Routing e accesso remoto RRAS, amministrazione RAS, descrizione
- RRAS amministrazione RAS
- Amministrazione RAS RRAS, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bdb55049e99b6d3df9980fc35879341b488531
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298295"
---
# <a name="about-remote-access-service-administration"></a><span data-ttu-id="58d41-107">Informazioni sull'amministrazione del servizio di accesso remoto</span><span class="sxs-lookup"><span data-stu-id="58d41-107">About Remote Access Service Administration</span></span>

<span data-ttu-id="58d41-108">I sistemi operativi Windows 2000 e versioni successive forniscono un set di funzioni per l'amministrazione delle autorizzazioni e delle porte utente nei server RAS.</span><span class="sxs-lookup"><span data-stu-id="58d41-108">Windows 2000 and later operating systems provide a set of functions for administering user permissions and ports on RAS servers.</span></span> <span data-ttu-id="58d41-109">Utilizzando queste funzioni, è possibile sviluppare un'applicazione di amministrazione del server RAS per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="58d41-109">Using these functions, you can develop a RAS server administration application to perform the following tasks:</span></span>

-   <span data-ttu-id="58d41-110">Enumerare gli utenti che dispongono di un set specificato di autorizzazioni RAS</span><span class="sxs-lookup"><span data-stu-id="58d41-110">Enumerate those users who have a specified set of RAS permissions</span></span>
-   <span data-ttu-id="58d41-111">Assegnare o revocare le autorizzazioni RAS per un utente specificato</span><span class="sxs-lookup"><span data-stu-id="58d41-111">Assign or revoke RAS permissions for a specified user</span></span>
-   <span data-ttu-id="58d41-112">Enumerare le porte configurate in un server RAS</span><span class="sxs-lookup"><span data-stu-id="58d41-112">Enumerate the configured ports on a RAS server</span></span>
-   <span data-ttu-id="58d41-113">Ottenere informazioni e statistiche su una porta specificata in un server RAS</span><span class="sxs-lookup"><span data-stu-id="58d41-113">Get information and statistics about a specified port on a RAS server</span></span>
-   <span data-ttu-id="58d41-114">Reimposta i contatori delle statistiche per una porta specificata</span><span class="sxs-lookup"><span data-stu-id="58d41-114">Reset the statistics counters for a specified port</span></span>
-   <span data-ttu-id="58d41-115">Disconnettere una porta specificata</span><span class="sxs-lookup"><span data-stu-id="58d41-115">Disconnect a specified port</span></span>

<span data-ttu-id="58d41-116">È anche possibile installare una DLL di amministrazione del server RAS per controllare le connessioni utente e assegnare gli indirizzi IP agli utenti con connessione remota.</span><span class="sxs-lookup"><span data-stu-id="58d41-116">You can also install a RAS server administration DLL to audit user connections and assign IP addresses to dial-in users.</span></span> <span data-ttu-id="58d41-117">La DLL esporta un set di funzioni che il server RAS chiama ogni volta che un utente tenta di connettersi o disconnettersi.</span><span class="sxs-lookup"><span data-stu-id="58d41-117">The DLL exports a set of functions that the RAS server calls whenever a user tries to connect or disconnect.</span></span>

<span data-ttu-id="58d41-118">In questa documentazione vengono descritti gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="58d41-118">This documentation describes the following topics:</span></span>

-   [<span data-ttu-id="58d41-119">Confronto tra le funzioni: Windows 2000 e RRAS ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="58d41-119">Function Comparison: Windows 2000 vs. RRAS Redistributable</span></span>](function-comparison-windows-2000-versus-rras-redistributable.md)
-   [<span data-ttu-id="58d41-120">Amministrazione utenti RAS</span><span class="sxs-lookup"><span data-stu-id="58d41-120">RAS User Administration</span></span>](ras-user-administration.md)
-   [<span data-ttu-id="58d41-121">Amministrazione di server e porte RAS</span><span class="sxs-lookup"><span data-stu-id="58d41-121">RAS Server and Port Administration</span></span>](ras-server-and-port-administration.md)
-   [<span data-ttu-id="58d41-122">DLL di amministrazione RAS</span><span class="sxs-lookup"><span data-stu-id="58d41-122">RAS Administration DLL</span></span>](ras-administration-dll.md)
-   [<span data-ttu-id="58d41-123">Configurazione del registro di sistema della DLL di amministrazione RAS</span><span class="sxs-lookup"><span data-stu-id="58d41-123">RAS Administration DLL Registry Setup</span></span>](ras-administration-dll-registry-setup.md)

 

 




