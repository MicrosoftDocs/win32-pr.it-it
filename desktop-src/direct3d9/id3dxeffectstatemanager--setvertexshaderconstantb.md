---
description: 'Metodo ID3DXEffectStateManager::SetVertexShaderConstantB: funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti booleane vertex shader.'
ms.assetid: 25fd0c68-11b5-4401-a2f8-86075ba3fa54
title: Metodo ID3DXEffectStateManager::SetVertexShaderConstantB (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantB
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 79d4972c301d7333869d68d36267186a67b37eb1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090409"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantb-method"></a><span data-ttu-id="885ee-103">Metodo ID3DXEffectStateManager::SetVertexShaderConstantB</span><span class="sxs-lookup"><span data-stu-id="885ee-103">ID3DXEffectStateManager::SetVertexShaderConstantB method</span></span>

<span data-ttu-id="885ee-104">Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti booleane vertex shader.</span><span class="sxs-lookup"><span data-stu-id="885ee-104">A callback function that must be implemented by a user to set an array of vertex shader Boolean constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="885ee-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="885ee-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantB(
  [out]       UINT StartRegister,
  [out] const BOOL *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="885ee-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="885ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="885ee-107">*StartRegister* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="885ee-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="885ee-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="885ee-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="885ee-109">Indice in base zero del primo registro costante.</span><span class="sxs-lookup"><span data-stu-id="885ee-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="885ee-110">*pConstantData* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="885ee-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="885ee-111">Tipo: **const [**BOOL**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="885ee-111">Type: **const [**BOOL**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="885ee-112">Matrice di costanti booleane.</span><span class="sxs-lookup"><span data-stu-id="885ee-112">An array of Boolean constants.</span></span>

</dd> <dt>

<span data-ttu-id="885ee-113">*RegisterCount* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="885ee-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="885ee-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="885ee-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="885ee-115">Numero di registri in pConstantData.</span><span class="sxs-lookup"><span data-stu-id="885ee-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="885ee-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="885ee-116">Return value</span></span>

<span data-ttu-id="885ee-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="885ee-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="885ee-118">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="885ee-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="885ee-119">Se il callback non riesce quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="885ee-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="885ee-120">L'effetto avrà esito negativo [**durante ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="885ee-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="885ee-121">La chiamata dello stato dell'effetto dinamico ( [**ad esempio IDirect3DDevice9::SetVertexShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)) avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="885ee-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantB**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="885ee-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="885ee-122">Requirements</span></span>



| <span data-ttu-id="885ee-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="885ee-123">Requirement</span></span> | <span data-ttu-id="885ee-124">Valore</span><span class="sxs-lookup"><span data-stu-id="885ee-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="885ee-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="885ee-125">Header</span></span><br/>  | <dl> <span data-ttu-id="885ee-126"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="885ee-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="885ee-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="885ee-127">Library</span></span><br/> | <dl> <span data-ttu-id="885ee-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="885ee-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="885ee-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="885ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="885ee-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="885ee-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
