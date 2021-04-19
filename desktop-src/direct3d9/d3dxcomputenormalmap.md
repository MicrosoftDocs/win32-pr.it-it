---
description: Converte una mappa di altezza in una mappa normale. Ai componenti (x, y, z) di ogni normale viene eseguito il mapping ai canali (r, g, b) della trama di output.
ms.assetid: ed9053c0-b1df-4f74-bdee-627c0f60d942
title: Funzione D3DXComputeNormalMap (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormalMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e22418f5a023dbe70fee8ea0fba8a449abbcc8d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323265"
---
# <a name="d3dxcomputenormalmap-function"></a><span data-ttu-id="d9086-104">D3DXComputeNormalMap (funzione)</span><span class="sxs-lookup"><span data-stu-id="d9086-104">D3DXComputeNormalMap function</span></span>

<span data-ttu-id="d9086-105">Converte una mappa di altezza in una mappa normale.</span><span class="sxs-lookup"><span data-stu-id="d9086-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="d9086-106">Ai componenti (x, y, z) di ogni normale viene eseguito il mapping ai canali (r, g, b) della trama di output.</span><span class="sxs-lookup"><span data-stu-id="d9086-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9086-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9086-107">Syntax</span></span>


```C++
HRESULT D3DXComputeNormalMap(
  _Out_       LPDIRECT3DTEXTURE9 pTexture,
  _In_        LPDIRECT3DTEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY       *pSrcPalette,
  _In_        DWORD              Flags,
  _In_        DWORD              Channel,
  _In_        FLOAT              Amplitude
);
```



## <a name="parameters"></a><span data-ttu-id="d9086-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9086-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9086-109">*pTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d9086-109">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9086-110">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="d9086-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="d9086-111">Puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta la trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d9086-111">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="d9086-112">*pSrcTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9086-112">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9086-113">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="d9086-113">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="d9086-114">Puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , che rappresenta la trama della mappa dell'altezza di origine.</span><span class="sxs-lookup"><span data-stu-id="d9086-114">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="d9086-115">*pSrcPalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9086-115">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9086-116">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="d9086-116">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="d9086-117">Puntatore a un tipo [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) che contiene la tavolozza di origine di 256 colori o **null**.</span><span class="sxs-lookup"><span data-stu-id="d9086-117">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) type that contains the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d9086-118">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9086-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9086-119">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9086-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9086-120">Uno o più [flag \_ normalmap D3DX](d3dx-normalmap.md) che controllano la generazione di mappe normali.</span><span class="sxs-lookup"><span data-stu-id="d9086-120">One or more [D3DX\_NORMALMAP](d3dx-normalmap.md) flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="d9086-121">*Canale* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d9086-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9086-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9086-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9086-123">Un flag del [ \_ canale D3DX](d3dx-channel.md) che specifica l'origine delle informazioni sull'altezza.</span><span class="sxs-lookup"><span data-stu-id="d9086-123">One [D3DX\_CHANNEL](d3dx-channel.md) flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="d9086-124">*Ampiezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9086-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9086-125">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9086-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9086-126">Valore costante moltiplicatore che aumenta (o diminuisce) i valori nella mappa normale.</span><span class="sxs-lookup"><span data-stu-id="d9086-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="d9086-127">I valori più elevati in genere rendono più visibili i riscontri, mentre i valori più bassi rendono meno visibili i riscontri.</span><span class="sxs-lookup"><span data-stu-id="d9086-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9086-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9086-128">Return value</span></span>

<span data-ttu-id="d9086-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d9086-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d9086-130">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d9086-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d9086-131">Se la funzione ha esito negativo, il valore restituito può essere il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d9086-131">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9086-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9086-132">Remarks</span></span>

<span data-ttu-id="d9086-133">Questo metodo calcola la normalità usando la differenza centrale con una dimensione del kernel di 3x3.</span><span class="sxs-lookup"><span data-stu-id="d9086-133">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="d9086-134">Il denominatore differenze centrale usato è 2,0.</span><span class="sxs-lookup"><span data-stu-id="d9086-134">The central differencing denominator used is 2.0.</span></span> <span data-ttu-id="d9086-135">I canali RGB nella destinazione contengono i componenti parziali (x, y, z) del normale.</span><span class="sxs-lookup"><span data-stu-id="d9086-135">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9086-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9086-136">Requirements</span></span>



| <span data-ttu-id="d9086-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9086-137">Requirement</span></span> | <span data-ttu-id="d9086-138">Valore</span><span class="sxs-lookup"><span data-stu-id="d9086-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d9086-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9086-139">Header</span></span><br/>  | <dl> <span data-ttu-id="d9086-140"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9086-140"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="d9086-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="d9086-141">Library</span></span><br/> | <dl> <span data-ttu-id="d9086-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d9086-142"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d9086-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9086-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9086-144">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="d9086-144">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
