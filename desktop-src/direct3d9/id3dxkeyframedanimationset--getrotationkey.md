---
description: Ottenere le informazioni sulla rotazione per un fotogramma chiave specifico nel set di animazioni.
ms.assetid: d62b8d5e-328e-4227-b2e8-cb6e5ccc4b3f
title: 'Metodo ID3DXKeyframedAnimationSet:: GetRotationKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetRotationKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8f5bf30eaf261e4baa032ed1411b3d70bddc706c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762311"
---
# <a name="id3dxkeyframedanimationsetgetrotationkey-method"></a><span data-ttu-id="061da-103">Metodo ID3DXKeyframedAnimationSet:: GetRotationKey</span><span class="sxs-lookup"><span data-stu-id="061da-103">ID3DXKeyframedAnimationSet::GetRotationKey method</span></span>

<span data-ttu-id="061da-104">Ottenere le informazioni sulla rotazione per un fotogramma chiave specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="061da-104">Get rotation information for a specific key frame in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="061da-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="061da-105">Syntax</span></span>


```C++
HRESULT GetRotationKey(
  [in] UINT                 Animation,
  [in] UINT                 Key,
  [in] LPD3DXKEY_QUATERNION pRotationKeys
);
```



## <a name="parameters"></a><span data-ttu-id="061da-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="061da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="061da-107">*Animazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="061da-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="061da-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="061da-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="061da-109">Indice di animazione.</span><span class="sxs-lookup"><span data-stu-id="061da-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="061da-110">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="061da-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="061da-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="061da-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="061da-112">Fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="061da-112">Key frame.</span></span>

</dd> <dt>

<span data-ttu-id="061da-113">*pRotationKeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="061da-113">*pRotationKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="061da-114">Tipo: **[ **LPD3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md)**</span><span class="sxs-lookup"><span data-stu-id="061da-114">Type: **[**LPD3DXKEY\_QUATERNION**](d3dxkey-quaternion.md)**</span></span>

<span data-ttu-id="061da-115">Puntatore ai dati di rotazione.</span><span class="sxs-lookup"><span data-stu-id="061da-115">Pointer to the rotation data.</span></span> <span data-ttu-id="061da-116">Vedere [**D3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md).</span><span class="sxs-lookup"><span data-stu-id="061da-116">See [**D3DXKEY\_QUATERNION**](d3dxkey-quaternion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="061da-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="061da-117">Return value</span></span>

<span data-ttu-id="061da-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="061da-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="061da-119">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="061da-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="061da-120">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="061da-120">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="061da-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="061da-121">Requirements</span></span>



| <span data-ttu-id="061da-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="061da-122">Requirement</span></span> | <span data-ttu-id="061da-123">Valore</span><span class="sxs-lookup"><span data-stu-id="061da-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="061da-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="061da-124">Header</span></span><br/>  | <dl> <span data-ttu-id="061da-125"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="061da-125"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="061da-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="061da-126">Library</span></span><br/> | <dl> <span data-ttu-id="061da-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="061da-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="061da-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="061da-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="061da-129">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="061da-129">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
