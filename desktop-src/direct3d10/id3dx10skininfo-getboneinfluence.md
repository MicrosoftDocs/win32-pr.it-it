---
description: Ottenere la quantità di influenza di un dato osso su un vertice specificato.
ms.assetid: 0586fdfd-e5b1-4699-b489-c54a0f305ee4
title: 'Metodo ID3DX10SkinInfo:: GetBoneInfluence (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b2f7e6b75e9c0f9f08463b6dacf9d7c9d72f4f28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323134"
---
# <a name="id3dx10skininfogetboneinfluence-method"></a><span data-ttu-id="1da10-103">Metodo ID3DX10SkinInfo:: GetBoneInfluence</span><span class="sxs-lookup"><span data-stu-id="1da10-103">ID3DX10SkinInfo::GetBoneInfluence method</span></span>

<span data-ttu-id="1da10-104">Ottenere la quantità di influenza di un dato osso su un vertice specificato.</span><span class="sxs-lookup"><span data-stu-id="1da10-104">Get the amount of influence a given bone has over a given vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="1da10-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1da10-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float *pWeight
);
```



## <a name="parameters"></a><span data-ttu-id="1da10-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1da10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1da10-107">*BoneIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1da10-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1da10-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1da10-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1da10-109">Indice che specifica un osso esistente.</span><span class="sxs-lookup"><span data-stu-id="1da10-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="1da10-110">Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="1da10-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="1da10-111">*InfluenceIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1da10-111">*InfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1da10-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1da10-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1da10-113">Indice nell'elenco di vertici dell'osso che influenza.</span><span class="sxs-lookup"><span data-stu-id="1da10-113">An index into the bone's list of vertices that it influences.</span></span>

</dd> <dt>

<span data-ttu-id="1da10-114">*pWeight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1da10-114">*pWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1da10-115">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="1da10-115">Type: **float\***</span></span>

<span data-ttu-id="1da10-116">La quantità di influenza, tra 0 e 1, che l'osso ha sul vertice.</span><span class="sxs-lookup"><span data-stu-id="1da10-116">The amount of influence, between 0 and 1, that the bone has over the vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1da10-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1da10-117">Return value</span></span>

<span data-ttu-id="1da10-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1da10-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1da10-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1da10-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1da10-120">Se il metodo ha esito negativo, il valore restituito può essere E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="1da10-120">If the method fails, the return value can be E\_INVALIDARG.</span></span>

## <a name="remarks"></a><span data-ttu-id="1da10-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="1da10-121">Remarks</span></span>

<span data-ttu-id="1da10-122">Usare ID3DX10SkinInfo:: GetBoneInfluenceCount per determinare il numero di vertici influenzati dall'osso.</span><span class="sxs-lookup"><span data-stu-id="1da10-122">Use ID3DX10SkinInfo::GetBoneInfluenceCount to find out how many vertices the bone influences.</span></span>

## <a name="requirements"></a><span data-ttu-id="1da10-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1da10-123">Requirements</span></span>



| <span data-ttu-id="1da10-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1da10-124">Requirement</span></span> | <span data-ttu-id="1da10-125">Valore</span><span class="sxs-lookup"><span data-stu-id="1da10-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1da10-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1da10-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1da10-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1da10-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1da10-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="1da10-128">Library</span></span><br/> | <dl> <span data-ttu-id="1da10-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1da10-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1da10-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1da10-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1da10-131">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="1da10-131">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="1da10-132">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="1da10-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
