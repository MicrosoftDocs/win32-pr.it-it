---
description: Una ventola a triangolo è simile a una striscia di triangolo, con la differenza che tutti i triangoli condividono un vertice, come illustrato nella figura seguente.
ms.assetid: a1fbfd78-121f-4f79-9ba8-44f23356a432
title: Ventilatori a triangolo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2357af0d999cc759453e34cd278f61064a637cfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566987"
---
# <a name="triangle-fans-direct3d-9"></a>Ventilatori a triangolo (Direct3D 9)

Una ventola a triangolo è simile a una striscia di triangolo, con la differenza che tutti i triangoli condividono un vertice, come illustrato nella figura seguente.

![illustrazione di una ventola a triangolo](images/trifan.gif)

Il sistema usa i vertici V2, V3 e V1 per creare il primo triangolo; V3, V4 e V1 per creare il secondo triangolo; V4, V5 e V1 per creare il terzo triangolo; E così via. Quando è abilitata l'ombreggiatura piatta, il sistema ombreggia il triangolo con il colore del primo vertice.

Nella figura seguente viene illustrata una ventola del triangolo sottoposta a rendering.

![illustrazione di una ventola del triangolo sottoposta a rendering](images/tfan2.gif)

Il codice seguente illustra come creare vertici per questa ventola del triangolo.


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    { 0.0, 0.0, 0.0},
    {-5.0, 5.0, 0.0},
    {-3.0,  7.0, 0.0},
    { 0.0, 10.0, 0.0},
    { 3.0,  7.0, 0.0},
    { 5.0,  5.0, 0.0},
};
```



L'esempio di codice seguente illustra come eseguire il rendering di questa ventola del triangolo in Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLEFAN, 0, 4 );
```



Le ventole del triangolo non sono supportate in Direct3D 10 o versioni successive.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Primitives](primitives.md)
</dt> </dl>

 

 
