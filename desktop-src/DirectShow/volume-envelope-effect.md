---
description: Effetto busta volume
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: Effetto busta volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9364b88b1928e533a031f0700cb8a2c44bc9822d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314368"
---
# <a name="volume-envelope-effect"></a><span data-ttu-id="839f9-103">Effetto busta volume</span><span class="sxs-lookup"><span data-stu-id="839f9-103">Volume Envelope Effect</span></span>

> [!Note]  
> <span data-ttu-id="839f9-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="839f9-104">\[Deprecated.</span></span> <span data-ttu-id="839f9-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="839f9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="839f9-106">L'effetto busta volume imposta il volume in un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="839f9-106">The Volume Envelope effect sets the volume on an audio stream.</span></span>

<span data-ttu-id="839f9-107">ID classe (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}</span><span class="sxs-lookup"><span data-stu-id="839f9-107">Class ID (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}</span></span>

<span data-ttu-id="839f9-108">Nome variabile CLSID: CLSID \_ AudMixer</span><span class="sxs-lookup"><span data-stu-id="839f9-108">CLSID Variable Name: CLSID\_AudMixer</span></span>

<span data-ttu-id="839f9-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="839f9-109">Properties</span></span>



| <span data-ttu-id="839f9-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="839f9-110">Property</span></span> | <span data-ttu-id="839f9-111">Type</span><span class="sxs-lookup"><span data-stu-id="839f9-111">Type</span></span>   | <span data-ttu-id="839f9-112">Predefinito</span><span class="sxs-lookup"><span data-stu-id="839f9-112">Default</span></span> | <span data-ttu-id="839f9-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="839f9-113">Description</span></span>                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="839f9-114">Vol.</span><span class="sxs-lookup"><span data-stu-id="839f9-114">Vol</span></span>      | <span data-ttu-id="839f9-115">double</span><span class="sxs-lookup"><span data-stu-id="839f9-115">double</span></span> | <span data-ttu-id="839f9-116">1.0</span><span class="sxs-lookup"><span data-stu-id="839f9-116">1.0</span></span>     | <span data-ttu-id="839f9-117">Volume, come percentuale del volume creato.</span><span class="sxs-lookup"><span data-stu-id="839f9-117">Volume, as a percentage of the authored volume.</span></span> <span data-ttu-id="839f9-118">È possibile produrre dissolvenze audio variando il valore di questa proprietà nel tempo.</span><span class="sxs-lookup"><span data-stu-id="839f9-118">You can produce audio fades by varying this property value over time.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="839f9-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="839f9-119">Remarks</span></span>

<span data-ttu-id="839f9-120">Ogni oggetto in una sequenza temporale può avere al massimo un effetto envelope del volume.</span><span class="sxs-lookup"><span data-stu-id="839f9-120">Each object in a timeline can have at most one volume envelope effect.</span></span> <span data-ttu-id="839f9-121">In una composizione o un gruppo, la busta del volume viene applicata per prima, prima di qualsiasi altro effetto audio, indipendentemente dalla relativa priorità.</span><span class="sxs-lookup"><span data-stu-id="839f9-121">In a composition or a group, the volume envelope is applied first, before any other audio effects, regardless of its priority.</span></span> <span data-ttu-id="839f9-122">In un'origine o in una traccia l'effetto del volume viene applicato in base alla priorità.</span><span class="sxs-lookup"><span data-stu-id="839f9-122">In a source or a track, the volume effect is applied according to its priority.</span></span>

 

 



