---
description: Imposta la quantità di influenza di un dato osso su un vertice specificato.
ms.assetid: adbdc784-c6b4-4e10-85c8-5e0b794d946f
title: 'Metodo ID3DX10SkinInfo:: SetBoneInfluence (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.SetBoneInfluence
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d136ddf4491a2a00c029422512c671a5439ba47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323133"
---
# <a name="id3dx10skininfosetboneinfluence-method"></a><span data-ttu-id="04ffb-103">Metodo ID3DX10SkinInfo:: SetBoneInfluence</span><span class="sxs-lookup"><span data-stu-id="04ffb-103">ID3DX10SkinInfo::SetBoneInfluence method</span></span>

<span data-ttu-id="04ffb-104">Imposta la quantità di influenza di un dato osso su un vertice specificato.</span><span class="sxs-lookup"><span data-stu-id="04ffb-104">Set the amount of influence a given bone has over a given vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="04ffb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04ffb-105">Syntax</span></span>


```C++
HRESULT SetBoneInfluence(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceIndex,
  [in] float Weight
);
```



## <a name="parameters"></a><span data-ttu-id="04ffb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="04ffb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04ffb-107">*BoneIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04ffb-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04ffb-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04ffb-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04ffb-109">Indice che specifica un osso esistente.</span><span class="sxs-lookup"><span data-stu-id="04ffb-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="04ffb-110">Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="04ffb-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="04ffb-111">*InfluenceIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04ffb-111">*InfluenceIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04ffb-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04ffb-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04ffb-113">Indice nell'elenco di vertici dell'osso che influenza.</span><span class="sxs-lookup"><span data-stu-id="04ffb-113">An index into the bone's list of vertices that it influences.</span></span>

</dd> <dt>

<span data-ttu-id="04ffb-114">*Peso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04ffb-114">*Weight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04ffb-115">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="04ffb-115">Type: **float**</span></span>

<span data-ttu-id="04ffb-116">La quantità di influenza, tra 0 e 1, che l'osso ha sul vertice.</span><span class="sxs-lookup"><span data-stu-id="04ffb-116">The amount of influence, between 0 and 1, that the bone has over the vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04ffb-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04ffb-117">Return value</span></span>

<span data-ttu-id="04ffb-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="04ffb-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="04ffb-119">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="04ffb-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="04ffb-120">Se il metodo ha esito negativo, il valore restituito può essere E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="04ffb-120">If the method fails, the return value can be E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="04ffb-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04ffb-121">Requirements</span></span>



| <span data-ttu-id="04ffb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="04ffb-122">Requirement</span></span> | <span data-ttu-id="04ffb-123">Valore</span><span class="sxs-lookup"><span data-stu-id="04ffb-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04ffb-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04ffb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="04ffb-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="04ffb-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="04ffb-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="04ffb-126">Library</span></span><br/> | <dl> <span data-ttu-id="04ffb-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04ffb-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04ffb-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04ffb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04ffb-129">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="04ffb-129">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="04ffb-130">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="04ffb-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
