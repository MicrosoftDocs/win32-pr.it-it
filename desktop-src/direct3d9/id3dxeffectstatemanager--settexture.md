---
description: Funzione di callback che deve essere implementata da un utente per impostare una trama.
ms.assetid: 971802f4-ea7a-4906-83b8-0cd83111716e
title: 'Metodo ID3DXEffectStateManager:: setexture (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b395c19b65bb39b8328da24f727292f7dbe2a0f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530973"
---
# <a name="id3dxeffectstatemanagersettexture-method"></a><span data-ttu-id="79e5c-103">Metodo ID3DXEffectStateManager:: setexture</span><span class="sxs-lookup"><span data-stu-id="79e5c-103">ID3DXEffectStateManager::SetTexture method</span></span>

<span data-ttu-id="79e5c-104">Funzione di callback che deve essere implementata da un utente per impostare una trama.</span><span class="sxs-lookup"><span data-stu-id="79e5c-104">A callback function that must be implemented by a user to set a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="79e5c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79e5c-105">Syntax</span></span>


```C++
HRESULT SetTexture(
  [in] DWORD                  Stage,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="79e5c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="79e5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79e5c-107">*Fase* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79e5c-107">*Stage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79e5c-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79e5c-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79e5c-109">Fase a cui è assegnata la trama.</span><span class="sxs-lookup"><span data-stu-id="79e5c-109">The stage to which the texture is assigned.</span></span> <span data-ttu-id="79e5c-110">Si tratta del valore di indice in [**IDirect3DDevice9:: setexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) o [**IDirect3DDevice9:: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span><span class="sxs-lookup"><span data-stu-id="79e5c-110">This is the index value in [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) or [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span>

</dd> <dt>

<span data-ttu-id="79e5c-111">*pTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79e5c-111">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79e5c-112">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="79e5c-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="79e5c-113">Puntatore all'oggetto texture.</span><span class="sxs-lookup"><span data-stu-id="79e5c-113">A pointer to the texture object.</span></span> <span data-ttu-id="79e5c-114">Può trattarsi di qualsiasi tipo di trama Direct3D (cubo, volume e così via).</span><span class="sxs-lookup"><span data-stu-id="79e5c-114">This can be any of the Direct3D texture types (cube, volume, etc.).</span></span> <span data-ttu-id="79e5c-115">Vedere [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span><span class="sxs-lookup"><span data-stu-id="79e5c-115">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79e5c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79e5c-116">Return value</span></span>

<span data-ttu-id="79e5c-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79e5c-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79e5c-118">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="79e5c-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="79e5c-119">Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="79e5c-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="79e5c-120">L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="79e5c-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="79e5c-121">La chiamata allo stato dell'effetto dinamico (ad esempio [**IDirect3DDevice9:: Setrame**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)) avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="79e5c-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="79e5c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79e5c-122">Requirements</span></span>



| <span data-ttu-id="79e5c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="79e5c-123">Requirement</span></span> | <span data-ttu-id="79e5c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="79e5c-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="79e5c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="79e5c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="79e5c-126"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="79e5c-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="79e5c-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="79e5c-127">Library</span></span><br/> | <dl> <span data-ttu-id="79e5c-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79e5c-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="79e5c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79e5c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e5c-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="79e5c-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
