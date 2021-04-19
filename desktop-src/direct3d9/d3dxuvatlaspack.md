---
description: Comprime i dati di partizionamento mesh in un Atlante.
ms.assetid: 4da85626-c36c-44d9-990b-0db80ed04423
title: Funzione D3DXUVAtlasPack (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31de326160120fe14a71841cb5f2d18e1c8d4e57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322569"
---
# <a name="d3dxuvatlaspack-function"></a><span data-ttu-id="79291-103">D3DXUVAtlasPack (funzione)</span><span class="sxs-lookup"><span data-stu-id="79291-103">D3DXUVAtlasPack function</span></span>

<span data-ttu-id="79291-104">Comprime i dati di partizionamento mesh in un Atlante.</span><span class="sxs-lookup"><span data-stu-id="79291-104">Pack mesh partitioning data into an atlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="79291-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79291-105">Syntax</span></span>


```C++
HRESULT D3DXUVAtlasPack(
  _In_       LPD3DXMESH      pMesh,
  _In_       UINT            dwWidth,
  _In_       UINT            dwHeight,
  _In_       FLOAT           fGutter,
  _In_       DWORD           dwTextureIndex,
       const DWORD           *pdwPartitionResultAdjacency,
  _In_       LPD3DXUVATLASCB pCallback,
  _In_       FLOAT           fCallbackFrequency,
  _In_       LPVOID          pUserContent,
  _In_       DWORD           dwOptions,
  _In_       LPD3DXBUFFER    pFacePartitioning
);
```



## <a name="parameters"></a><span data-ttu-id="79291-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="79291-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79291-107">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79291-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79291-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="79291-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="79291-109">Puntatore a una mesh di input (vedere [**ID3DXMesh**](id3dxmesh.md)) che contiene la geometria dell'oggetto per il calcolo dell'Atlante.</span><span class="sxs-lookup"><span data-stu-id="79291-109">Pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the atlas.</span></span> <span data-ttu-id="79291-110">Come minimo, la mesh deve contenere dati sulla posizione e coordinate di trama 2D.</span><span class="sxs-lookup"><span data-stu-id="79291-110">At a minimum, the mesh must contain position data and 2D texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="79291-111">*dwWidth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79291-111">*dwWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79291-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79291-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79291-113">Spessore trama.</span><span class="sxs-lookup"><span data-stu-id="79291-113">Texture width.</span></span>

</dd> <dt>

<span data-ttu-id="79291-114">*dwHeight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79291-114">*dwHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79291-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79291-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79291-116">Altezza trama.</span><span class="sxs-lookup"><span data-stu-id="79291-116">Texture height.</span></span>

</dd> <dt>

<span data-ttu-id="79291-117">*fGutter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79291-117">*fGutter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79291-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79291-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79291-119">Distanza minima, in Texel, tra due grafici nell'Atlante.</span><span class="sxs-lookup"><span data-stu-id="79291-119">The minimum distance, in texels, between two charts on the atlas.</span></span> <span data-ttu-id="79291-120">La gronda viene sempre ridimensionata in base alla larghezza; Se quindi si usa una gronda di 2,5 su una trama 512x512, la distanza minima tra due grafici è 2,5/512,0 Texels.</span><span class="sxs-lookup"><span data-stu-id="79291-120">The gutter is always scaled by the width; so, if a gutter of 2.5 is used on a 512x512 texture, then the minimum distance between two charts is 2.5 / 512.0 texels.</span></span>

</dd> <dt>

<span data-ttu-id="79291-121">*dwTextureIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79291-121">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79291-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79291-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79291-123">Indice di coordinate di trama in base zero che identifica il set di coordinate di trama da usare.</span><span class="sxs-lookup"><span data-stu-id="79291-123">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="79291-124">*pdwPartitionResultAdjacency*</span><span class="sxs-lookup"><span data-stu-id="79291-124">*pdwPartitionResultAdjacency*</span></span> 
</dt> <dd>

<span data-ttu-id="79291-125">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="79291-125">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="79291-126">Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh.</span><span class="sxs-lookup"><span data-stu-id="79291-126">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="79291-127">Deve derivare da ppPartitionResultAdjacency restituito da [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md).</span><span class="sxs-lookup"><span data-stu-id="79291-127">It should be derived from the ppPartitionResultAdjacency returned from [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md).</span></span> <span data-ttu-id="79291-128">Questo valore non può essere **null**, perché Pack deve sapere dove sono stati tagliati i grafici nel passaggio della partizione per trovare i bordi di ogni grafico.</span><span class="sxs-lookup"><span data-stu-id="79291-128">This value cannot be **NULL**, because Pack needs to know where charts were cut in the partition step in order to find the edges of each chart.</span></span>

</dd> <dt>

<span data-ttu-id="79291-129">*pCallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79291-129">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79291-130">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="79291-130">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="79291-131">Puntatore a una funzione di callback (vedere [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) utile per il monitoraggio dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="79291-131">A pointer to a callback function (see [LPD3DXUVATLASCB](lpd3dxuvatlascb.md)) that is useful for monitoring progress.</span></span>

</dd> <dt>

<span data-ttu-id="79291-132">*fCallbackFrequency* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79291-132">*fCallbackFrequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79291-133">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79291-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79291-134">Specificare la frequenza con cui D3DX chiamerà il callback; un valore predefinito ragionevole è 0,0001 f.</span><span class="sxs-lookup"><span data-stu-id="79291-134">Specify how often D3DX will call the callback; a reasonable default value is 0.0001f.</span></span>

</dd> <dt>

<span data-ttu-id="79291-135">*pUserContent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79291-135">*pUserContent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79291-136">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79291-136">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79291-137">Puntatore void da passare di nuovo alla funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="79291-137">A void pointer to be passed back to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="79291-138">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79291-138">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79291-139">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79291-139">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79291-140">Questo parametro di opzioni è attualmente riservato.</span><span class="sxs-lookup"><span data-stu-id="79291-140">This options parameter is currently reserved.</span></span>

</dd> <dt>

<span data-ttu-id="79291-141">*pFacePartitioning* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79291-141">*pFacePartitioning* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79291-142">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="79291-142">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)**</span></span>

<span data-ttu-id="79291-143">Puntatore a un [**ID3DXBuffer**](id3dxbuffer.md) contenente la matrice del partizionamento finale della faccia.</span><span class="sxs-lookup"><span data-stu-id="79291-143">A pointer to an [**ID3DXBuffer**](id3dxbuffer.md) containing the array of the final face-partitioning.</span></span> <span data-ttu-id="79291-144">Ogni elemento contiene un valore DWORD per ogni faccia.</span><span class="sxs-lookup"><span data-stu-id="79291-144">Each element contains one DWORD per face.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79291-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79291-145">Return value</span></span>

<span data-ttu-id="79291-146">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79291-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79291-147">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. in caso contrario, il valore è D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="79291-147">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="79291-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79291-148">Requirements</span></span>



| <span data-ttu-id="79291-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="79291-149">Requirement</span></span> | <span data-ttu-id="79291-150">Valore</span><span class="sxs-lookup"><span data-stu-id="79291-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79291-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79291-151">Header</span></span><br/>  | <dl> <span data-ttu-id="79291-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="79291-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="79291-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="79291-153">Library</span></span><br/> | <dl> <span data-ttu-id="79291-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79291-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="79291-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79291-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79291-156">Funzioni UVAtlas</span><span class="sxs-lookup"><span data-stu-id="79291-156">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> </dl>

 

 
