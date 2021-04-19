---
description: Modificare le ossa che influenzano i vertici.
ms.assetid: 0955e0ba-ffc5-408b-ab38-2abd39e1c429
title: 'Metodo ID3DX10SkinInfo:: RemapBones (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 238e4628740fa74e055312c82de2635316f5bde5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322738"
---
# <a name="id3dx10skininforemapbones-method"></a><span data-ttu-id="07420-103">Metodo ID3DX10SkinInfo:: RemapBones</span><span class="sxs-lookup"><span data-stu-id="07420-103">ID3DX10SkinInfo::RemapBones method</span></span>

<span data-ttu-id="07420-104">Modificare le ossa che influenzano i vertici.</span><span class="sxs-lookup"><span data-stu-id="07420-104">Change which bones influence which vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="07420-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07420-105">Syntax</span></span>


```C++
HRESULT RemapBones(
  [in] UINT NewBoneCount,
  [in] UINT *pBoneRemap
);
```



## <a name="parameters"></a><span data-ttu-id="07420-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="07420-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07420-107">*NewBoneCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07420-107">*NewBoneCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07420-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="07420-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="07420-109">Nuovo numero di ossa.</span><span class="sxs-lookup"><span data-stu-id="07420-109">The new number of bones.</span></span>

</dd> <dt>

<span data-ttu-id="07420-110">*pBoneRemap* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07420-110">*pBoneRemap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07420-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="07420-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="07420-112">Puntatore a una matrice di indici di osso, che descrivono la modifica del mapping.</span><span class="sxs-lookup"><span data-stu-id="07420-112">A pointer to an array of bone indices, which describe the remapping.</span></span> <span data-ttu-id="07420-113">Si immagini, ad esempio, che SkinInfo contiene alcune ossa in modo che bone0 sia mappato a V0, bone1 a V1 e bone2 a V2 e che sia specificata una matrice con 2, 1, 0 per pBoneRemap.</span><span class="sxs-lookup"><span data-stu-id="07420-113">For example, say SkinInfo contains some bones such that bone0 is mapped to v0, bone1 to v1, and bone2 to v2, and array with 2,1,0 is specified for pBoneRemap.</span></span> <span data-ttu-id="07420-114">In questo modo verrà eseguito il mapping di bone0 a V2, da bone1 a V1 e da bone2 a V0.</span><span class="sxs-lookup"><span data-stu-id="07420-114">This will cause bone0 to be mapped to v2, bone1 to v1, and bone2 to v0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07420-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07420-115">Return value</span></span>

<span data-ttu-id="07420-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="07420-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="07420-117">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="07420-117">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="07420-118">Se il metodo ha esito negativo, il valore restituito può essere: E \_ OutOfMemory o e \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="07420-118">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="07420-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07420-119">Requirements</span></span>



| <span data-ttu-id="07420-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="07420-120">Requirement</span></span> | <span data-ttu-id="07420-121">Valore</span><span class="sxs-lookup"><span data-stu-id="07420-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07420-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07420-122">Header</span></span><br/>  | <dl> <span data-ttu-id="07420-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="07420-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="07420-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="07420-124">Library</span></span><br/> | <dl> <span data-ttu-id="07420-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07420-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07420-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07420-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07420-127">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="07420-127">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="07420-128">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="07420-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
