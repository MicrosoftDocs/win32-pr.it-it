---
description: 'Metodo ID3DXEffectStateManager::SetVertexShaderConstantF: funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti a virgola mobile vertex shader.'
ms.assetid: 3a13040d-5d5a-4454-bf11-cda9653585c0
title: Metodo ID3DXEffectStateManager::SetVertexShaderConstantF (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ffbad3c695758a0388baf8161c322c1ff423699b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090389"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantf-method"></a><span data-ttu-id="b511c-103">Metodo ID3DXEffectStateManager::SetVertexShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="b511c-103">ID3DXEffectStateManager::SetVertexShaderConstantF method</span></span>

<span data-ttu-id="b511c-104">Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti a virgola mobile vertex shader.</span><span class="sxs-lookup"><span data-stu-id="b511c-104">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="b511c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b511c-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="b511c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b511c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b511c-107">*StartRegister* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="b511c-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b511c-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b511c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b511c-109">Indice in base zero del primo registro costante.</span><span class="sxs-lookup"><span data-stu-id="b511c-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="b511c-110">*pConstantData* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="b511c-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b511c-111">Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b511c-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b511c-112">Matrice di costanti a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="b511c-112">An array of floating-point constants.</span></span>

</dd> <dt>

<span data-ttu-id="b511c-113">*RegisterCount* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="b511c-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b511c-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b511c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b511c-115">Numero di registri in pConstantData.</span><span class="sxs-lookup"><span data-stu-id="b511c-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b511c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b511c-116">Return value</span></span>

<span data-ttu-id="b511c-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b511c-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b511c-118">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b511c-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="b511c-119">Se il callback ha esito negativo durante l'impostazione dello stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b511c-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="b511c-120">L'effetto avrà esito negativo durante [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="b511c-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="b511c-121">La chiamata allo stato dell'effetto dinamico ( ad esempio [**IDirect3DDevice9::SetVertexShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b511c-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="b511c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b511c-122">Requirements</span></span>



| <span data-ttu-id="b511c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b511c-123">Requirement</span></span> | <span data-ttu-id="b511c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b511c-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b511c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b511c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b511c-126"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="b511c-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b511c-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="b511c-127">Library</span></span><br/> | <dl> <span data-ttu-id="b511c-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b511c-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b511c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b511c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b511c-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="b511c-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
