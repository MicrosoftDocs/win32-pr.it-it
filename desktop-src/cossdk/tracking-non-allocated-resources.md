---
description: Rilevamento di risorse non allocate
ms.assetid: ebaca876-5249-4b6b-b0d5-08f098e3f5f5
title: Rilevamento di risorse non allocate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c9f814e08798b4fbb0f160e0d0e0f8aabebba7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305130"
---
# <a name="tracking-non-allocated-resources"></a><span data-ttu-id="1c022-103">Rilevamento di risorse non allocate</span><span class="sxs-lookup"><span data-stu-id="1c022-103">Tracking Non-Allocated Resources</span></span>

<span data-ttu-id="1c022-104">Il responsabile del dispenser può tenere traccia di una risorsa che non è in inventario, in base alla conoscenza della durata dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1c022-104">The dispenser manager can track a resource that is not inventoried, based on knowledge of the object's lifetime.</span></span> <span data-ttu-id="1c022-105">Quando viene liberata, una risorsa rilevata non allocata viene eliminata e pertanto non viene restituita all'inventario.</span><span class="sxs-lookup"><span data-stu-id="1c022-105">When a tracked, non-allocated resource is freed, it is destroyed and therefore not returned to inventory.</span></span> <span data-ttu-id="1c022-106">Questa modalità di sola registrazione per le risorse che possono essere create ed eliminate in modo economico è più utile che archiviarle nell'inventario.</span><span class="sxs-lookup"><span data-stu-id="1c022-106">This track-only mode for resources that are inexpensive to create and destroy is more useful than storing them in inventory.</span></span> <span data-ttu-id="1c022-107">Questa modalità è utile anche per la gestione di un dispenser di memoria o per una risorsa difficile da inventariare perché sono presenti troppi tipi diversi.</span><span class="sxs-lookup"><span data-stu-id="1c022-107">This mode is also useful for managing a memory dispenser or for a resource that is difficult to inventory because there are too many different types.</span></span>

<span data-ttu-id="1c022-108">In modalità di sola registrazione, un dispenser di risorse crea direttamente una risorsa richiesta anziché chiedere al responsabile del dispenser di allocarne una dall'inventario.</span><span class="sxs-lookup"><span data-stu-id="1c022-108">In track-only mode, a resource dispenser directly creates a requested resource instead of asking the dispenser manager to allocate one from inventory.</span></span> <span data-ttu-id="1c022-109">Prima di restituire questa risorsa al componente dell'applicazione richiedente, il dispenser di risorse indica al responsabile del dispenser di tenere traccia della risorsa, garantendo che anche se il componente trascura di liberare la risorsa, il gestore di dispenser lo eseguirà al termine della durata del componente.</span><span class="sxs-lookup"><span data-stu-id="1c022-109">Before returning this resource to the requesting application component, the resource dispenser tells the dispenser manager to track the resource, which ensures that even if the component neglects to free the resource, the dispenser manager will do so when the component's lifetime is over.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c022-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1c022-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c022-111">Concetti relativi al dispenser di risorse COM+</span><span class="sxs-lookup"><span data-stu-id="1c022-111">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



