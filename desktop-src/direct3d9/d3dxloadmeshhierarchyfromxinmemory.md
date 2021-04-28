---
description: 'Funzione D3DXLoadMeshHierarchyFromXInMemory: carica la prima gerarchia di frame da un file con estensione x.'
ms.assetid: 428e5cfb-d6a5-4a7f-b082-2d8898e65490
title: Funzione D3DXLoadMeshHierarchyFromXInMemory (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 551810c839e619985d9a380197553f5fe4fc9be8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098209"
---
# <a name="d3dxloadmeshhierarchyfromxinmemory-function"></a><span data-ttu-id="fb10f-103">Funzione D3DXLoadMeshHierarchyFromXInMemory</span><span class="sxs-lookup"><span data-stu-id="fb10f-103">D3DXLoadMeshHierarchyFromXInMemory function</span></span>

<span data-ttu-id="fb10f-104">Carica la prima gerarchia di frame da un file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="fb10f-104">Loads the first frame hierarchy from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb10f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb10f-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshHierarchyFromXInMemory(
  _In_  LPCVOID                   pMemory,
  _In_  DWORD                     SizeOfMemory,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHeirarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="fb10f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb10f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb10f-107">*pMemory* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fb10f-107">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb10f-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb10f-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb10f-109">Puntatore a un buffer che contiene la gerarchia mesh.</span><span class="sxs-lookup"><span data-stu-id="fb10f-109">Pointer to a buffer that contains the mesh hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="fb10f-110">*SizeOfMemory* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fb10f-110">*SizeOfMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb10f-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb10f-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb10f-112">Dimensioni del buffer pMemory, in byte.</span><span class="sxs-lookup"><span data-stu-id="fb10f-112">Size of the pMemory buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="fb10f-113">*MeshOptions* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fb10f-113">*MeshOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb10f-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb10f-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb10f-115">Combinazione di uno o più flag [**dell'enumerazione D3DXMESH**](./d3dxmesh.md) che specificano le opzioni di creazione per la mesh.</span><span class="sxs-lookup"><span data-stu-id="fb10f-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="fb10f-116">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fb10f-116">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb10f-117">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="fb10f-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="fb10f-118">Puntatore a [**un'interfaccia IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) l'oggetto dispositivo associato alla mesh.</span><span class="sxs-lookup"><span data-stu-id="fb10f-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="fb10f-119">*pAlloc* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fb10f-119">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb10f-120">Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="fb10f-120">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="fb10f-121">Puntatore a [**un'interfaccia ID3DXAllocateHierarchy.**](id3dxallocatehierarchy.md)</span><span class="sxs-lookup"><span data-stu-id="fb10f-121">Pointer to an [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="fb10f-122">*pUserDataLoader* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="fb10f-122">*pUserDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb10f-123">Tipo: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="fb10f-123">Type: **[**LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span></span>

<span data-ttu-id="fb10f-124">Interfaccia fornita dall'applicazione che consente il caricamento dei dati utente.</span><span class="sxs-lookup"><span data-stu-id="fb10f-124">Application provided interface that allows loading of user data.</span></span> <span data-ttu-id="fb10f-125">Vedere [**ID3DXLoadUserData.**](id3dxloaduserdata.md)</span><span class="sxs-lookup"><span data-stu-id="fb10f-125">See [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb10f-126">*ppFrameHeirarchy* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="fb10f-126">*ppFrameHeirarchy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb10f-127">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="fb10f-127">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="fb10f-128">Restituisce un puntatore alla gerarchia di frame caricata.</span><span class="sxs-lookup"><span data-stu-id="fb10f-128">Returns a pointer to the loaded frame hierarchy.</span></span> <span data-ttu-id="fb10f-129">Vedere [**D3DXFRAME.**](d3dxframe.md)</span><span class="sxs-lookup"><span data-stu-id="fb10f-129">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="fb10f-130">*ppAnimController* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="fb10f-130">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb10f-131">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="fb10f-131">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="fb10f-132">Restituisce un puntatore al controller di animazione corrispondente all'animazione nel file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="fb10f-132">Returns a pointer to the animation controller corresponding to animation in the .x file.</span></span> <span data-ttu-id="fb10f-133">Viene creato con tracce ed eventi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="fb10f-133">This is created with default tracks and events.</span></span> <span data-ttu-id="fb10f-134">Vedere [**ID3DXAnimationController.**](id3dxanimationcontroller.md)</span><span class="sxs-lookup"><span data-stu-id="fb10f-134">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb10f-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb10f-135">Return value</span></span>

<span data-ttu-id="fb10f-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb10f-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb10f-137">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fb10f-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fb10f-138">Se la funzione ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="fb10f-138">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb10f-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb10f-139">Remarks</span></span>

<span data-ttu-id="fb10f-140">Tutte le mesh nel file verranno compresse in un'unica mesh di output.</span><span class="sxs-lookup"><span data-stu-id="fb10f-140">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="fb10f-141">Se il file contiene una gerarchia di frame, tutte le trasformazioni verranno applicate alla mesh.</span><span class="sxs-lookup"><span data-stu-id="fb10f-141">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb10f-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb10f-142">Requirements</span></span>



| <span data-ttu-id="fb10f-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb10f-143">Requirement</span></span> | <span data-ttu-id="fb10f-144">Valore</span><span class="sxs-lookup"><span data-stu-id="fb10f-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb10f-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb10f-145">Header</span></span><br/>  | <dl> <span data-ttu-id="fb10f-146"><dt>D3dx9anim.h</dt></span><span class="sxs-lookup"><span data-stu-id="fb10f-146"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="fb10f-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="fb10f-147">Library</span></span><br/> | <dl> <span data-ttu-id="fb10f-148"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb10f-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb10f-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb10f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb10f-150">Funzioni di animazione</span><span class="sxs-lookup"><span data-stu-id="fb10f-150">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
