---
title: Licenze
description: Licenze
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, licenze DRM
- Windows Media Format SDK, licenze per DRM
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- Digital Rights Management (DRM), licenze file protette
- DRM (Digital Rights Management), licenze file protette
- licenze, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fbf2d7c0a25b2b19241d90743f43f46a71d7e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332308"
---
# <a name="licenses"></a><span data-ttu-id="2352d-111">Licenze</span><span class="sxs-lookup"><span data-stu-id="2352d-111">Licenses</span></span>

<span data-ttu-id="2352d-112">Una licenza è un set di dati che descrive le condizioni in base alle quali è possibile leggere i dati nei file protetti.</span><span class="sxs-lookup"><span data-stu-id="2352d-112">A license is a set of data that describes the conditions under which data in protected files can be read.</span></span> <span data-ttu-id="2352d-113">Ogni licenza viene applicata a un identificatore di chiave, che in genere viene assegnato a un singolo file multimediale.</span><span class="sxs-lookup"><span data-stu-id="2352d-113">Each license applies to a key identifier, which is typically assigned to a single media file.</span></span> <span data-ttu-id="2352d-114">Questo identificatore viene usato per identificare il contenuto protetto nella licenza.</span><span class="sxs-lookup"><span data-stu-id="2352d-114">This identifier is what is used to identify the protected content in the license.</span></span>

<span data-ttu-id="2352d-115">Ogni licenza specifica una o più azioni che possono essere eseguite con il contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="2352d-115">Each license specifies one or more actions that can be performed with the protected content.</span></span> <span data-ttu-id="2352d-116">Queste azioni, denominate anche diritti, possono essere limitate in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="2352d-116">These actions, also called rights, can be limited in a number of ways.</span></span> <span data-ttu-id="2352d-117">Combinando le date di inizio, le date di fine, i conteggi e i limiti di tempo, l'emittente della licenza può creare qualsiasi limitazione immaginabile su un diritto.</span><span class="sxs-lookup"><span data-stu-id="2352d-117">By combining start dates, end dates, counts, and time limits, the license issuer can create almost any imaginable limitation on a right.</span></span>

<span data-ttu-id="2352d-118">Le licenze vengono rilasciate da un servizio Web.</span><span class="sxs-lookup"><span data-stu-id="2352d-118">Licenses are issued by a Web service.</span></span> <span data-ttu-id="2352d-119">Quando viene acquisita una licenza, questa viene archiviata nel computer client nell'archivio licenze locale, ovvero un file protetto che contiene licenze e altri dati DRM.</span><span class="sxs-lookup"><span data-stu-id="2352d-119">When a license is acquired, it is stored on the client computer in the local license store, which is a protected file that contains licenses and other DRM data.</span></span> <span data-ttu-id="2352d-120">Quando un'applicazione accede al contenuto protetto, il sottosistema DRM Cerca nell'archivio licenze locale una licenza che conceda il diritto appropriato.</span><span class="sxs-lookup"><span data-stu-id="2352d-120">When protected content is accessed by an application, the DRM subsystem searches the local license store for a license that grants the appropriate right.</span></span> <span data-ttu-id="2352d-121">Se non viene trovata alcuna licenza, l'applicazione può acquisirne una in base alle informazioni archiviate nell'intestazione DRM del file.</span><span class="sxs-lookup"><span data-stu-id="2352d-121">If no license is found, the application can acquire one based on information stored in the DRM header of the file.</span></span>

<span data-ttu-id="2352d-122">È possibile emettere più licenze per lo stesso file protetto.</span><span class="sxs-lookup"><span data-stu-id="2352d-122">Multiple licenses can be issued for the same protected file.</span></span> <span data-ttu-id="2352d-123">Quando il sottosistema DRM determina se un'azione è consentita, aggrega i diritti da tutte le licenze che si applicano.</span><span class="sxs-lookup"><span data-stu-id="2352d-123">When the DRM subsystem determines whether an action is allowed, it aggregates the rights from all licenses that apply.</span></span> <span data-ttu-id="2352d-124">A ogni licenza può essere assegnata una priorità.</span><span class="sxs-lookup"><span data-stu-id="2352d-124">Each license can be assigned a priority.</span></span> <span data-ttu-id="2352d-125">Se a un'azione viene applicata più di una licenza, viene verificata la licenza con priorità più elevata per determinare se è necessario decrementare i conteggi.</span><span class="sxs-lookup"><span data-stu-id="2352d-125">If more than one license applies to an action, the highest priority license is checked to determine whether counts need to be decremented.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2352d-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2352d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2352d-127">**Concetti**</span><span class="sxs-lookup"><span data-stu-id="2352d-127">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




