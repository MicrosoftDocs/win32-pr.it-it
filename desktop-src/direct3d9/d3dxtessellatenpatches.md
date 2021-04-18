---
description: Tessellates la mesh specificata usando lo schema a mosaico N-patch.
ms.assetid: e804905d-ee0b-484f-a621-58b197bd370b
title: Funzione D3DXTessellateNPatches (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateNPatches
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c8811816447deb858b5c8b42d651d219f06fef5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322471"
---
# <a name="d3dxtessellatenpatches-function"></a><span data-ttu-id="deb66-103">D3DXTessellateNPatches (funzione)</span><span class="sxs-lookup"><span data-stu-id="deb66-103">D3DXTessellateNPatches function</span></span>

<span data-ttu-id="deb66-104">Tessellates la mesh specificata usando lo schema a mosaico N-patch.</span><span class="sxs-lookup"><span data-stu-id="deb66-104">Tessellates the given mesh using the N-patch tessellation scheme.</span></span>

## <a name="syntax"></a><span data-ttu-id="deb66-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="deb66-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateNPatches(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const CONST DWORD  *pAdjacencyIn,
  _In_        FLOAT        NumSegs,
  _In_        BOOL         QuadraticInterpNormals,
  _Out_       LPD3DXMESH   *ppMeshOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyOut
);
```



## <a name="parameters"></a><span data-ttu-id="deb66-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="deb66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deb66-107">*pMeshIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="deb66-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deb66-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="deb66-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="deb66-109">Puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh in conteggiarla suddividerla.</span><span class="sxs-lookup"><span data-stu-id="deb66-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="deb66-110">*pAdjacencyIn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="deb66-110">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deb66-111">Tipo: **const const DWORD \***</span><span class="sxs-lookup"><span data-stu-id="deb66-111">Type: **const CONST DWORD\***</span></span>

<span data-ttu-id="deb66-112">Puntatore a una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh di origine.</span><span class="sxs-lookup"><span data-stu-id="deb66-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="deb66-113">Questo parametro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="deb66-113">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="deb66-114">*NumSegs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="deb66-114">*NumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deb66-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="deb66-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="deb66-116">Numero di segmenti per perimetro a conteggiarla suddividerla.</span><span class="sxs-lookup"><span data-stu-id="deb66-116">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="deb66-117">*QuadraticInterpNormals* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="deb66-117">*QuadraticInterpNormals* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="deb66-118">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="deb66-118">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="deb66-119">Impostare su **true** per usare l'interpolazione quadratica per le normali; impostare su **false** per l'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="deb66-119">Set to **TRUE** to use quadratic interpolation for normals; set to **FALSE** for linear interpolation.</span></span>

</dd> <dt>

<span data-ttu-id="deb66-120">*ppMeshOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="deb66-120">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="deb66-121">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="deb66-121">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="deb66-122">Indirizzo di un puntatore a un'interfaccia [**ID3DXMesh**](id3dxmesh.md) , che rappresenta la mesh tassellati restituita.</span><span class="sxs-lookup"><span data-stu-id="deb66-122">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned tessellated mesh.</span></span>

</dd> <dt>

<span data-ttu-id="deb66-123">*ppAdjacencyOut* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="deb66-123">*ppAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="deb66-124">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="deb66-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="deb66-125">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="deb66-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="deb66-126">Se il valore di questo parametro non è impostato su **null**, questo buffer conterrà una matrice di tre DWORD per ogni volto che specifica i tre elementi adiacenti per ogni viso nella mesh di output.</span><span class="sxs-lookup"><span data-stu-id="deb66-126">If the value of this parameter is not set to **NULL**, this buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="deb66-127">Questo parametro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="deb66-127">This parameter may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deb66-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="deb66-128">Return value</span></span>

<span data-ttu-id="deb66-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="deb66-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="deb66-130">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="deb66-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="deb66-131">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="deb66-131">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="deb66-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="deb66-132">Remarks</span></span>

<span data-ttu-id="deb66-133">Questa funzione tessellates usando l'algoritmo N-patch.</span><span class="sxs-lookup"><span data-stu-id="deb66-133">This function tessellates by using the N-patch algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="deb66-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="deb66-134">Requirements</span></span>



| <span data-ttu-id="deb66-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="deb66-135">Requirement</span></span> | <span data-ttu-id="deb66-136">Valore</span><span class="sxs-lookup"><span data-stu-id="deb66-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="deb66-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="deb66-137">Header</span></span><br/>  | <dl> <span data-ttu-id="deb66-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="deb66-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="deb66-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="deb66-139">Library</span></span><br/> | <dl> <span data-ttu-id="deb66-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="deb66-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="deb66-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="deb66-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="deb66-142">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="deb66-142">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
