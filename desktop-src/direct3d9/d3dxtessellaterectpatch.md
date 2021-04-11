---
description: Tessellates una patch della superficie di ordine superiore rettangolare in una mesh triangolare.
ms.assetid: d941d994-8a13-49ff-a0b1-b21a3f84ed78
title: Funzione D3DXTessellateRectPatch (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateRectPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 887f0035b50efd860149410e50dd6abff301968d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234997"
---
# <a name="d3dxtessellaterectpatch-function"></a><span data-ttu-id="f61f9-103">D3DXTessellateRectPatch (funzione)</span><span class="sxs-lookup"><span data-stu-id="f61f9-103">D3DXTessellateRectPatch function</span></span>

<span data-ttu-id="f61f9-104">Tessellates una patch della superficie di ordine superiore rettangolare in una mesh triangolare.</span><span class="sxs-lookup"><span data-stu-id="f61f9-104">Tessellates a rectangular higher-order surface patch into a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="f61f9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f61f9-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateRectPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3DRECTPATCH_INFO       *pRectPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="f61f9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f61f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f61f9-107">*pVB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f61f9-107">*pVB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f61f9-108">Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="f61f9-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span></span>

<span data-ttu-id="f61f9-109">Buffer vertex che contiene i dati della patch.</span><span class="sxs-lookup"><span data-stu-id="f61f9-109">Vertex buffer containing the patch data.</span></span>

</dd> <dt>

<span data-ttu-id="f61f9-110">*pNumSegs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f61f9-110">*pNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f61f9-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f61f9-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f61f9-112">Puntatore a una matrice di quattro valori a virgola mobile che identificano il numero di segmenti in cui ogni bordo della patch rettangolo deve essere diviso quando tassellati.</span><span class="sxs-lookup"><span data-stu-id="f61f9-112">Pointer to an array of four floating-point values that identify the number of segments into which each edge of the rectangle patch should be divided when tessellated.</span></span> <span data-ttu-id="f61f9-113">Vedere [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="f61f9-113">See [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f9-114">*pInDecl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f61f9-114">*pInDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f61f9-115">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="f61f9-115">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="f61f9-116">Struttura di dichiarazione vertici che definisce i dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="f61f9-116">Vertex declaration structure that defines the vertex data.</span></span> <span data-ttu-id="f61f9-117">Vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="f61f9-117">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f9-118">*pRectPatchInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f61f9-118">*pRectPatchInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f61f9-119">Tipo: **const [**D3DRECTPATCH \_ info**](d3drectpatch-info.md) \***</span><span class="sxs-lookup"><span data-stu-id="f61f9-119">Type: **const [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md)\***</span></span>

<span data-ttu-id="f61f9-120">Descrive una patch rettangolare.</span><span class="sxs-lookup"><span data-stu-id="f61f9-120">Describes a rectangular patch.</span></span> <span data-ttu-id="f61f9-121">Vedere [**D3DRECTPATCH \_ info**](d3drectpatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="f61f9-121">See [**D3DRECTPATCH\_INFO**](d3drectpatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="f61f9-122">*pMesh* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f61f9-122">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f61f9-123">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="f61f9-123">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="f61f9-124">Puntatore alla mesh creata.</span><span class="sxs-lookup"><span data-stu-id="f61f9-124">Pointer to the created mesh.</span></span> <span data-ttu-id="f61f9-125">Vedere [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="f61f9-125">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f61f9-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f61f9-126">Return value</span></span>

<span data-ttu-id="f61f9-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f61f9-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f61f9-128">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f61f9-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f61f9-129">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="f61f9-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f61f9-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="f61f9-130">Remarks</span></span>

<span data-ttu-id="f61f9-131">Usare [**D3DXRectPatchSize**](d3dxrectpatchsize.md) per ottenere il numero di vertici e indici di output necessari per la funzione mosaico.</span><span class="sxs-lookup"><span data-stu-id="f61f9-131">Use [**D3DXRectPatchSize**](d3dxrectpatchsize.md) to get the number of output vertices and indices that the tessellation function needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="f61f9-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f61f9-132">Requirements</span></span>



| <span data-ttu-id="f61f9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f61f9-133">Requirement</span></span> | <span data-ttu-id="f61f9-134">Valore</span><span class="sxs-lookup"><span data-stu-id="f61f9-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f61f9-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f61f9-135">Header</span></span><br/>  | <dl> <span data-ttu-id="f61f9-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f61f9-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f61f9-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="f61f9-137">Library</span></span><br/> | <dl> <span data-ttu-id="f61f9-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f61f9-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f61f9-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f61f9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f61f9-140">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="f61f9-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="f61f9-141">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="f61f9-141">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
