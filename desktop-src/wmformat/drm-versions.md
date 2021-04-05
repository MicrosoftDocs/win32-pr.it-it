---
title: Versioni DRM
description: Versioni DRM
ms.assetid: ac802547-a3cc-4b30-a8e6-62b679326486
keywords:
- Windows Media Format SDK, versioni DRM
- Digital Rights Management (DRM), versioni
- DRM (Digital Rights Management), versioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be792554e553ccc35dbec71d40ff304af76fafd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955327"
---
# <a name="drm-versions"></a><span data-ttu-id="03706-106">Versioni DRM</span><span class="sxs-lookup"><span data-stu-id="03706-106">DRM Versions</span></span>

<span data-ttu-id="03706-107">Sono disponibili diverse versioni di Windows Media Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="03706-107">There are several versions of Windows Media digital rights management (DRM).</span></span> <span data-ttu-id="03706-108">La versione 1 di DRM è spesso impostata separatamente dalle altre versioni di questa documentazione, perché viene implementata usando tecniche diverse dalle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="03706-108">DRM version 1 is often set apart from the other versions in this documentation, because it is implemented using techniques that are different from the later versions.</span></span> <span data-ttu-id="03706-109">La seconda generazione di Windows Media DRM è denominata DRM versione 7 perché è stata introdotta come parte di Windows Media Format 7 SDK.</span><span class="sxs-lookup"><span data-stu-id="03706-109">The second generation of Windows Media DRM is called DRM version 7 because it was introduced as part of the Windows Media Format 7 SDK.</span></span> <span data-ttu-id="03706-110">Viene talvolta definito DRM versione 2.</span><span class="sxs-lookup"><span data-stu-id="03706-110">It is sometimes called DRM version 2.</span></span> <span data-ttu-id="03706-111">Le versioni successive di Windows Media DRM, DRM versione 9 e il nuovo Windows Media DRM 10 sono estensioni di DRM versione 7 e utilizzano le stesse procedure per l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="03706-111">The later versions of Windows Media DRM, DRM version 9 and the new Windows Media DRM 10, are extensions of DRM version 7 and use the same procedures for implementation.</span></span> <span data-ttu-id="03706-112">Tutte le versioni di Windows Media DRM utilizzano le stesse routine di crittografia; le differenze tra le versioni riguardano le funzionalità delle licenze.</span><span class="sxs-lookup"><span data-stu-id="03706-112">All versions of Windows Media DRM use the same encryption routines; the differences between versions have to do with license features.</span></span>

<span data-ttu-id="03706-113">Quando si creano file protetti usando gli oggetti di Windows Media Format SDK, è necessario supportare sia la versione 1 che la versione più recente.</span><span class="sxs-lookup"><span data-stu-id="03706-113">When you create protected files by using the objects of the Windows Media Format SDK, you should support both version 1 and the most current version.</span></span> <span data-ttu-id="03706-114">I file protetti da DRM versione 1 sono diversi da quelli protetti da versioni successive solo nel contenuto dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="03706-114">Files protected by DRM version 1 differ from files protected by later versions only in the contents of the header.</span></span> <span data-ttu-id="03706-115">I file più recenti contenenti le informazioni aggiuntive sull'intestazione possono comunque essere usati nei client che eseguono il rendering solo del contenuto della versione 1.</span><span class="sxs-lookup"><span data-stu-id="03706-115">Newer files that contain the additional header information can still be used on clients that render only version 1 content.</span></span> <span data-ttu-id="03706-116">Sebbene le versioni successive di DRM offrano un livello più elevato di sicurezza e funzionalità aggiuntive, esistono ancora molti giocatori che usano solo la versione 1.</span><span class="sxs-lookup"><span data-stu-id="03706-116">While later versions of DRM offer a higher level of security and additional features, there are still many players that use only version 1.</span></span>

<span data-ttu-id="03706-117">Per ulteriori informazioni sulle versioni DRM, vedere la documentazione di Windows Media Rights Manager SDK.</span><span class="sxs-lookup"><span data-stu-id="03706-117">For more information on DRM versions, see the Windows Media Rights Manager SDK documentation.</span></span>

> [!Note]  
> <span data-ttu-id="03706-118">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="03706-118">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="03706-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03706-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03706-120">**Funzionalità di Rights Management digitali**</span><span class="sxs-lookup"><span data-stu-id="03706-120">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="03706-121">**Abilitazione del supporto DRM**</span><span class="sxs-lookup"><span data-stu-id="03706-121">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




