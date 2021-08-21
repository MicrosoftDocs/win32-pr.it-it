---
description: Una ventola di triangolo è simile a una striscia triangolare, ad eccezione del fatto che tutti i triangoli condividono un vertice, come illustrato nella figura seguente.
ms.assetid: a1fbfd78-121f-4f79-9ba8-44f23356a432
title: Ventole triangolare (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 806dc57545f4cb8341eee2b586aa062ba93d98568e6269e209dbf616fbb081d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044179"
---
# <a name="triangle-fans-direct3d-9"></a>Ventole triangolare (Direct3D 9)

Una ventola di triangolo è simile a una striscia triangolare, ad eccezione del fatto che tutti i triangoli condividono un vertice, come illustrato nella figura seguente.

![illustrazione di una ventola triangolare](images/trifan.gif)

Il sistema usa i vertici v2, v3 e v1 per disegnare il primo triangolo. v3, v4 e v1 per disegnare il secondo triangolo; v4, v5 e v1 per disegnare il terzo triangolo; E così via. Quando è abilitata l'ombreggiatura piatta, il sistema sfumatura il triangolo con il colore del primo vertice.

La figura seguente illustra una ventola triangolare di cui è stato eseguito il rendering.

![illustrazione di una ventola triangolare sottoposta a rendering](images/tfan2.gif)

Il codice seguente illustra come creare vertici per questa ventola triangolare.


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



L'esempio di codice seguente illustra come eseguire il rendering di questa ventola triangolare in Direct3D 9 [**usando IDirect3DDevice9::D rawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLEFAN, 0, 4 );
```



Le ventole a triangolo non sono supportate in Direct3D 10 o versioni successive.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Primitives](primitives.md)
</dt> </dl>

 

 
