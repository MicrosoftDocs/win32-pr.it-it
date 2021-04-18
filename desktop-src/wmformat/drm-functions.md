---
title: Funzioni client DRM di Microsoft Windows Media
description: Funzioni client DRM di Microsoft Windows Media
ms.assetid: 5d726c56-d0f3-4eb8-829f-3a0c1a0e0802
keywords:
- Windows Media Format SDK, funzioni
- Digital Rights Management (DRM), funzioni
- DRM (Digital Rights Management), funzioni
- API estese del client DRM, funzioni
- API estese client, funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c1730413a4918b0f748099fbd55714339a7e9b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300796"
---
# <a name="microsoft-windows-media-drm-client-functions"></a><span data-ttu-id="681c8-108">Funzioni client DRM di Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="681c8-108">Microsoft Windows Media DRM Client Functions</span></span>

<span data-ttu-id="681c8-109">Le funzioni seguenti sono implementate come parte delle API estese del client DRM di Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="681c8-109">The following functions are implemented as part of the Microsoft Windows Media DRM Client Extended APIs.</span></span>



| <span data-ttu-id="681c8-110">Funzione</span><span class="sxs-lookup"><span data-stu-id="681c8-110">Function</span></span>                                                             | <span data-ttu-id="681c8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="681c8-111">Description</span></span>                                                                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="681c8-112">**WMDRMCreateProvider**</span><span class="sxs-lookup"><span data-stu-id="681c8-112">**WMDRMCreateProvider**</span></span>](wmdrmcreateprovider.md)                   | <span data-ttu-id="681c8-113">Crea un class factory in grado di creare gli altri oggetti DRM.</span><span class="sxs-lookup"><span data-stu-id="681c8-113">Creates a class factory that can create the other DRM objects.</span></span> <span data-ttu-id="681c8-114">Questa funzione non richiede una libreria stub di Microsoft e crea oggetti che non supportano le funzionalità DRM protette.</span><span class="sxs-lookup"><span data-stu-id="681c8-114">This function does not require a stub library from Microsoft and creates objects that do not support the protected DRM features.</span></span> |
| [<span data-ttu-id="681c8-115">**WMDRMCreateProtectedProvider**</span><span class="sxs-lookup"><span data-stu-id="681c8-115">**WMDRMCreateProtectedProvider**</span></span>](wmdrmcreateprotectedprovider.md) | <span data-ttu-id="681c8-116">Crea un class factory in grado di creare gli altri oggetti DRM.</span><span class="sxs-lookup"><span data-stu-id="681c8-116">Creates a class factory that can create the other DRM objects.</span></span> <span data-ttu-id="681c8-117">Questa funzione richiede una libreria stub di Microsoft e crea oggetti che supportano le funzionalità DRM protette.</span><span class="sxs-lookup"><span data-stu-id="681c8-117">This function requires a stub library from Microsoft and creates objects that support the protected DRM features.</span></span>                |
| [<span data-ttu-id="681c8-118">**WMDRMShutdown**</span><span class="sxs-lookup"><span data-stu-id="681c8-118">**WMDRMShutdown**</span></span>](wmdrmshutdown.md)                               | <span data-ttu-id="681c8-119">Rilascia le risorse usate dalle API.</span><span class="sxs-lookup"><span data-stu-id="681c8-119">Releases resources used by the APIs.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="681c8-120">**WMDRMStartup**</span><span class="sxs-lookup"><span data-stu-id="681c8-120">**WMDRMStartup**</span></span>](wmdrmstartup.md)                                 | <span data-ttu-id="681c8-121">Inizializza le risorse usate dalle API.</span><span class="sxs-lookup"><span data-stu-id="681c8-121">Initializes resources used by the APIs.</span></span>                                                                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="681c8-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="681c8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="681c8-123">**Guida di riferimento alla programmazione**</span><span class="sxs-lookup"><span data-stu-id="681c8-123">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




