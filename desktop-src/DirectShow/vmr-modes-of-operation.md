---
description: Modalità di funzionamento VMR
ms.assetid: 98244af1-5934-4d1c-b9c3-7a414b065fe7
title: Modalità di funzionamento VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43427c4119bb912d2bc2cf92b1c740b1d22e1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308951"
---
# <a name="vmr-modes-of-operation"></a><span data-ttu-id="c2f61-103">Modalità di funzionamento VMR</span><span class="sxs-lookup"><span data-stu-id="c2f61-103">VMR Modes of Operation</span></span>

<span data-ttu-id="c2f61-104">L'architettura dei componenti di VMR consente alle applicazioni di configurarlo in vari modi, a seconda del modo in cui deve essere eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="c2f61-104">The component architecture of the VMR enables applications to configure it in various ways, depending on how rendering is to be performed.</span></span> <span data-ttu-id="c2f61-105">La tabella seguente illustra le tre modalità di presentazione e le due modalità di combinazione e i componenti presenti per ogni configurazione.</span><span class="sxs-lookup"><span data-stu-id="c2f61-105">The following table shows the three presentation modes and the two mixing modes, and the components that are present for each configuration.</span></span>



| <span data-ttu-id="c2f61-106">Modalità</span><span class="sxs-lookup"><span data-stu-id="c2f61-106">Mode</span></span>       | <span data-ttu-id="c2f61-107">Flusso singolo</span><span class="sxs-lookup"><span data-stu-id="c2f61-107">Single Stream</span></span>                                                                     | <span data-ttu-id="c2f61-108">Più flussi (modalità di combinazione)</span><span class="sxs-lookup"><span data-stu-id="c2f61-108">Multiple Streams (Mixing Mode)</span></span>                                                                                             |
|------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2f61-109">Finestra</span><span class="sxs-lookup"><span data-stu-id="c2f61-109">Windowed</span></span>   | <span data-ttu-id="c2f61-110">Allocatore-unità di sincronizzazione presenterCore</span><span class="sxs-lookup"><span data-stu-id="c2f61-110">Allocator-presenterCore Synchronization Unit</span></span><br/> <span data-ttu-id="c2f61-111">Gestione finestre</span><span class="sxs-lookup"><span data-stu-id="c2f61-111">Window Manager</span></span><br/> | <span data-ttu-id="c2f61-112">MixerCompositor\*</span><span class="sxs-lookup"><span data-stu-id="c2f61-112">MixerCompositor\*</span></span><br/> <span data-ttu-id="c2f61-113">Allocatore-Presenter</span><span class="sxs-lookup"><span data-stu-id="c2f61-113">Allocator-presenter</span></span><br/> <span data-ttu-id="c2f61-114">Unità di sincronizzazione principale</span><span class="sxs-lookup"><span data-stu-id="c2f61-114">Core Synchronization Unit</span></span><br/> <span data-ttu-id="c2f61-115">Gestione finestre</span><span class="sxs-lookup"><span data-stu-id="c2f61-115">Window Manager</span></span><br/> |
| <span data-ttu-id="c2f61-116">Windowless</span><span class="sxs-lookup"><span data-stu-id="c2f61-116">Windowless</span></span> | <span data-ttu-id="c2f61-117">Allocatore-unità di sincronizzazione presenterCore</span><span class="sxs-lookup"><span data-stu-id="c2f61-117">Allocator-presenterCore Synchronization Unit</span></span><br/>                           | <span data-ttu-id="c2f61-118">MixerCompositor\*</span><span class="sxs-lookup"><span data-stu-id="c2f61-118">MixerCompositor\*</span></span><br/> <span data-ttu-id="c2f61-119">Allocatore-Presenter</span><span class="sxs-lookup"><span data-stu-id="c2f61-119">Allocator-presenter</span></span><br/> <span data-ttu-id="c2f61-120">Unità di sincronizzazione principale</span><span class="sxs-lookup"><span data-stu-id="c2f61-120">Core Synchronization Unit</span></span><br/>                           |
| <span data-ttu-id="c2f61-121">Renderless</span><span class="sxs-lookup"><span data-stu-id="c2f61-121">Renderless</span></span> | <span data-ttu-id="c2f61-122">Allocator-Presenter (fornito dall'applicazione) unità di sincronizzazione principale</span><span class="sxs-lookup"><span data-stu-id="c2f61-122">Allocator-presenter (provided by application)Core Synchronization Unit</span></span><br/> | <span data-ttu-id="c2f61-123">MixerCompositor\*</span><span class="sxs-lookup"><span data-stu-id="c2f61-123">MixerCompositor\*</span></span><br/> <span data-ttu-id="c2f61-124">Allocatore-Presenter (fornito dall'applicazione)</span><span class="sxs-lookup"><span data-stu-id="c2f61-124">Allocator-presenter (provided by application)</span></span><br/> <span data-ttu-id="c2f61-125">Unità di sincronizzazione principale</span><span class="sxs-lookup"><span data-stu-id="c2f61-125">Core Synchronization Unit</span></span><br/> |



 

<span data-ttu-id="c2f61-126">\* Indica che l'applicazione dispone dell'opzione per fornire un componente personalizzato o utilizzare il componente predefinito.</span><span class="sxs-lookup"><span data-stu-id="c2f61-126">\* Indicates that the application has the option to provide a custom component or use the default component.</span></span>

<span data-ttu-id="c2f61-127">In tutte le configurazioni, il punto principale da ricordare quando si creano i grafici di filtro con VMR è che è necessario configurare il VMR prima di connetterlo.</span><span class="sxs-lookup"><span data-stu-id="c2f61-127">In all configurations, the main point to remember when you create filter graphs with the VMR is that you must configure the VMR before you connect it.</span></span>

<span data-ttu-id="c2f61-128">Per tutte le configurazioni, i pin non possono essere aggiunti o rimossi in modo dinamico dopo la connessione di VMR al filtro upstream, ma possono essere connessi e disconnessi.</span><span class="sxs-lookup"><span data-stu-id="c2f61-128">For all configurations, pins cannot be dynamically added or removed after the VMR is connected to the upstream filter, but they can be connected and disconnected.</span></span> <span data-ttu-id="c2f61-129">Se l'applicazione non è sicura di quanti pin saranno necessari, è necessario configurare il VMR per il numero massimo che potrebbe essere necessario.</span><span class="sxs-lookup"><span data-stu-id="c2f61-129">If the application is unsure how many pins will be needed, it should configure the VMR for the maximum number that might be needed.</span></span> <span data-ttu-id="c2f61-130">La presenza di pin di input non utilizzati sul filtro non comporta un peggioramento delle prestazioni di rendering.</span><span class="sxs-lookup"><span data-stu-id="c2f61-130">The presence of unused input pins on the filter does not degrade rendering performance.</span></span> <span data-ttu-id="c2f61-131">A differenza del vecchio mixer sovrapposto, VMR non ha un pin di output perché non richiede un filtro separato per la gestione della finestra.</span><span class="sxs-lookup"><span data-stu-id="c2f61-131">Unlike the old Overlay Mixer, the VMR has no output pin because it does not require a separate filter for window management.</span></span>

<span data-ttu-id="c2f61-132">Le sezioni seguenti descrivono come configurare VMR per una determinata modalità:</span><span class="sxs-lookup"><span data-stu-id="c2f61-132">The following sections describe how to configure the VMR for a given mode:</span></span>

-   [<span data-ttu-id="c2f61-133">Modalità a finestra (compatibilità) VMR</span><span class="sxs-lookup"><span data-stu-id="c2f61-133">VMR Windowed (Compatibility) Mode</span></span>](vmr-windowed--compatibility--mode.md)
-   [<span data-ttu-id="c2f61-134">Modalità senza finestra VMR</span><span class="sxs-lookup"><span data-stu-id="c2f61-134">VMR Windowless Mode</span></span>](vmr-windowless-mode.md)
-   [<span data-ttu-id="c2f61-135">VMR con più flussi (modalità di combinazione)</span><span class="sxs-lookup"><span data-stu-id="c2f61-135">VMR with Multiple Streams (Mixing Mode)</span></span>](vmr-with-multiple-streams--mixing-mode.md)
-   [<span data-ttu-id="c2f61-136">Modalità di combinazione YUV</span><span class="sxs-lookup"><span data-stu-id="c2f61-136">YUV Mixing Mode</span></span>](yuv-mixing-mode.md)
-   [<span data-ttu-id="c2f61-137">Posizionamento e trasferimento di rettangoli video nello spazio di composizione</span><span class="sxs-lookup"><span data-stu-id="c2f61-137">Positioning and Moving Video Rectangles in Composition Space</span></span>](positioning-and-moving-video-rectangles-in-composition-space.md)
-   [<span data-ttu-id="c2f61-138">Modalità di riproduzione con rendering VMR (allocatore personalizzato-Presenter)</span><span class="sxs-lookup"><span data-stu-id="c2f61-138">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>](vmr-renderless-playback-mode--custom-allocator-presenters.md)
-   [<span data-ttu-id="c2f61-139">Modalità esclusiva di DirectDraw</span><span class="sxs-lookup"><span data-stu-id="c2f61-139">DirectDraw Exclusive Mode</span></span>](directdraw-exclusive-mode.md)

 

 




