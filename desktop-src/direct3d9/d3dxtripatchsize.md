---
description: Ottiene le dimensioni della patch del triangolo.
ms.assetid: 3bfbed4c-59af-43eb-a462-478e89cfe9ae
title: Funzione D3DXTriPatchSize (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTriPatchSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5ee254b12485153f4d5c5ba0843189399d1aed0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322571"
---
# <a name="d3dxtripatchsize-function"></a><span data-ttu-id="ef87d-103">D3DXTriPatchSize (funzione)</span><span class="sxs-lookup"><span data-stu-id="ef87d-103">D3DXTriPatchSize function</span></span>

<span data-ttu-id="ef87d-104">Ottiene le dimensioni della patch del triangolo.</span><span class="sxs-lookup"><span data-stu-id="ef87d-104">Gets the size of the triangle patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef87d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef87d-105">Syntax</span></span>


```C++
HRESULT D3DXTriPatchSize(
  _In_  const FLOAT *pfNumSegs,
  _Out_       DWORD *pdwTriangles,
  _Out_       DWORD *pdwVertices
);
```



## <a name="parameters"></a><span data-ttu-id="ef87d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef87d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef87d-107">*pfNumSegs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef87d-107">*pfNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef87d-108">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ef87d-108">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ef87d-109">Numero di segmenti per perimetro a conteggiarla suddividerla.</span><span class="sxs-lookup"><span data-stu-id="ef87d-109">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="ef87d-110">*pdwTriangles* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ef87d-110">*pdwTriangles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef87d-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ef87d-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ef87d-112">Puntatore a un valore DWORD che contiene il numero di triangoli nella patch.</span><span class="sxs-lookup"><span data-stu-id="ef87d-112">Pointer to a DWORD that contains the number of triangles in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="ef87d-113">*pdwVertices* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ef87d-113">*pdwVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef87d-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ef87d-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ef87d-115">Puntatore a un valore DWORD che contiene il numero di vertici nella patch del triangolo.</span><span class="sxs-lookup"><span data-stu-id="ef87d-115">Pointer to a DWORD that contains the number of vertices in the triangle patch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef87d-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef87d-116">Return value</span></span>

<span data-ttu-id="ef87d-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ef87d-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ef87d-118">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ef87d-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ef87d-119">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="ef87d-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef87d-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef87d-120">Requirements</span></span>



| <span data-ttu-id="ef87d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef87d-121">Requirement</span></span> | <span data-ttu-id="ef87d-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ef87d-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef87d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef87d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ef87d-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef87d-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ef87d-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="ef87d-125">Library</span></span><br/> | <dl> <span data-ttu-id="ef87d-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef87d-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ef87d-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef87d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef87d-128">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="ef87d-128">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="ef87d-129">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="ef87d-129">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
