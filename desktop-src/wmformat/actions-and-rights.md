---
title: Azioni e diritti
description: Azioni e diritti
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, licenze DRM
- Windows Media Format SDK, licenze per DRM
- Digital Rights Management (DRM), azioni
- DRM (Digital Rights Management), azioni
- Digital Rights Management (DRM), diritti
- DRM (Digital Rights Management), diritti
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- licenze, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d044850bb5ee73e804065c67840362ec0b7b0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044182"
---
# <a name="actions-and-rights"></a><span data-ttu-id="b32b0-113">Azioni e diritti</span><span class="sxs-lookup"><span data-stu-id="b32b0-113">Actions and Rights</span></span>

<span data-ttu-id="b32b0-114">Quando un file viene protetto con Windows Media DRM, l'utilizzo è completamente limitato.</span><span class="sxs-lookup"><span data-stu-id="b32b0-114">When a file is protected by using Windows Media DRM, its use is completely restricted.</span></span> <span data-ttu-id="b32b0-115">È possibile emettere licenze per consentire a un utente di usare il contenuto in modi specifici.</span><span class="sxs-lookup"><span data-stu-id="b32b0-115">Licenses can be issued to enable a user to use the content in specific ways.</span></span> <span data-ttu-id="b32b0-116">Ogni modo in cui un utente può usare il contenuto è descritto da un'azione.</span><span class="sxs-lookup"><span data-stu-id="b32b0-116">Each way in which a user might use the content is described by an action.</span></span> <span data-ttu-id="b32b0-117">Ad esempio, la riproduzione di un file in un computer è un'azione.</span><span class="sxs-lookup"><span data-stu-id="b32b0-117">For example, playing a file on a computer is an action.</span></span>

<span data-ttu-id="b32b0-118">Una licenza che Abilita una determinata azione è detta concessione di un diritto.</span><span class="sxs-lookup"><span data-stu-id="b32b0-118">A license that enables a given action is said to grant a right.</span></span> <span data-ttu-id="b32b0-119">Ad esempio, una licenza può concedere il diritto di riprodurre il contenuto in un computer.</span><span class="sxs-lookup"><span data-stu-id="b32b0-119">For example, a license can grant the right to play content on a computer.</span></span>

<span data-ttu-id="b32b0-120">Le azioni e i diritti si riferiscono alle stesse modalità di utilizzo del contenuto.</span><span class="sxs-lookup"><span data-stu-id="b32b0-120">Actions and rights refer to the same ways of using content.</span></span> <span data-ttu-id="b32b0-121">La differenza consiste nel fatto che l'azione fa riferimento all'uso, mentre il diritto fa riferimento all'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="b32b0-121">The difference is that the action refers to the use while the right refers to the permission.</span></span> <span data-ttu-id="b32b0-122">Nonostante questa distinzione, le parole Action e right vengono spesso usate in modo interscambiabile in questa documentazione e in altri documenti che descrivono Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="b32b0-122">Despite this distinction, the words action and right are often used interchangeably in this documentation and in other documents that describe Windows Media DRM.</span></span>

<span data-ttu-id="b32b0-123">Le azioni gestite da diritti DRM di Windows Media sono elencate nella sezione [costanti di diritti](rights-constants.md) di questa documentazione.</span><span class="sxs-lookup"><span data-stu-id="b32b0-123">The actions governed by Windows Media DRM rights are listed in the [Rights Constants](rights-constants.md) section of this documentation.</span></span>

<span data-ttu-id="b32b0-124">Alcuni metodi delle API estese del client Windows Media DRM utilizzano costanti diverse per fare riferimento ai diritti DRM di base.</span><span class="sxs-lookup"><span data-stu-id="b32b0-124">Certain methods of the Windows Media DRM Client Extended APIs use different constants to refer to the basic DRM rights.</span></span> <span data-ttu-id="b32b0-125">Ad esempio, il metodo [**IWMDRMLicenseQuery:: QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) usa un set di stringhe specifiche per gli Stati delle licenze.</span><span class="sxs-lookup"><span data-stu-id="b32b0-125">For example, the [**IWMDRMLicenseQuery::QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) method uses a set of strings specific to license states.</span></span> <span data-ttu-id="b32b0-126">Anche se queste costanti definiscono stringhe diverse rispetto alle costanti Rights di base, fanno riferimento agli stessi diritti nella licenza.</span><span class="sxs-lookup"><span data-stu-id="b32b0-126">Even though these constants are defining different strings than the basic rights constants, they refer to the same rights in the license.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b32b0-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b32b0-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b32b0-128">**Concetti**</span><span class="sxs-lookup"><span data-stu-id="b32b0-128">**Concepts**</span></span>](drmconcepts.md)
</dt> </dl>

 

 




