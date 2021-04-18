---
description: Un elenco di righe è un elenco di segmenti di linea rettilinei isolati.
ms.assetid: bb02b3d6-f30f-4f2b-8b40-a7e37faf524a
title: Elenchi di righe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27bd58ea2de6b5944b8511e99154c50f671439
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304073"
---
# <a name="line-lists"></a>Elenchi di righe

Un elenco di righe è un elenco di segmenti di linea rettilinei isolati. Gli elenchi di linee sono utili per attività quali l'aggiunta di nevischio o una pioggia intensa a una scena 3D. Le applicazioni creano un elenco di righe riempiendo una matrice di vertici. Si noti che il numero di vertici in un elenco di righe deve essere un numero pari maggiore o uguale a due.

La figura seguente mostra un elenco di righe di cui è stato eseguito il rendering.

![illustrazione di un elenco di righe](images/linelst.png)

È possibile applicare materiali e trame a un elenco di righe. I colori del materiale o della trama vengono visualizzati solo lungo le linee disegnate, non in qualsiasi punto tra le linee.

Nel codice seguente viene illustrato come creare vertici per questo elenco di righe.


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



L'esempio di codice seguente illustra come eseguire il rendering di un elenco di righe in Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINELIST, 0, 3 );
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Primitives](primitives.md)
</dt> </dl>

 

 
