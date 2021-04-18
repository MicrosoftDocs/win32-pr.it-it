---
description: Un elenco di triangolo è un elenco di triangoli isolati. Potrebbero essere vicini o meno. Un elenco di triangolo deve avere almeno tre vertici e il numero totale di vertici deve essere divisibile per tre.
ms.assetid: e5c3470f-361c-458a-a42a-3549c51d8794
title: Elenchi di triangolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230cac9b4120d31821d70db022ab50d311d7b73e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304367"
---
# <a name="triangle-lists"></a>Elenchi di triangolo

Un elenco di triangolo è un elenco di triangoli isolati. Potrebbero essere vicini o meno. Un elenco di triangolo deve avere almeno tre vertici e il numero totale di vertici deve essere divisibile per tre.

Usare gli elenchi di triangolo per creare un oggetto composto da parti non contigue. Ad esempio, un modo per creare un muro di campo forzato in un gioco 3D consiste nel specificare un elenco esteso di piccoli triangoli non connessi. Applicare quindi un materiale e una trama che sembrano emettere luce nell'elenco dei triangoli. Ogni triangolo nella parete sembra illuminare. La scena dietro la parete diventa parzialmente visibile attraverso i gap tra i triangoli, in quanto un lettore potrebbe aspettarsi quando si esamina un campo forzato.

Gli elenchi di triangolo sono utili anche per creare primitive con spigoli acuti e ombreggiati con ombreggiatura Gouraud. Vedere [vettori normali per visi e vertici (Direct3D 9)](face-and-vertex-normal-vectors.md).

Nella figura seguente viene illustrato un elenco di triangolo di cui è stato eseguito il rendering.

![illustrazione di un elenco di triangolo sottoposto a rendering](images/trilist.png)

Il codice seguente illustra come creare vertici per questo elenco di triangolo.


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



L'esempio di codice seguente illustra come eseguire il rendering di questo elenco di triangolo in Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 2 );
```



È anche possibile usare le strisce di triangolo per eseguire il rendering di triangoli non connessi tra loro. A tale scopo, specificare un triangolo degenerato (ovvero un triangolo con dimensioni pari a zero) nell'elenco; verrà creata una linea tra i due triangoli che non verranno visualizzati durante il rendering. Ad esempio, per eseguire il rendering solo del primo e dell'ultimo triangolo dell'esempio precedente, inizializzare il buffer dei vertici con i vertici seguenti:


```
CUSTOMVERTEX Vertices[] =
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    { 5.0, -5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Primitives](primitives.md)
</dt> </dl>

 

 
