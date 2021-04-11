---
description: Una primitiva 3D è una raccolta di vertici che formano una singola entità 3D. La primitiva più semplice è costituita da una raccolta di punti in un sistema di coordinate 3D, denominato elenco di punti.
ms.assetid: vs|directx_sdk|~\primitives.htm
title: Primitive (grafica Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38916e85add69574a2437b0e48c209b14a341e44
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123432"
---
# <a name="primitives-direct3d-9-graphics"></a>Primitive (grafica Direct3D 9)

Una primitiva 3D è una raccolta di vertici che formano una singola entità 3D. La primitiva più semplice è costituita da una raccolta di punti in un sistema di coordinate 3D, denominato elenco di punti.

Spesso le primitive 3D sono poligoni. Un poligono è una figura 3D chiusa delimitata da almeno tre vertici. Il poligono più semplice è un triangolo. Microsoft Direct3D usa triangoli per comporre la maggior parte dei relativi poligoni perché tutti e tre i vertici in un triangolo sono sicuramente complanari. Il rendering di vertici non pianificati non è efficiente. È possibile combinare triangoli per formare poligoni e mesh complessi di grandi dimensioni.

Nella figura seguente viene illustrato un cubo. Due triangoli formano ogni faccia del cubo. L'intero set di triangoli costituisce una primitiva cubica. È possibile applicare trame e materiali alle superfici delle primitive per fare in modo che vengano visualizzate come una singola forma a tinta unita. Per informazioni dettagliate, vedere [materiali (Direct3D 9)](materials.md) e [trame Direct3D (Direct3D 9)](direct3d-textures.md).

![illustrazione di un cubo con due triangoli in ogni viso](images/cube3d.png)

È anche possibile usare triangoli per creare primitive le cui superfici sembrano essere curve smussate. Nella figura seguente viene illustrato come una sfera può essere simulata con triangoli. Dopo l'applicazione di un materiale, la sfera appare curva quando viene sottoposta a rendering. Ciò è particolarmente vero se si usa l'ombreggiatura Gouraud. Per informazioni dettagliate, vedere [ombreggiatura Gouraud](shading-modes.md).

![illustrazione di una sfera simulata usando triangoli](images/sphere3d.png)

I dispositivi Direct3D possono creare e modificare i tipi di primitivi seguenti.

-   [Elenchi di punti](point-lists.md)
-   [Elenchi di righe](line-lists.md)
-   [Strisce di linea](line-strips.md)
-   [Elenchi di triangolo](triangle-lists.md)
-   [Strisce triangolari](triangle-strips.md)
-   [Ventilatori a triangolo (Direct3D 9)](triangle-fans.md)

È possibile eseguire il rendering di tipi primitivi da un'applicazione C++ con uno dei metodi di rendering dell'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Dispositivi Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
