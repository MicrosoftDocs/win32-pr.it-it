---
description: Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti integer del vertex shader.
ms.assetid: 0035c97a-1b17-4665-9032-7b3b9a9d2cff
title: 'Metodo ID3DXEffectStateManager:: SetVertexShaderConstantI (D3DX9Effect. h)'
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
ms.openlocfilehash: be95d678ee6b0c44dc49e180df4d3332a84d5fe7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322992"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstanti-method"></a><span data-ttu-id="50feb-103">Metodo ID3DXEffectStateManager:: SetVertexShaderConstantI</span><span class="sxs-lookup"><span data-stu-id="50feb-103">ID3DXEffectStateManager::SetVertexShaderConstantI method</span></span>

<span data-ttu-id="50feb-104">Funzione di callback che deve essere implementata da un utente per impostare una matrice di costanti integer del vertex shader.</span><span class="sxs-lookup"><span data-stu-id="50feb-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="50feb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50feb-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="50feb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="50feb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50feb-107">*StartRegister* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="50feb-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50feb-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50feb-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50feb-109">Indice in base zero del primo registro costante.</span><span class="sxs-lookup"><span data-stu-id="50feb-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="50feb-110">*pConstantData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="50feb-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50feb-111">Tipo: **const [**int**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="50feb-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="50feb-112">Matrice di costanti integer.</span><span class="sxs-lookup"><span data-stu-id="50feb-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="50feb-113">*RegisterCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="50feb-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50feb-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="50feb-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="50feb-115">Numero di registri in pConstantData.</span><span class="sxs-lookup"><span data-stu-id="50feb-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50feb-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50feb-116">Return value</span></span>

<span data-ttu-id="50feb-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="50feb-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="50feb-118">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="50feb-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="50feb-119">Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="50feb-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="50feb-120">L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="50feb-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="50feb-121">La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti), avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="50feb-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="50feb-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50feb-122">Requirements</span></span>



| <span data-ttu-id="50feb-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="50feb-123">Requirement</span></span> | <span data-ttu-id="50feb-124">Valore</span><span class="sxs-lookup"><span data-stu-id="50feb-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="50feb-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50feb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="50feb-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="50feb-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="50feb-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="50feb-127">Library</span></span><br/> | <dl> <span data-ttu-id="50feb-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50feb-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="50feb-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50feb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50feb-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="50feb-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
