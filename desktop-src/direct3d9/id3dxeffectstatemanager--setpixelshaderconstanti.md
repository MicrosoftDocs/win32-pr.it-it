---
description: Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti integer del vertex shader.
ms.assetid: 55f5747d-b7f8-4d13-ac2c-df2dcb160091
title: 'Metodo ID3DXEffectStateManager:: SetPixelShaderConstantI (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2e84d883370038435dc59bb948ef94fcd82223db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322999"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstanti-method"></a><span data-ttu-id="60fcf-103">Metodo ID3DXEffectStateManager:: SetPixelShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="60fcf-103">ID3DXEffectStateManager::SetPixelShaderConstantI method</span></span>

<span data-ttu-id="60fcf-104">Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti integer del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="60fcf-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="60fcf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60fcf-105">Syntax</span></span>


```C++
HRESULT SetPixelShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="60fcf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="60fcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60fcf-107">*StartRegister* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="60fcf-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60fcf-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60fcf-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60fcf-109">Indice in base zero del primo registro costante.</span><span class="sxs-lookup"><span data-stu-id="60fcf-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="60fcf-110">*pConstantData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="60fcf-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60fcf-111">Tipo: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="60fcf-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="60fcf-112">Matrice di costanti integer.</span><span class="sxs-lookup"><span data-stu-id="60fcf-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="60fcf-113">*RegisterCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="60fcf-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60fcf-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60fcf-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60fcf-115">Numero di registri in pConstantData.</span><span class="sxs-lookup"><span data-stu-id="60fcf-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60fcf-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60fcf-116">Return value</span></span>

<span data-ttu-id="60fcf-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="60fcf-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="60fcf-118">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="60fcf-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="60fcf-119">Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="60fcf-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="60fcf-120">L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="60fcf-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="60fcf-121">La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: SetPixelShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti), avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="60fcf-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="60fcf-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60fcf-122">Requirements</span></span>



| <span data-ttu-id="60fcf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="60fcf-123">Requirement</span></span> | <span data-ttu-id="60fcf-124">Valore</span><span class="sxs-lookup"><span data-stu-id="60fcf-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="60fcf-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60fcf-125">Header</span></span><br/>  | <dl> <span data-ttu-id="60fcf-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="60fcf-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="60fcf-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="60fcf-127">Library</span></span><br/> | <dl> <span data-ttu-id="60fcf-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60fcf-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="60fcf-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60fcf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60fcf-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="60fcf-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
