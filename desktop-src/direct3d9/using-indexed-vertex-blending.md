---
description: Gli Stati di trasformazione 256-511 sono riservati per archiviare fino a 256 matrici che possono essere indicizzate tramite indici a 8 bit.
ms.assetid: 4c15cfc5-afdf-48d4-8fd1-b10cbe596a1c
title: Uso della combinazione di vertici indicizzati (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120362e4a86081ff51aee9053d1526a9a08f014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876185"
---
# <a name="using-indexed-vertex-blending-direct3d-9"></a><span data-ttu-id="cba4b-103">Uso della combinazione di vertici indicizzati (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cba4b-103">Using Indexed Vertex Blending (Direct3D 9)</span></span>

<span data-ttu-id="cba4b-104">Gli Stati di trasformazione 256-511 sono riservati per archiviare fino a 256 matrici che possono essere indicizzate tramite indici a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="cba4b-104">Transform states 256-511 are reserved to store up to 256 matrices that can be indexed using 8-bit indices.</span></span> <span data-ttu-id="cba4b-105">Usare la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) per eseguire il mapping degli indici 0-255 agli Stati di trasformazione corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="cba4b-105">Use the macro [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) to map indices 0-255 to the corresponding transform states.</span></span> <span data-ttu-id="cba4b-106">Nell'esempio di codice seguente viene illustrato come utilizzare il metodo [**IDirect3DDevice9:: setransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) per impostare la matrice in base al numero di stato della trasformazione 256 su una matrice di identità.</span><span class="sxs-lookup"><span data-stu-id="cba4b-106">The following code example shows how to use the [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) method to set the matrix at transform state number 256 to an identity matrix.</span></span>


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



<span data-ttu-id="cba4b-107">Per abilitare o disabilitare la fusione dei vertici indicizzati, impostare lo \_ stato di rendering INDEXEDVERTEXBLENDENABLE di D3DRS su **true**.</span><span class="sxs-lookup"><span data-stu-id="cba4b-107">To enable or disable indexed vertex blending, set the D3DRS\_INDEXEDVERTEXBLENDENABLE render state to **TRUE**.</span></span> <span data-ttu-id="cba4b-108">Quando lo stato di rendering è abilitato, è necessario passare gli indici di matrice come DWORD compressi con ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="cba4b-108">When the render state is enabled ,you must pass matrix indices as packed DWORDs with every vertex.</span></span> <span data-ttu-id="cba4b-109">Quando questo stato di rendering è disabilitato e la fusione dei vertici è abilitata, equivale a avere gli indici di matrice 0, 1, 2 e 3 in ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="cba4b-109">When this render state is disabled and vertex blending is enabled, it is equivalent to having the matrix indices 0, 1, 2, and 3 in every vertex.</span></span> <span data-ttu-id="cba4b-110">L'esempio di codice seguente usa il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) per abilitare la fusione dei vertici indicizzati.</span><span class="sxs-lookup"><span data-stu-id="cba4b-110">The code example below uses the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method to enable indexed vertex blending.</span></span>


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



<span data-ttu-id="cba4b-111">Per abilitare o disabilitare la fusione dei vertici, impostare lo stato di rendering [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) su un valore diverso \_ da D3DRS Disable dal tipo enumerato [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="cba4b-111">To enable or disable vertex blending, set the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) render state to a value other than D3DRS\_DISABLE from the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="cba4b-112">Se questo stato di rendering non è impostato su D3DRS \_ Disable, è necessario passare il numero necessario di pesi per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="cba4b-112">If this render state is not set to D3DRS\_DISABLE, then you must pass the required number of weights for each vertex.</span></span> <span data-ttu-id="cba4b-113">L'esempio di codice seguente usa **IDirect3DDevice9:: SetRenderState** per abilitare la fusione dei vertici con tre pesi per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="cba4b-113">The following code example uses **IDirect3DDevice9::SetRenderState** to enable vertex blending with three weights for each vertex.</span></span>


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a><span data-ttu-id="cba4b-114">Determinazione del supporto per la fusione di vertici indicizzati</span><span class="sxs-lookup"><span data-stu-id="cba4b-114">Determining Indexed Vertex Blending Support</span></span>

<span data-ttu-id="cba4b-115">Per determinare le dimensioni massime per la matrice di combinazione dei vertici indicizzati, controllare il membro MaxVertexBlendMatrixIndex della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="cba4b-115">To determine the maximum size for the indexed vertex blending matrix, check the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's MaxVertexBlendMatrixIndex member.</span></span> <span data-ttu-id="cba4b-116">L'esempio di codice seguente usa il metodo [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) per recuperare questa dimensione.</span><span class="sxs-lookup"><span data-stu-id="cba4b-116">The code example below uses the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method to retrieve this size.</span></span>


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



<span data-ttu-id="cba4b-117">Se il valore impostato in MaxVertexBlendMatrixIndex è 0, il dispositivo non supporta le matrici indicizzate.</span><span class="sxs-lookup"><span data-stu-id="cba4b-117">If the value set in MaxVertexBlendMatrixIndex is 0, the device does not support indexed matrices.</span></span>

> [!Note]  
> <span data-ttu-id="cba4b-118">Quando si usa l'elaborazione di vertici software, è possibile usare le matrici 256 per la fusione di vertici indicizzati, con o senza la normale fusione.</span><span class="sxs-lookup"><span data-stu-id="cba4b-118">When software vertex processing is used, 256 matrices can be used for indexed vertex blending, with or without normal blending.</span></span>

 

## <a name="passing-matrix-indices-to-direct3d"></a><span data-ttu-id="cba4b-119">Passaggio di indici matrice a Direct3D</span><span class="sxs-lookup"><span data-stu-id="cba4b-119">Passing Matrix Indices to Direct3D</span></span>

<span data-ttu-id="cba4b-120">Gli indici di matrice globale possono essere passati a Direct3D usando le dichiarazioni vertex shader legacy-FVF-or.</span><span class="sxs-lookup"><span data-stu-id="cba4b-120">World matrix indices can be passed to Direct3D by using legacy vertex shaders - FVF - or declarations.</span></span>

<span data-ttu-id="cba4b-121">Nell'esempio di codice seguente viene illustrato come utilizzare vertex shader legacy.</span><span class="sxs-lookup"><span data-stu-id="cba4b-121">The code example below shows how to use legacy vertex shaders.</span></span>


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
};
    
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZB2 | D3DFVF_LASTBETA_UBYTE4 |
                             D3DFVF_NORMAL);
```



<span data-ttu-id="cba4b-122">Quando viene usato un vertex shader legacy, gli indici di matrice vengono passati insieme alle posizioni dei vertici usando i \_ flag XYZBn di D3DFVF.</span><span class="sxs-lookup"><span data-stu-id="cba4b-122">When a legacy vertex shader is used, matrix indices are passed together with vertex positions using D3DFVF\_XYZBn flags.</span></span> <span data-ttu-id="cba4b-123">Gli indici di matrice vengono passati come byte all'interno di un DWORD e devono essere presenti immediatamente dopo l'ultimo peso del vertice.</span><span class="sxs-lookup"><span data-stu-id="cba4b-123">Matrix indices are passed as bytes inside a DWORD and must be present immediately after the last vertex weight.</span></span> <span data-ttu-id="cba4b-124">Le ponderazioni del vertice vengono passate anche usando D3DFVF \_ XYZBn.</span><span class="sxs-lookup"><span data-stu-id="cba4b-124">Vertex weights are also passed using D3DFVF\_XYZBn.</span></span> <span data-ttu-id="cba4b-125">Un valore DWORD compresso contiene Index3, index2, index1 e index0, dove index0 si trova nel byte più basso del valore DWORD.</span><span class="sxs-lookup"><span data-stu-id="cba4b-125">A packed DWORD contains index3, index2, index1, and index0, where index0 is located in the lowest byte of the DWORD.</span></span> <span data-ttu-id="cba4b-126">Il numero di indici di matrice globale usati è uguale al numero passato al numero di matrici usate per la fusione come definito da [**D3DRS \_ VERTEXBLEND**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="cba4b-126">The number of used world-matrix indices is equal to the number passed to the number of matrices used for blending as defined by [**D3DRS\_VERTEXBLEND**](./d3drenderstatetype.md).</span></span>

<span data-ttu-id="cba4b-127">Quando viene usata una dichiarazione, D3DVSDE \_ BLENDINDICES definisce il registro dei vertici di input da cui ottenere gli indici della matrice.</span><span class="sxs-lookup"><span data-stu-id="cba4b-127">When a declaration is used, D3DVSDE\_BLENDINDICES defines the input vertex register to get matrix indices from.</span></span> <span data-ttu-id="cba4b-128">Gli indici della matrice devono essere passati come D3DVSDT \_ UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="cba4b-128">Matrix indices must be passed as D3DVSDT\_UBYTE4.</span></span>

<span data-ttu-id="cba4b-129">Nell'esempio di codice seguente viene illustrato come utilizzare le dichiarazioni.</span><span class="sxs-lookup"><span data-stu-id="cba4b-129">The code example below shows how to use declarations.</span></span> <span data-ttu-id="cba4b-130">Si noti che l'ordine dei componenti non è più importante a meno che non si utilizzi un vertex shader a funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="cba4b-130">Note that the order of the components is no longer important unless using a fixed-function vertex shader.</span></span>

<span data-ttu-id="cba4b-131">Di seguito è illustrata la dichiarazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="cba4b-131">Here is the vertex declaration.</span></span>


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
}
```



<span data-ttu-id="cba4b-132">Di seguito è illustrata la dichiarazione Register corrispondente.</span><span class="sxs-lookup"><span data-stu-id="cba4b-132">Here is the corresponding register declaration.</span></span>


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT1, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDWEIGHT, 0 },
    { 0, 16, D3DDECLTYPE_UBYTE4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDINDICES, 0 },
    { 0, 20, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    D3DDECL_END()
};
```



## <a name="related-topics"></a><span data-ttu-id="cba4b-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cba4b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cba4b-134">Unione di vertici indicizzati</span><span class="sxs-lookup"><span data-stu-id="cba4b-134">Indexed Vertex Blending</span></span>](indexed-vertex-blending.md)
</dt> </dl>

 

 
