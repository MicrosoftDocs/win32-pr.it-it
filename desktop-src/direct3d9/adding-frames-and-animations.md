---
description: In questa sezione viene illustrato come aggiungere frame e animazioni a un semplice cubo.
ms.assetid: a909b1f1-b54d-469c-8689-003db41a8f25
title: Aggiunta di frame e animazioni (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da88cf431825797943ed33df94742360f7629787
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304553"
---
# <a name="adding-frames-and-animations-direct3d-9"></a><span data-ttu-id="e8b51-103">Aggiunta di frame e animazioni (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e8b51-103">Adding Frames and Animations (Direct3D 9)</span></span>

<span data-ttu-id="e8b51-104">In questa sezione viene illustrato come aggiungere frame e animazioni a un semplice cubo.</span><span class="sxs-lookup"><span data-stu-id="e8b51-104">This section shows how to add frames and animations to a simple cube.</span></span>

## <a name="working-with-frames"></a><span data-ttu-id="e8b51-105">Utilizzo dei frame</span><span class="sxs-lookup"><span data-stu-id="e8b51-105">Working with Frames</span></span>

<span data-ttu-id="e8b51-106">Si prevede che un frame prenda la struttura seguente.</span><span class="sxs-lookup"><span data-stu-id="e8b51-106">A frame is expected to take the following structure.</span></span>


```
Frame Aframe {        // The frame name is chosen for convenience.
FrameTransformMatrix {
...transform data...
}
[ Meshes ] and/or [ More frames]
}
```



<span data-ttu-id="e8b51-107">Posizionare la mesh del cubo definita all'interno di un frame con una trasformazione di identità.</span><span class="sxs-lookup"><span data-stu-id="e8b51-107">Place the defined cube mesh inside a frame with an identity transform.</span></span> <span data-ttu-id="e8b51-108">Applicare quindi un'animazione a questo frame.</span><span class="sxs-lookup"><span data-stu-id="e8b51-108">Then apply an animation to this frame.</span></span>


```
Frame CubeFrame {
FrameTransformMatrix {
1.000000, 0.000000, 0.000000, 0.000000,
0.000000, 1.000000, 0.000000, 0.000000,
0.000000, 0.000000, 1.000000, 0.000000,
0.000000, 0.000000, 0.000000, 1.000000;;
}
{CubeMesh}        // You could have the mesh inline, but this 
                  // uses an object reference instead.
}
```



## <a name="working-with-animations"></a><span data-ttu-id="e8b51-109">Uso delle animazioni</span><span class="sxs-lookup"><span data-stu-id="e8b51-109">Working with Animations</span></span>

<span data-ttu-id="e8b51-110">Un'animazione viene definita da un set di chiavi.</span><span class="sxs-lookup"><span data-stu-id="e8b51-110">An animation is defined by a set of keys.</span></span> <span data-ttu-id="e8b51-111">Una chiave è un valore di ora associato a un'operazione di ridimensionamento, a un orientamento o a una posizione.</span><span class="sxs-lookup"><span data-stu-id="e8b51-111">A key is a time value associated with a scaling operation, an orientation, or a position.</span></span>


```
Animation Animation0 {        // The name is chosen for convenience.
{ Frame that it applies to - normally a reference }
AnimationKey {
...animation key data...
}
{ ...more animation keys... }
}
```



<span data-ttu-id="e8b51-112">Le animazioni vengono quindi raggruppate in AnimationSets:</span><span class="sxs-lookup"><span data-stu-id="e8b51-112">Animations are then grouped into AnimationSets:</span></span>


```
AnimationSet AnimationSet0 { // The name is chosen for convenience.
{ an animation - could be inline or a reference }
{ ... more animations ... } 
} 
```



<span data-ttu-id="e8b51-113">A questo punto, il cubo viene portato attraverso un'animazione.</span><span class="sxs-lookup"><span data-stu-id="e8b51-113">Now take the cube through an animation.</span></span>


```
AnimationSet AnimationSet0 {
Animation Animation0 {
{CubeFrame}    // Use the frame containing the cube.
AnimationKey {
2;             // Position keys
9;             // 9 keys
10; 3; -100.000000, 0.000000, 0.000000;;,
20; 3; -75.000000, 0.000000, 0.000000;;,
30; 3; -50.000000, 0.000000, 0.000000;;,
40; 3; -25.500000, 0.000000, 0.000000;;,
50; 3; 0.000000, 0.000000, 0.000000;;,
60; 3; 25.500000, 0.000000, 0.000000;;,
70; 3; 50.000000, 0.000000, 0.000000;;,
80; 3; 75.500000, 0.000000, 0.000000;;,
90; 3; 100.000000, 0.000000, 0.000000;;;
}
}
}
```



<span data-ttu-id="e8b51-114">Per ulteriori informazioni, vedere i modelli [**animazione**](animation.md) e [**animazioni**](animationset.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b51-114">For more information, see the [**Animation**](animation.md) and [**AnimationSet**](animationset.md) templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8b51-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e8b51-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8b51-116">File X (legacy)</span><span class="sxs-lookup"><span data-stu-id="e8b51-116">X Files (Legacy)</span></span>](x-files--legacy-.md)
</dt> </dl>

 

 



