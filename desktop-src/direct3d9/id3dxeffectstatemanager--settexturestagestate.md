---
description: Funzione di callback che deve essere implementata da un utente per impostare lo stato della fase della trama.
ms.assetid: cc86a483-ccf0-400d-b14d-ab55a3cf4b98
title: 'Metodo ID3DXEffectStateManager:: SetTextureStageState (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTextureStageState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 937fd3f2b89dc093d9dceb9441f53d6be2cb06b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323080"
---
# <a name="id3dxeffectstatemanagersettexturestagestate-method"></a><span data-ttu-id="4db41-103">Metodo ID3DXEffectStateManager:: SetTextureStageState</span><span class="sxs-lookup"><span data-stu-id="4db41-103">ID3DXEffectStateManager::SetTextureStageState method</span></span>

<span data-ttu-id="4db41-104">Funzione di callback che deve essere implementata da un utente per impostare lo stato della fase della trama.</span><span class="sxs-lookup"><span data-stu-id="4db41-104">A callback function that must be implemented by a user to set the texture stage state.</span></span>

## <a name="syntax"></a><span data-ttu-id="4db41-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4db41-105">Syntax</span></span>


```C++
HRESULT SetTextureStageState(
  [in] DWORD                    Stage,
  [in] D3DTEXTURESTAGESTATETYPE Type,
  [in] DWORD                    Value
);
```



## <a name="parameters"></a><span data-ttu-id="4db41-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4db41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4db41-107">*Fase* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4db41-107">*Stage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db41-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4db41-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4db41-109">Fase a cui è assegnata la trama.</span><span class="sxs-lookup"><span data-stu-id="4db41-109">The stage that the texture is assigned to.</span></span> <span data-ttu-id="4db41-110">Si tratta del valore di indice in [**IDirect3DDevice9:: setexture**](/windows/desktop/api) o [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span><span class="sxs-lookup"><span data-stu-id="4db41-110">This is the index value in [**IDirect3DDevice9::SetTexture**](/windows/desktop/api) or [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span>

</dd> <dt>

<span data-ttu-id="4db41-111">*Tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4db41-111">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db41-112">Tipo: **[ **D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="4db41-112">Type: **[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**</span></span>

<span data-ttu-id="4db41-113">Definisce il tipo di operazione che viene eseguita da una fase della trama.</span><span class="sxs-lookup"><span data-stu-id="4db41-113">Defines the type of operation that a texture stage will perform.</span></span> <span data-ttu-id="4db41-114">Vedere [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span><span class="sxs-lookup"><span data-stu-id="4db41-114">See [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="4db41-115">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4db41-115">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db41-116">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4db41-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4db41-117">Può essere un'operazione ([**D3DTEXTUREOP**](./d3dtextureop.md)) o un valore di argomento ([D3DTA](d3dta.md)), a seconda di ciò che viene scelto per il tipo.</span><span class="sxs-lookup"><span data-stu-id="4db41-117">Can be either an operation ([**D3DTEXTUREOP**](./d3dtextureop.md)) or an argument value ([D3DTA](d3dta.md)), depending on what is chosen for Type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4db41-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4db41-118">Return value</span></span>

<span data-ttu-id="4db41-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4db41-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4db41-120">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4db41-120">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="4db41-121">Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4db41-121">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="4db41-122">L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="4db41-122">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="4db41-123">La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate), avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="4db41-123">The dynamic effect state call (such as [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="4db41-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4db41-124">Requirements</span></span>



| <span data-ttu-id="4db41-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4db41-125">Requirement</span></span> | <span data-ttu-id="4db41-126">Valore</span><span class="sxs-lookup"><span data-stu-id="4db41-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4db41-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4db41-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4db41-128"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4db41-128"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="4db41-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="4db41-129">Library</span></span><br/> | <dl> <span data-ttu-id="4db41-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4db41-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4db41-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4db41-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db41-132">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="4db41-132">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
