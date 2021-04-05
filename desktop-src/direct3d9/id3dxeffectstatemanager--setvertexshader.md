---
description: Funzione di callback che deve essere implementata da un utente per impostare un vertex shader.
ms.assetid: 8f3d3be3-c073-441d-a318-6d2cd5e7aca5
title: 'Metodo ID3DXEffectStateManager:: SetVertexShader (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9fd25158f2aa6ab0a22d6226e8e709c3b498b0e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886307"
---
# <a name="id3dxeffectstatemanagersetvertexshader-method"></a><span data-ttu-id="5ff89-103">Metodo ID3DXEffectStateManager:: SetVertexShader</span><span class="sxs-lookup"><span data-stu-id="5ff89-103">ID3DXEffectStateManager::SetVertexShader method</span></span>

<span data-ttu-id="5ff89-104">Funzione di callback che deve essere implementata da un utente per impostare un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="5ff89-104">A callback function that must be implemented by a user to set a vertex shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ff89-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ff89-105">Syntax</span></span>


```C++
HRESULT SetVertexShader(
  [in] LPDIRECT3DVERTEXSHADER9 pShader
);
```



## <a name="parameters"></a><span data-ttu-id="5ff89-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ff89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ff89-107">*pShader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ff89-107">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ff89-108">Tipo: **[ **LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**</span><span class="sxs-lookup"><span data-stu-id="5ff89-108">Type: **[**LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**</span></span>

<span data-ttu-id="5ff89-109">Puntatore a un oggetto vertex shader.</span><span class="sxs-lookup"><span data-stu-id="5ff89-109">A pointer to a vertex shader object.</span></span> <span data-ttu-id="5ff89-110">Vedere [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span><span class="sxs-lookup"><span data-stu-id="5ff89-110">See [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ff89-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ff89-111">Return value</span></span>

<span data-ttu-id="5ff89-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5ff89-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5ff89-113">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5ff89-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="5ff89-114">Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5ff89-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="5ff89-115">L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="5ff89-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="5ff89-116">La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader), avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5ff89-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ff89-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ff89-117">Requirements</span></span>



| <span data-ttu-id="5ff89-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ff89-118">Requirement</span></span> | <span data-ttu-id="5ff89-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5ff89-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ff89-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ff89-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5ff89-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ff89-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="5ff89-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="5ff89-122">Library</span></span><br/> | <dl> <span data-ttu-id="5ff89-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5ff89-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5ff89-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ff89-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ff89-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="5ff89-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
