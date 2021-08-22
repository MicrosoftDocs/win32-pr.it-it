---
description: Un elenco di linee è un elenco di segmenti rette isolate.
ms.assetid: bb02b3d6-f30f-4f2b-8b40-a7e37faf524a
title: Elenchi di righe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f06ca68e3fefab1217e77bbf41bc30aa42dac9631b70480fe4bf0a98d38d913
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606797"
---
# <a name="line-lists"></a>Elenchi di righe

Un elenco di linee è un elenco di segmenti rette isolate. Gli elenchi di righe sono utili per attività come l'aggiunta di neet o di forte pioggia a una scena 3D. Le applicazioni creano un elenco di righe compilando una matrice di vertici. Si noti che il numero di vertici in un elenco di righe deve essere un numero pari maggiore o uguale a due.

La figura seguente mostra un elenco di righe sottoposto a rendering.

![illustrazione di un elenco di righe](images/linelst.png)

È possibile applicare materiali e trame a un elenco di righe. I colori nel materiale o nella trama vengono visualizzati solo lungo le linee disegnate, non in qualsiasi punto tra le linee.

Il codice seguente illustra come creare vertici per questo elenco di righe.


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



L'esempio di codice seguente illustra come eseguire il rendering di un elenco di righe in Direct3D 9 usando [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


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

 

 
