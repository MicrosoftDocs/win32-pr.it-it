---
description: Funzione di callback che deve essere implementata da un utente per abilitare o disabilitare una luce.
ms.assetid: 11522ca3-8a2f-4767-a6e6-4186cb4f3115
title: 'Metodo ID3DXEffectStateManager:: Alleggerible (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.LightEnable
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d065540eb036b26cdd19791dc393d32c5b45e3ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235102"
---
# <a name="id3dxeffectstatemanagerlightenable-method"></a><span data-ttu-id="f96fc-103">Metodo ID3DXEffectStateManager:: Schiarenteable</span><span class="sxs-lookup"><span data-stu-id="f96fc-103">ID3DXEffectStateManager::LightEnable method</span></span>

<span data-ttu-id="f96fc-104">Funzione di callback che deve essere implementata da un utente per abilitare o disabilitare una luce.</span><span class="sxs-lookup"><span data-stu-id="f96fc-104">A callback function that must be implemented by a user to enable/disable a light.</span></span>

## <a name="syntax"></a><span data-ttu-id="f96fc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f96fc-105">Syntax</span></span>


```C++
HRESULT LightEnable(
  [in] DWORD Index,
  [in] BOOL  Enable
);
```



## <a name="parameters"></a><span data-ttu-id="f96fc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f96fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f96fc-107">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f96fc-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f96fc-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f96fc-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f96fc-109">Indice in base zero della luce.</span><span class="sxs-lookup"><span data-stu-id="f96fc-109">The zero-based index of the light.</span></span> <span data-ttu-id="f96fc-110">Si tratta dello stesso indice in [**IDirect3DDevice9:: selight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span><span class="sxs-lookup"><span data-stu-id="f96fc-110">This is the same index in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span></span>

</dd> <dt>

<span data-ttu-id="f96fc-111">*Abilita* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f96fc-111">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f96fc-112">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f96fc-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f96fc-113">True per abilitare la luce, false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f96fc-113">True to enable the light, false otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f96fc-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f96fc-114">Return value</span></span>

<span data-ttu-id="f96fc-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f96fc-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f96fc-116">Il metodo implementato dall'utente deve restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f96fc-116">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="f96fc-117">Se il callback ha esito negativo quando si imposta lo stato del dispositivo, si verificherà una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="f96fc-117">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="f96fc-118">L'effetto avrà esito negativo durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="f96fc-118">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="f96fc-119">La chiamata di stato dell'effetto dinamico (ad esempio [**IDirect3DDevice9:: alleggerible**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)) avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f96fc-119">The dynamic effect state call (such as [**IDirect3DDevice9::LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="f96fc-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f96fc-120">Requirements</span></span>



| <span data-ttu-id="f96fc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f96fc-121">Requirement</span></span> | <span data-ttu-id="f96fc-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f96fc-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f96fc-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f96fc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f96fc-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f96fc-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f96fc-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="f96fc-125">Library</span></span><br/> | <dl> <span data-ttu-id="f96fc-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f96fc-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f96fc-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f96fc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f96fc-128">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="f96fc-128">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
