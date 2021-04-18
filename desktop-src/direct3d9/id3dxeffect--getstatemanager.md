---
description: Ottenere il gestore degli Stati dell'effetto.
ms.assetid: 4a09eb2a-2393-40b0-81b9-3c27998c2b77
title: 'Metodo ID3DXEffect:: GetStateManager (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 293b642dfecfa4cc14426addf2567d43dffa7233
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322358"
---
# <a name="id3dxeffectgetstatemanager-method"></a><span data-ttu-id="e0eb5-103">Metodo ID3DXEffect:: GetStateManager</span><span class="sxs-lookup"><span data-stu-id="e0eb5-103">ID3DXEffect::GetStateManager method</span></span>

<span data-ttu-id="e0eb5-104">Ottenere il gestore degli Stati dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="e0eb5-104">Get the effect state manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0eb5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0eb5-105">Syntax</span></span>


```C++
HRESULT GetStateManager(
  [out] LPD3DXEFFECTSTATEMANAGER *ppManager
);
```



## <a name="parameters"></a><span data-ttu-id="e0eb5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0eb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0eb5-107">*ppManager* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e0eb5-107">*ppManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0eb5-108">Tipo: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***</span><span class="sxs-lookup"><span data-stu-id="e0eb5-108">Type: **[**LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***</span></span>

<span data-ttu-id="e0eb5-109">Restituisce un puntatore al gestore di stato.</span><span class="sxs-lookup"><span data-stu-id="e0eb5-109">Returns a pointer to the state manager.</span></span> <span data-ttu-id="e0eb5-110">Vedere [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span><span class="sxs-lookup"><span data-stu-id="e0eb5-110">See [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0eb5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0eb5-111">Return value</span></span>

<span data-ttu-id="e0eb5-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0eb5-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0eb5-113">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e0eb5-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e0eb5-114">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="e0eb5-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0eb5-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0eb5-115">Remarks</span></span>

<span data-ttu-id="e0eb5-116">[**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) è un'interfaccia implementata dall'utente che fornisce callback in un'applicazione per l'impostazione dello stato del dispositivo da un effetto.</span><span class="sxs-lookup"><span data-stu-id="e0eb5-116">The [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) is a user-implemented interface that furnishes callbacks into an application for setting device state from an effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0eb5-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0eb5-117">Requirements</span></span>



| <span data-ttu-id="e0eb5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0eb5-118">Requirement</span></span> | <span data-ttu-id="e0eb5-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e0eb5-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0eb5-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0eb5-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e0eb5-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0eb5-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e0eb5-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="e0eb5-122">Library</span></span><br/> | <dl> <span data-ttu-id="e0eb5-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0eb5-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e0eb5-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0eb5-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0eb5-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="e0eb5-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="e0eb5-126">**ID3DXEffect::SetStateManager**</span><span class="sxs-lookup"><span data-stu-id="e0eb5-126">**ID3DXEffect::SetStateManager**</span></span>](id3dxeffect--setstatemanager.md)
</dt> </dl>

 

 




