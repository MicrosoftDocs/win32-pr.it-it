---
description: Verifica i parametri di creazione della trama del volume.
ms.assetid: 1a02cb99-2582-4d8f-aacf-67ed75f6deb8
title: Funzione D3DXCheckVolumeTextureRequirements (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVolumeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4940cab936ed14c847e7224c9f619244c6e422a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401975"
---
# <a name="d3dxcheckvolumetexturerequirements-function"></a><span data-ttu-id="49baf-103">D3DXCheckVolumeTextureRequirements (funzione)</span><span class="sxs-lookup"><span data-stu-id="49baf-103">D3DXCheckVolumeTextureRequirements function</span></span>

<span data-ttu-id="49baf-104">Verifica i parametri di creazione della trama del volume.</span><span class="sxs-lookup"><span data-stu-id="49baf-104">Checks volume-texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="49baf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49baf-105">Syntax</span></span>


```C++
HRESULT D3DXCheckVolumeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pDepth,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="49baf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="49baf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49baf-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49baf-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49baf-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="49baf-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="49baf-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo da associare alla trama del volume.</span><span class="sxs-lookup"><span data-stu-id="49baf-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="49baf-110">*pWidth* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="49baf-110">*pWidth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="49baf-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="49baf-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="49baf-112">Puntatore alla larghezza richiesta, in pixel, o **null**.</span><span class="sxs-lookup"><span data-stu-id="49baf-112">Pointer to the requested width in pixels, or **NULL**.</span></span> <span data-ttu-id="49baf-113">Restituisce la dimensione corretta.</span><span class="sxs-lookup"><span data-stu-id="49baf-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="49baf-114">*pHeight* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="49baf-114">*pHeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="49baf-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="49baf-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="49baf-116">Puntatore all'altezza richiesta, in pixel, o **null**.</span><span class="sxs-lookup"><span data-stu-id="49baf-116">Pointer to the requested height in pixels, or **NULL**.</span></span> <span data-ttu-id="49baf-117">Restituisce la dimensione corretta.</span><span class="sxs-lookup"><span data-stu-id="49baf-117">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="49baf-118">*pDepth* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="49baf-118">*pDepth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="49baf-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="49baf-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="49baf-120">Puntatore alla profondità richiesta in pixel o **null**.</span><span class="sxs-lookup"><span data-stu-id="49baf-120">Pointer to the requested depth in pixels, or **NULL**.</span></span> <span data-ttu-id="49baf-121">Restituisce la dimensione corretta.</span><span class="sxs-lookup"><span data-stu-id="49baf-121">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="49baf-122">*pNumMipLevels* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="49baf-122">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="49baf-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="49baf-123">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="49baf-124">Puntatore al numero di livelli di mipmap richiesti o **null**.</span><span class="sxs-lookup"><span data-stu-id="49baf-124">Pointer to the number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="49baf-125">Restituisce il numero corretto di livelli di mipmap.</span><span class="sxs-lookup"><span data-stu-id="49baf-125">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="49baf-126">*Utilizzo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="49baf-126">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49baf-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49baf-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49baf-128">Attualmente non utilizzato, impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="49baf-128">Currently not used, set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="49baf-129">*pFormat* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="49baf-129">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="49baf-130">Tipo: **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="49baf-130">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="49baf-131">Puntatore a un membro del tipo enumerato [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="49baf-131">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="49baf-132">Specifica il formato pixel desiderato o **null**.</span><span class="sxs-lookup"><span data-stu-id="49baf-132">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="49baf-133">Restituisce il formato corretto.</span><span class="sxs-lookup"><span data-stu-id="49baf-133">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="49baf-134">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="49baf-134">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49baf-135">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="49baf-135">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="49baf-136">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che descrive la classe di memoria in cui deve essere inserita la trama del volume.</span><span class="sxs-lookup"><span data-stu-id="49baf-136">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the volume texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49baf-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49baf-137">Return value</span></span>

<span data-ttu-id="49baf-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49baf-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49baf-139">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="49baf-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="49baf-140">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ NOTAVAILABLE, D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="49baf-140">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="49baf-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="49baf-141">Remarks</span></span>

<span data-ttu-id="49baf-142">Se i parametri di questa funzione non sono validi, questa funzione restituisce parametri corretti.</span><span class="sxs-lookup"><span data-stu-id="49baf-142">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="49baf-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49baf-143">Requirements</span></span>



| <span data-ttu-id="49baf-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="49baf-144">Requirement</span></span> | <span data-ttu-id="49baf-145">Valore</span><span class="sxs-lookup"><span data-stu-id="49baf-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49baf-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49baf-146">Header</span></span><br/>  | <dl> <span data-ttu-id="49baf-147"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="49baf-147"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="49baf-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="49baf-148">Library</span></span><br/> | <dl> <span data-ttu-id="49baf-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49baf-149"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="49baf-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49baf-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49baf-151">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="49baf-151">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
