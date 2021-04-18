---
description: Crea un oggetto ID3DXTextureGutterHelper da una mesh di input e dati di trama.
ms.assetid: 1696fc3d-5b35-48cc-a79b-c0d4ed44e420
title: Funzione D3DXCreateTextureGutterHelper (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureGutterHelper
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8957649f3cef6ea67932579918163613160ee993
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322723"
---
# <a name="d3dxcreatetexturegutterhelper-function"></a><span data-ttu-id="46943-103">D3DXCreateTextureGutterHelper (funzione)</span><span class="sxs-lookup"><span data-stu-id="46943-103">D3DXCreateTextureGutterHelper function</span></span>

<span data-ttu-id="46943-104">Crea un oggetto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) da una mesh di input e dati di trama.</span><span class="sxs-lookup"><span data-stu-id="46943-104">Creates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object from an input mesh and texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="46943-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46943-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureGutterHelper(
  _In_    UINT                      Width,
  _In_    UINT                      Height,
  _In_    LPD3DXMESH                pMesh,
  _In_    FLOAT                     GutterSize,
  _Inout_ LPD3DXTEXTUREGUTTERHELPER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="46943-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="46943-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46943-107">*Larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46943-107">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46943-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46943-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46943-109">Larghezza, in pixel, della trama.</span><span class="sxs-lookup"><span data-stu-id="46943-109">Width of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="46943-110">*Altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46943-110">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46943-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46943-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46943-112">Altezza, in pixel, della trama.</span><span class="sxs-lookup"><span data-stu-id="46943-112">Height of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="46943-113">*pMesh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46943-113">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46943-114">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="46943-114">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="46943-115">Puntatore a un oggetto mesh [**ID3DXMesh**](id3dxmesh.md) di input.</span><span class="sxs-lookup"><span data-stu-id="46943-115">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="46943-116">*GutterSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46943-116">*GutterSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46943-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46943-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46943-118">Numero di Texel in base ai quali sovracampionare la trama e creare l'area di gronda.</span><span class="sxs-lookup"><span data-stu-id="46943-118">Number of texels by which to over-sample the texture and create the gutter region.</span></span> <span data-ttu-id="46943-119">Deve essere almeno 1.</span><span class="sxs-lookup"><span data-stu-id="46943-119">Must be at least 1.</span></span>

</dd> <dt>

<span data-ttu-id="46943-120">*ppBuffer* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="46943-120">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="46943-121">Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***</span><span class="sxs-lookup"><span data-stu-id="46943-121">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***</span></span>

<span data-ttu-id="46943-122">Puntatore a un oggetto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) da creare.</span><span class="sxs-lookup"><span data-stu-id="46943-122">Pointer to an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46943-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46943-123">Return value</span></span>

<span data-ttu-id="46943-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46943-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46943-125">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="46943-125">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="46943-126">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="46943-126">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="46943-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="46943-127">Remarks</span></span>

<span data-ttu-id="46943-128">Usare [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) per trasformare una scena in nuove coordinate.</span><span class="sxs-lookup"><span data-stu-id="46943-128">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) to transform a scene to new coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="46943-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46943-129">Requirements</span></span>



| <span data-ttu-id="46943-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="46943-130">Requirement</span></span> | <span data-ttu-id="46943-131">Valore</span><span class="sxs-lookup"><span data-stu-id="46943-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46943-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46943-132">Header</span></span><br/>  | <dl> <span data-ttu-id="46943-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="46943-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="46943-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="46943-134">Library</span></span><br/> | <dl> <span data-ttu-id="46943-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="46943-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="46943-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46943-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46943-137">Funzioni di trasferimento Radiance pre-calcolate</span><span class="sxs-lookup"><span data-stu-id="46943-137">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
