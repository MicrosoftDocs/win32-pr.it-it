---
description: Creare un Atlante UV per una rete mesh.
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: Funzione D3DXUVAtlasPartition (D3DX9Mesh. h)
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
ms.openlocfilehash: 707a503832a4fd66ab2e8d9346587d11544a885c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322566"
---
# <a name="d3dxuvatlaspartition-function"></a><span data-ttu-id="59773-103">D3DXUVAtlasPartition (funzione)</span><span class="sxs-lookup"><span data-stu-id="59773-103">D3DXUVAtlasPartition function</span></span>

<span data-ttu-id="59773-104">Creare un Atlante UV per una rete mesh.</span><span class="sxs-lookup"><span data-stu-id="59773-104">Create a UV atlas for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="59773-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59773-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="59773-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="59773-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59773-107">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59773-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59773-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="59773-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="59773-109">Puntatore a una mesh di input (vedere [**ID3DXMesh**](id3dxmesh.md)) che contiene la geometria dell'oggetto per il calcolo dell'Atlante.</span><span class="sxs-lookup"><span data-stu-id="59773-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) that contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="59773-110">Come minimo, la mesh deve contenere dati sulla posizione e coordinate di trama 2D.</span><span class="sxs-lookup"><span data-stu-id="59773-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="59773-111">*dwMaxChartNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59773-111">*dwMaxChartNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59773-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59773-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59773-113">Numero massimo di grafici in cui partizionare la mesh.</span><span class="sxs-lookup"><span data-stu-id="59773-113">The maximum number of charts to partition the mesh into.</span></span> <span data-ttu-id="59773-114">Vedere la sezione Osservazioni sulle modalità di partizionamento.</span><span class="sxs-lookup"><span data-stu-id="59773-114">See remarks about the partitioning modes.</span></span> <span data-ttu-id="59773-115">Usare 0 per indicare a D3DX che l'Atlante deve essere parametrizzato in base all'estensione.</span><span class="sxs-lookup"><span data-stu-id="59773-115">Use 0 to tell D3DX that the atlas should be parameterized based on stretch.</span></span>

</dd> <dt>

<span data-ttu-id="59773-116">*fMaxStretch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59773-116">*fMaxStretch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59773-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59773-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59773-118">Quantità di estensione consentita.</span><span class="sxs-lookup"><span data-stu-id="59773-118">The amount of stretching allowed.</span></span> <span data-ttu-id="59773-119">0 indica che non è consentita l'estensione. 1 indica che è possibile utilizzare qualsiasi estensione.</span><span class="sxs-lookup"><span data-stu-id="59773-119">0 means no stretching is allowed, 1 means any amount of stretching can be used.</span></span>

</dd> <dt>

<span data-ttu-id="59773-120">*dwTextureIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59773-120">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59773-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59773-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59773-122">Indice di coordinate di trama in base zero che identifica il set di coordinate di trama da usare.</span><span class="sxs-lookup"><span data-stu-id="59773-122">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="59773-123">*pdwAdjacency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59773-123">*pdwAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59773-124">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="59773-124">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="59773-125">Puntatore a una matrice di dati adiacenza con 3 DWORD per volto, che indica quali triangoli sono adiacenti tra loro (vedere [**ID3DXBaseMesh:: GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span><span class="sxs-lookup"><span data-stu-id="59773-125">A pointer to an array of adjacency data with 3 DWORDs per face, indicating which triangles are adjacent to each other (see [**ID3DXBaseMesh::GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)).</span></span>

</dd> <dt>

<span data-ttu-id="59773-126">*pdwFalseEdges*</span><span class="sxs-lookup"><span data-stu-id="59773-126">*pdwFalseEdges*</span></span> 
</dt> <dd>

<span data-ttu-id="59773-127">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="59773-127">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="59773-128">Matrice con 3 DWORD per faccia.</span><span class="sxs-lookup"><span data-stu-id="59773-128">An array with 3 DWORDS per face.</span></span> <span data-ttu-id="59773-129">Ogni volto indica se un bordo è false o no.</span><span class="sxs-lookup"><span data-stu-id="59773-129">Each face indicates if an edge is false or not.</span></span> <span data-ttu-id="59773-130">Un bordo non false è indicato da-1, mentre un bordo false è indicato da un altro valore.</span><span class="sxs-lookup"><span data-stu-id="59773-130">A non-false edge is indicated by -1, a false edge is indicated by any other value.</span></span> <span data-ttu-id="59773-131">In questo modo viene abilitata la parametrizzazione di una mesh di quad in cui i bordi al centro di ogni quad non vengono tagliati.</span><span class="sxs-lookup"><span data-stu-id="59773-131">This enables the parameterization of a mesh of quads where the edges down the middle of each quad will not be cut.</span></span>

</dd> <dt>

<span data-ttu-id="59773-132">*pfIMTArray* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59773-132">*pfIMTArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59773-133">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="59773-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="59773-134">Puntatore a una matrice di tensori metrici integrati che descrive come estendere un triangolo (vedere [IntegratedMetricTensor](using-uvatlas.md)).</span><span class="sxs-lookup"><span data-stu-id="59773-134">A pointer to an array of integrated metric tensors that describes how to stretch a triangle (see [IntegratedMetricTensor](using-uvatlas.md)).</span></span>

</dd> <dt>

<span data-ttu-id="59773-135">*pCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59773-135">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59773-136">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="59773-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="59773-137">Puntatore a una funzione di callback (vedere [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) utile per il monitoraggio dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="59773-137">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="59773-138">*fCallbackFrequency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59773-138">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59773-139">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59773-139">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59773-140">Specificare la frequenza con cui D3DX chiamerà il callback; un valore predefinito ragionevole è 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="59773-140">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="59773-141">*pUserContent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59773-141">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59773-142">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59773-142">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59773-143">Puntatore a un valore definito dall'utente che viene passato alla funzione di callback; usato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="59773-143">Pointer to a user-defined value that is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="59773-144">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59773-144">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59773-145">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59773-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59773-146">Consente di specificare la qualità dei grafici generati combinando uno o più flag [**D3DXUVATLAS**](./d3dxuvatlas.md) .</span><span class="sxs-lookup"><span data-stu-id="59773-146">Specify the quality of the charts generated by combining one or more [**D3DXUVATLAS**](./d3dxuvatlas.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="59773-147">*ppMeshOut* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59773-147">*ppMeshOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59773-148">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="59773-148">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="59773-149">Puntatore alla mesh creata con Atlas (vedere [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="59773-149">Pointer to the created mesh with the atlas (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> <dt>

<span data-ttu-id="59773-150">*pFacePartitioning* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="59773-150">*pFacePartitioning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59773-151">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="59773-151">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="59773-152">Puntatore a una matrice dei dati finali di partizionamento delle facce.</span><span class="sxs-lookup"><span data-stu-id="59773-152">A pointer to an array of the final face-partitioning data.</span></span> <span data-ttu-id="59773-153">Ogni elemento contiene un valore DWORD per faccia (vedere [**ID3DXBuffer**](id3dxbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="59773-153">Each element contains one DWORD per face (see [**ID3DXBuffer**](id3dxbuffer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="59773-154">*ppVertexRemapArray* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="59773-154">*ppVertexRemapArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59773-155">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="59773-155">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="59773-156">Puntatore a una matrice di vertici di cui è stato eseguito il mapping.</span><span class="sxs-lookup"><span data-stu-id="59773-156">A pointer to an array of remapped vertices.</span></span> <span data-ttu-id="59773-157">Ogni elemento della matrice identifica il vertice originale da cui provengono i vertici finali (se il vertice è stato suddiviso durante la modifica del mapping).</span><span class="sxs-lookup"><span data-stu-id="59773-157">Each array element identifies the original vertex each final vertex came from (if the vertex was split during remapping).</span></span> <span data-ttu-id="59773-158">Ogni elemento di matrice contiene un valore DWORD per vertice.</span><span class="sxs-lookup"><span data-stu-id="59773-158">Each array element contains one DWORD per vertex.</span></span>

</dd> <dt>

<span data-ttu-id="59773-159">*ppPartitionResultAdjacency*</span><span class="sxs-lookup"><span data-stu-id="59773-159">*ppPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="59773-160">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="59773-160">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="59773-161">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="59773-161">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="59773-162">Questo buffer conterrà una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh di output.</span><span class="sxs-lookup"><span data-stu-id="59773-162">This buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="59773-163">Questo parametro non deve essere **null** perché la chiamata successiva a D3DXUVAtlasPack () la richiede.</span><span class="sxs-lookup"><span data-stu-id="59773-163">This parameter must not be **NULL**, because the subsequent call to D3DXUVAtlasPack() requires it.</span></span>

</dd> <dt>

<span data-ttu-id="59773-164">*pfMaxStretchOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="59773-164">*pfMaxStretchOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59773-165">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="59773-165">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="59773-166">Puntatore al valore di estensione massimo generato dall'algoritmo Atlas.</span><span class="sxs-lookup"><span data-stu-id="59773-166">A pointer to the maximum stretch value generated by the atlas algorithm.</span></span> <span data-ttu-id="59773-167">L'intervallo è compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="59773-167">The range is between 0.0 and 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="59773-168">*pdwNumChartsOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="59773-168">*pdwNumChartsOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59773-169">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="59773-169">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="59773-170">Puntatore al numero di grafici creato dall'algoritmo Atlas.</span><span class="sxs-lookup"><span data-stu-id="59773-170">A pointer to the number of charts created by the atlas algorithm.</span></span> <span data-ttu-id="59773-171">Se dwMaxChartNumber è troppo basso, questo parametro restituirà il numero minimo di grafici necessari per creare un Atlante.</span><span class="sxs-lookup"><span data-stu-id="59773-171">If dwMaxChartNumber is too low, this parameter will return the minimum number of charts required to create an atlas.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59773-172">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59773-172">Return value</span></span>

<span data-ttu-id="59773-173">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59773-173">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59773-174">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. in caso contrario, il valore è D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="59773-174">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="59773-175">Commenti</span><span class="sxs-lookup"><span data-stu-id="59773-175">Remarks</span></span>

<span data-ttu-id="59773-176">D3DXUVAtlasPartition è simile a [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), ad eccezione del fatto che D3DXUVAtlasPartition non esegue il passaggio finale di compressione.</span><span class="sxs-lookup"><span data-stu-id="59773-176">D3DXUVAtlasPartition is similar to [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md), except that D3DXUVAtlasPartition does not performing the final packing step.</span></span>

## <a name="requirements"></a><span data-ttu-id="59773-177">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59773-177">Requirements</span></span>



| <span data-ttu-id="59773-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="59773-178">Requirement</span></span> | <span data-ttu-id="59773-179">Valore</span><span class="sxs-lookup"><span data-stu-id="59773-179">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59773-180">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59773-180">Header</span></span><br/>  | <dl> <span data-ttu-id="59773-181"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="59773-181"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="59773-182">Libreria</span><span class="sxs-lookup"><span data-stu-id="59773-182">Library</span></span><br/> | <dl> <span data-ttu-id="59773-183"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59773-183"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="59773-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59773-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59773-185">Funzioni UVAtlas</span><span class="sxs-lookup"><span data-stu-id="59773-185">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

<span data-ttu-id="59773-186">[Strumento Command-Line UV Atlas (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="59773-186">[UV Atlas Command-Line Tool (uvatlas.exe)](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
