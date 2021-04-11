---
description: Imposta le informazioni su un callback specifico nel set di animazioni.
ms.assetid: 899f3a85-c878-4eeb-8bda-fc4e9083bd1f
title: 'Metodo ID3DXKeyframedAnimationSet:: SetCallbackKey (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49d3373e0ab0fa221e707ca6eda9ac9bb468a5a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235183"
---
# <a name="id3dxkeyframedanimationsetsetcallbackkey-method"></a><span data-ttu-id="5958d-103">Metodo ID3DXKeyframedAnimationSet:: SetCallbackKey</span><span class="sxs-lookup"><span data-stu-id="5958d-103">ID3DXKeyframedAnimationSet::SetCallbackKey method</span></span>

<span data-ttu-id="5958d-104">Imposta le informazioni su un callback specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="5958d-104">Sets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="5958d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5958d-105">Syntax</span></span>


```C++
HRESULT SetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a><span data-ttu-id="5958d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5958d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5958d-107">*Animazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5958d-107">*Animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5958d-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5958d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5958d-109">Indice di animazione.</span><span class="sxs-lookup"><span data-stu-id="5958d-109">Animation index.</span></span>

</dd> <dt>

<span data-ttu-id="5958d-110">*pCallbackKeys* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5958d-110">*pCallbackKeys* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5958d-111">Tipo: **[ **\_ callback LPD3DXKEY**](d3dxkey-callback.md)**</span><span class="sxs-lookup"><span data-stu-id="5958d-111">Type: **[**LPD3DXKEY\_CALLBACK**](d3dxkey-callback.md)**</span></span>

<span data-ttu-id="5958d-112">Puntatore alla [**funzione di callback**](d3dxkey-callback.md).</span><span class="sxs-lookup"><span data-stu-id="5958d-112">Pointer to the [**callback function**](d3dxkey-callback.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5958d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5958d-113">Return value</span></span>

<span data-ttu-id="5958d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5958d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5958d-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5958d-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5958d-116">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5958d-116">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5958d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5958d-117">Requirements</span></span>



| <span data-ttu-id="5958d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5958d-118">Requirement</span></span> | <span data-ttu-id="5958d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5958d-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5958d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5958d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5958d-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5958d-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5958d-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="5958d-122">Library</span></span><br/> | <dl> <span data-ttu-id="5958d-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5958d-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5958d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5958d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5958d-125">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="5958d-125">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
