---
description: Recupero automatico delle risorse
ms.assetid: c889dd3f-82d1-4bc3-ac2c-6f468d5b2c7f
title: Recupero automatico delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f76721df1a3858c9ad97d2f696115fff2eb6d3d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342291"
---
# <a name="automatic-resource-reclamation"></a><span data-ttu-id="ad1ce-103">Recupero automatico delle risorse</span><span class="sxs-lookup"><span data-stu-id="ad1ce-103">Automatic Resource Reclamation</span></span>

<span data-ttu-id="ad1ce-104">COM+ invia una notifica al Manager di dispenser ogni volta che termina la durata di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-104">COM+ notifies the dispenser manager each time an object's lifetime ends.</span></span> <span data-ttu-id="ad1ce-105">Il responsabile del dispenser invia quindi una notifica a ogni titolare del dispenser di risorse registrate per verificare se sono presenti risorse ancora utilizzate da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-105">The dispenser manager then notifies each registered resource dispenser's Holder to see whether it has any resources still held by this object.</span></span> <span data-ttu-id="ad1ce-106">In tal caso, tali risorse vengono liberate, impedendo la possibilità di perdite di risorse da parte di componenti che ottengono risorse tramite un dispenser di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-106">If so, those resources are freed, preventing the possibility of resource leaks by components that get resources through a resource dispenser.</span></span>

<span data-ttu-id="ad1ce-107">La funzionalità di recupero automatico è un'opzione che è disattivata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-107">The auto-reclamation feature is an option that is turned off by default.</span></span> <span data-ttu-id="ad1ce-108">Un dispenser di risorse può scegliere di abilitare questa opzione e, in questo modo, garantisce che un riferimento a una risorsa distribuita a un oggetto non venga mai restituito dai metodi dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ad1ce-108">A resource dispenser can choose to enable this option and, in doing so, guarantees that a reference to any resource dispensed to an object is never returned by the object methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad1ce-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad1ce-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad1ce-110">Concetti relativi al dispenser di risorse COM+</span><span class="sxs-lookup"><span data-stu-id="ad1ce-110">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



