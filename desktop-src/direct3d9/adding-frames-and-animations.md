---
description: In questa sezione viene illustrato come aggiungere fotogrammi e animazioni a un cubo semplice.
ms.assetid: a909b1f1-b54d-469c-8689-003db41a8f25
title: Aggiunta di frame e animazioni (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbe0da64e5eabff72f0977a8a55f23d3e4756c7681aa2c806b6ee1d794362cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097193"
---
# <a name="adding-frames-and-animations-direct3d-9"></a>Aggiunta di frame e animazioni (Direct3D 9)

In questa sezione viene illustrato come aggiungere fotogrammi e animazioni a un cubo semplice.

## <a name="working-with-frames"></a>Uso dei frame

È previsto che un frame prenda la struttura seguente.


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

Un'animazione è definita da un set di chiavi. Una chiave è un valore temporale associato a un'operazione di ridimensionamento, un orientamento o una posizione.


```
Animation Animation0 {        // The name is chosen for convenience.
{ Frame that it applies to - normally a reference }
AnimationKey {
...animation key data...
}
{ ...more animation keys... }
}
```



Le animazioni vengono quindi raggruppate in Oggetti AnimationSet:


```
AnimationSet AnimationSet0 { // The name is chosen for convenience.
{ an animation - could be inline or a reference }
{ ... more animations ... } 
} 
```



A questo punto, eseguire un'animazione per il cubo.


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



Per altre informazioni, vedere i modelli [**Animation**](animation.md) e [**AnimationSet.**](animationset.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[File X (legacy)](x-files--legacy-.md)
</dt> </dl>

 

 



