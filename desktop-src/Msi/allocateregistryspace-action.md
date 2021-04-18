---
description: L'azione AllocateRegistrySpace garantisce che nel registro di sistema esista la quantità di spazio disponibile nel registro di sistema specificato dalla proprietà AVAILABLEFREEREG.
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: Azione AllocateRegistrySpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6f986561595c73bf3bb1188d899af3d3d7d528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311064"
---
# <a name="allocateregistryspace-action"></a><span data-ttu-id="3548d-103">Azione AllocateRegistrySpace</span><span class="sxs-lookup"><span data-stu-id="3548d-103">AllocateRegistrySpace Action</span></span>

<span data-ttu-id="3548d-104">L'azione AllocateRegistrySpace garantisce che nel registro di sistema esista la quantità di spazio disponibile nel registro di sistema specificato dalla proprietà [**AVAILABLEFREEREG**](availablefreereg.md) .</span><span class="sxs-lookup"><span data-stu-id="3548d-104">The AllocateRegistrySpace action ensures that the amount of free registry space specified by the [**AVAILABLEFREEREG**](availablefreereg.md) property exists in the registry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="3548d-105">Restrizioni sequenza</span><span class="sxs-lookup"><span data-stu-id="3548d-105">Sequence Restrictions</span></span>

<span data-ttu-id="3548d-106">L'azione AllocateRegistrySpace deve essere chiamata dopo [InstallInitialize](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="3548d-106">The AllocateRegistrySpace action must be called after [InstallInitialize](installinitialize-action.md).</span></span> <span data-ttu-id="3548d-107">È consigliabile pianificare il AllocateRegistrySpace prima di tutte le altre azioni per assicurarsi che lo spazio disponibile nel registro di sistema sia sufficiente per continuare.</span><span class="sxs-lookup"><span data-stu-id="3548d-107">It is advisable to schedule the AllocateRegistrySpace before all other actions to ensure there is enough registry space available to continue.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="3548d-108">Messaggi ActionData</span><span class="sxs-lookup"><span data-stu-id="3548d-108">ActionData Messages</span></span>



| <span data-ttu-id="3548d-109">Campo</span><span class="sxs-lookup"><span data-stu-id="3548d-109">Field</span></span> | <span data-ttu-id="3548d-110">Descrizione dei dati dell'azione</span><span class="sxs-lookup"><span data-stu-id="3548d-110">Description of action data</span></span>     |
|-------|--------------------------------|
| <span data-ttu-id="3548d-111">\[1\]</span><span class="sxs-lookup"><span data-stu-id="3548d-111">\[1\]</span></span> | <span data-ttu-id="3548d-112">Spazio del registro di sistema obbligatorio in KB.</span><span class="sxs-lookup"><span data-stu-id="3548d-112">Registry space required in KB.</span></span> |



 

 

 



