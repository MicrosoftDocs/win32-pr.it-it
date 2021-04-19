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
# <a name="adding-frames-and-animations-direct3d-9"></a>Aggiunta di frame e animazioni (Direct3D 9)

In questa sezione viene illustrato come aggiungere frame e animazioni a un semplice cubo.

## <a name="working-with-frames"></a>Utilizzo dei frame

Si prevede che un frame prenda la struttura seguente.


```
Frame Aframe {        // The frame name is chosen for convenience.
FrameTransformMatrix {
...transform data...
}
[ Meshes ] and/or [ More frames]
}
```



Posizionare la mesh del cubo definita all'interno di un frame con una trasformazione di identità. Applicare quindi un'animazione a questo frame.


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



## <a name="working-with-animations"></a>Uso delle animazioni

Un'animazione viene definita da un set di chiavi. Una chiave è un valore di ora associato a un'operazione di ridimensionamento, a un orientamento o a una posizione.


```
Animation Animation0 {        // The name is chosen for convenience.
{ Frame that it applies to - normally a reference }
AnimationKey {
...animation key data...
}
{ ...more animation keys... }
}
```



Le animazioni vengono quindi raggruppate in AnimationSets:


```
AnimationSet AnimationSet0 { // The name is chosen for convenience.
{ an animation - could be inline or a reference }
{ ... more animations ... } 
} 
```



A questo punto, il cubo viene portato attraverso un'animazione.


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



Per ulteriori informazioni, vedere i modelli [**animazione**](animation.md) e [**animazioni**](animationset.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[File X (legacy)](x-files--legacy-.md)
</dt> </dl>

 

 



