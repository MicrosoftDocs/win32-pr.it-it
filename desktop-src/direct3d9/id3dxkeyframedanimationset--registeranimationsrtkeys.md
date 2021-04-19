---
description: Registrare i dati del fotogramma chiave SRT (scale, Rotate e translate) per un'animazione.
ms.assetid: 10e5b391-1529-4952-abbb-ef560a35d667
title: 'Metodo ID3DXKeyframedAnimationSet:: RegisterAnimationSRTKeys (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.RegisterAnimationSRTKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3098c8e779834daf273d5e85469e3f45b01cb039
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323492"
---
# <a name="id3dxkeyframedanimationsetregisteranimationsrtkeys-method"></a><span data-ttu-id="036eb-103">Metodo ID3DXKeyframedAnimationSet:: RegisterAnimationSRTKeys</span><span class="sxs-lookup"><span data-stu-id="036eb-103">ID3DXKeyframedAnimationSet::RegisterAnimationSRTKeys method</span></span>

<span data-ttu-id="036eb-104">Registrare i dati del fotogramma chiave SRT (scale, Rotate e translate) per un'animazione.</span><span class="sxs-lookup"><span data-stu-id="036eb-104">Register the scale, rotate, and translate (SRT) key frame data for an animation.</span></span>

## <a name="syntax"></a><span data-ttu-id="036eb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="036eb-105">Syntax</span></span>


```C++
HRESULT RegisterAnimationSRTKeys(
  [in]        LPCSTR               pName,
  [in]        UINT                 NumScaleKeys,
  [in]        UINT                 NumRotationKeys,
  [in]        UINT                 NumTranslationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pScaleKeys,
  [in]  const LPD3DXKEY_QUATERNION *pRotationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pTranslationKeys,
  [out]       DWORD                *pAnimationIndex
);
```



## <a name="parameters"></a><span data-ttu-id="036eb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="036eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="036eb-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="036eb-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="036eb-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="036eb-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="036eb-109">Puntatore al nome dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="036eb-109">Pointer to the animation name.</span></span>

</dd> <dt>

<span data-ttu-id="036eb-110">*NumScaleKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="036eb-110">*NumScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="036eb-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="036eb-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="036eb-112">Numero di chiavi di scala.</span><span class="sxs-lookup"><span data-stu-id="036eb-112">Number of scale keys.</span></span>

</dd> <dt>

<span data-ttu-id="036eb-113">*NumRotationKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="036eb-113">*NumRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="036eb-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="036eb-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="036eb-115">Numero di chiavi di rotazione.</span><span class="sxs-lookup"><span data-stu-id="036eb-115">Number of rotation keys.</span></span>

</dd> <dt>

<span data-ttu-id="036eb-116">*NumTranslationKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="036eb-116">*NumTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="036eb-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="036eb-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="036eb-118">Numero di chiavi di conversione.</span><span class="sxs-lookup"><span data-stu-id="036eb-118">Number of translation keys.</span></span>

</dd> <dt>

<span data-ttu-id="036eb-119">*pScaleKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="036eb-119">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="036eb-120">Tipo: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="036eb-120">Type: **const [**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)\***</span></span>

<span data-ttu-id="036eb-121">Indirizzo di un puntatore a una matrice allocata dall'utente di vettori [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) che il metodo compila con i dati di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="036eb-121">Address of a pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method fills with scale data.</span></span>

</dd> <dt>

<span data-ttu-id="036eb-122">*pRotationKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="036eb-122">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="036eb-123">Tipo: **const [**LPD3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="036eb-123">Type: **const [**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)\***</span></span>

<span data-ttu-id="036eb-124">Indirizzo di un puntatore a una matrice allocata dall'utente di quaternioni [**\_ Quaternion D3DXKEY**](d3dxkey-quaternion.md) che il metodo compila con i dati di rotazione.</span><span class="sxs-lookup"><span data-stu-id="036eb-124">Address of a pointer to a user-allocated array of [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md) quaternions that the method fills with rotation data.</span></span>

</dd> <dt>

<span data-ttu-id="036eb-125">*pTranslationKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="036eb-125">*pTranslationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="036eb-126">Tipo: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="036eb-126">Type: **const [**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)\***</span></span>

<span data-ttu-id="036eb-127">Indirizzo di un puntatore a una matrice allocata dall'utente di vettori [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) che il metodo compila con i dati di traduzione.</span><span class="sxs-lookup"><span data-stu-id="036eb-127">Address of a pointer to a user-allocated array of [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md) vectors that the method fills with translation data.</span></span>

</dd> <dt>

<span data-ttu-id="036eb-128">*pAnimationIndex* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="036eb-128">*pAnimationIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="036eb-129">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="036eb-129">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="036eb-130">Restituisce l'indice di animazione.</span><span class="sxs-lookup"><span data-stu-id="036eb-130">Returns the animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="036eb-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="036eb-131">Return value</span></span>

<span data-ttu-id="036eb-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="036eb-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="036eb-133">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="036eb-133">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="036eb-134">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="036eb-134">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="036eb-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="036eb-135">Requirements</span></span>



| <span data-ttu-id="036eb-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="036eb-136">Requirement</span></span> | <span data-ttu-id="036eb-137">Valore</span><span class="sxs-lookup"><span data-stu-id="036eb-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="036eb-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="036eb-138">Header</span></span><br/>  | <dl> <span data-ttu-id="036eb-139"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="036eb-139"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="036eb-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="036eb-140">Library</span></span><br/> | <dl> <span data-ttu-id="036eb-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="036eb-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="036eb-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="036eb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="036eb-143">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="036eb-143">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> <dt>

[<span data-ttu-id="036eb-144">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span><span class="sxs-lookup"><span data-stu-id="036eb-144">**ID3DXKeyframedAnimationSet::GetNumScaleKeys**</span></span>](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> <dt>

[<span data-ttu-id="036eb-145">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span><span class="sxs-lookup"><span data-stu-id="036eb-145">**ID3DXKeyframedAnimationSet::GetNumRotationKeys**</span></span>](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> <dt>

[<span data-ttu-id="036eb-146">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span><span class="sxs-lookup"><span data-stu-id="036eb-146">**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**</span></span>](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
