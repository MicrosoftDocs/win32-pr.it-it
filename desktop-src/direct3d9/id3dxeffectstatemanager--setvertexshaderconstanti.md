---
description: 'Metodo ID3DXEffectStateManager::SetVertexShaderConstantI: funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti integer di vertex shader.'
ms.assetid: 0035c97a-1b17-4665-9032-7b3b9a9d2cff
title: Metodo ID3DXEffectStateManager::SetVertexShaderConstantI (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c129e3e01fe6fbae6ba7ede1b9ea8c4bee5338a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090399"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstanti-method"></a><span data-ttu-id="b9e6c-103">Metodo ID3DXEffectStateManager::SetVertexShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="b9e6c-103">ID3DXEffectStateManager::SetVertexShaderConstantI method</span></span>

<span data-ttu-id="b9e6c-104">Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti integer vertex shader.</span><span class="sxs-lookup"><span data-stu-id="b9e6c-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9e6c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9e6c-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="b9e6c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9e6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9e6c-107">*StartRegister* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="b9e6c-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e6c-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9e6c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b9e6c-109">Indice in base zero del primo registro delle costanti.</span><span class="sxs-lookup"><span data-stu-id="b9e6c-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="b9e6c-110">*pConstantData* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="b9e6c-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e6c-111">Tipo: **const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="b9e6c-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b9e6c-112">Matrice di costanti integer.</span><span class="sxs-lookup"><span data-stu-id="b9e6c-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="b9e6c-113">*RegisterCount* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="b9e6c-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9e6c-114">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b9e6c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b9e6c-115">Numero di registri in pConstantData.</span><span class="sxs-lookup"><span data-stu-id="b9e6c-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9e6c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9e6c-116">Return value</span></span>

<span data-ttu-id="b9e6c-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b9e6c-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b9e6c-118">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b9e6c-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="b9e6c-119">Se il callback ha esito negativo durante l'impostazione dello stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9e6c-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="b9e6c-120">L'effetto avrà esito negativo durante [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="b9e6c-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="b9e6c-121">La chiamata allo stato dell'effetto dinamico ( ad esempio [**IDirect3DDevice9::SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b9e6c-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9e6c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9e6c-122">Requirements</span></span>



| <span data-ttu-id="b9e6c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9e6c-123">Requirement</span></span> | <span data-ttu-id="b9e6c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b9e6c-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9e6c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9e6c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b9e6c-126"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="b9e6c-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b9e6c-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="b9e6c-127">Library</span></span><br/> | <dl> <span data-ttu-id="b9e6c-128"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9e6c-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b9e6c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9e6c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9e6c-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="b9e6c-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
