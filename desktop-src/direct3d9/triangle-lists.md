---
description: Un elenco di triangoli è un elenco di triangoli isolati. Potrebbero o meno essere vicini tra loro. Un elenco di triangoli deve avere almeno tre vertici e il numero totale di vertici deve essere divisibile per tre.
ms.assetid: e5c3470f-361c-458a-a42a-3549c51d8794
title: Elenchi di triangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d0f9df4d9a0a6d883abd2ccf6b4f3e86c03bb54bcc404901b3c3fa6d10ede03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797439"
---
# <a name="triangle-lists"></a>Elenchi di triangoli

Un elenco di triangoli è un elenco di triangoli isolati. Potrebbero o meno essere vicini tra loro. Un elenco di triangoli deve avere almeno tre vertici e il numero totale di vertici deve essere divisibile per tre.

Usare elenchi di triangoli per creare un oggetto composto da parti non contigue. Ad esempio, un modo per creare una barriera di campo forzato in un gioco 3D è specificare un ampio elenco di piccoli triangoli non collegati. Applicare quindi un materiale e una trama che sembra emettere luce all'elenco di triangoli. Ogni triangolo nella bacheca sembra alone. La scena dietro la barriera diventa parzialmente visibile attraverso gli spazi vuoti tra i triangoli, come un giocatore potrebbe aspettarsi quando guarda un campo di forza.

Gli elenchi di triangoli sono utili anche per la creazione di primitive con bordi acuti e ombreggiati con ombreggiatura Gouraud. Vedere [Face and Vertex Normal Vectors (Direct3D 9) (Vettori](face-and-vertex-normal-vectors.md)normali di viso e vertici (Direct3D 9).

La figura seguente illustra un elenco di triangoli di cui è stato eseguito il rendering.

![illustrazione di un elenco di triangoli di cui è stato eseguito il rendering](images/trilist.png)

Il codice seguente illustra come creare vertici per questo elenco di triangoli.


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



L'esempio di codice seguente illustra come eseguire il rendering di questo elenco di triangoli in Direct3D 9 [**usando IDirect3DDevice9::D rawPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 2 );
```



È anche possibile usare strisce di triangoli per eseguire il rendering di triangoli non connessi tra loro. A tale scopo, specificare un triangolo degenere (ovvero un triangolo con dimensione zero) nell'elenco; Verrà creata una linea tra i due triangoli che non verrà visualizzata durante il rendering. Ad esempio, per eseguire il rendering solo del primo e dell'ultimo triangolo dell'esempio precedente, inizializzare il buffer dei vertici con i vertici seguenti:


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

 

 
