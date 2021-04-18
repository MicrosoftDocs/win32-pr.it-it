---
description: Impostare le informazioni di traduzione per un fotogramma chiave specifico nel set di animazioni.
ms.assetid: 4a926c0f-6d57-48d4-bb3b-60766fc78e40
title: 'Metodo ID3DXKeyframedAnimationSet:: SetTranslationKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetTranslationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5bdfb8fb02a2b06dc797317d35cc14e75bd6f221
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323488"
---
# <a name="id3dxkeyframedanimationsetsettranslationkey-method"></a><span data-ttu-id="454c3-103">Metodo ID3DXKeyframedAnimationSet:: SetTranslationKey</span><span class="sxs-lookup"><span data-stu-id="454c3-103">ID3DXKeyframedAnimationSet::SetTranslationKey method</span></span>

<span data-ttu-id="454c3-104">Impostare le informazioni di traduzione per un fotogramma chiave specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="454c3-104">Set translation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="454c3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="454c3-105">Syntax</span></span>


```C++
HRESULT SetTranslationKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pTranslationKey
);
```



## <a name="parameters"></a><span data-ttu-id="454c3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="454c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="454c3-107">*Animazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="454c3-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="454c3-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="454c3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="454c3-109">Indice di animazione.</span><span class="sxs-lookup"><span data-stu-id="454c3-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="454c3-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="454c3-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="454c3-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="454c3-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="454c3-112">Fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="454c3-112">Key Frame.</span></span>

</dd> <dt>

<span data-ttu-id="454c3-113">*pTranslationKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="454c3-113">*pTranslationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="454c3-114">Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="454c3-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="454c3-115">Puntatore ai dati di traduzione.</span><span class="sxs-lookup"><span data-stu-id="454c3-115">Pointer to the translation data.</span></span> <span data-ttu-id="454c3-116">Vedere [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="454c3-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="454c3-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="454c3-117">Return value</span></span>

<span data-ttu-id="454c3-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="454c3-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="454c3-119">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="454c3-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="454c3-120">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="454c3-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="454c3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="454c3-121">Requirements</span></span>



| <span data-ttu-id="454c3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="454c3-122">Requirement</span></span> | <span data-ttu-id="454c3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="454c3-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="454c3-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="454c3-124">Header</span></span><br/>  | <dl> <span data-ttu-id="454c3-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="454c3-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="454c3-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="454c3-126">Library</span></span><br/> | <dl> <span data-ttu-id="454c3-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="454c3-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="454c3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="454c3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="454c3-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="454c3-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
