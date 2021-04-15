---
title: Funzioni Get
description: Le funzioni Get di gestione della rete recuperano le informazioni relative a un dominio. È inoltre possibile chiamare queste funzioni per recuperare informazioni sugli account utente locali, globali, workstation e server.
ms.assetid: 9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da830e1b86d3de3359d3ed3627a8d392737569
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515853"
---
# <a name="get-functions"></a><span data-ttu-id="69809-104">Funzioni Get</span><span class="sxs-lookup"><span data-stu-id="69809-104">Get Functions</span></span>

<span data-ttu-id="69809-105">Le funzioni Get di gestione della rete recuperano le informazioni relative a un dominio.</span><span class="sxs-lookup"><span data-stu-id="69809-105">The network management get functions retrieve information about a domain.</span></span> <span data-ttu-id="69809-106">È inoltre possibile chiamare queste funzioni per recuperare informazioni sugli account utente locali, globali, workstation e server.</span><span class="sxs-lookup"><span data-stu-id="69809-106">You can also call these functions to retrieve information about local, global, workstation, and server user accounts.</span></span>

<span data-ttu-id="69809-107">Le funzioni di Get di gestione della rete sono elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="69809-107">The network management get functions are listed following.</span></span>



| <span data-ttu-id="69809-108">Funzione</span><span class="sxs-lookup"><span data-stu-id="69809-108">Function</span></span>                                                               | <span data-ttu-id="69809-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69809-109">Description</span></span>                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69809-110">**NetGetAnyDCName**</span><span class="sxs-lookup"><span data-stu-id="69809-110">**NetGetAnyDCName**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | <span data-ttu-id="69809-111">Restituisce il nome di un controller di dominio che è direttamente attendibile da un server specificato.</span><span class="sxs-lookup"><span data-stu-id="69809-111">Returns the name of any domain controller for a domain that is directly trusted by a specified server.</span></span>                                   |
| [<span data-ttu-id="69809-112">**NetGetDCName**</span><span class="sxs-lookup"><span data-stu-id="69809-112">**NetGetDCName**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | <span data-ttu-id="69809-113">Restituisce il nome del controller di dominio primario (PDC) per il dominio specificato.</span><span class="sxs-lookup"><span data-stu-id="69809-113">Returns the name of the primary domain controller (PDC) for the specified domain.</span></span>                                                        |
| [<span data-ttu-id="69809-114">**NetGetDisplayInformationIndex**</span><span class="sxs-lookup"><span data-stu-id="69809-114">**NetGetDisplayInformationIndex**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | <span data-ttu-id="69809-115">Restituisce l'indice della prima voce di informazioni di visualizzazione il cui nome inizia con una stringa specificata o segue la stringa in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="69809-115">Returns the index of the first display information entry whose name begins with a specified string or alphabetically follows the string.</span></span> |
| [<span data-ttu-id="69809-116">**NetQueryDisplayInformation**</span><span class="sxs-lookup"><span data-stu-id="69809-116">**NetQueryDisplayInformation**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | <span data-ttu-id="69809-117">Restituisce le informazioni sull'account utente, computer o gruppo globale.</span><span class="sxs-lookup"><span data-stu-id="69809-117">Returns user, computer, or global group account information.</span></span>                                                                             |



 

<span data-ttu-id="69809-118">Le informazioni restituite dalla funzione [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) sono disponibili ai livelli seguenti:</span><span class="sxs-lookup"><span data-stu-id="69809-118">The information returned by the [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) function is available at the following levels:</span></span>

-   [<span data-ttu-id="69809-119">**\_gruppo di visualizzazione NET \_**</span><span class="sxs-lookup"><span data-stu-id="69809-119">**NET\_DISPLAY\_GROUP**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_group)
-   [<span data-ttu-id="69809-120">**NET \_ display \_ computer**</span><span class="sxs-lookup"><span data-stu-id="69809-120">**NET\_DISPLAY\_MACHINE**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_machine)
-   [<span data-ttu-id="69809-121">**NET \_ display \_ User**</span><span class="sxs-lookup"><span data-stu-id="69809-121">**NET\_DISPLAY\_USER**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_user)

 

 




