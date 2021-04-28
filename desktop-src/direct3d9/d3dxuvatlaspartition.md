---
description: 'Funzione D3DXUVAtlasPartition: crea un at atlas UV per una mesh.'
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: Funzione D3DXUVAtlasPartition (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPartition
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 63df6bbcc1b811b9617796bc6e7e51af2dfdca56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117799"
---
# <a name="d3dxuvatlaspartition-function"></a><span data-ttu-id="6c936-103">Funzione D3DXUVAtlasPartition</span><span class="sxs-lookup"><span data-stu-id="6c936-103">D3DXUVAtlasPartition function</span></span>

<span data-ttu-id="6c936-104">Creare un at atlas UV per una mesh.</span><span class="sxs-lookup"><span data-stu-id="6c936-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c936-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c936-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasPartition(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContent,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    pFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
              LPD3DXBUFFER    *ppPartitionResultAdjacency,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a><span data-ttu-id="6c936-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c936-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c936-107">*pMesh* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6c936-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c936-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="6c936-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="6c936-109">Puntatore a una mesh di input (vedere [**ID3DXMesh)**](id3dxmesh.md)che contiene la geometria dell'oggetto per il calcolo dell'at atlas.</span><span class="sxs-lookup"><span data-stu-id="6c936-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) that contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="6c936-110">Come minimo, la mesh deve contenere dati di posizione e coordinate di trama 2D.</span><span class="sxs-lookup"><span data-stu-id="6c936-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="6c936-111">*dwMaxChartNumber* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6c936-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c936-112">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c936-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c936-113">Numero massimo di grafici in cui partizionare la mesh.</span><span class="sxs-lookup"><span data-stu-id="6c936-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="6c936-114">Vedere le osservazioni sulle modalità di partizionamento.</span><span class="sxs-lookup"><span data-stu-id="6c936-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="6c936-115">Usare 0 per indicare a D3DX che l'atlas deve essere parametrizzato in base all'estensione.</span><span class="sxs-lookup"><span data-stu-id="6c936-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="6c936-116">*fMaxStretch* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6c936-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c936-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c936-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c936-118">Quantità di estensione consentita.</span><span class="sxs-lookup"><span data-stu-id="6c936-118">The amount of stretching allowed.</span></span> <span data-ttu-id="6c936-119">0 indica che non è consentita alcuna estensione, 1 indica che è possibile usare qualsiasi quantità di estensione.</span><span class="sxs-lookup"><span data-stu-id="6c936-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="6c936-120">*dwTextureIndex* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6c936-120">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c936-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c936-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c936-122">Indice delle coordinate della trama in base zero che identifica il set di coordinate di trama da usare.</span><span class="sxs-lookup"><span data-stu-id="6c936-122">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="6c936-123">*pdwAdjacency* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6c936-123">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c936-124">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6c936-124">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6c936-125">Puntatore a una matrice di dati di adiacenza con 3 DWORD per viso, che indica quali triangoli sono adiacenti l'uno all'altro (vedere [**ID3DXBaseMesh::GenerateAdjacency).**](id3dxbasemesh--generateadjacency.md)</span><span class="sxs-lookup"><span data-stu-id="6c936-125">A pointer to an array of adjacency data with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6c936-126">*pdwFalseEdges*</span><span class="sxs-lookup"><span data-stu-id="6c936-126">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="6c936-127">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="6c936-127">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6c936-128">Matrice con 3 DWORD per viso.</span><span class="sxs-lookup"><span data-stu-id="6c936-128">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="6c936-129">Ogni viso indica se un bordo è false o meno.</span><span class="sxs-lookup"><span data-stu-id="6c936-129">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="6c936-130">Un bordo non false è indicato da -1, un bordo falso è indicato da qualsiasi altro valore.</span><span class="sxs-lookup"><span data-stu-id="6c936-130">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="6c936-131">Ciò consente la parametrizzazione di una mesh di quad in cui i bordi al centro di ogni quad non verranno tagliati.</span><span class="sxs-lookup"><span data-stu-id="6c936-131">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="6c936-132">*pfIMTArray* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6c936-132">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c936-133">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c936-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6c936-134">Puntatore a una matrice di tensori delle metriche integrati che descrive come estendere un triangolo (vedere [IntegratedMetricTensor).](using-uvatlas.md)</span><span class="sxs-lookup"><span data-stu-id="6c936-134">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6c936-135">*pCallback* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6c936-135">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c936-136">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="6c936-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="6c936-137">Puntatore a una funzione di callback (vedere [LPD3DXUVATLASCB)](lpd3dxuvatlascb.md)utile per monitorare lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="6c936-137">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="6c936-138">*fCallbackFrequency* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6c936-138">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c936-139">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c936-139">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c936-140">Specificare la frequenza con cui D3DX chiamerà il callback. un valore predefinito ragionevole è 0,0001f.</span><span class="sxs-lookup"><span data-stu-id="6c936-140">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="6c936-141">*pUserContent* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6c936-141">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c936-142">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c936-142">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c936-143">Puntatore a un valore definito dall'utente passato alla funzione di callback. in genere usato da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="6c936-143">Pointer to a user-defined value that is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="6c936-144">*dwOptions* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6c936-144">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c936-145">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6c936-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6c936-146">Specificare la qualità dei grafici generati combinando uno o più flag [**D3DXUVATLAS.**](./d3dxuvatlas.md)</span><span class="sxs-lookup"><span data-stu-id="6c936-146">Specify the quality of the charts generated by combining one or more [**D3DXUVATLAS**](./d3dxuvatlas.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="6c936-147">*ppMeshOut* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6c936-147">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c936-148">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c936-148">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="6c936-149">Puntatore alla mesh creata con l'at atlas (vedere [**ID3DXMesh).**](id3dxmesh.md)</span><span class="sxs-lookup"><span data-stu-id="6c936-149">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6c936-150">*pFacePartitioning* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="6c936-150">*pFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c936-151">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="6c936-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="6c936-152">Puntatore a una matrice dei dati finali di partizionamento del viso.</span><span class="sxs-lookup"><span data-stu-id="6c936-152">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="6c936-153">Ogni elemento contiene un valore DWORD per ogni viso (vedere [**ID3DXBuffer**](id3dxbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="6c936-153">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6c936-154">*ppVertexRemapArray* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="6c936-154">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c936-155">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c936-155">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6c936-156">Puntatore a una matrice di vertici di cui è stato ridefinito il mapping.</span><span class="sxs-lookup"><span data-stu-id="6c936-156">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="6c936-157">Ogni elemento della matrice identifica il vertice originale da cui deriva ogni vertice finale (se il vertice è stato suddiviso durante il nuovo mapping).</span><span class="sxs-lookup"><span data-stu-id="6c936-157">Each array element identifies the original vertex each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="6c936-158">Ogni elemento della matrice contiene un valore DWORD per vertice.</span><span class="sxs-lookup"><span data-stu-id="6c936-158">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="6c936-159">*ppPartitionResultAdjacency*</span><span class="sxs-lookup"><span data-stu-id="6c936-159">*ppPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="6c936-160">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c936-160">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6c936-161">Indirizzo di un puntatore a [**un'interfaccia ID3DXBuffer.**](id3dxbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="6c936-161">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="6c936-162">Questo buffer conterrà una matrice di tre DWORD per ogni viso che specifica i tre elementi adiacenti per ogni viso nella mesh di output.</span><span class="sxs-lookup"><span data-stu-id="6c936-162">This buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="6c936-163">Questo parametro non deve essere **NULL** perché la chiamata successiva a D3DXUVAtlasPack() lo richiede.</span><span class="sxs-lookup"><span data-stu-id="6c936-163">This parameter must not be **NULL**, because the subsequent call to D3DXUVAtlasPack() requires it.</span></span>

</dd> <dt>

<span data-ttu-id="6c936-164">*pfMaxStretchOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="6c936-164">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c936-165">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c936-165">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6c936-166">Puntatore al valore di estensione massimo generato dall'algoritmo Atlas.</span><span class="sxs-lookup"><span data-stu-id="6c936-166">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="6c936-167">L'intervallo è compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="6c936-167">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="6c936-168">*pdwNumChartsOut* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="6c936-168">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c936-169">Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c936-169">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6c936-170">Puntatore al numero di grafici creati dall'algoritmo Atlas.</span><span class="sxs-lookup"><span data-stu-id="6c936-170">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="6c936-171">Se dwMaxChartNumber è troppo basso, questo parametro restituirà il numero minimo di grafici necessari per creare un atlas.</span><span class="sxs-lookup"><span data-stu-id="6c936-171">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c936-172">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c936-172">Return value</span></span>

<span data-ttu-id="6c936-173">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6c936-173">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6c936-174">Se la funzione ha esito positivo, il valore restituito è D3D OK; in caso contrario, il valore \_ è D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6c936-174">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c936-175">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c936-175">Remarks</span></span>

<span data-ttu-id="6c936-176">D3DXUVAtlasPartition è simile a [**D3DXUVAtlasCreate,**](d3dxuvatlascreate.md)ad eccezione del fatto che D3DXUVAtlasPartition non esegue il passaggio di creazione del pacchetto finale.</span><span class="sxs-lookup"><span data-stu-id="6c936-176">D3DXUVAtlasPartition is similar to [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), except that D3DXUVAtlasPartition does not performing the final packing step.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c936-177">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c936-177">Requirements</span></span>



| <span data-ttu-id="6c936-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c936-178">Requirement</span></span> | <span data-ttu-id="6c936-179">Valore</span><span class="sxs-lookup"><span data-stu-id="6c936-179">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c936-180">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c936-180">Header</span></span><br/>  | <dl> <span data-ttu-id="6c936-181"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="6c936-181"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="6c936-182">Libreria</span><span class="sxs-lookup"><span data-stu-id="6c936-182">Library</span></span><br/> | <dl> <span data-ttu-id="6c936-183"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c936-183"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6c936-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c936-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c936-185">Funzioni UVAtlas</span><span class="sxs-lookup"><span data-stu-id="6c936-185">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="6c936-186">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="6c936-186">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
