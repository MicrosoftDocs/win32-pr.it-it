---
description: Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti a virgola mobile del vertex shader.
ms.assetid: 3a13040d-5d5a-4454-bf11-cda9653585c0
title: 'Metodo ID3DXEffectStateManager:: SetVertexShaderConstantF (D3DX9Effect. h)'
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
ms.openlocfilehash: 378af983e0ed7ca1709ae8bb6cfe8615a481b3f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323077"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstantf-method"></a><span data-ttu-id="583f5-103">Metodo ID3DXEffectStateManager:: SetVertexShaderConstantF</span><span class="sxs-lookup"><span data-stu-id="583f5-103">ID3DXEffectStateManager::SetVertexShaderConstantF method</span></span>

<span data-ttu-id="583f5-104">Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti a virgola mobile del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="583f5-104">A callback function that must be implemented by a user to set an array of vertex shader floating-point constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="583f5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="583f5-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantF(
  [out]       UINT  StartRegister,
  [out] const FLOAT *pConstantData,
  [out]       UINT  RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="583f5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="583f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="583f5-107">*StartRegister* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="583f5-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="583f5-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="583f5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="583f5-109">Indice in base zero del primo registro costante.</span><span class="sxs-lookup"><span data-stu-id="583f5-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="583f5-110">*pConstantData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="583f5-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="583f5-111">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="583f5-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="583f5-112">Matrice di costanti a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="583f5-112">An array of floating-point constants.</span></span>

</dd> <dt>

<span data-ttu-id="583f5-113">*RegisterCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="583f5-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="583f5-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="583f5-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="583f5-115">Numero di registri in pConstantData.</span><span class="sxs-lookup"><span data-stu-id="583f5-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="583f5-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="583f5-116">Return value</span></span>

<span data-ttu-id="583f5-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="583f5-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="583f5-118">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="583f5-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="583f5-119">Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="583f5-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="583f5-120">L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="583f5-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="583f5-121">La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: SetVertexShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf), avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="583f5-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="583f5-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="583f5-122">Requirements</span></span>



| <span data-ttu-id="583f5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="583f5-123">Requirement</span></span> | <span data-ttu-id="583f5-124">Valore</span><span class="sxs-lookup"><span data-stu-id="583f5-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="583f5-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="583f5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="583f5-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="583f5-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="583f5-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="583f5-127">Library</span></span><br/> | <dl> <span data-ttu-id="583f5-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="583f5-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="583f5-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="583f5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="583f5-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="583f5-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
