---
description: "Per il rendering dei dati del vertice da un buffer vertex sono necessari alcuni passaggi. Per prima cosa, è necessario impostare l'origine del flusso chiamando il metodo IDirect3DDevice9:: SetStreamSource, come illustrato nell'esempio seguente."
ms.assetid: a0435a3d-e1dd-4365-904d-8e5713e379ce
title: Rendering da un buffer vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cebb68c5395a827a9aee4ea1f8465257c436bb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123429"
---
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="1bda5-104">Rendering da un buffer vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1bda5-104">Rendering from a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="1bda5-105">Per il rendering dei dati del vertice da un buffer vertex sono necessari alcuni passaggi.</span><span class="sxs-lookup"><span data-stu-id="1bda5-105">Rendering vertex data from a vertex buffer requires a few steps.</span></span> <span data-ttu-id="1bda5-106">Per prima cosa, è necessario impostare l'origine del flusso chiamando il metodo [**IDirect3DDevice9:: SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) , come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="1bda5-106">First, you need to set the stream source by calling the [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) method, as shown in the following example.</span></span>


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



<span data-ttu-id="1bda5-107">Il primo parametro di [**IDirect3DDevice9:: SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) indica a Direct3D l'origine del flusso di dati del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1bda5-107">The first parameter of [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) tells Direct3D the source of the device data stream.</span></span> <span data-ttu-id="1bda5-108">Il secondo parametro è il buffer vertex da associare al flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="1bda5-108">The second parameter is the vertex buffer to bind to the data stream.</span></span> <span data-ttu-id="1bda5-109">Il terzo parametro è l'offset dall'inizio del flusso all'inizio dei dati del vertice, espresso in byte.</span><span class="sxs-lookup"><span data-stu-id="1bda5-109">The third parameter is the offset from the beginning of the stream to the beginning of the vertex data, in bytes.</span></span> <span data-ttu-id="1bda5-110">Il quarto parametro è lo stride del componente, in byte.</span><span class="sxs-lookup"><span data-stu-id="1bda5-110">The fourth parameter is the stride of the component, in bytes.</span></span> <span data-ttu-id="1bda5-111">Nel codice di esempio precedente, la dimensione di un oggetto CUSTOMVERTEX viene utilizzata per lo stride del componente.</span><span class="sxs-lookup"><span data-stu-id="1bda5-111">In the sample code above, the size of a CUSTOMVERTEX is used for the stride of the component.</span></span>

<span data-ttu-id="1bda5-112">Il passaggio successivo consiste nell'informare Direct3D quale vertex shader utilizzare chiamando il metodo [**IDirect3DDevice9:: SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) .</span><span class="sxs-lookup"><span data-stu-id="1bda5-112">The next step is to inform Direct3D which vertex shader to use by calling the [**IDirect3DDevice9::SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) method.</span></span> <span data-ttu-id="1bda5-113">Il codice di esempio seguente imposta un codice FVF per il vertex shader.</span><span class="sxs-lookup"><span data-stu-id="1bda5-113">The following sample code sets an FVF code for the vertex shader.</span></span> <span data-ttu-id="1bda5-114">Questo informa Direct3D dei tipi di vertici che sta occupando.</span><span class="sxs-lookup"><span data-stu-id="1bda5-114">This informs Direct3D of the types of vertices it is dealing with.</span></span>


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



<span data-ttu-id="1bda5-115">Dopo aver impostato l'origine del flusso e il vertex shader, tutti i metodi di creazione utilizzeranno il buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="1bda5-115">After setting the stream source and vertex shader, any draw methods will use the vertex buffer.</span></span> <span data-ttu-id="1bda5-116">Nell'esempio di codice seguente viene illustrato come eseguire il rendering dei vertici da un buffer vertex con il metodo [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span><span class="sxs-lookup"><span data-stu-id="1bda5-116">The code example below shows how to render vertices from a vertex buffer with the [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method.</span></span>


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



<span data-ttu-id="1bda5-117">Il secondo parametro che [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) accetta è l'indice del primo vettore nel buffer del vertice da caricare.</span><span class="sxs-lookup"><span data-stu-id="1bda5-117">The second parameter that [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) accepts is the index of the first vector in the vertex buffer to load.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bda5-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1bda5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bda5-119">Buffer vertici</span><span class="sxs-lookup"><span data-stu-id="1bda5-119">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> <dt>

[<span data-ttu-id="1bda5-120">Rendering dai buffer di Vertex e index (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1bda5-120">Rendering from Vertex and Index Buffers (Direct3D 9)</span></span>](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
