---
description: Ottiene le dimensioni della patch del rettangolo.
ms.assetid: d25373ef-789d-4515-83da-7049f040c9a4
title: Funzione D3DXRectPatchSize (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXRectPatchSize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5770e05493164db9da75fb38fa1e41594bfae8f8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322482"
---
# <a name="d3dxrectpatchsize-function"></a><span data-ttu-id="1c9a8-103">D3DXRectPatchSize (funzione)</span><span class="sxs-lookup"><span data-stu-id="1c9a8-103">D3DXRectPatchSize function</span></span>

<span data-ttu-id="1c9a8-104">Ottiene le dimensioni della patch del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="1c9a8-104">Gets the size of the rectangle patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c9a8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c9a8-105">Syntax</span></span>


```C++
HRESULT D3DXRectPatchSize(
  _In_  const FLOAT *pfNumSegs,
  _Out_       DWORD *pdwTriangles,
  _Out_       DWORD *pwdVertices
);
```



## <a name="parameters"></a><span data-ttu-id="1c9a8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c9a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c9a8-107">*pfNumSegs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c9a8-107">*pfNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c9a8-108">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="1c9a8-108">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1c9a8-109">Numero di segmenti per perimetro a conteggiarla suddividerla.</span><span class="sxs-lookup"><span data-stu-id="1c9a8-109">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="1c9a8-110">*pdwTriangles* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1c9a8-110">*pdwTriangles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c9a8-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1c9a8-111">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1c9a8-112">Puntatore a un valore DWORD che contiene il numero di triangoli nella patch.</span><span class="sxs-lookup"><span data-stu-id="1c9a8-112">Pointer to a DWORD that contains the number of triangles in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="1c9a8-113">*pwdVertices* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1c9a8-113">*pwdVertices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c9a8-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1c9a8-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1c9a8-115">Puntatore a un valore DWORD che contiene il numero di vertici nella patch.</span><span class="sxs-lookup"><span data-stu-id="1c9a8-115">Pointer to a DWORD that contains the number of vertices in the patch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c9a8-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c9a8-116">Return value</span></span>

<span data-ttu-id="1c9a8-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1c9a8-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1c9a8-118">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1c9a8-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1c9a8-119">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="1c9a8-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c9a8-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c9a8-120">Requirements</span></span>



| <span data-ttu-id="1c9a8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c9a8-121">Requirement</span></span> | <span data-ttu-id="1c9a8-122">Valore</span><span class="sxs-lookup"><span data-stu-id="1c9a8-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c9a8-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1c9a8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1c9a8-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c9a8-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1c9a8-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="1c9a8-125">Library</span></span><br/> | <dl> <span data-ttu-id="1c9a8-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c9a8-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1c9a8-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c9a8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c9a8-128">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="1c9a8-128">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="1c9a8-129">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="1c9a8-129">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
