---
description: Funzione di callback che deve essere implementata da un utente per impostare un codice FVF.
ms.assetid: 701a4333-a71e-4d84-a06c-1c86312ee4ff
title: 'Metodo ID3DXEffectStateManager:: SetFVF (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetFVF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a68ab07e4f486a8df80ecde5844739a6a010c2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323008"
---
# <a name="id3dxeffectstatemanagersetfvf-method"></a><span data-ttu-id="4e842-103">Metodo ID3DXEffectStateManager:: SetFVF</span><span class="sxs-lookup"><span data-stu-id="4e842-103">ID3DXEffectStateManager::SetFVF method</span></span>

<span data-ttu-id="4e842-104">Funzione di callback che deve essere implementata da un utente per impostare un codice FVF.</span><span class="sxs-lookup"><span data-stu-id="4e842-104">A callback function that must be implemented by a user to set a FVF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e842-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e842-105">Syntax</span></span>


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="4e842-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e842-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e842-107">*FVF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e842-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e842-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e842-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e842-109">Costante FVF, che determina come interpretare i dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="4e842-109">The FVF constant, that determines how to interpret vertex data.</span></span> <span data-ttu-id="4e842-110">Vedere [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="4e842-110">See [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e842-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e842-111">Return value</span></span>

<span data-ttu-id="4e842-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4e842-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4e842-113">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e842-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="4e842-114">Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4e842-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="4e842-115">L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="4e842-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="4e842-116">La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf), avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4e842-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e842-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e842-117">Requirements</span></span>



| <span data-ttu-id="4e842-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e842-118">Requirement</span></span> | <span data-ttu-id="4e842-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4e842-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e842-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e842-120">Header</span></span><br/>  | <dl> <span data-ttu-id="4e842-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e842-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="4e842-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="4e842-122">Library</span></span><br/> | <dl> <span data-ttu-id="4e842-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e842-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4e842-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e842-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e842-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="4e842-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
