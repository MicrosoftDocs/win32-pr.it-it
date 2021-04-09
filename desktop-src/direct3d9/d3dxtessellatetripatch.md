---
description: Tessellates una patch di superficie di ordine superiore triangolare in una mesh triangolare.
ms.assetid: bcc9143f-fec0-491a-8d32-1df961b8dade
title: Funzione D3DXTessellateTriPatch (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateTriPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 61d5a426f9fe3331b85c4a881219319622283820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762017"
---
# <a name="d3dxtessellatetripatch-function"></a><span data-ttu-id="52416-103">D3DXTessellateTriPatch (funzione)</span><span class="sxs-lookup"><span data-stu-id="52416-103">D3DXTessellateTriPatch function</span></span>

<span data-ttu-id="52416-104">Tessellates una patch di superficie di ordine superiore triangolare in una mesh triangolare.</span><span class="sxs-lookup"><span data-stu-id="52416-104">Tessellates a triangular higher-order surface patch into a triangle mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="52416-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52416-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateTriPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3TRIPATCH_INFO         *pTriPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="52416-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="52416-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52416-107">*pVB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52416-107">*pVB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52416-108">Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span><span class="sxs-lookup"><span data-stu-id="52416-108">Type: **[**LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**</span></span>

<span data-ttu-id="52416-109">Buffer vertex che contiene i dati della patch.</span><span class="sxs-lookup"><span data-stu-id="52416-109">Vertex buffer containing the patch data.</span></span>

</dd> <dt>

<span data-ttu-id="52416-110">*pNumSegs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52416-110">*pNumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52416-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="52416-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="52416-112">Puntatore a una matrice di tre valori a virgola mobile che identificano il numero di segmenti in cui deve essere diviso ogni bordo della patch del triangolo quando tassellati.</span><span class="sxs-lookup"><span data-stu-id="52416-112">Pointer to an array of three floating-point values that identify the number of segments into which each edge of the triangle patch should be divided when tessellated.</span></span> <span data-ttu-id="52416-113">Vedere [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="52416-113">See [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="52416-114">*pInDecl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52416-114">*pInDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52416-115">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="52416-115">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="52416-116">Struttura di dichiarazione vertici che definisce i dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="52416-116">Vertex declaration structure that defines the vertex data.</span></span> <span data-ttu-id="52416-117">Vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="52416-117">See [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

</dd> <dt>

<span data-ttu-id="52416-118">*pTriPatchInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52416-118">*pTriPatchInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52416-119">Tipo: **const [**D3TRIPATCH \_ info**](d3dtripatch-info.md) \***</span><span class="sxs-lookup"><span data-stu-id="52416-119">Type: **const [**D3TRIPATCH\_INFO**](d3dtripatch-info.md)\***</span></span>

<span data-ttu-id="52416-120">Descrive una patch di triangolo.</span><span class="sxs-lookup"><span data-stu-id="52416-120">Describes a triangle patch.</span></span> <span data-ttu-id="52416-121">Vedere [**D3DTRIPATCH \_ info**](d3dtripatch-info.md).</span><span class="sxs-lookup"><span data-stu-id="52416-121">See [**D3DTRIPATCH\_INFO**](d3dtripatch-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="52416-122">*pMesh* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="52416-122">*pMesh* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="52416-123">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="52416-123">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="52416-124">Puntatore alla mesh creata.</span><span class="sxs-lookup"><span data-stu-id="52416-124">Pointer to the created mesh.</span></span> <span data-ttu-id="52416-125">Vedere [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="52416-125">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52416-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52416-126">Return value</span></span>

<span data-ttu-id="52416-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52416-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52416-128">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="52416-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="52416-129">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="52416-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="52416-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="52416-130">Remarks</span></span>

<span data-ttu-id="52416-131">Usare [**D3DXTriPatchSize**](d3dxtripatchsize.md) per ottenere il numero di vertici e indici di output necessari per la funzione mosaico.</span><span class="sxs-lookup"><span data-stu-id="52416-131">Use [**D3DXTriPatchSize**](d3dxtripatchsize.md) to get the number of output vertices and indices that the tessellation function needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="52416-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52416-132">Requirements</span></span>



| <span data-ttu-id="52416-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="52416-133">Requirement</span></span> | <span data-ttu-id="52416-134">Valore</span><span class="sxs-lookup"><span data-stu-id="52416-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52416-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52416-135">Header</span></span><br/>  | <dl> <span data-ttu-id="52416-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="52416-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="52416-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="52416-137">Library</span></span><br/> | <dl> <span data-ttu-id="52416-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52416-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="52416-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52416-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52416-140">Funzioni mesh</span><span class="sxs-lookup"><span data-stu-id="52416-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="52416-141">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="52416-141">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
