---
description: Anteprima degli effetti e delle transizioni
ms.assetid: aa13bd57-69c1-462c-86e3-64026a03bfc4
title: Anteprima degli effetti e delle transizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25506b7e50fe83c2e4fca7bb4166748ec43d33dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125079"
---
# <a name="previewing-effects-and-transitions"></a><span data-ttu-id="78ca4-103">Anteprima degli effetti e delle transizioni</span><span class="sxs-lookup"><span data-stu-id="78ca4-103">Previewing Effects and Transitions</span></span>

<span data-ttu-id="78ca4-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="78ca4-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="78ca4-105">Alcuni effetti e transizioni importano un tempo relativamente lungo per il rendering.</span><span class="sxs-lookup"><span data-stu-id="78ca4-105">Some effects and transitions take a relatively long time to render.</span></span> <span data-ttu-id="78ca4-106">Durante l'anteprima questo può causare la sincronizzazione del video con l'audio.</span><span class="sxs-lookup"><span data-stu-id="78ca4-106">During preview this can cause the video to become choppy or out of sync with the audio.</span></span> <span data-ttu-id="78ca4-107">È possibile aumentare la velocità di anteprima disabilitando gli effetti o le transizioni:</span><span class="sxs-lookup"><span data-stu-id="78ca4-107">You can increase preview speed by disabling effects or transitions:</span></span>

-   <span data-ttu-id="78ca4-108">Per disabilitare tutti gli effetti, chiamare [**IAMTimeline:: EnableEffects**](iamtimeline-enableeffects.md).</span><span class="sxs-lookup"><span data-stu-id="78ca4-108">To disable all effects, call [**IAMTimeline::EnableEffects**](iamtimeline-enableeffects.md).</span></span>
-   <span data-ttu-id="78ca4-109">Per disabilitare tutte le transizioni, chiamare [**IAMTimeline:: EnableTransitions**](iamtimeline-enabletransitions.md).</span><span class="sxs-lookup"><span data-stu-id="78ca4-109">To disable all transitions, call [**IAMTimeline::EnableTransitions**](iamtimeline-enabletransitions.md).</span></span>
-   <span data-ttu-id="78ca4-110">Per disabilitare una particolare transizione, chiamare [**IAMTimelineTrans:: SetCutsOnly**](iamtimelinetrans-setcutsonly.md).</span><span class="sxs-lookup"><span data-stu-id="78ca4-110">To disable a particular transition, call [**IAMTimelineTrans::SetCutsOnly**](iamtimelinetrans-setcutsonly.md).</span></span>

<span data-ttu-id="78ca4-111">Quando gli effetti sono disabilitati, il rendering non viene eseguito durante l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="78ca4-111">When effects are disabled, they are not rendered during preview.</span></span> <span data-ttu-id="78ca4-112">Quando una transizione è disabilitata, viene visualizzata come un salto.</span><span class="sxs-lookup"><span data-stu-id="78ca4-112">When a transition is disabled, it is rendered as a jump cut.</span></span> <span data-ttu-id="78ca4-113">Il segue tra le tracce si verifica ancora, ma non viene eseguito il rendering dell'effetto visivo.</span><span class="sxs-lookup"><span data-stu-id="78ca4-113">The segue between tracks still occurs, but the visual effect is not rendered.</span></span>

<span data-ttu-id="78ca4-114">Se non è possibile eseguire il rendering di un effetto o di una transizione, il motore di rendering sostituisce un effetto predefinito o una transizione.</span><span class="sxs-lookup"><span data-stu-id="78ca4-114">If an effect or transition cannot be rendered, the render engine substitutes a default effect or transition.</span></span> <span data-ttu-id="78ca4-115">Chiamare il metodo [**IAMTimeline:: SetDefaultEffect**](iamtimeline-setdefaulteffect.md) per impostare l'effetto predefinito e il metodo [**IAMTimeline:: SetDefaultTransition**](iamtimeline-setdefaulttransition.md) per impostare la transizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="78ca4-115">Call the [**IAMTimeline::SetDefaultEffect**](iamtimeline-setdefaulteffect.md) method to set the default effect, and the [**IAMTimeline::SetDefaultTransition**](iamtimeline-setdefaulttransition.md) method to set the default transition.</span></span> <span data-ttu-id="78ca4-116">Se non si specifica un valore predefinito o se quello specificato genera anche un errore, DES usa il proprio valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="78ca4-116">If you do not specify a default, or if the one you specify also causes an error, DES uses its own default.</span></span>

> [!Note]  
> <span data-ttu-id="78ca4-117">È anche possibile migliorare la qualità di anteprima aumentando la quantità di buffering dei frame.</span><span class="sxs-lookup"><span data-stu-id="78ca4-117">You can also improve preview quality by increasing the amount of frame buffering.</span></span> <span data-ttu-id="78ca4-118">Vedere [**IAMTimelineGroup:: SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).</span><span class="sxs-lookup"><span data-stu-id="78ca4-118">See [**IAMTimelineGroup::SetOutputBuffering**](iamtimelinegroup-setoutputbuffering.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="78ca4-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="78ca4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78ca4-120">Utilizzo degli effetti e delle transizioni</span><span class="sxs-lookup"><span data-stu-id="78ca4-120">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



