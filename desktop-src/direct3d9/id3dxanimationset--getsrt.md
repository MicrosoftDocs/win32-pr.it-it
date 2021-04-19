---
description: Ottiene i valori di scala, rotazione e traslazione del set di animazioni.
ms.assetid: 84fc56f3-15bf-4e27-ad06-57fab94f3a33
title: 'Metodo ID3DXAnimationSet:: GetSRT (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetSRT
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b70243dd9aa2f304d80eaff2e2cc7695dad43379
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323616"
---
# <a name="id3dxanimationsetgetsrt-method"></a><span data-ttu-id="44b7e-103">Metodo ID3DXAnimationSet:: GetSRT</span><span class="sxs-lookup"><span data-stu-id="44b7e-103">ID3DXAnimationSet::GetSRT method</span></span>

<span data-ttu-id="44b7e-104">Ottiene i valori di scala, rotazione e traslazione del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="44b7e-104">Gets the scale, rotation, and translation values of the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="44b7e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44b7e-105">Syntax</span></span>


```C++
HRESULT GetSRT(
  [in]  DOUBLE         PeriodicPosition,
  [in]  UINT           Animation,
  [out] D3DXVECTOR3    *pScale,
  [out] D3DXQUATERNION *pRotation,
  [out] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a><span data-ttu-id="44b7e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="44b7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44b7e-107">*PeriodicPosition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44b7e-107">*PeriodicPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44b7e-108">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44b7e-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44b7e-109">Posizione del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="44b7e-109">Position of the animation set.</span></span> <span data-ttu-id="44b7e-110">La posizione può essere ottenuta chiamando [**ID3DXAnimationSet:: GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md).</span><span class="sxs-lookup"><span data-stu-id="44b7e-110">The position can be obtained by calling [**ID3DXAnimationSet::GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md).</span></span>

</dd> <dt>

<span data-ttu-id="44b7e-111">*Animazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="44b7e-111">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44b7e-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44b7e-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44b7e-113">Indice di animazione.</span><span class="sxs-lookup"><span data-stu-id="44b7e-113">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="44b7e-114">*pScale* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="44b7e-114">*pScale* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44b7e-115">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="44b7e-115">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="44b7e-116">Puntatore al vettore [**D3DXVECTOR3**](d3dxvector3.md) che descrive la scala del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="44b7e-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the scale of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="44b7e-117">*protazione* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="44b7e-117">*pRotation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44b7e-118">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="44b7e-118">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="44b7e-119">Puntatore al quaternione [**D3DXQUATERNION**](d3dxquaternion.md) che descrive la rotazione del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="44b7e-119">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) quaternion that describes the rotation of the animation set.</span></span>

</dd> <dt>

<span data-ttu-id="44b7e-120">*pTranslation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="44b7e-120">*pTranslation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44b7e-121">Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="44b7e-121">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="44b7e-122">Puntatore al vettore [**D3DXVECTOR3**](d3dxvector3.md) che descrive la traduzione del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="44b7e-122">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation of the animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44b7e-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="44b7e-123">Return value</span></span>

<span data-ttu-id="44b7e-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="44b7e-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="44b7e-125">I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="44b7e-125">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="44b7e-126">In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="44b7e-126">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="44b7e-127">In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="44b7e-127">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44b7e-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44b7e-128">Requirements</span></span>



| <span data-ttu-id="44b7e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="44b7e-129">Requirement</span></span> | <span data-ttu-id="44b7e-130">Valore</span><span class="sxs-lookup"><span data-stu-id="44b7e-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44b7e-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="44b7e-131">Header</span></span><br/>  | <dl> <span data-ttu-id="44b7e-132"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="44b7e-132"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="44b7e-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="44b7e-133">Library</span></span><br/> | <dl> <span data-ttu-id="44b7e-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44b7e-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="44b7e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44b7e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44b7e-136">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="44b7e-136">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
