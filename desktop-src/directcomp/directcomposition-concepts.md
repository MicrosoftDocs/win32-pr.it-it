---
title: Concetti di DirectComposition
description: Questa sezione fornisce una panoramica concettuale di DirectComposition.
ms.assetid: 7839C264-C15F-4E89-82B6-2963A5C61CEC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bea823d2edd27b2c725cefdd73cd053e94124d7f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045520"
---
# <a name="directcomposition-concepts"></a><span data-ttu-id="dca88-103">Concetti di DirectComposition</span><span class="sxs-lookup"><span data-stu-id="dca88-103">DirectComposition concepts</span></span>

> [!NOTE]
> <span data-ttu-id="dca88-104">Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="dca88-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="dca88-105">Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="dca88-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="dca88-106">Questa sezione fornisce una panoramica concettuale di DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="dca88-106">This section provides a conceptual overview of DirectComposition.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dca88-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="dca88-107">In this section</span></span>



| <span data-ttu-id="dca88-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="dca88-108">Topic</span></span>                                                                     | <span data-ttu-id="dca88-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dca88-109">Description</span></span>                                                                                                                                                                            |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dca88-110">Concetti fondamentali</span><span class="sxs-lookup"><span data-stu-id="dca88-110">Basic concepts</span></span>](basic-concepts.md)<br/>                           | <span data-ttu-id="dca88-111">Questo argomento fornisce una panoramica dei concetti di base di Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="dca88-111">This topic provides an overview of the basic concepts of Microsoft DirectComposition.</span></span><br/>                                                                                       |
| [<span data-ttu-id="dca88-112">Oggetti bitmap</span><span class="sxs-lookup"><span data-stu-id="dca88-112">Bitmap objects</span></span>](bitmap-surfaces.md)<br/>                          | <span data-ttu-id="dca88-113">Questo argomento descrive i tipi di contenuto bitmap supportati da DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="dca88-113">This topic describes the types of bitmap content that DirectComposition supports.</span></span><br/>                                                                                           |
| [<span data-ttu-id="dca88-114">Superficie di composizione</span><span class="sxs-lookup"><span data-stu-id="dca88-114">Composition surface</span></span>](composition-surface.md)<br/>                 | <span data-ttu-id="dca88-115">In questo argomento vengono descritti i tipi di superfici supportati da DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="dca88-115">This topic describes the types of types of surfaces that DirectComposition supports.</span></span><br/>                                                                                        |
| [<span data-ttu-id="dca88-116">Trasformazioni</span><span class="sxs-lookup"><span data-stu-id="dca88-116">Transforms</span></span>](transforms.md)<br/>                                   | <span data-ttu-id="dca88-117">In questo argomento viene illustrato il supporto di DirectComposition per le trasformazioni affini (lineari) bidimensionali (2D) e vengono descritti i tipi di trasformazioni supportati da DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="dca88-117">This topic discusses DirectComposition support for two-dimensional (2D) affine (linear) transforms, and describes the types of transforms that DirectComposition supports.</span></span> <br/> |
| [<span data-ttu-id="dca88-118">Effetti</span><span class="sxs-lookup"><span data-stu-id="dca88-118">Effects</span></span>](effects.md)<br/>                                         | <span data-ttu-id="dca88-119">Questo argomento illustra le nozioni di base degli effetti DirectComposition e descrive i tipi di effetti supportati da DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="dca88-119">This topic discusses the basics of DirectComposition effects, and describes the types of effects that DirectComposition supports.</span></span> <br/>                                          |
| [<span data-ttu-id="dca88-120">Animazione</span><span class="sxs-lookup"><span data-stu-id="dca88-120">Animation</span></span>](animation.md)<br/>                                     | <span data-ttu-id="dca88-121">In questo argomento vengono illustrate le nozioni di base dell'animazione DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="dca88-121">This topic discusses the basics of DirectComposition animation.</span></span> <br/>                                                                                                            |
| [<span data-ttu-id="dca88-122">Ritaglio</span><span class="sxs-lookup"><span data-stu-id="dca88-122">Clipping</span></span>](clipping.md)<br/>                                       | <span data-ttu-id="dca88-123">Questo argomento descrive il supporto di DirectComposition per gli oggetti visivi di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="dca88-123">This topic describes DirectComposition support for clipping visuals.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="dca88-124">Architettura e componenti</span><span class="sxs-lookup"><span data-stu-id="dca88-124">Architecture and components</span></span>](architecture-and-components.md)<br/> | <span data-ttu-id="dca88-125">Questo argomento descrive i componenti che costituiscono DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="dca88-125">This topic describes the components that make up DirectComposition.</span></span><br/>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="dca88-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dca88-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dca88-127">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="dca88-127">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





