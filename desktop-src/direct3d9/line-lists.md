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
# <a name="line-lists"></a><span data-ttu-id="053e5-103">Elenchi di righe</span><span class="sxs-lookup"><span data-stu-id="053e5-103">Line Lists</span></span>

<span data-ttu-id="053e5-104">Un elenco di righe è un elenco di segmenti di linea rettilinei isolati.</span><span class="sxs-lookup"><span data-stu-id="053e5-104">A line list is a list of isolated, straight line segments.</span></span> <span data-ttu-id="053e5-105">Gli elenchi di linee sono utili per attività quali l'aggiunta di nevischio o una pioggia intensa a una scena 3D.</span><span class="sxs-lookup"><span data-stu-id="053e5-105">Line lists are useful for such tasks as adding sleet or heavy rain to a 3D scene.</span></span> <span data-ttu-id="053e5-106">Le applicazioni creano un elenco di righe riempiendo una matrice di vertici.</span><span class="sxs-lookup"><span data-stu-id="053e5-106">Applications create a line list by filling an array of vertices.</span></span> <span data-ttu-id="053e5-107">Si noti che il numero di vertici in un elenco di righe deve essere un numero pari maggiore o uguale a due.</span><span class="sxs-lookup"><span data-stu-id="053e5-107">Note that the number of vertices in a line list must be an even number greater than or equal to two.</span></span>

<span data-ttu-id="053e5-108">La figura seguente mostra un elenco di righe di cui è stato eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="053e5-108">The following illustration shows a rendered line list.</span></span>

![illustrazione di un elenco di righe](images/linelst.png)

<span data-ttu-id="053e5-110">È possibile applicare materiali e trame a un elenco di righe.</span><span class="sxs-lookup"><span data-stu-id="053e5-110">You can apply materials and textures to a line list.</span></span> <span data-ttu-id="053e5-111">I colori del materiale o della trama vengono visualizzati solo lungo le linee disegnate, non in qualsiasi punto tra le linee.</span><span class="sxs-lookup"><span data-stu-id="053e5-111">The colors in the material or texture appear only along the lines drawn, not at any point in between the lines.</span></span>

<span data-ttu-id="053e5-112">Nel codice seguente viene illustrato come creare vertici per questo elenco di righe.</span><span class="sxs-lookup"><span data-stu-id="053e5-112">The following code shows how to create vertices for this line list.</span></span>


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



<span data-ttu-id="053e5-113">L'esempio di codice seguente illustra come eseguire il rendering di un elenco di righe in Direct3D 9 usando [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="053e5-113">The code example below shows how to render a line list in Direct3D 9 using [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span></span>


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINELIST, 0, 3 );
```



## <a name="related-topics"></a><span data-ttu-id="053e5-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="053e5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="053e5-115">Primitives</span><span class="sxs-lookup"><span data-stu-id="053e5-115">Primitives</span></span>](primitives.md)
</dt> </dl>

 

 
