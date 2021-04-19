---
description: Funzione di callback che deve essere implementata da un utente per impostare una luce.
ms.assetid: 3b9b2cbd-79f5-4ea4-a47b-da23b091adfd
title: 'Metodo ID3DXEffectStateManager:: selight (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetLight
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1306283b098922706f39abc7ffe2514d2fba0e5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323005"
---
# <a name="id3dxeffectstatemanagersetlight-method"></a><span data-ttu-id="6a2f2-103">Metodo ID3DXEffectStateManager:: selight</span><span class="sxs-lookup"><span data-stu-id="6a2f2-103">ID3DXEffectStateManager::SetLight method</span></span>

<span data-ttu-id="6a2f2-104">Funzione di callback che deve essere implementata da un utente per impostare una luce.</span><span class="sxs-lookup"><span data-stu-id="6a2f2-104">A callback function that must be implemented by a user to set a light.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a2f2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a2f2-105">Syntax</span></span>


```C++
HRESULT SetLight(
  [in]       DWORD     Index,
  [in] const D3DLight9 *pLight
);
```



## <a name="parameters"></a><span data-ttu-id="6a2f2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a2f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a2f2-107">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="6a2f2-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a2f2-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6a2f2-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6a2f2-109">Indice in base zero della luce.</span><span class="sxs-lookup"><span data-stu-id="6a2f2-109">The zero-based index of the light.</span></span> <span data-ttu-id="6a2f2-110">Si tratta dello stesso indice in [**IDirect3DDevice9:: selight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span><span class="sxs-lookup"><span data-stu-id="6a2f2-110">This is the same index in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span></span>

</dd> <dt>

<span data-ttu-id="6a2f2-111">*situazione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a2f2-111">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a2f2-112">Tipo: **const [**D3DLight9**](d3dlight9.md) \***</span><span class="sxs-lookup"><span data-stu-id="6a2f2-112">Type: **const [**D3DLight9**](d3dlight9.md)\***</span></span>

<span data-ttu-id="6a2f2-113">Oggetto chiaro.</span><span class="sxs-lookup"><span data-stu-id="6a2f2-113">The light object.</span></span> <span data-ttu-id="6a2f2-114">Vedere [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="6a2f2-114">See [**D3DLIGHT9**](d3dlight9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a2f2-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a2f2-115">Return value</span></span>

<span data-ttu-id="6a2f2-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6a2f2-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6a2f2-117">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6a2f2-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="6a2f2-118">Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6a2f2-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="6a2f2-119">L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="6a2f2-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="6a2f2-120">La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: selight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight), avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6a2f2-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a2f2-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a2f2-121">Requirements</span></span>



| <span data-ttu-id="6a2f2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a2f2-122">Requirement</span></span> | <span data-ttu-id="6a2f2-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6a2f2-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a2f2-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a2f2-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6a2f2-125"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a2f2-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6a2f2-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="6a2f2-126">Library</span></span><br/> | <dl> <span data-ttu-id="6a2f2-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a2f2-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6a2f2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a2f2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a2f2-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="6a2f2-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
