---
description: Una striscia di linee è una primitiva costituita da segmenti di linea connessi.
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: Strisce di linee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8ba98518cac542a9b8272e4f96494889ef24f269744626aa24e882c7af509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799633"
---
# <a name="line-strips"></a>Strisce di linee

Una striscia di linee è una primitiva costituita da segmenti di linea connessi. L'applicazione può usare strisce di linee per la creazione di poligoni non chiusi. Un poligono chiuso è un poligono il cui ultimo vertice è connesso al primo vertice da un segmento di linea. Se l'applicazione crea poligoni basati su strisce di linee, non è garantito che i vertici siano coplanari.

La figura seguente mostra una striscia di linee sottoposta a rendering.

![illustrazione di una striscia di linee](images/linstrip.gif)

Il codice seguente illustra come creare vertici per questa striscia di linee.


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



L'esempio di codice seguente illustra come eseguire il rendering di una striscia di linee in Direct3D 9 [**usando IDirect3DDevice9::D rawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINESTRIP, 0, 5 );
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Primitives](primitives.md)
</dt> </dl>

 

 
