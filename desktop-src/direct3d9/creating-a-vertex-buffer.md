---
description: 'Si crea un oggetto vertex buffer chiamando il metodo IDirect3DDevice9:: CreateVertexBuffer, che accetta cinque parametri.'
ms.assetid: 95116ef5-af88-47e7-abf7-1ade9735e2a7
title: Creazione di un buffer vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ffc831ab508f14d61b8e42861f75422ff6a04bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305188"
---
# <a name="creating-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="e4b72-103">Creazione di un buffer vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e4b72-103">Creating a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="e4b72-104">Si crea un oggetto vertex buffer chiamando il metodo [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) , che accetta cinque parametri.</span><span class="sxs-lookup"><span data-stu-id="e4b72-104">You create a vertex buffer object by calling the [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) method, which accepts five parameters.</span></span> <span data-ttu-id="e4b72-105">Il primo parametro specifica la lunghezza in byte del buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="e4b72-105">The first parameter specifies the vertex buffer length, in bytes.</span></span> <span data-ttu-id="e4b72-106">Usare l'operatore sizeof per determinare le dimensioni in byte del formato del vertice.</span><span class="sxs-lookup"><span data-stu-id="e4b72-106">Use the sizeof operator to determine the size of a vertex format, in bytes.</span></span> <span data-ttu-id="e4b72-107">Si consideri il seguente formato di vertice personalizzato.</span><span class="sxs-lookup"><span data-stu-id="e4b72-107">Consider the following custom vertex format.</span></span>


```
struct CUSTOMVERTEX {
        FLOAT x, y, z;
        FLOAT rhw;
        DWORD color;
        FLOAT tu, tv;   // Texture coordinates
};

// Custom flexible vertex format (FVF) describing the custom vertex structure
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)
```



<span data-ttu-id="e4b72-108">Per creare un buffer vertex per mantenere quattro strutture CUSTOMVERTEX, specificare \[ 4 \* sizeof (CUSTOMVERTEX) \] per il parametro *length* .</span><span class="sxs-lookup"><span data-stu-id="e4b72-108">To create a vertex buffer to hold four CUSTOMVERTEX structures, specify \[4\*sizeof(CUSTOMVERTEX)\] for the *Length* parameter.</span></span>

<span data-ttu-id="e4b72-109">Il secondo parametro è un set di controlli di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="e4b72-109">The second parameter is a set of usage controls.</span></span> <span data-ttu-id="e4b72-110">Tra le altre cose, il valore determina se il buffer dei vertici è in grado di contenere informazioni di ritaglio, sotto forma di flag di ritaglio, per i vertici presenti all'esterno dell'area di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e4b72-110">Among other things, its value determines whether the vertex buffer is capable of containing clipping information - in the form of clip flags - for vertices that exist outside the viewing area.</span></span> <span data-ttu-id="e4b72-111">Per creare un buffer vertex che non può contenere i flag di ritaglio, includere il \_ flag D3DUSAGE DONOTCLIP per il parametro *Usage* .</span><span class="sxs-lookup"><span data-stu-id="e4b72-111">To create a vertex buffer that cannot contain clip flags, include the D3DUSAGE\_DONOTCLIP flag for the *Usage* parameter.</span></span> <span data-ttu-id="e4b72-112">Il \_ flag DONOTCLIP di D3DUSAGE viene applicato solo se si indica anche che il buffer dei vertici conterrà i vertici trasformati \_ . il flag XYZRHW di D3DFVF è incluso nel parametro *FVF* .</span><span class="sxs-lookup"><span data-stu-id="e4b72-112">The D3DUSAGE\_DONOTCLIP flag is applied only if you also indicate that the vertex buffer will contain transformed vertices - the D3DFVF\_XYZRHW flag is included in the *FVF* parameter.</span></span> <span data-ttu-id="e4b72-113">Il metodo [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) ignora il \_ flag DONOTCLIP di D3DUSAGE se si indica che il buffer conterrà i vertici non trasformati (il \_ flag D3DFVF XYZ).</span><span class="sxs-lookup"><span data-stu-id="e4b72-113">The [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) method ignores the D3DUSAGE\_DONOTCLIP flag if you indicate that the buffer will contain untransformed vertices (the D3DFVF\_XYZ flag).</span></span> <span data-ttu-id="e4b72-114">I flag di ritaglio occupano memoria aggiuntiva, rendendo leggermente più grande un buffer di vertici con supporto per il ritaglio rispetto a un buffer di vertex che non supporta i flag di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="e4b72-114">Clipping flags occupy additional memory, making a clipping-capable vertex buffer slightly larger than a vertex buffer incapable of containing clipping flags.</span></span> <span data-ttu-id="e4b72-115">Poiché queste risorse vengono allocate quando viene creato il buffer dei vertici, è necessario richiedere in anticipo un buffer dei vertici con supporto di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="e4b72-115">Because these resources are allocated when the vertex buffer is created, you must request a clipping-capable vertex buffer ahead of time.</span></span>

<span data-ttu-id="e4b72-116">Il terzo parametro, *FVF*, è una combinazione di [D3DFVF](d3dfvf.md) che descrivono il formato dei vertici del buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="e4b72-116">The third parameter, *FVF*, is a combination of [D3DFVF](d3dfvf.md) that describe the vertex format of the vertex buffer.</span></span> <span data-ttu-id="e4b72-117">Se si specifica 0 per questo parametro, il buffer dei vertici è un vertex buffer non FVF.</span><span class="sxs-lookup"><span data-stu-id="e4b72-117">If you specify 0 for this parameter, then the vertex buffer is a non-FVF vertex buffer.</span></span> <span data-ttu-id="e4b72-118">Per altre informazioni, vedere [FVF vertex buffers (Direct3D 9)](fvf-vertex-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="e4b72-118">For more information, see [FVF Vertex Buffers (Direct3D 9)](fvf-vertex-buffers.md).</span></span> <span data-ttu-id="e4b72-119">Il quarto parametro descrive la classe di memoria in cui posizionare il buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="e4b72-119">The fourth parameter describes the memory class into which to place the vertex buffer.</span></span>

<span data-ttu-id="e4b72-120">Il parametro finale che [**IDirect3DDevice9:: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) accetta è l'indirizzo di una variabile che verrà compilata con un puntatore alla nuova interfaccia [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) dell'oggetto vertex buffer, se la chiamata ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="e4b72-120">The final parameter that [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer) accepts is the address of a variable that will be filled with a pointer to the new [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) interface of the vertex buffer object, if the call succeeds.</span></span>

<span data-ttu-id="e4b72-121">Non è possibile produrre i flag di ritaglio per un buffer di vertex creato senza supporto.</span><span class="sxs-lookup"><span data-stu-id="e4b72-121">You cannot produce clip flags for a vertex buffer that was created without support for them.</span></span>

<span data-ttu-id="e4b72-122">Nell'esempio di codice C++ riportato di seguito viene illustrato l'aspetto della creazione di un buffer vertex nel codice.</span><span class="sxs-lookup"><span data-stu-id="e4b72-122">The following C++ code example shows what creating a vertex buffer might look like in code.</span></span>


```
   
// d3dDevice contains the address of an IDirect3DDevice9 interface
// g_pVB is a variable of type LPDIRECT3DVERTEXBUFFER9 

// The custom vertex type
struct CUSTOMVERTEX {
    FLOAT x, y, z;
    FLOAT rhw;
    DWORD color;
    FLOAT tu, tv;   // The texture coordinates
};

#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW | D3DFVF_DIFFUSE | D3DFVF_TEX1)

// Create a clipping-capable vertex buffer. Allocate enough memory 
// in the default memory pool to hold three CUSTOMVERTEX 
// structures

    if( FAILED( d3dDevice->CreateVertexBuffer( 3*sizeof(CUSTOMVERTEX),
            0 /*Usage*/, D3DFVF_CUSTOMVERTEX, D3DPOOL_DEFAULT, &g_pVB, NULL ) ) )
        return E_FAIL;
```



## <a name="related-topics"></a><span data-ttu-id="e4b72-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4b72-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4b72-124">Buffer vertici</span><span class="sxs-lookup"><span data-stu-id="e4b72-124">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
