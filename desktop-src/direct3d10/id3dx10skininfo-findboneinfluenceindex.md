---
description: Trovare l'indice che indica la posizione in cui un vertice specificato si trova in un elenco di vertici influenzato di un dato osso.
ms.assetid: vs|directx_sdk|~\id3dx10skininfo_findboneinfluenceindex.htm
title: 'Metodo ID3DX10SkinInfo:: FindBoneInfluenceIndex (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.FindBoneInfluenceIndex
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1468fed3c0cf999e7635ba0f5ae53cee72fe70c6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235111"
---
# <a name="id3dx10skininfofindboneinfluenceindex-method"></a><span data-ttu-id="69319-103">Metodo ID3DX10SkinInfo:: FindBoneInfluenceIndex</span><span class="sxs-lookup"><span data-stu-id="69319-103">ID3DX10SkinInfo::FindBoneInfluenceIndex method</span></span>

<span data-ttu-id="69319-104">Trovare l'indice che indica la posizione in cui un vertice specificato si trova in un elenco di vertici influenzato di un dato osso.</span><span class="sxs-lookup"><span data-stu-id="69319-104">Find the index that indicates where a given vertex is in a given bone's list of influenced vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="69319-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69319-105">Syntax</span></span>


```C++
HRESULT FindBoneInfluenceIndex(
  [in] UINT BoneIndex,
  [in] UINT VertexIndex,
  [in] UINT *pInfluenceIndex
);
```



## <a name="parameters"></a><span data-ttu-id="69319-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="69319-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69319-107">*BoneIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69319-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69319-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69319-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69319-109">Indice che specifica un osso esistente.</span><span class="sxs-lookup"><span data-stu-id="69319-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="69319-110">Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="69319-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="69319-111">*VertexIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69319-111">*VertexIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69319-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="69319-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="69319-113">Indice del vertice nel buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="69319-113">The index of the vertex in the vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="69319-114">*pInfluenceIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69319-114">*pInfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69319-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="69319-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="69319-116">Indice del vertice nell'elenco dell'osso dei vertici influenzati.</span><span class="sxs-lookup"><span data-stu-id="69319-116">The index of the vertex in the bone's list of influenced vertices.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69319-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="69319-117">Return value</span></span>

<span data-ttu-id="69319-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="69319-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="69319-119">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="69319-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="69319-120">Se il metodo ha esito negativo, il valore restituito può essere: E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="69319-120">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="69319-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="69319-121">Requirements</span></span>



| <span data-ttu-id="69319-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="69319-122">Requirement</span></span> | <span data-ttu-id="69319-123">Valore</span><span class="sxs-lookup"><span data-stu-id="69319-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="69319-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="69319-124">Header</span></span><br/>  | <dl> <span data-ttu-id="69319-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="69319-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="69319-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="69319-126">Library</span></span><br/> | <dl> <span data-ttu-id="69319-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69319-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69319-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69319-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69319-129">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="69319-129">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="69319-130">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="69319-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
