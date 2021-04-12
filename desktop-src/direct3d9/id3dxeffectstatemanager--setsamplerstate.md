---
description: Funzione di callback che deve essere implementata da un utente per impostare un campionatore.
ms.assetid: 1e19e8cd-341d-4372-9182-8b3c82155407
title: 'Metodo ID3DXEffectStateManager:: SetSamplerState (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetSamplerState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bba12db8dbc1902adc5c64b4cc1726e081dfea70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355179"
---
# <a name="id3dxeffectstatemanagersetsamplerstate-method"></a><span data-ttu-id="ed9ed-103">Metodo ID3DXEffectStateManager:: SetSamplerState</span><span class="sxs-lookup"><span data-stu-id="ed9ed-103">ID3DXEffectStateManager::SetSamplerState method</span></span>

<span data-ttu-id="ed9ed-104">Funzione di callback che deve essere implementata da un utente per impostare un campionatore.</span><span class="sxs-lookup"><span data-stu-id="ed9ed-104">A callback function that must be implemented by a user to set a sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed9ed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed9ed-105">Syntax</span></span>


```C++
HRESULT SetSamplerState(
  [in] DWORD               Sampler,
  [in] D3DSAMPLERSTATETYPE Type,
  [in] DWORD               Value
);
```



## <a name="parameters"></a><span data-ttu-id="ed9ed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed9ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed9ed-107">*Campionatore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed9ed-107">*Sampler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed9ed-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed9ed-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed9ed-109">Numero di campionatore in base zero.</span><span class="sxs-lookup"><span data-stu-id="ed9ed-109">The zero-based sampler number.</span></span>

</dd> <dt>

<span data-ttu-id="ed9ed-110">*Tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ed9ed-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed9ed-111">Tipo: **[ **D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="ed9ed-111">Type: **[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**</span></span>

<span data-ttu-id="ed9ed-112">Identifica lo stato del campionatore, che può specificare il filtro, l'indirizzamento o il colore del bordo.</span><span class="sxs-lookup"><span data-stu-id="ed9ed-112">Identifies sampler state, which can specify the filtering, addressing, or the border color.</span></span> <span data-ttu-id="ed9ed-113">Vedere [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="ed9ed-113">See [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed9ed-114">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ed9ed-114">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed9ed-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed9ed-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed9ed-116">Valore di uno dei tipi di stato del campionatore nel tipo.</span><span class="sxs-lookup"><span data-stu-id="ed9ed-116">A value from one of the sampler state types in Type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed9ed-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed9ed-117">Return value</span></span>

<span data-ttu-id="ed9ed-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed9ed-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed9ed-119">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed9ed-119">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="ed9ed-120">Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ed9ed-120">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="ed9ed-121">L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="ed9ed-121">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="ed9ed-122">La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate), avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="ed9ed-122">The dynamic effect state call (such as [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed9ed-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed9ed-123">Requirements</span></span>



| <span data-ttu-id="ed9ed-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed9ed-124">Requirement</span></span> | <span data-ttu-id="ed9ed-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ed9ed-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed9ed-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ed9ed-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ed9ed-127"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed9ed-127"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="ed9ed-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="ed9ed-128">Library</span></span><br/> | <dl> <span data-ttu-id="ed9ed-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed9ed-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ed9ed-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed9ed-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed9ed-131">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="ed9ed-131">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
