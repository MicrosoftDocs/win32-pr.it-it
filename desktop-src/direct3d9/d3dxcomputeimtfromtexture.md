---
description: Calcola gli IMT per triangolo da una trama mappata su una mesh, da usare facoltativamente come input per le funzioni UVAtlas di D3DX.
ms.assetid: 6671edc4-e494-4847-ae99-b9e56651a875
title: Funzione D3DXComputeIMTFromTexture (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2fbed0411f3562e3a05ec2ec4df99dfad6d8c902
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058658"
---
# <a name="d3dxcomputeimtfromtexture-function"></a><span data-ttu-id="9238f-103">D3DXComputeIMTFromTexture (funzione)</span><span class="sxs-lookup"><span data-stu-id="9238f-103">D3DXComputeIMTFromTexture function</span></span>

<span data-ttu-id="9238f-104">Calcola gli IMT per triangolo da una trama mappata su una mesh, da usare facoltativamente come input per le [funzioni UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)di D3DX.</span><span class="sxs-lookup"><span data-stu-id="9238f-104">Calculates per-triangle IMT's from a texture mapped onto a mesh, to be used optionally as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9238f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9238f-105">Syntax</span></span>


```C++
HRESULT D3DXComputeIMTFromTexture(
  _In_  LPD3DXMESH         pMesh,
  _In_  LPDIRECT3DTEXTURE9 pTexture,
  _In_  DWORD              dwTextureIndex,
  _In_  DWORD              dwOptions,
        LPD3DXUVATLASCB    pStatusCallback,
        LPVOID             pUserContext,
  _Out_ LPD3DXBUFFER       *ppIMTData
);
```



## <a name="parameters"></a><span data-ttu-id="9238f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9238f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9238f-107">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9238f-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9238f-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="9238f-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="9238f-109">Puntatore a una mesh di input (vedere [**ID3DXMesh**](id3dxmesh.md)) che contiene la geometria dell'oggetto per il calcolo di IMT.</span><span class="sxs-lookup"><span data-stu-id="9238f-109">A pointer to an input mesh (see [**ID3DXMesh**](id3dxmesh.md)) which contains the object geometry for calculating the IMT.</span></span>

</dd> <dt>

<span data-ttu-id="9238f-110">*pTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9238f-110">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9238f-111">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="9238f-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="9238f-112">Puntatore alla trama (vedere [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) mappato alla rete.</span><span class="sxs-lookup"><span data-stu-id="9238f-112">A pointer to the texture (see [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) that is mapped to the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="9238f-113">*dwTextureIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9238f-113">*dwTextureIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9238f-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9238f-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9238f-115">Indice di coordinate di trama in base zero che identifica il set di coordinate di trama da usare.</span><span class="sxs-lookup"><span data-stu-id="9238f-115">Zero-based texture coordinate index that identifies which set of texture coordinates to use.</span></span>

</dd> <dt>

<span data-ttu-id="9238f-116">*dwOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9238f-116">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9238f-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9238f-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9238f-118">Opzioni di incapsulamento della trama.</span><span class="sxs-lookup"><span data-stu-id="9238f-118">Texture wrap options.</span></span> <span data-ttu-id="9238f-119">Si tratta di una combinazione di uno o più [**flag D3DXIMT**](./d3dximt-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9238f-119">This is a combination of one or more [**D3DXIMT FLAGS**](./d3dximt-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="9238f-120">*pStatusCallback*</span><span class="sxs-lookup"><span data-stu-id="9238f-120">*pStatusCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="9238f-121">Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span><span class="sxs-lookup"><span data-stu-id="9238f-121">Type: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**</span></span>

<span data-ttu-id="9238f-122">Puntatore a una funzione di callback per monitorare lo stato di avanzamento del calcolo di IMT.</span><span class="sxs-lookup"><span data-stu-id="9238f-122">A pointer to a callback function to monitor IMT computation progress.</span></span>

</dd> <dt>

<span data-ttu-id="9238f-123">*pUserContext*</span><span class="sxs-lookup"><span data-stu-id="9238f-123">*pUserContext*</span></span> 
</dt> <dd>

<span data-ttu-id="9238f-124">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9238f-124">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9238f-125">Puntatore a una variabile definita dall'utente che viene passata alla funzione di callback dello stato.</span><span class="sxs-lookup"><span data-stu-id="9238f-125">A pointer to a user-defined variable which is passed to the status callback function.</span></span> <span data-ttu-id="9238f-126">Usato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="9238f-126">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="9238f-127">*ppIMTData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9238f-127">*ppIMTData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9238f-128">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9238f-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9238f-129">Puntatore al buffer (vedere [**ID3DXBuffer**](id3dxbuffer.md)) contenente la matrice IMT restituita.</span><span class="sxs-lookup"><span data-stu-id="9238f-129">A pointer to the buffer (see [**ID3DXBuffer**](id3dxbuffer.md)) containing the returned IMT array.</span></span> <span data-ttu-id="9238f-130">Questa matrice può essere fornita come input per le [funzioni UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) di D3DX per definire la priorità dell'allocazione dello spazio di trama nella parametrizzazione della trama.</span><span class="sxs-lookup"><span data-stu-id="9238f-130">This array can be provided as input to the D3DX [UVAtlas Functions](dx9-graphics-reference-d3dx-functions-uvatlas.md) to prioritize texture-space allocation in the texture parameterization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9238f-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9238f-131">Return value</span></span>

<span data-ttu-id="9238f-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9238f-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9238f-133">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK. in caso contrario, il valore è D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="9238f-133">If the function succeeds, the return value is D3D\_OK; otherwise, the value is D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="9238f-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="9238f-134">Remarks</span></span>

<span data-ttu-id="9238f-135">Data una trama che esegue il mapping sulla superficie della mesh, l'algoritmo calcola l'IMT per ogni viso.</span><span class="sxs-lookup"><span data-stu-id="9238f-135">Given a texture that maps over the surface of the mesh, the algorithm computes the IMT for each face.</span></span> <span data-ttu-id="9238f-136">In questo modo, i triangoli contenenti i dati dei segnali con frequenza inferiore possono occupare meno spazio nell'Atlante della trama finale quando vengono parametrizzati con le funzioni UVAtlas.</span><span class="sxs-lookup"><span data-stu-id="9238f-136">This will cause triangles containing lower-frequency signal data to take up less space in the final texture atlas when parameterized with the UVAtlas functions.</span></span> <span data-ttu-id="9238f-137">Si presuppone che la trama venga interpolata sulla rete in modo bilineare.</span><span class="sxs-lookup"><span data-stu-id="9238f-137">The texture is assumed to be interpolated over the mesh bilinearly.</span></span>

## <a name="requirements"></a><span data-ttu-id="9238f-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9238f-138">Requirements</span></span>



| <span data-ttu-id="9238f-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="9238f-139">Requirement</span></span> | <span data-ttu-id="9238f-140">Valore</span><span class="sxs-lookup"><span data-stu-id="9238f-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9238f-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9238f-141">Header</span></span><br/>  | <dl> <span data-ttu-id="9238f-142"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9238f-142"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9238f-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="9238f-143">Library</span></span><br/> | <dl> <span data-ttu-id="9238f-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9238f-144"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9238f-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9238f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9238f-146">Funzioni UVAtlas</span><span class="sxs-lookup"><span data-stu-id="9238f-146">UVAtlas Functions</span></span>](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[<span data-ttu-id="9238f-147">Uso di UVAtlas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9238f-147">Using UVAtlas (Direct3D 9)</span></span>](using-uvatlas.md)
</dt> </dl>

 

 
