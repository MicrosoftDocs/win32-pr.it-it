---
description: Direzione della transizione
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: Direzione della transizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d43ec4258d2f23c8b8961e3e1b8fd3d554b057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566292"
---
# <a name="transition-direction"></a><span data-ttu-id="f45b8-103">Direzione della transizione</span><span class="sxs-lookup"><span data-stu-id="f45b8-103">Transition Direction</span></span>

<span data-ttu-id="f45b8-104">\[Questa API non è supportata e può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="f45b8-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="f45b8-105">Una transizione passa da input a a input B e da Time t ₀ a t ₁.</span><span class="sxs-lookup"><span data-stu-id="f45b8-105">A transition goes from input A to input B, and from time t₀ to t₁.</span></span> <span data-ttu-id="f45b8-106">Pertanto, la *direzione* di una transizione può indicare uno dei due elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f45b8-106">Therefore, the *direction* of a transition can mean one of two things:</span></span>

-   <span data-ttu-id="f45b8-107">Mapping dei livelli della sequenza temporale agli input.</span><span class="sxs-lookup"><span data-stu-id="f45b8-107">The mapping of timeline layers to inputs.</span></span>
-   <span data-ttu-id="f45b8-108">Progressione nel tempo.</span><span class="sxs-lookup"><span data-stu-id="f45b8-108">The progression over time.</span></span>

<span data-ttu-id="f45b8-109">Il primo è la *direzione di input* e il secondo è la *direzione di avanzamento*.</span><span class="sxs-lookup"><span data-stu-id="f45b8-109">The first is the *input direction*, and the second is the *progress direction*.</span></span> <span data-ttu-id="f45b8-110">È possibile controllare entrambe le direzioni.</span><span class="sxs-lookup"><span data-stu-id="f45b8-110">You can control both directions.</span></span>

-   <span data-ttu-id="f45b8-111">Direzione di input: per impostazione predefinita, una transizione passa dalla composizione dei livelli di priorità inferiore al livello che contiene la transizione.</span><span class="sxs-lookup"><span data-stu-id="f45b8-111">Input direction: By default, a transition goes from the composite of the lower-priority layers to the layer that contains the transition.</span></span> <span data-ttu-id="f45b8-112">Per invertire questa direzione, chiamare il metodo [**IAMTimelineTrans:: SetSwapInputs**](iamtimelinetrans-setswapinputs.md) .</span><span class="sxs-lookup"><span data-stu-id="f45b8-112">To reverse this direction, call the [**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md) method.</span></span>
-   <span data-ttu-id="f45b8-113">Direzione avanzamento: la maggior parte delle transizioni supporta una proprietà di **stato** standard, che specifica la percentuale della transizione che viene riflessa nell'output in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="f45b8-113">Progress direction: Most transitions support a standard **Progress** property, which specifies what percentage of the transition is reflected in the output at a given moment.</span></span> <span data-ttu-id="f45b8-114">Per impostazione predefinita, il valore della proprietà **Progress** passa da 0,0 a 1,0 per la durata della transizione.</span><span class="sxs-lookup"><span data-stu-id="f45b8-114">By default, the value of the **Progress** property goes from 0.0 to 1.0 over the duration of the transition.</span></span> <span data-ttu-id="f45b8-115">Per invertire lo stato di avanzamento, impostare la proprietà **stato** su vai da 1,0 a 0,0.</span><span class="sxs-lookup"><span data-stu-id="f45b8-115">To reverse the progress, set the **Progress** property to go from 1.0 to 0.0.</span></span>

<span data-ttu-id="f45b8-116">Il diagramma seguente illustra la differenza tra direzione di input e direzione di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="f45b8-116">The following diagram illustrates the difference between input direction and progress direction.</span></span> <span data-ttu-id="f45b8-117">Vengono mostrate quattro variazioni in una transizione standard di [cancellazione SMPTE](smpte-wipe-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="f45b8-117">It shows four variations on a standard [SMPTE Wipe](smpte-wipe-transition.md) transition.</span></span>

![Cancella direzioni](images/wipedirections.png)

<span data-ttu-id="f45b8-119">La transizione si trova nella traccia 1.</span><span class="sxs-lookup"><span data-stu-id="f45b8-119">The transition resides on track 1.</span></span> <span data-ttu-id="f45b8-120">Per impostazione predefinita, la cancellazione passa da sinistra a destra e da Track 0 a Track 1.</span><span class="sxs-lookup"><span data-stu-id="f45b8-120">By default, the wipe goes from left to right and from track 0 to track 1.</span></span> <span data-ttu-id="f45b8-121">Lo scambio degli input causa la cancellazione della cancellazione dalla traccia 1 alla traccia 0, ma ancora da sinistra verso destra.</span><span class="sxs-lookup"><span data-stu-id="f45b8-121">Swapping inputs causes the wipe to go from track 1 to track 0, but still from left to right.</span></span> <span data-ttu-id="f45b8-122">Invertendo lo stato, la transizione va da destra a sinistra.</span><span class="sxs-lookup"><span data-stu-id="f45b8-122">Reversing the progress makes the transition go from right to left.</span></span> <span data-ttu-id="f45b8-123">È possibile combinare entrambi, come illustrato all'estrema sinistra.</span><span class="sxs-lookup"><span data-stu-id="f45b8-123">You can combine both, as shown on the far left.</span></span>

<span data-ttu-id="f45b8-124">Per ulteriori informazioni sul rendering delle transizioni DES, vedere [il modello di sequenza temporale](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="f45b8-124">For more information about how DES renders transitions, see [The Timeline Model](the-timeline-model.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f45b8-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f45b8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f45b8-126">Utilizzo degli effetti e delle transizioni</span><span class="sxs-lookup"><span data-stu-id="f45b8-126">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



