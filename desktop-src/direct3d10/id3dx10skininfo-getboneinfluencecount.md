---
description: Ottiene il numero di vertici influenzati da un determinato osso.
ms.assetid: e92361ea-4269-4d63-a8d1-560a486b6563
title: 'Metodo ID3DX10SkinInfo:: GetBoneInfluenceCount (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluenceCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 5ad6ddc6ebc80c51e07b7ff0c887371fd45fd42b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322743"
---
# <a name="id3dx10skininfogetboneinfluencecount-method"></a><span data-ttu-id="1bf45-103">Metodo ID3DX10SkinInfo:: GetBoneInfluenceCount</span><span class="sxs-lookup"><span data-stu-id="1bf45-103">ID3DX10SkinInfo::GetBoneInfluenceCount method</span></span>

<span data-ttu-id="1bf45-104">Ottiene il numero di vertici influenzati da un determinato osso.</span><span class="sxs-lookup"><span data-stu-id="1bf45-104">Get the number of vertices that a given bone influences.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bf45-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1bf45-105">Syntax</span></span>


```C++
UINT GetBoneInfluenceCount(
  [in] UINT BoneIndex
);
```



## <a name="parameters"></a><span data-ttu-id="1bf45-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1bf45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bf45-107">*BoneIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1bf45-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bf45-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bf45-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bf45-109">Indice che specifica un osso esistente.</span><span class="sxs-lookup"><span data-stu-id="1bf45-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="1bf45-110">Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="1bf45-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bf45-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1bf45-111">Return value</span></span>

<span data-ttu-id="1bf45-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1bf45-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1bf45-113">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1bf45-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1bf45-114">Se il metodo ha esito negativo, il valore restituito può essere: E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="1bf45-114">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bf45-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1bf45-115">Requirements</span></span>



| <span data-ttu-id="1bf45-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bf45-116">Requirement</span></span> | <span data-ttu-id="1bf45-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1bf45-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1bf45-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1bf45-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1bf45-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bf45-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1bf45-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="1bf45-120">Library</span></span><br/> | <dl> <span data-ttu-id="1bf45-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bf45-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bf45-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1bf45-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bf45-123">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="1bf45-123">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="1bf45-124">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="1bf45-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
