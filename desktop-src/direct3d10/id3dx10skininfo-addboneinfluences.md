---
description: Consentire a un osso esistente di influenzare un gruppo di vertici e definire la quantità di influenza dell'osso su ogni vertice.
ms.assetid: 37ba97a8-ba40-4700-b8b8-fa7cc9118307
title: 'Metodo ID3DX10SkinInfo:: AddBoneInfluences (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8531d70e301b0583309817ac23a36762cacf563f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235034"
---
# <a name="id3dx10skininfoaddboneinfluences-method"></a><span data-ttu-id="7d8c7-103">Metodo ID3DX10SkinInfo:: AddBoneInfluences</span><span class="sxs-lookup"><span data-stu-id="7d8c7-103">ID3DX10SkinInfo::AddBoneInfluences method</span></span>

<span data-ttu-id="7d8c7-104">Consentire a un osso esistente di influenzare un gruppo di vertici e definire la quantità di influenza dell'osso su ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="7d8c7-104">Enable an existing bone to influence a group of vertices and define how much influence the bone has on each vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d8c7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d8c7-105">Syntax</span></span>


```C++
HRESULT AddBoneInfluences(
  [in] UINT  BoneIndex,
  [in] UINT  InfluenceCount,
  [in] UINT  *pIndices,
  [in] float *pWeights
);
```



## <a name="parameters"></a><span data-ttu-id="7d8c7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d8c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d8c7-107">*BoneIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d8c7-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d8c7-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d8c7-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7d8c7-109">Indice che specifica un osso esistente.</span><span class="sxs-lookup"><span data-stu-id="7d8c7-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="7d8c7-110">Deve essere compreso tra 0 e il valore restituito da [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="7d8c7-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> <dt>

<span data-ttu-id="7d8c7-111">*InfluenceCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d8c7-111">*InfluenceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d8c7-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7d8c7-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7d8c7-113">Numero di vertici da aggiungere all'influenza dell'osso.</span><span class="sxs-lookup"><span data-stu-id="7d8c7-113">Number of vertices to add to the bone's influence.</span></span>

</dd> <dt>

<span data-ttu-id="7d8c7-114">*pIndices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d8c7-114">*pIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d8c7-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="7d8c7-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="7d8c7-116">Puntatore a una matrice di indici di vertice.</span><span class="sxs-lookup"><span data-stu-id="7d8c7-116">Pointer to an array of vertex indices.</span></span> <span data-ttu-id="7d8c7-117">Ogni membro di questa matrice ha un membro corrispondente in pWeights, in modo che pIndices \[ i \] corrisponda a pWeights \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="7d8c7-117">Each member of this array has a corresponding member in pWeights, such that pIndices\[i\] corresponds to pWeights\[i\].</span></span> <span data-ttu-id="7d8c7-118">Il valore corrispondente in pWeights \[ \] determina la quantità di influenza che BoneIndex avrà sul vertice indicizzato da pIndices \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="7d8c7-118">The corresponding value in pWeights\[i\] determines how much influence BoneIndex will have on the vertex indexed by pIndices\[i\].</span></span> <span data-ttu-id="7d8c7-119">La dimensione della matrice pIndices deve essere maggiore o uguale a InfluenceCount.</span><span class="sxs-lookup"><span data-stu-id="7d8c7-119">The size of the pIndices array must be equal to or greater than InfluenceCount.</span></span>

</dd> <dt>

<span data-ttu-id="7d8c7-120">*pWeights* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7d8c7-120">*pWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d8c7-121">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="7d8c7-121">Type: **float\***</span></span>

<span data-ttu-id="7d8c7-122">Puntatore a una matrice di pesi ossei.</span><span class="sxs-lookup"><span data-stu-id="7d8c7-122">Pointer to an array of bone weights.</span></span> <span data-ttu-id="7d8c7-123">Ogni membro di questa matrice ha un membro corrispondente in pIndices, in modo che pWeights \[ i \] corrisponda a pIndices \[ i \] .</span><span class="sxs-lookup"><span data-stu-id="7d8c7-123">Each member of this array has a corresponding member in pIndices, such that pWeights\[i\] corresponds to pIndices\[i\].</span></span> <span data-ttu-id="7d8c7-124">Ogni valore in pWeights è compreso tra 0 e 1 e definisce la quantità di influenza che l'osso ha su ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="7d8c7-124">Each value in pWeights is between 0 and 1 and defines the amount of influence the bone has over each vertex.</span></span> <span data-ttu-id="7d8c7-125">La dimensione di pWeights deve essere maggiore o uguale a InfluenceCount.</span><span class="sxs-lookup"><span data-stu-id="7d8c7-125">The size of pWeights must be equal to or greater than InfluenceCount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d8c7-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d8c7-126">Return value</span></span>

<span data-ttu-id="7d8c7-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7d8c7-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7d8c7-128">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7d8c7-128">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="7d8c7-129">Se il metodo ha esito negativo, il valore restituito può essere: E \_ INVALIDARG o e \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="7d8c7-129">If the method fails, the return value can be: E\_INVALIDARG or E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d8c7-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d8c7-130">Requirements</span></span>



| <span data-ttu-id="7d8c7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d8c7-131">Requirement</span></span> | <span data-ttu-id="7d8c7-132">Valore</span><span class="sxs-lookup"><span data-stu-id="7d8c7-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d8c7-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d8c7-133">Header</span></span><br/>  | <dl> <span data-ttu-id="7d8c7-134"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d8c7-134"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7d8c7-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="7d8c7-135">Library</span></span><br/> | <dl> <span data-ttu-id="7d8c7-136"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d8c7-136"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d8c7-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d8c7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d8c7-138">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="7d8c7-138">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="7d8c7-139">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="7d8c7-139">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
