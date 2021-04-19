---
description: Funzione di callback che deve essere implementata da un utente per impostare lo stato di rendering.
ms.assetid: a5a27e30-c141-44a4-b8d4-38c1d6076b2a
title: 'Metodo ID3DXEffectStateManager:: SetRenderState (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetRenderState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 111ab8ff379d5b095500101674fc45b6a2b31bc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322997"
---
# <a name="id3dxeffectstatemanagersetrenderstate-method"></a><span data-ttu-id="4bf4b-103">Metodo ID3DXEffectStateManager:: SetRenderState</span><span class="sxs-lookup"><span data-stu-id="4bf4b-103">ID3DXEffectStateManager::SetRenderState method</span></span>

<span data-ttu-id="4bf4b-104">Funzione di callback che deve essere implementata da un utente per impostare lo stato di rendering.</span><span class="sxs-lookup"><span data-stu-id="4bf4b-104">A callback function that must be implemented by a user to set render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bf4b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4bf4b-105">Syntax</span></span>


```C++
HRESULT SetRenderState(
  [in] D3DRENDERSTATETYPE State,
  [in] DWORD              Value
);
```



## <a name="parameters"></a><span data-ttu-id="4bf4b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4bf4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bf4b-107">*Stato* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4bf4b-107">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bf4b-108">Tipo: **[ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="4bf4b-108">Type: **[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**</span></span>

<span data-ttu-id="4bf4b-109">Stato di rendering da impostare.</span><span class="sxs-lookup"><span data-stu-id="4bf4b-109">The render state to set.</span></span> [<span data-ttu-id="4bf4b-110">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="4bf4b-110">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)

</dd> <dt>

<span data-ttu-id="4bf4b-111">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4bf4b-111">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bf4b-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4bf4b-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4bf4b-113">Valore dello stato di rendering.</span><span class="sxs-lookup"><span data-stu-id="4bf4b-113">The render state value.</span></span> <span data-ttu-id="4bf4b-114">Vedere [gli Stati degli effetti (Direct3D 9)](effect-states.md).</span><span class="sxs-lookup"><span data-stu-id="4bf4b-114">See [Effect States (Direct3D 9)](effect-states.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bf4b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4bf4b-115">Return value</span></span>

<span data-ttu-id="4bf4b-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4bf4b-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4bf4b-117">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4bf4b-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="4bf4b-118">Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4bf4b-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="4bf4b-119">L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="4bf4b-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="4bf4b-120">La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate), avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4bf4b-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bf4b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4bf4b-121">Requirements</span></span>



| <span data-ttu-id="4bf4b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bf4b-122">Requirement</span></span> | <span data-ttu-id="4bf4b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="4bf4b-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf4b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4bf4b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="4bf4b-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bf4b-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="4bf4b-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="4bf4b-126">Library</span></span><br/> | <dl> <span data-ttu-id="4bf4b-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bf4b-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4bf4b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4bf4b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bf4b-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="4bf4b-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
