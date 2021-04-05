---
description: Transizioni
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: Transizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fef1cd888293ad83ab1ba9f05ab4bb83ddafa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884906"
---
# <a name="transitions"></a><span data-ttu-id="975e7-103">Transizioni</span><span class="sxs-lookup"><span data-stu-id="975e7-103">Transitions</span></span>

<span data-ttu-id="975e7-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="975e7-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="975e7-105">Una transizione è un modo per segue da una traccia video a un'altra, usando un effetto visivo come una dissolvenza o una cancellazione.</span><span class="sxs-lookup"><span data-stu-id="975e7-105">A transition is a way to segue from one video track to another, using a visual effect such as a fade or a wipe.</span></span> <span data-ttu-id="975e7-106">Nella figura seguente viene illustrata una sequenza temporale con una transizione:</span><span class="sxs-lookup"><span data-stu-id="975e7-106">The following illustration shows a timeline with a transition:</span></span>

![sequenza temporale con transizione](images/timeline3.png)

<span data-ttu-id="975e7-108">L'oggetto Transition si trova nella traccia 1 e rappresenta una transizione da Track 0 a Track 1.</span><span class="sxs-lookup"><span data-stu-id="975e7-108">The transition object is on track 1, and it represents a transition from track 0 to track 1.</span></span> <span data-ttu-id="975e7-109">All'inizio della transizione, il video sottoposto a rendering è interamente da Track 0 (Source A).</span><span class="sxs-lookup"><span data-stu-id="975e7-109">At the start of the transition, the rendered video is entirely from Track 0 (source A).</span></span> <span data-ttu-id="975e7-110">Alla fine, il video è interamente di Track 1 (Source C).</span><span class="sxs-lookup"><span data-stu-id="975e7-110">At the end, the video is entirely from Track 1 (source C).</span></span> <span data-ttu-id="975e7-111">In between, l'output passa dall'origine a all'origine C. In una transizione dissolvenza, ad esempio, un'origine si dissolve progressivamente nell'altra.</span><span class="sxs-lookup"><span data-stu-id="975e7-111">In between, the output transitions from source A to source C. For example, in a fade transition, one source progressively fades to the other.</span></span> <span data-ttu-id="975e7-112">L'output finale è schematizzato lungo la parte inferiore dell'illustrazione.</span><span class="sxs-lookup"><span data-stu-id="975e7-112">The final output is schematized along the bottom of the illustration.</span></span>

<span data-ttu-id="975e7-113">Le transizioni non possono sovrapporsi nel tempo all'interno della stessa traccia, ma è possibile creare transizioni sovrapposte usando l'oggetto Composition, come descritto in [composizione e livelli](composition-and-layering.md).</span><span class="sxs-lookup"><span data-stu-id="975e7-113">Transitions cannot overlap in time within the same track, but you can create overlapping transitions by using the composition object, as described in [Composition and Layering](composition-and-layering.md).</span></span>

<span data-ttu-id="975e7-114">Una transizione ha una direzione.</span><span class="sxs-lookup"><span data-stu-id="975e7-114">A transition has a direction.</span></span> <span data-ttu-id="975e7-115">Per impostazione predefinita, inizia dalla traccia con priorità inferiore (origine A, nell'esempio precedente) e termina in corrispondenza della traccia con priorità maggiore (origine C).</span><span class="sxs-lookup"><span data-stu-id="975e7-115">By default, it starts from the lower priority track (source A, in the previous example.) and ends at the higher-priority track (source C).</span></span> <span data-ttu-id="975e7-116">In between il video è costituito da una combinazione delle due origini.</span><span class="sxs-lookup"><span data-stu-id="975e7-116">In between, the video is a mixture of the two sources.</span></span> <span data-ttu-id="975e7-117">Tuttavia, è possibile specificare il comportamento opposto, come illustrato nella figura seguente:</span><span class="sxs-lookup"><span data-stu-id="975e7-117">However, you can specify the opposite behavior, as shown in the following illustration:</span></span>

![ntrack con due transizioni](images/fade.png)

<span data-ttu-id="975e7-119">In questo caso, la prima transizione si dissolve da Track 0 Fades Track 1, che è il comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="975e7-119">Here, the first transition fades from track 0 fades track 1, which is the default behavior.</span></span> <span data-ttu-id="975e7-120">La seconda transizione si dissolve da Track 1 fino a Track 0.</span><span class="sxs-lookup"><span data-stu-id="975e7-120">The second transition fades from track 1 back to Track 0.</span></span> <span data-ttu-id="975e7-121">Si noti che entrambe le transizioni si trovano nella traccia 1.</span><span class="sxs-lookup"><span data-stu-id="975e7-121">Note that both transitions are located on track 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="975e7-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="975e7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="975e7-123">Introduzione con i servizi di modifica DirectShow</span><span class="sxs-lookup"><span data-stu-id="975e7-123">Getting Started with DirectShow Editing Services</span></span>](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[<span data-ttu-id="975e7-124">Transizioni ed effetti</span><span class="sxs-lookup"><span data-stu-id="975e7-124">Transitions and Effects</span></span>](transitions-and-effects.md)
</dt> <dt>

[<span data-ttu-id="975e7-125">Utilizzo degli effetti e delle transizioni</span><span class="sxs-lookup"><span data-stu-id="975e7-125">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



