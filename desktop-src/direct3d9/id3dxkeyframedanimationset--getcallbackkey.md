---
description: 'Metodo ID3DXKeyframedAnimationSet::GetCallbackKey: ottiene informazioni su un callback specifico nel set di animazioni.'
ms.assetid: a1d3ca96-2852-420a-aa5c-a434970e5523
title: Metodo ID3DXKeyframedAnimationSet::GetCallbackKey (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f3ebbf93bd482a2259ffdaaf272c65b5e86d5270
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090319"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkey-method"></a><span data-ttu-id="22754-103">Metodo ID3DXKeyframedAnimationSet::GetCallbackKey</span><span class="sxs-lookup"><span data-stu-id="22754-103">ID3DXKeyframedAnimationSet::GetCallbackKey method</span></span>

<span data-ttu-id="22754-104">Ottiene informazioni su un callback specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="22754-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="22754-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22754-105">Syntax</span></span>


```C++
HRESULT GetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="22754-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="22754-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22754-107">*Animazione* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="22754-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22754-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="22754-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="22754-109">Indice dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="22754-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="22754-110">*pCallbackKeys* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="22754-110">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22754-111">Tipo: **[ **CALLBACK LPD3DXKEY \_**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="22754-111">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="22754-112">Puntatore alla [**funzione di callback**](d3dxkey-callback.md).</span><span class="sxs-lookup"><span data-stu-id="22754-112">Pointer to the [**callback function**](d3dxkey-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22754-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22754-113">Return value</span></span>

<span data-ttu-id="22754-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="22754-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="22754-115">Se il metodo ha esito positivo, il valore restituito è S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="22754-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="22754-116">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="22754-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="22754-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22754-117">Requirements</span></span>



| <span data-ttu-id="22754-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="22754-118">Requirement</span></span> | <span data-ttu-id="22754-119">Valore</span><span class="sxs-lookup"><span data-stu-id="22754-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22754-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22754-120">Header</span></span><br/>  | <dl> <span data-ttu-id="22754-121"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="22754-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="22754-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="22754-122">Library</span></span><br/> | <dl> <span data-ttu-id="22754-123"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="22754-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="22754-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22754-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22754-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="22754-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
