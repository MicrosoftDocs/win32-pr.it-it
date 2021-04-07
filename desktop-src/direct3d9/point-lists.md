---
description: Un elenco di punti è una raccolta di vertici di cui viene eseguito il rendering come punti isolati. L'applicazione può usarle nelle scene 3D per i campi Star o linee tratteggiate sulla superficie di un poligono.
ms.assetid: 82866b07-5043-433f-974a-0a301d4b5491
title: Elenchi di punti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57086a445209d9e60173910e07166a6149e0b8d2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746778"
---
# <a name="point-lists"></a>Elenchi di punti

Un elenco di punti è una raccolta di vertici di cui viene eseguito il rendering come punti isolati. L'applicazione può usarle nelle scene 3D per i campi Star o linee tratteggiate sulla superficie di un poligono.

Nella figura seguente viene illustrato un elenco di punti di cui è stato eseguito il rendering.

![illustrazione di un elenco di punti](images/pointlst.png)

L'applicazione può applicare materiali e trame a un elenco di punti. I colori del materiale o della trama vengono visualizzati solo in corrispondenza dei punti disegnati e non tra i punti.

Nel codice seguente viene illustrato come creare vertici per questo elenco di punti.


```
struct CUSTOMVERTEX
{
    float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



L'esempio di codice seguente illustra come eseguire il rendering di questo elenco di punti in Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_POINTLIST, 0, 6 );
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Primitives](primitives.md)
</dt> </dl>

 

 
