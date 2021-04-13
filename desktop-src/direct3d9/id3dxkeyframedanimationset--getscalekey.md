---
description: Ottenere informazioni sulla scala per un fotogramma chiave specifico nel set di animazioni.
ms.assetid: 7f4a0bf3-2922-4fd7-bb85-b387d3e983a7
title: 'Metodo ID3DXKeyframedAnimationSet:: GetScaleKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58cbd432404fcd511140a7368999161f5e44f77f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355724"
---
# <a name="id3dxkeyframedanimationsetgetscalekey-method"></a><span data-ttu-id="d4471-103">Metodo ID3DXKeyframedAnimationSet:: GetScaleKey</span><span class="sxs-lookup"><span data-stu-id="d4471-103">ID3DXKeyframedAnimationSet::GetScaleKey method</span></span>

<span data-ttu-id="d4471-104">Ottenere informazioni sulla scala per un fotogramma chiave specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="d4471-104">Get scale information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4471-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4471-105">Syntax</span></span>


```C++
HRESULT GetScaleKey(
  [in] UINT              Animation,
  [in] UINT              Key,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a><span data-ttu-id="d4471-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4471-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4471-107">*Animazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d4471-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4471-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4471-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4471-109">Indice di animazione.</span><span class="sxs-lookup"><span data-stu-id="d4471-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="d4471-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d4471-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4471-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d4471-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d4471-112">Fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="d4471-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="d4471-113">*pScaleKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4471-113">*pScaleKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4471-114">Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**</span><span class="sxs-lookup"><span data-stu-id="d4471-114">Type: **[**LPD3DXKEY\_VECTOR3**](d3dxkey-vector3.md)**</span></span>

<span data-ttu-id="d4471-115">Puntatore ai dati della scala.</span><span class="sxs-lookup"><span data-stu-id="d4471-115">Pointer to the scale data.</span></span> <span data-ttu-id="d4471-116">Vedere [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).</span><span class="sxs-lookup"><span data-stu-id="d4471-116">See [**D3DXKEY\_VECTOR3**](d3dxkey-vector3.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4471-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4471-117">Return value</span></span>

<span data-ttu-id="d4471-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d4471-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d4471-119">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d4471-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d4471-120">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d4471-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4471-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4471-121">Requirements</span></span>



| <span data-ttu-id="d4471-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4471-122">Requirement</span></span> | <span data-ttu-id="d4471-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d4471-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4471-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4471-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d4471-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4471-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="d4471-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="d4471-126">Library</span></span><br/> | <dl> <span data-ttu-id="d4471-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4471-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d4471-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4471-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4471-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="d4471-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
