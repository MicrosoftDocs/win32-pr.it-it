---
description: Impostare le informazioni sulla scala per un fotogramma chiave specifico nel set di animazioni.
ms.assetid: b606e5d3-11c9-4997-ad3c-d3ae21c32e10
title: 'Metodo ID3DXKeyframedAnimationSet:: SetScaleKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 12ac4d46a2719e452d44d2da67f178e6146b799b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323489"
---
# <a name="id3dxkeyframedanimationsetsetscalekey-method"></a><span data-ttu-id="0b230-103">Metodo ID3DXKeyframedAnimationSet:: SetScaleKey</span><span class="sxs-lookup"><span data-stu-id="0b230-103">ID3DXKeyframedAnimationSet::SetScaleKey method</span></span>

<span data-ttu-id="0b230-104">Impostare le informazioni sulla scala per un fotogramma chiave specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="0b230-104">Set scale information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b230-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b230-105">Syntax</span></span>


```C++
HRESULT SetScaleKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a><span data-ttu-id="0b230-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b230-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b230-107">*Animazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="0b230-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b230-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b230-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b230-109">Indice di animazione.</span><span class="sxs-lookup"><span data-stu-id="0b230-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="0b230-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="0b230-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b230-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0b230-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0b230-112">Fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="0b230-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="0b230-113">*pScaleKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b230-113">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b230-114">Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="0b230-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="0b230-115">Puntatore ai dati della scala.</span><span class="sxs-lookup"><span data-stu-id="0b230-115">Pointer to the scale data.</span></span> <span data-ttu-id="0b230-116">Vedere [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="0b230-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b230-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b230-117">Return value</span></span>

<span data-ttu-id="0b230-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0b230-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0b230-119">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0b230-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="0b230-120">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="0b230-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b230-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b230-121">Requirements</span></span>



| <span data-ttu-id="0b230-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b230-122">Requirement</span></span> | <span data-ttu-id="0b230-123">Valore</span><span class="sxs-lookup"><span data-stu-id="0b230-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b230-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b230-124">Header</span></span><br/>  | <dl> <span data-ttu-id="0b230-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b230-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="0b230-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="0b230-126">Library</span></span><br/> | <dl> <span data-ttu-id="0b230-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b230-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0b230-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b230-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b230-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="0b230-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
