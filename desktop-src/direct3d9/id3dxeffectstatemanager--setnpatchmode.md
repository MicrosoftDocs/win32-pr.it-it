---
description: Funzione di callback che deve essere implementata da un utente per impostare il numero di segmenti di suddivisione per N-patch.
ms.assetid: f94910ee-3385-44d3-b4f1-a0e88c7afa39
title: 'Metodo ID3DXEffectStateManager:: SetNPatchMode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetNPatchMode
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9b8725a0482b6945b04013df43d34a502f25b7b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969504"
---
# <a name="id3dxeffectstatemanagersetnpatchmode-method"></a><span data-ttu-id="eb4b7-103">Metodo ID3DXEffectStateManager:: SetNPatchMode</span><span class="sxs-lookup"><span data-stu-id="eb4b7-103">ID3DXEffectStateManager::SetNPatchMode method</span></span>

<span data-ttu-id="eb4b7-104">Funzione di callback che deve essere implementata da un utente per impostare il numero di segmenti di suddivisione per N-patch.</span><span class="sxs-lookup"><span data-stu-id="eb4b7-104">A callback function that must be implemented by a user to set the number of subdivision segments for N-patches.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb4b7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb4b7-105">Syntax</span></span>


```C++
HRESULT SetNPatchMode(
  [in] FLOAT nSegments
);
```



## <a name="parameters"></a><span data-ttu-id="eb4b7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb4b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb4b7-107">*nSegments* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb4b7-107">*nSegments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb4b7-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eb4b7-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eb4b7-109">Suddividere la superficie in questo numero di suddivisioni.</span><span class="sxs-lookup"><span data-stu-id="eb4b7-109">Break the surface into this number of subdivisions.</span></span> <span data-ttu-id="eb4b7-110">Corrisponde al numero usato da [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="eb4b7-110">This is the same as the number used by [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb4b7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb4b7-111">Return value</span></span>

<span data-ttu-id="eb4b7-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eb4b7-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eb4b7-113">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eb4b7-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="eb4b7-114">Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="eb4b7-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="eb4b7-115">L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="eb4b7-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="eb4b7-116">La chiamata allo stato dell'effetto dinamico, ad esempio [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode), avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="eb4b7-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb4b7-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb4b7-117">Requirements</span></span>



| <span data-ttu-id="eb4b7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb4b7-118">Requirement</span></span> | <span data-ttu-id="eb4b7-119">Valore</span><span class="sxs-lookup"><span data-stu-id="eb4b7-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb4b7-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb4b7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="eb4b7-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb4b7-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="eb4b7-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="eb4b7-122">Library</span></span><br/> | <dl> <span data-ttu-id="eb4b7-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb4b7-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="eb4b7-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb4b7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb4b7-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="eb4b7-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
