---
title: Come usare DirectComposition
description: In questa sezione vengono descritte le procedure consigliate per l'utilizzo di Microsoft DirectComposition \ 32; API e illustra come usare l'API per eseguire diverse attività comuni.
ms.assetid: 49F6E356-90C7-423A-A31A-AEE41F882D3B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0658a9693567dfd88e9a986893048fa1d0fa1e5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299101"
---
# <a name="how-to-use-directcomposition"></a><span data-ttu-id="4fb59-103">Come usare DirectComposition</span><span class="sxs-lookup"><span data-stu-id="4fb59-103">How to use DirectComposition</span></span>

> [!NOTE]
> <span data-ttu-id="4fb59-104">Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="4fb59-104">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="4fb59-105">Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="4fb59-105">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="4fb59-106">In questa sezione vengono descritte le procedure consigliate per l'utilizzo dell'API Microsoft DirectComposition e viene illustrato come utilizzare l'API per eseguire diverse attività comuni.</span><span class="sxs-lookup"><span data-stu-id="4fb59-106">This section describes best practices for using the Microsoft DirectComposition API, and demonstrates how to use the API to accomplish several common tasks.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4fb59-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="4fb59-107">In this section</span></span>



| <span data-ttu-id="4fb59-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="4fb59-108">Topic</span></span>                                                                                                                      | <span data-ttu-id="4fb59-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fb59-109">Description</span></span>                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4fb59-110">Procedure consigliate per DirectComposition</span><span class="sxs-lookup"><span data-stu-id="4fb59-110">Best practices for DirectComposition</span></span>](best-practices-for-directcomposition.md)<br/>                                | <span data-ttu-id="4fb59-111">Questo argomento descrive le procedure consigliate per l'uso di DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="4fb59-111">This topic describes best practices for using DirectComposition.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="4fb59-112">Come inizializzare DirectComposition</span><span class="sxs-lookup"><span data-stu-id="4fb59-112">How to initialize DirectComposition</span></span>](initialize-directcomposition.md)<br/>                                         | <span data-ttu-id="4fb59-113">In questo argomento viene illustrato come creare e inizializzare il set minimo di oggetti DirectComposition necessari per creare una semplice composizione.</span><span class="sxs-lookup"><span data-stu-id="4fb59-113">This topic demonstrates how to create and initialize the minimum set of DirectComposition objects needed to create a simple composition.</span></span><br/>                                                          |
| [<span data-ttu-id="4fb59-114">Come compilare una semplice struttura ad albero visuale</span><span class="sxs-lookup"><span data-stu-id="4fb59-114">How to build a simple visual tree</span></span>](how-to--build-a-visual-tree.md)<br/>                                            | <span data-ttu-id="4fb59-115">In questo argomento viene illustrato come compilare una semplice struttura ad albero visuale DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="4fb59-115">This topic demonstrates how to build a simple DirectComposition visual tree.</span></span> <span data-ttu-id="4fb59-116">Nell'esempio riportato in questo argomento viene compilata e composta una struttura ad albero visuale costituita da un oggetto visivo radice e da tre oggetti visivi figlio.</span><span class="sxs-lookup"><span data-stu-id="4fb59-116">The example in this topic builds and composes a visual tree that consists of a root visual and three child visuals.</span></span> <br/> |
| [<span data-ttu-id="4fb59-117">Come eseguire il clip con un oggetto rettangolo clip</span><span class="sxs-lookup"><span data-stu-id="4fb59-117">How to clip with a rectangle clip object</span></span>](how-to--set-the-clip-rectangle-for-a-visual.md)<br/>                     | <span data-ttu-id="4fb59-118">In questo argomento viene illustrato come utilizzare un oggetto clip rettangolare per ritagliare una struttura ad albero visuale o visuale.</span><span class="sxs-lookup"><span data-stu-id="4fb59-118">This topic demonstrates how to use a rectangle clip object to clip a visual or visual tree.</span></span> <br/>                                                                                                      |
| [<span data-ttu-id="4fb59-119">Come applicare le trasformazioni 2D</span><span class="sxs-lookup"><span data-stu-id="4fb59-119">How to apply 2D transforms</span></span>](apply-2d-transforms.md)<br/>                                                           | <span data-ttu-id="4fb59-120">Questo argomento illustra come applicare le trasformazioni 2D a un oggetto visivo usando DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="4fb59-120">This topic demonstrates how to apply 2D transforms to a visual by using DirectComposition.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="4fb59-121">Come applicare effetti</span><span class="sxs-lookup"><span data-stu-id="4fb59-121">How to apply effects</span></span>](how-to--apply-transforms-and-effects-to-a-visual.md)<br/>                                    | <span data-ttu-id="4fb59-122">Questo argomento illustra come usare DirectComposition per applicare effetti e trasformazioni 3D a un oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="4fb59-122">This topic demonstrates how to use DirectComposition to apply effects and 3D transformations to a visual.</span></span><br/>                                                                                         |
| [<span data-ttu-id="4fb59-123">Come applicare animazioni</span><span class="sxs-lookup"><span data-stu-id="4fb59-123">How to apply animations</span></span>](how-to--animate-a-visual.md)<br/>                                                         | <span data-ttu-id="4fb59-124">In questo argomento viene illustrato come animare le proprietà di un oggetto visivo utilizzando DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="4fb59-124">This topic demonstrates how to animate the properties of a visual by using DirectComposition.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="4fb59-125">Come aggiungere un'animazione alla bitmap di una finestra figlio a più livelli</span><span class="sxs-lookup"><span data-stu-id="4fb59-125">How to animate the bitmap of a layered child window</span></span>](how-to--animate-the-bitmap-of-a-layered-child-window.md)<br/> | <span data-ttu-id="4fb59-126">In questo argomento viene descritto come creare e animare un oggetto visivo che utilizza la bitmap di una finestra figlio sovrapposta come contenuto dell'oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="4fb59-126">This topic describes how to create and animate a visual that uses the bitmap of a layered child window as the visual's content.</span></span> <br/>                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="4fb59-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4fb59-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fb59-128">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="4fb59-128">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 





