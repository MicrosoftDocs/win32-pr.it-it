---
description: Creare un Atlante UV per una rete mesh.
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: Funzione D3DXUVAtlasCreate (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasCreate
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 814f213b0195b0922270d0548d8b5fd4c48fb3e3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322468"
---
# <a name="d3dxuvatlascreate-function"></a><span data-ttu-id="cdd04-103">D3DXUVAtlasCreate (funzione)</span><span class="sxs-lookup"><span data-stu-id="cdd04-103">D3DXUVAtlasCreate function</span></span>

<span data-ttu-id="cdd04-104">Creare un Atlante UV per una rete mesh.</span><span class="sxs-lookup"><span data-stu-id="cdd04-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdd04-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cdd04-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasCreate(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        UINT            dwWidth,
  _In_        UINT            dwHeight,
  _In_        FLOAT           fGutter,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContext,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    *ppFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a><span data-ttu-id="cdd04-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cdd04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdd04-107">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="cdd04-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="cdd04-109">Puntatore a una mesh di input (vedere [**ID3DXMesh**](id3dxmesh.md)) che contiene la geometria dell'oggetto per il calcolo dell'Atlante.</span><span class="sxs-lookup"><span data-stu-id="cdd04-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="cdd04-110">Come minimo, la mesh deve contenere dati sulla posizione e coordinate di trama 2D.</span><span class="sxs-lookup"><span data-stu-id="cdd04-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-111">*dwMaxChartNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cdd04-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cdd04-113">Numero massimo di grafici in cui partizionare la mesh.</span><span class="sxs-lookup"><span data-stu-id="cdd04-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="cdd04-114">Vedere la sezione Osservazioni sulle modalità di partizionamento.</span><span class="sxs-lookup"><span data-stu-id="cdd04-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="cdd04-115">Usare 0 per indicare a D3DX che l'Atlante deve essere parametrizzato in base all'estensione.</span><span class="sxs-lookup"><span data-stu-id="cdd04-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-116">*fMaxStretch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cdd04-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cdd04-118">Quantità di estensione consentita.</span><span class="sxs-lookup"><span data-stu-id="cdd04-118">The amount of stretching allowed.</span></span> <span data-ttu-id="cdd04-119">0 indica che non è consentita l'estensione. 1 indica che è possibile utilizzare qualsiasi estensione.</span><span class="sxs-lookup"><span data-stu-id="cdd04-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-120">*dwWidth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-120">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cdd04-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cdd04-122">Spessore trama.</span><span class="sxs-lookup"><span data-stu-id="cdd04-122">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-123">*dwHeight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-123">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-124">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cdd04-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cdd04-125">Altezza trama.</span><span class="sxs-lookup"><span data-stu-id="cdd04-125">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-126">*fGutter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-126">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-127">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cdd04-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cdd04-128">Distanza minima, in Texel, tra due grafici nell'Atlante.</span><span class="sxs-lookup"><span data-stu-id="cdd04-128">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="cdd04-129">La gronda viene sempre ridimensionata in base alla larghezza; Se quindi si usa una gronda di 2,5 su una trama 512x512, la distanza minima tra due grafici è 2,5/512,0 Texels.</span><span class="sxs-lookup"><span data-stu-id="cdd04-129">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-130">*dwTextureIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-130">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cdd04-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cdd04-132">Indice di coordinate di trama in base zero che identifica il set di coordinate di trama da usare.</span><span class="sxs-lookup"><span data-stu-id="cdd04-132">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-133">*pdwAdjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-133">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-134">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cdd04-134">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cdd04-135">Puntatore a una matrice di dati adiacenza.</span><span class="sxs-lookup"><span data-stu-id="cdd04-135">A pointer to an array of adjacency data.</span></span> <span data-ttu-id="cdd04-136">con 3 DWORD per faccia, che indicano i triangoli adiacenti tra loro (vedere [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span><span class="sxs-lookup"><span data-stu-id="cdd04-136">with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-137">*pdwFalseEdges*</span><span class="sxs-lookup"><span data-stu-id="cdd04-137">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="cdd04-138">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cdd04-138">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cdd04-139">Matrice con 3 DWORD per faccia.</span><span class="sxs-lookup"><span data-stu-id="cdd04-139">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="cdd04-140">Ogni volto indica se un bordo è false o no.</span><span class="sxs-lookup"><span data-stu-id="cdd04-140">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="cdd04-141">Un bordo non false è indicato da-1, mentre un bordo false è indicato da un altro valore.</span><span class="sxs-lookup"><span data-stu-id="cdd04-141">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="cdd04-142">In questo modo viene abilitata la parametrizzazione di una mesh di quad in cui i bordi al centro di ogni quad non vengono tagliati.</span><span class="sxs-lookup"><span data-stu-id="cdd04-142">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-143">*pfIMTArray* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-143">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-144">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdd04-144">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cdd04-145">Puntatore a una matrice di tensori metrici integrati che descrive come estendere un triangolo (vedere [IntegratedMetricTensor](using-uvatlas.md)).</span><span class="sxs-lookup"><span data-stu-id="cdd04-145">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-146">*pCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-146">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-147">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="cdd04-147">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="cdd04-148">Puntatore a una funzione di callback (vedere [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) utile per il monitoraggio dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="cdd04-148">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-149">*fCallbackFrequency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-149">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-150">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cdd04-150">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cdd04-151">Specificare la frequenza con cui D3DX chiamerà il callback; un valore predefinito ragionevole è 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="cdd04-151">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-152">*pUserContent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-152">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-153">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cdd04-153">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cdd04-154">Puntatore a un valore definito dall'utente che viene passato alla funzione di callback; usato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="cdd04-154">Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-155">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-155">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-156">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cdd04-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cdd04-157">Consente di specificare la qualità dei grafici generati.</span><span class="sxs-lookup"><span data-stu-id="cdd04-157">Specify the quality of the charts generated.</span></span> <span data-ttu-id="cdd04-158">Vedere [**D3DXUVATLAS**](./d3dxuvatlas.md).</span><span class="sxs-lookup"><span data-stu-id="cdd04-158">See [**D3DXUVATLAS**](./d3dxuvatlas.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-159">*ppMeshOut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-159">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-160">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdd04-160">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="cdd04-161">Puntatore alla mesh creata con Atlas (vedere [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="cdd04-161">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-162">*ppFacePartitioning* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-162">*ppFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-163">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdd04-163">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cdd04-164">Puntatore a una matrice dei dati finali di partizionamento delle facce.</span><span class="sxs-lookup"><span data-stu-id="cdd04-164">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="cdd04-165">Ogni elemento contiene un valore DWORD per faccia (vedere [**ID3DXBuffer**](id3dxbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="cdd04-165">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-166">*ppVertexRemapArray* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-166">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-167">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdd04-167">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cdd04-168">Puntatore a una matrice di vertici di cui è stato eseguito il mapping.</span><span class="sxs-lookup"><span data-stu-id="cdd04-168">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="cdd04-169">Ogni elemento della matrice identifica il vertice originale da cui provengono ogni vertice finale (se il vertice è stato suddiviso durante la modifica del mapping).</span><span class="sxs-lookup"><span data-stu-id="cdd04-169">Each array element identifies the original vertex that each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="cdd04-170">Ogni elemento di matrice contiene un valore DWORD per vertice.</span><span class="sxs-lookup"><span data-stu-id="cdd04-170">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-171">*pfMaxStretchOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-171">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-172">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdd04-172">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cdd04-173">Puntatore al valore di estensione massimo generato dall'algoritmo Atlas.</span><span class="sxs-lookup"><span data-stu-id="cdd04-173">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="cdd04-174">L'intervallo è compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="cdd04-174">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="cdd04-175">*pdwNumChartsOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cdd04-175">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdd04-176">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cdd04-176">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cdd04-177">Puntatore al numero di grafici creato dall'algoritmo Atlas.</span><span class="sxs-lookup"><span data-stu-id="cdd04-177">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="cdd04-178">Se dwMaxChartNumber è troppo basso, questo parametro restituirà il numero minimo di grafici necessari per creare un Atlante.</span><span class="sxs-lookup"><span data-stu-id="cdd04-178">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdd04-179">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cdd04-179">Return value</span></span>

<span data-ttu-id="cdd04-180">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cdd04-180">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cdd04-181">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. in caso contrario, il valore è D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="cdd04-181">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdd04-182">Commenti</span><span class="sxs-lookup"><span data-stu-id="cdd04-182">Remarks</span></span>

<span data-ttu-id="cdd04-183">D3DXUVAtlasCreate può partizionare la geometria mesh in due modi:</span><span class="sxs-lookup"><span data-stu-id="cdd04-183">D3DXUVAtlasCreate can partition mesh geometry two ways:</span></span>

-   <span data-ttu-id="cdd04-184">In base al numero di grafici</span><span class="sxs-lookup"><span data-stu-id="cdd04-184">Based on the number of charts</span></span>
-   <span data-ttu-id="cdd04-185">In base all'estensione massima consentita.</span><span class="sxs-lookup"><span data-stu-id="cdd04-185">Based on the maximum allowed stretch.</span></span> <span data-ttu-id="cdd04-186">Se l'estensione massima consentita è 0, è probabile che ogni triangolo si trovi in un grafico.</span><span class="sxs-lookup"><span data-stu-id="cdd04-186">If the maximum allowed stretch is 0, each triangle will likely be in its own chart.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdd04-187">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdd04-187">Requirements</span></span>



| <span data-ttu-id="cdd04-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdd04-188">Requirement</span></span> | <span data-ttu-id="cdd04-189">Valore</span><span class="sxs-lookup"><span data-stu-id="cdd04-189">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd04-190">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cdd04-190">Header</span></span><br/>  | <dl> <span data-ttu-id="cdd04-191"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdd04-191"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cdd04-192">Libreria</span><span class="sxs-lookup"><span data-stu-id="cdd04-192">Library</span></span><br/> | <dl> <span data-ttu-id="cdd04-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cdd04-193"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cdd04-194">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdd04-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd04-195">Funzioni UVAtlas</span><span class="sxs-lookup"><span data-stu-id="cdd04-195">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="cdd04-196">[Strumento Command-Line UV Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="cdd04-196">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
