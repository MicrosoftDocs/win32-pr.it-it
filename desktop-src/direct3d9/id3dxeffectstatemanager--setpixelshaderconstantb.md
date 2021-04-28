---
description: 'Metodo ID3DXEffectStateManager::SetPixelShaderConstantB: funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti booleane vertex shader.'
ms.assetid: ad4d9beb-fd34-4574-9787-61bd3bfaaaaa
title: Metodo ID3DXEffectStateManager::SetPixelShaderConstantB (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ace60b72345c992c3f35943362f6a0958f043aba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090489"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstantb-method"></a><span data-ttu-id="3e6ad-103">Metodo ID3DXEffectStateManager::SetPixelShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="3e6ad-103">ID3DXEffectStateManager::SetPixelShaderConstantB method</span></span>

<span data-ttu-id="3e6ad-104">Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti booleane vertex shader.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-104">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e6ad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e6ad-105">Syntax</span></span>


```C++
HRESULT SetPixelShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="3e6ad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e6ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e6ad-107">*StartRegister* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="3e6ad-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e6ad-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e6ad-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e6ad-109">Indice in base zero del primo registro costante.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="3e6ad-110">*pConstantData* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="3e6ad-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e6ad-111">Tipo: **const [**BOOL**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="3e6ad-111">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3e6ad-112">Matrice di costanti booleane.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-112">An array of Boolean constants.</span></span>

</dd> <dt>

<span data-ttu-id="3e6ad-113">*RegisterCount* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="3e6ad-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e6ad-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e6ad-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e6ad-115">Numero di registri in pConstantData.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e6ad-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e6ad-116">Return value</span></span>

<span data-ttu-id="3e6ad-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3e6ad-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3e6ad-118">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="3e6ad-119">Se il callback ha esito negativo durante l'impostazione dello stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3e6ad-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="3e6ad-120">L'effetto avrà esito negativo durante [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="3e6ad-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="3e6ad-121">La chiamata allo stato dell'effetto dinamico ( ad esempio [**IDirect3DDevice9::SetPixelShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)) avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3e6ad-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e6ad-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e6ad-122">Requirements</span></span>



| <span data-ttu-id="3e6ad-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e6ad-123">Requirement</span></span> | <span data-ttu-id="3e6ad-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3e6ad-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e6ad-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e6ad-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3e6ad-126"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="3e6ad-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="3e6ad-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="3e6ad-127">Library</span></span><br/> | <dl> <span data-ttu-id="3e6ad-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e6ad-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3e6ad-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e6ad-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e6ad-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="3e6ad-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
