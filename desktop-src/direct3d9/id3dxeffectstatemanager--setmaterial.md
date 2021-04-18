---
description: Funzione di callback che deve essere implementata da un utente per impostare lo stato del materiale.
ms.assetid: 4c5e903f-551b-4346-a5eb-301a3a5b9b44
title: 'Metodo ID3DXEffectStateManager:: sematerial (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetMaterial
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b503bd195468fb323e7e655c0bdd201e25dfdce2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323003"
---
# <a name="id3dxeffectstatemanagersetmaterial-method"></a><span data-ttu-id="9364f-103">Metodo ID3DXEffectStateManager:: sematerial</span><span class="sxs-lookup"><span data-stu-id="9364f-103">ID3DXEffectStateManager::SetMaterial method</span></span>

<span data-ttu-id="9364f-104">Funzione di callback che deve essere implementata da un utente per impostare lo stato del materiale.</span><span class="sxs-lookup"><span data-stu-id="9364f-104">A callback function that must be implemented by a user to set material state.</span></span>

## <a name="syntax"></a><span data-ttu-id="9364f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9364f-105">Syntax</span></span>


```C++
HRESULT SetMaterial(
  [in] const D3DMATERIAL9 *pMaterial
);
```



## <a name="parameters"></a><span data-ttu-id="9364f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9364f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9364f-107">*pMaterial* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9364f-107">*pMaterial* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9364f-108">Tipo: **const [**D3DMATERIAL9**](d3dmaterial9.md) \***</span><span class="sxs-lookup"><span data-stu-id="9364f-108">Type: **const [**D3DMATERIAL9**](d3dmaterial9.md)\***</span></span>

<span data-ttu-id="9364f-109">Puntatore allo stato del materiale.</span><span class="sxs-lookup"><span data-stu-id="9364f-109">A pointer to the material state.</span></span> <span data-ttu-id="9364f-110">Vedere [**D3DMATERIAL9**](d3dmaterial9.md).</span><span class="sxs-lookup"><span data-stu-id="9364f-110">See [**D3DMATERIAL9**](d3dmaterial9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9364f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9364f-111">Return value</span></span>

<span data-ttu-id="9364f-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9364f-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9364f-113">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9364f-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="9364f-114">Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9364f-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="9364f-115">L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="9364f-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="9364f-116">La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: sematerial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial), avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="9364f-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="9364f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9364f-117">Requirements</span></span>



| <span data-ttu-id="9364f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9364f-118">Requirement</span></span> | <span data-ttu-id="9364f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9364f-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9364f-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9364f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9364f-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9364f-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="9364f-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="9364f-122">Library</span></span><br/> | <dl> <span data-ttu-id="9364f-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9364f-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9364f-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9364f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9364f-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="9364f-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
