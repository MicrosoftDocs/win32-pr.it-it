---
description: Ottiene le informazioni di conversione per un fotogramma chiave specifico nel set di animazioni.
ms.assetid: 757af408-8a9c-4294-9343-91f52d4cc1ab
title: 'Metodo ID3DXKeyframedAnimationSet:: GetTranslationKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f61d1caecb46477d16be4367588ab5609bfd6224
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323497"
---
# <a name="id3dxkeyframedanimationsetgettranslationkey-method"></a><span data-ttu-id="6d3ca-103">Metodo ID3DXKeyframedAnimationSet:: GetTranslationKey</span><span class="sxs-lookup"><span data-stu-id="6d3ca-103">ID3DXKeyframedAnimationSet::GetTranslationKey method</span></span>

<span data-ttu-id="6d3ca-104">Ottiene le informazioni di conversione per un fotogramma chiave specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="6d3ca-104">Get translation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d3ca-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d3ca-105">Syntax</span></span>


```C++
HRESULT GetTranslationKey(
  [in]  UINT              Animation,
  [in]  UINT              Key,
  [out] LPD3DXKEY_VECTOR3 pTranslationKey
);
```



## <a name="parameters"></a><span data-ttu-id="6d3ca-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6d3ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d3ca-107">*Animazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="6d3ca-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d3ca-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3ca-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6d3ca-109">Indice di animazione.</span><span class="sxs-lookup"><span data-stu-id="6d3ca-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="6d3ca-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="6d3ca-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d3ca-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3ca-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6d3ca-112">Fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="6d3ca-112">Key Frame.</span></span>

</dd> <dt>

<span data-ttu-id="6d3ca-113">*pTranslationKey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6d3ca-113">*pTranslationKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d3ca-114">Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="6d3ca-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="6d3ca-115">Puntatore alle informazioni di rotazione.</span><span class="sxs-lookup"><span data-stu-id="6d3ca-115">Pointer to the rotation information.</span></span> <span data-ttu-id="6d3ca-116">Vedere [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="6d3ca-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d3ca-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6d3ca-117">Return value</span></span>

<span data-ttu-id="6d3ca-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6d3ca-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6d3ca-119">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6d3ca-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6d3ca-120">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6d3ca-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d3ca-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d3ca-121">Requirements</span></span>



| <span data-ttu-id="6d3ca-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d3ca-122">Requirement</span></span> | <span data-ttu-id="6d3ca-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6d3ca-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d3ca-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d3ca-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6d3ca-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d3ca-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="6d3ca-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="6d3ca-126">Library</span></span><br/> | <dl> <span data-ttu-id="6d3ca-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d3ca-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6d3ca-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d3ca-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d3ca-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="6d3ca-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
