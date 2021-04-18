---
description: Calcolare le IMT per triangolo da dati per Texel. Questa funzione è simile a D3DXComputeIMTFromTexture, ma usa una matrice float per passare i dati e può calcolare valori dimensionali più alti di 4.
ms.assetid: 4a151184-e67e-41e9-83c6-63da72f262fa
title: Funzione D3DXComputeIMTFromPerTexelSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerTexelSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3db71fbc931f7bdb3e73c8d949a163607e66c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322868"
---
# <a name="d3dxcomputeimtfrompertexelsignal-function"></a><span data-ttu-id="4df9a-104">D3DXComputeIMTFromPerTexelSignal (funzione)</span><span class="sxs-lookup"><span data-stu-id="4df9a-104">D3DXComputeIMTFromPerTexelSignal function</span></span>

<span data-ttu-id="4df9a-105">Calcolare le IMT per triangolo da dati per Texel.</span><span class="sxs-lookup"><span data-stu-id="4df9a-105">Calculate per-triangle IMT's from per-texel data.</span></span> <span data-ttu-id="4df9a-106">Questa funzione è simile a [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md), ma usa una matrice float per passare i dati e può calcolare valori dimensionali più alti di 4.</span><span class="sxs-lookup"><span data-stu-id="4df9a-106">This function is similar to [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md), but it uses a float array to pass in the data, and it can calculate higher dimensional values than 4.</span></span>

## <a name="syntax"></a><span data-ttu-id="4df9a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4df9a-107">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromPerTexelSignal(
  _In_  LPD3DXMESH      pMesh,
  _In_  DWORD           dwTextureIndex,
  _In_  FLOAT           *pfTexelSignal,
  _In_  UINT            uWidth,
  _In_  UINT            uHeight,
  _In_  UINT            uSignalDimension,
  _In_  UINT            uComponents,
  _In_  DWORD           dwOptions,
        LPD3DXUVATLASCB pStatusCallback,
        LPVOID          pUserContext,
  _Out_ LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="4df9a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4df9a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4df9a-109">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4df9a-109">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4df9a-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="4df9a-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="4df9a-111">Puntatore a una mesh di input (vedere [**ID3DXMesh**](id3dxmesh.md)) che contiene la geometria dell'oggetto per il calcolo di IMT.</span><span class="sxs-lookup"><span data-stu-id="4df9a-111">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="4df9a-112">*dwTextureIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4df9a-112">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4df9a-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4df9a-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4df9a-114">Indice di coordinate di trama in base zero che identifica il set di coordinate di trama da usare.</span><span class="sxs-lookup"><span data-stu-id="4df9a-114">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="4df9a-115">*pfTexelSignal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4df9a-115">*pfTexelSignal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4df9a-116">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4df9a-116">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4df9a-117">Puntatore a una matrice di Texel di input da cui verrà calcolato IMT.</span><span class="sxs-lookup"><span data-stu-id="4df9a-117">A pointer to an array of input texels from which IMT will be computed.</span></span> <span data-ttu-id="4df9a-118">La dimensione della matrice è uWidth \* uHeight \* uComponents.</span><span class="sxs-lookup"><span data-stu-id="4df9a-118">The array size is uWidth\*uHeight\*uComponents.</span></span>

</dd> <dt>

<span data-ttu-id="4df9a-119">*uWidth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4df9a-119">*uWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4df9a-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4df9a-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4df9a-121">Larghezza della trama in pixel.</span><span class="sxs-lookup"><span data-stu-id="4df9a-121">Texture width in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="4df9a-122">*uHeight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4df9a-122">*uHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4df9a-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4df9a-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4df9a-124">Altezza della trama in pixel.</span><span class="sxs-lookup"><span data-stu-id="4df9a-124">Texture height in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="4df9a-125">*uSignalDimension* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4df9a-125">*uSignalDimension* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4df9a-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4df9a-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4df9a-127">Numero di float per componente in ogni elemento della matrice di segnali.</span><span class="sxs-lookup"><span data-stu-id="4df9a-127">The number of floats per-component in each element of the signal array.</span></span>

</dd> <dt>

<span data-ttu-id="4df9a-128">*uComponents* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4df9a-128">*uComponents* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4df9a-129">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4df9a-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4df9a-130">Il numero di componenti in ogni Texel.</span><span class="sxs-lookup"><span data-stu-id="4df9a-130">The number of components in each texel.</span></span>

</dd> <dt>

<span data-ttu-id="4df9a-131">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4df9a-131">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4df9a-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4df9a-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4df9a-133">Opzioni di incapsulamento della trama.</span><span class="sxs-lookup"><span data-stu-id="4df9a-133">Texture wrap options.</span></span> <span data-ttu-id="4df9a-134">Si tratta di una combinazione di uno o più [**flag D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4df9a-134">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="4df9a-135">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="4df9a-135">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="4df9a-136">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="4df9a-136">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="4df9a-137">Puntatore a una funzione di callback per monitorare lo stato di avanzamento del calcolo di IMT.</span><span class="sxs-lookup"><span data-stu-id="4df9a-137">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="4df9a-138">*pUserContext*</span><span class="sxs-lookup"><span data-stu-id="4df9a-138">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="4df9a-139">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4df9a-139">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4df9a-140">Puntatore a una variabile definita dall'utente che viene passata alla funzione di callback dello stato.</span><span class="sxs-lookup"><span data-stu-id="4df9a-140">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="4df9a-141">Usato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="4df9a-141">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="4df9a-142">*ppIMTData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4df9a-142">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4df9a-143">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="4df9a-143">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="4df9a-144">Puntatore al buffer (vedere [**ID3DXBuffer**](id3dxbuffer.md)) contenente la matrice IMT restituita.</span><span class="sxs-lookup"><span data-stu-id="4df9a-144">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="4df9a-145">Questa matrice può essere fornita come input per le [funzioni UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) di D3DX per definire la priorità dell'allocazione dello spazio di trama nella parametrizzazione della trama.</span><span class="sxs-lookup"><span data-stu-id="4df9a-145">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4df9a-146">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4df9a-146">Return value</span></span>

<span data-ttu-id="4df9a-147">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4df9a-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4df9a-148">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. in caso contrario, il valore è D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="4df9a-148">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="4df9a-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4df9a-149">Requirements</span></span>



| <span data-ttu-id="4df9a-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="4df9a-150">Requirement</span></span> | <span data-ttu-id="4df9a-151">Valore</span><span class="sxs-lookup"><span data-stu-id="4df9a-151">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4df9a-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4df9a-152">Header</span></span><br/>  | <dl> <span data-ttu-id="4df9a-153"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="4df9a-153"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="4df9a-154">Libreria</span><span class="sxs-lookup"><span data-stu-id="4df9a-154">Library</span></span><br/> | <dl> <span data-ttu-id="4df9a-155"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4df9a-155"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4df9a-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4df9a-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4df9a-157">Funzioni UVAtlas</span><span class="sxs-lookup"><span data-stu-id="4df9a-157">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="4df9a-158">Uso di UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4df9a-158">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
