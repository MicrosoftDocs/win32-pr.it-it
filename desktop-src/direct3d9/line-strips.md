---
description: Una striscia di linea è una primitiva composta da segmenti di linea collegati.
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: Strisce di linea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dee7eb79b583ad04dc0ed576a7d9426e8dda9fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521953"
---
# <a name="line-strips"></a>Strisce di linea

Una striscia di linea è una primitiva composta da segmenti di linea collegati. L'applicazione può usare strisce di riga per la creazione di poligoni che non sono chiusi. Un poligono chiuso è un poligono il cui ultimo vertice è connesso al primo vertice da un segmento di linea. Se l'applicazione crea poligoni in base alle strisce di riga, non è garantito che i vertici siano complanari.

Nell'illustrazione seguente viene mostrata una striscia di riga sottoposta a rendering.

![illustrazione di una striscia di linea](images/linstrip.gif)

Nel codice seguente viene illustrato come creare vertici per questa striscia di riga.


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



L'esempio di codice seguente illustra come eseguire il rendering di una striscia di riga in Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .


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

 

 
