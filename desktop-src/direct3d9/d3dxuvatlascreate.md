---
description: 'Funzione D3DXUVAtlasCreate: consente di creare un at atlas UV per una mesh.'
ms.assetid: 70256990-b177-451e-b42a-84799fdc2a17
title: Funzione D3DXUVAtlasCreate (D3DX9Mesh.h)
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
ms.openlocfilehash: 5f382e7d59f3a5b5db8ba3cfd65ba6cc1a11e86d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117829"
---
# <a name="d3dxuvatlascreate-function"></a><span data-ttu-id="b0ba8-103">Funzione D3DXUVAtlasCreate</span><span class="sxs-lookup"><span data-stu-id="b0ba8-103">D3DXUVAtlasCreate function</span></span>

<span data-ttu-id="b0ba8-104">Creare un at atlas UV per una mesh.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0ba8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0ba8-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="b0ba8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0ba8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0ba8-107">*pMesh* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="b0ba8-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="b0ba8-109">Puntatore a una mesh di input (vedere [**ID3DXMesh)**](id3dxmesh.md)che contiene la geometria dell'oggetto per il calcolo dell'at atlas.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="b0ba8-110">Come minimo, la mesh deve contenere dati di posizione e coordinate di trama 2D.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-111">*dwMaxChartNumber* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-112">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0ba8-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0ba8-113">Numero massimo di grafici in cui partizionare la mesh.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="b0ba8-114">Vedere le osservazioni sulle modalità di partizionamento.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="b0ba8-115">Usare 0 per indicare a D3DX che l'atlas deve essere parametrizzato in base all'estensione.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-116">*fMaxStretch* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0ba8-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0ba8-118">Quantità di estensione consentita.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-118">The amount of stretching allowed.</span></span> <span data-ttu-id="b0ba8-119">0 indica che non è consentita alcuna estensione, 1 indica che è possibile usare qualsiasi quantità di estensione.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-120">*dwWidth* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-120">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-121">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0ba8-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0ba8-122">Larghezza della trama.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-122">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-123">*dwHeight* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-123">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-124">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0ba8-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0ba8-125">Altezza della trama.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-125">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-126">*fGutter* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-126">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-127">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0ba8-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0ba8-128">Distanza minima, in texel, tra due grafici sull'at atlas.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-128">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="b0ba8-129">Il margine viene sempre ridimensionato in base alla larghezza. Pertanto, se viene usata una distanza di 2,5 su una trama 512x512, la distanza minima tra due grafici è 2,5/512,0 texel.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-129">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-130">*dwTextureIndex* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-130">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0ba8-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0ba8-132">Indice delle coordinate della trama in base zero che identifica il set di coordinate di trama da usare.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-132">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-133">*pdwAdjacency* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-133">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-134">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b0ba8-134">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b0ba8-135">Puntatore a una matrice di dati di adienza.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-135">A pointer to an array of adjacency data.</span></span> <span data-ttu-id="b0ba8-136">con 3 DWORD per ogni viso, che indica quali triangoli sono adiacenti tra loro (vedere [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span><span class="sxs-lookup"><span data-stu-id="b0ba8-136">with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-137">*pdwFalseEdges*</span><span class="sxs-lookup"><span data-stu-id="b0ba8-137">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="b0ba8-138">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b0ba8-138">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b0ba8-139">Matrice con 3 DWORD per ogni viso.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-139">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="b0ba8-140">Ogni viso indica se un bordo è falso o meno.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-140">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="b0ba8-141">Un bordo non falso è indicato da -1, un bordo falso è indicato da qualsiasi altro valore.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-141">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="b0ba8-142">Ciò consente la parametrizzazione di una mesh di quad in cui i bordi al centro di ogni quad non verranno tagliati.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-142">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-143">*pfIMTArray* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-143">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-144">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0ba8-144">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b0ba8-145">Puntatore a una matrice di tensori delle metriche integrati che descrive come estendere un triangolo (vedere [IntegratedMetricTensor).](using-uvatlas.md)</span><span class="sxs-lookup"><span data-stu-id="b0ba8-145">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-146">*pCallback* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-146">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-147">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="b0ba8-147">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="b0ba8-148">Puntatore a una funzione di callback (vedere [LPD3DXUVATLASCB)](lpd3dxuvatlascb.md)utile per monitorare lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-148">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-149">*fCallbackFrequency* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-149">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-150">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0ba8-150">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0ba8-151">Specificare la frequenza con cui D3DX chiamerà il callback. un valore predefinito ragionevole è 0,0001f.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-151">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-152">*pUserContent* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-152">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-153">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0ba8-153">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0ba8-154">Puntatore a un valore definito dall'utente passato alla funzione di callback. utilizzato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni di contesto per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-154">Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-155">*dwOptions* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-155">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-156">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0ba8-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0ba8-157">Specificare la qualità dei grafici generati.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-157">Specify the quality of the charts generated.</span></span> <span data-ttu-id="b0ba8-158">Vedere [**D3DXUVATLAS.**](./d3dxuvatlas.md)</span><span class="sxs-lookup"><span data-stu-id="b0ba8-158">See [**D3DXUVATLAS**](./d3dxuvatlas.md).</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-159">*ppMeshOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-159">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-160">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0ba8-160">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="b0ba8-161">Puntatore alla mesh creata con l'atlas (vedere [**ID3DXMesh).**](id3dxmesh.md)</span><span class="sxs-lookup"><span data-stu-id="b0ba8-161">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-162">*PpFacePartitioning* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-162">*ppFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-163">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0ba8-163">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b0ba8-164">Puntatore a una matrice dei dati finali di partizionamento viso.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-164">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="b0ba8-165">Ogni elemento contiene un valore DWORD per ogni viso (vedere [**ID3DXBuffer**](id3dxbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="b0ba8-165">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-166">*ppVertexRemapArray* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-166">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-167">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0ba8-167">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b0ba8-168">Puntatore a una matrice di vertici mappati.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-168">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="b0ba8-169">Ogni elemento della matrice identifica il vertice originale da cui deriva ogni vertice finale (se il vertice è stato suddiviso durante il mapping).</span><span class="sxs-lookup"><span data-stu-id="b0ba8-169">Each array element identifies the original vertex that each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="b0ba8-170">Ogni elemento della matrice contiene un valore DWORD per vertice.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-170">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-171">*pfMaxStretchOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-171">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-172">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0ba8-172">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b0ba8-173">Puntatore al valore di estensione massimo generato dall'algoritmo Atlas.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-173">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="b0ba8-174">L'intervallo è compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-174">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="b0ba8-175">*pdwNumChartsOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="b0ba8-175">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0ba8-176">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b0ba8-176">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b0ba8-177">Puntatore al numero di grafici creati dall'algoritmo Atlas.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-177">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="b0ba8-178">Se dwMaxChartNumber è troppo basso, questo parametro restituirà il numero minimo di grafici necessari per creare un at atlas.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-178">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0ba8-179">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0ba8-179">Return value</span></span>

<span data-ttu-id="b0ba8-180">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b0ba8-180">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b0ba8-181">Se la funzione ha esito positivo, il valore restituito è D3D OK; in caso contrario, il valore \_ è D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-181">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0ba8-182">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0ba8-182">Remarks</span></span>

<span data-ttu-id="b0ba8-183">D3DXUVAtlasCreate può partizionare la geometria della mesh in due modi:</span><span class="sxs-lookup"><span data-stu-id="b0ba8-183">D3DXUVAtlasCreate can partition mesh geometry two ways:</span></span>

-   <span data-ttu-id="b0ba8-184">In base al numero di grafici</span><span class="sxs-lookup"><span data-stu-id="b0ba8-184">Based on the number of charts</span></span>
-   <span data-ttu-id="b0ba8-185">In base all'estensione massima consentita.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-185">Based on the maximum allowed stretch.</span></span> <span data-ttu-id="b0ba8-186">Se l'estensione massima consentita è 0, è probabile che ogni triangolo si trova nel proprio grafico.</span><span class="sxs-lookup"><span data-stu-id="b0ba8-186">If the maximum allowed stretch is 0, each triangle will likely be in its own chart.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0ba8-187">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0ba8-187">Requirements</span></span>



| <span data-ttu-id="b0ba8-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0ba8-188">Requirement</span></span> | <span data-ttu-id="b0ba8-189">Valore</span><span class="sxs-lookup"><span data-stu-id="b0ba8-189">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0ba8-190">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b0ba8-190">Header</span></span><br/>  | <dl> <span data-ttu-id="b0ba8-191"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="b0ba8-191"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b0ba8-192">Libreria</span><span class="sxs-lookup"><span data-stu-id="b0ba8-192">Library</span></span><br/> | <dl> <span data-ttu-id="b0ba8-193"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0ba8-193"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b0ba8-194">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0ba8-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0ba8-195">Funzioni UVAtlas</span><span class="sxs-lookup"><span data-stu-id="b0ba8-195">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="b0ba8-196">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="b0ba8-196">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
