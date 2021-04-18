---
description: Modificare i vertici influenzati da quali ossa.
ms.assetid: b0d71f3e-9a2d-469d-808b-2fa768cf14b0
title: 'Metodo ID3DX10SkinInfo:: RemapVertices (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc51c912794135b456542bb9a8a779601681f393
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322737"
---
# <a name="id3dx10skininforemapvertices-method"></a><span data-ttu-id="4314a-103">Metodo ID3DX10SkinInfo:: RemapVertices</span><span class="sxs-lookup"><span data-stu-id="4314a-103">ID3DX10SkinInfo::RemapVertices method</span></span>

<span data-ttu-id="4314a-104">Modificare i vertici influenzati da quali ossa.</span><span class="sxs-lookup"><span data-stu-id="4314a-104">Change which vertices are influenced by which bones.</span></span>

## <a name="syntax"></a><span data-ttu-id="4314a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4314a-105">Syntax</span></span>


```C++
HRESULT RemapVertices(
  [in] UINT NewVertexCount,
  [in] UINT *pVertexRemap
);
```



## <a name="parameters"></a><span data-ttu-id="4314a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4314a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4314a-107">*NewVertexCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4314a-107">*NewVertexCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4314a-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4314a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4314a-109">Nuovo numero di vertici.</span><span class="sxs-lookup"><span data-stu-id="4314a-109">The new number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="4314a-110">*pVertexRemap* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4314a-110">*pVertexRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4314a-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="4314a-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="4314a-112">Puntatore a una matrice di indici dei vertici, che descrivono la modifica del mapping.</span><span class="sxs-lookup"><span data-stu-id="4314a-112">A pointer to an array of vertex indices, which describe the remapping.</span></span> <span data-ttu-id="4314a-113">Si immagini, ad esempio, che SkinInfo contenga alcuni vertici in modo che bone0 sia mappato a V0, bone1 a V1 e bone2 a V2 e che sia specificata una matrice con 2, 1, 0 per pBoneRemap.</span><span class="sxs-lookup"><span data-stu-id="4314a-113">For example, say SkinInfo contains some vertices such that bone0 is mapped to v0, bone1 to v1, and bone2 to v2, and array with 2,1,0 is specified for pBoneRemap.</span></span> <span data-ttu-id="4314a-114">In questo modo verrà eseguito il mapping di bone0 a V2, da bone1 a V1 e da bone2 a V0.</span><span class="sxs-lookup"><span data-stu-id="4314a-114">This will cause bone0 to be mapped to v2, bone1 to v1, and bone2 to v0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4314a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4314a-115">Return value</span></span>

<span data-ttu-id="4314a-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4314a-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4314a-117">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4314a-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="4314a-118">Se il metodo ha esito negativo, il valore restituito può essere: E \_ OutOfMemory o e \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="4314a-118">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="4314a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4314a-119">Requirements</span></span>



| <span data-ttu-id="4314a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4314a-120">Requirement</span></span> | <span data-ttu-id="4314a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4314a-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4314a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4314a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4314a-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="4314a-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="4314a-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="4314a-124">Library</span></span><br/> | <dl> <span data-ttu-id="4314a-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4314a-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4314a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4314a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4314a-127">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="4314a-127">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="4314a-128">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="4314a-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
