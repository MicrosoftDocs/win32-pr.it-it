---
description: Aggiorna le informazioni sull'influenza ossea in modo che corrispondano ai vertici dopo essere stati riordinati. Questo metodo deve essere chiamato se il buffer dei vertici di destinazione è stato riordinato esternamente.
ms.assetid: bff5229f-e547-4ab3-84c6-58b15a7825e9
title: 'Metodo ID3DXSkinInfo:: mapping (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.Remap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 657cf0977592a8e19e68b8aeb950c62d404e7cdb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322059"
---
# <a name="id3dxskininforemap-method"></a><span data-ttu-id="fb82a-104">Metodo ID3DXSkinInfo:: mapping</span><span class="sxs-lookup"><span data-stu-id="fb82a-104">ID3DXSkinInfo::Remap method</span></span>

<span data-ttu-id="fb82a-105">Aggiorna le informazioni sull'influenza ossea in modo che corrispondano ai vertici dopo essere stati riordinati.</span><span class="sxs-lookup"><span data-stu-id="fb82a-105">Updates bone influence information to match vertices after they are reordered.</span></span> <span data-ttu-id="fb82a-106">Questo metodo deve essere chiamato se il buffer dei vertici di destinazione è stato riordinato esternamente.</span><span class="sxs-lookup"><span data-stu-id="fb82a-106">This method should be called if the target vertex buffer has been reordered externally.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb82a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb82a-107">Syntax</span></span>


```C++
HRESULT Remap(
  [in] DWORD NumVertices,
  [in] DWORD *pVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="fb82a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb82a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb82a-109">*NumVertices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb82a-109">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb82a-110">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb82a-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb82a-111">Numero di vertici di cui modificare il mapping.</span><span class="sxs-lookup"><span data-stu-id="fb82a-111">Number of vertices to remap.</span></span>

</dd> <dt>

<span data-ttu-id="fb82a-112">*pVertexRemap* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb82a-112">*pVertexRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb82a-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fb82a-113">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fb82a-114">Matrice di DWORD la cui lunghezza è specificata da NumVertices.</span><span class="sxs-lookup"><span data-stu-id="fb82a-114">Array of DWORDS whose length is specified by NumVertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb82a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb82a-115">Return value</span></span>

<span data-ttu-id="fb82a-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb82a-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb82a-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fb82a-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fb82a-118">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="fb82a-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb82a-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb82a-119">Remarks</span></span>

<span data-ttu-id="fb82a-120">Ogni elemento in pVertexRemap specifica l'indice Vertex precedente per tale posizione.</span><span class="sxs-lookup"><span data-stu-id="fb82a-120">Each element in pVertexRemap specifies the previous vertex index for that position.</span></span> <span data-ttu-id="fb82a-121">Se, ad esempio, un vertice si trova nella posizione 3 ma è stato rimappato alla posizione 5, il quinto elemento di pVertexRemap deve contenere 3.</span><span class="sxs-lookup"><span data-stu-id="fb82a-121">For example, if a vertex was in position 3 but has been remapped to position 5, then the fifth element of pVertexRemap should contain 3.</span></span> <span data-ttu-id="fb82a-122">È possibile usare la matrice di riassociazione dei vertici restituita da [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) .</span><span class="sxs-lookup"><span data-stu-id="fb82a-122">The vertex remap array returned by [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) can be used.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb82a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb82a-123">Requirements</span></span>



| <span data-ttu-id="fb82a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb82a-124">Requirement</span></span> | <span data-ttu-id="fb82a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="fb82a-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb82a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb82a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="fb82a-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb82a-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fb82a-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="fb82a-128">Library</span></span><br/> | <dl> <span data-ttu-id="fb82a-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb82a-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb82a-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb82a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb82a-131">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="fb82a-131">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
