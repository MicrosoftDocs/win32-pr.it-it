---
description: Funzione di callback che deve essere implementata da un utente per impostare un pixel shader.
ms.assetid: 4124eff2-1d88-429c-b7ed-8d87155b5ddc
title: 'Metodo ID3DXEffectStateManager:: SetPixelShader (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 71a16bc267df95ed7efc1e0f74871b131e34ebe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530979"
---
# <a name="id3dxeffectstatemanagersetpixelshader-method"></a><span data-ttu-id="89f56-103">Metodo ID3DXEffectStateManager:: SetPixelShader</span><span class="sxs-lookup"><span data-stu-id="89f56-103">ID3DXEffectStateManager::SetPixelShader method</span></span>

<span data-ttu-id="89f56-104">Funzione di callback che deve essere implementata da un utente per impostare un pixel shader.</span><span class="sxs-lookup"><span data-stu-id="89f56-104">A callback function that must be implemented by a user to set a pixel shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="89f56-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89f56-105">Syntax</span></span>


```C++
HRESULT SetPixelShader(
  [in] LPDIRECT3DPIXELSHADER9 pShader
);
```



## <a name="parameters"></a><span data-ttu-id="89f56-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="89f56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89f56-107">*pShader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89f56-107">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89f56-108">Tipo: **[ **LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)**</span><span class="sxs-lookup"><span data-stu-id="89f56-108">Type: **[**LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)**</span></span>

<span data-ttu-id="89f56-109">Puntatore a un oggetto pixel shader.</span><span class="sxs-lookup"><span data-stu-id="89f56-109">A pointer to a pixel shader object.</span></span> <span data-ttu-id="89f56-110">Vedere [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9).</span><span class="sxs-lookup"><span data-stu-id="89f56-110">See [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89f56-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89f56-111">Return value</span></span>

<span data-ttu-id="89f56-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="89f56-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="89f56-113">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="89f56-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="89f56-114">Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="89f56-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="89f56-115">L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="89f56-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="89f56-116">La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: SetPixelShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader), avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="89f56-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="89f56-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89f56-117">Requirements</span></span>



| <span data-ttu-id="89f56-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="89f56-118">Requirement</span></span> | <span data-ttu-id="89f56-119">Valore</span><span class="sxs-lookup"><span data-stu-id="89f56-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="89f56-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89f56-120">Header</span></span><br/>  | <dl> <span data-ttu-id="89f56-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="89f56-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="89f56-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="89f56-122">Library</span></span><br/> | <dl> <span data-ttu-id="89f56-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89f56-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="89f56-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89f56-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89f56-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="89f56-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
