---
description: Ottiene un elenco di vertici influenzati da un dato osso e un elenco della quantità di influenza che l'osso ha su ogni vertice.
ms.assetid: d1dea694-874d-4f21-87a8-f6b013617544
title: 'Metodo ID3DX10SkinInfo:: GetBoneInfluences (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.GetBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9aead6b1dd381011a922c5bfbc1874976a78417c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235212"
---
# <a name="id3dx10skininfogetboneinfluences-method"></a><span data-ttu-id="75245-103">Metodo ID3DX10SkinInfo:: GetBoneInfluences</span><span class="sxs-lookup"><span data-stu-id="75245-103">ID3DX10SkinInfo::GetBoneInfluences method</span></span>

<span data-ttu-id="75245-104">Ottiene un elenco di vertici influenzati da un dato osso e un elenco della quantità di influenza che l'osso ha su ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="75245-104">Get a list of vertices that a given bone influences and a list of the amount of influence that bone has on each vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="75245-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75245-105">Syntax</span></span>


```C++
HRESULT GetBoneInfluences(
  [in]      UINT  BoneIndex,
  [in]      UINT  Offset,
  [in]      UINT  Count,
  [in, out] UINT  *pDestIndices,
  [in, out] float *pDestWeights
);
```



## <a name="parameters"></a><span data-ttu-id="75245-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="75245-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75245-107">*BoneIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75245-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75245-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75245-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75245-109">Indice che specifica un osso esistente.</span><span class="sxs-lookup"><span data-stu-id="75245-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="75245-110">Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="75245-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="75245-111">*Offset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75245-111">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75245-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75245-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75245-113">Offset dalla parte superiore dell'elenco dell'osso dei vertici influenzati.</span><span class="sxs-lookup"><span data-stu-id="75245-113">An offset from the top of the bone's list of influenced vertices.</span></span> <span data-ttu-id="75245-114">Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo:: GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).</span><span class="sxs-lookup"><span data-stu-id="75245-114">This must be between 0 and the value returned by [**ID3DX10SkinInfo::GetBoneInfluenceCount**](id3dx10skininfo-getboneinfluencecount.md).</span></span>

</dd> <dt>

<span data-ttu-id="75245-115">*Numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="75245-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75245-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75245-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75245-117">Numero di indici e pesi da recuperare.</span><span class="sxs-lookup"><span data-stu-id="75245-117">The number of indices and weights to retrieve.</span></span> <span data-ttu-id="75245-118">Deve essere compreso tra 0 e il valore restituito da ID3DX10SkinInfo:: GetBoneInfluenceCount.</span><span class="sxs-lookup"><span data-stu-id="75245-118">Must be between 0 and the value returned by ID3DX10SkinInfo::GetBoneInfluenceCount.</span></span>

</dd> <dt>

<span data-ttu-id="75245-119">*pDestIndices* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="75245-119">*pDestIndices* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="75245-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="75245-120">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="75245-121">Elenco di indici nel buffer dei vertici, ciascuno dei quali rappresenta un vertice influenzato dall'osso.</span><span class="sxs-lookup"><span data-stu-id="75245-121">A list of indices into the vertex buffer, each one representing a vertex influenced by the bone.</span></span> <span data-ttu-id="75245-122">Questi valori corrispondono ai valori di pDestWeights, in modo che pDestIndices \[ \] corrisponda a pDestWeights \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="75245-122">These values correspond to the values in pDestWeights, such that pDestIndices\[i\] corresponds to pDestWeights\[i\].</span></span>

</dd> <dt>

<span data-ttu-id="75245-123">*pDestWeights* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="75245-123">*pDestWeights* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="75245-124">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="75245-124">Type: **float\***</span></span>

<span data-ttu-id="75245-125">Elenco della quantità di influenza dell'osso in ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="75245-125">A list of the amount of influence the bone has on each vertex.</span></span> <span data-ttu-id="75245-126">Questi valori corrispondono ai valori di pDestIndices, in modo che pDestWeights \[ \] corrisponda a pDestIndices \[ i \] . f</span><span class="sxs-lookup"><span data-stu-id="75245-126">These values correspond to the values in pDestIndices, such that pDestWeights\[i\] corresponds to pDestIndices\[i\].f</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75245-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75245-127">Return value</span></span>

<span data-ttu-id="75245-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="75245-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="75245-129">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="75245-129">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="75245-130">Se il metodo ha esito negativo, il valore restituito può essere: E \_ INVALIDARG o e \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="75245-130">If the method fails, the return value can be: E\_INVALIDARG or E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="75245-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75245-131">Requirements</span></span>



| <span data-ttu-id="75245-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="75245-132">Requirement</span></span> | <span data-ttu-id="75245-133">Valore</span><span class="sxs-lookup"><span data-stu-id="75245-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="75245-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75245-134">Header</span></span><br/>  | <dl> <span data-ttu-id="75245-135"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="75245-135"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="75245-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="75245-136">Library</span></span><br/> | <dl> <span data-ttu-id="75245-137"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75245-137"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75245-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75245-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75245-139">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="75245-139">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="75245-140">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="75245-140">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
