---
description: 'Funzione D3DXComputeNormalMap: converte una mappa di altezza in una mappa normale. I componenti (x,y,z) di ogni normale vengono mappati ai canali (r,g,b) della trama di output.'
ms.assetid: ed9053c0-b1df-4f74-bdee-627c0f60d942
title: Funzione D3DXComputeNormalMap (D3dx9tex.h)
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
ms.openlocfilehash: 920ad763f478a2e6bcb9fbe98cc7e2a677ebe783
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105229"
---
# <a name="d3dxcomputenormalmap-function"></a><span data-ttu-id="c4685-104">Funzione D3DXComputeNormalMap</span><span class="sxs-lookup"><span data-stu-id="c4685-104">D3DXComputeNormalMap function</span></span>

<span data-ttu-id="c4685-105">Converte una mappa di altezza in una mappa normale.</span><span class="sxs-lookup"><span data-stu-id="c4685-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="c4685-106">I componenti (x,y,z) di ogni normale vengono mappati ai canali (r,g,b) della trama di output.</span><span class="sxs-lookup"><span data-stu-id="c4685-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4685-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4685-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c4685-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4685-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4685-109">*pTexture* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="c4685-109">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4685-110">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="c4685-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="c4685-111">Puntatore a [**un'interfaccia IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta la trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c4685-111">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="c4685-112">*pSrcTexture* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c4685-112">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4685-113">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="c4685-113">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="c4685-114">Puntatore a [**un'interfaccia IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che rappresenta la trama della mappa dell'altezza di origine.</span><span class="sxs-lookup"><span data-stu-id="c4685-114">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="c4685-115">*pSrcPalette* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c4685-115">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4685-116">Tipo: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="c4685-116">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="c4685-117">Puntatore a [**un tipo PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) che contiene la tavolozza di origine di 256 colori o **NULL.**</span><span class="sxs-lookup"><span data-stu-id="c4685-117">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) type that contains the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c4685-118">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c4685-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4685-119">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4685-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4685-120">Uno o più [flag D3DX \_ NORMALMAP](d3dx-normalmap.md) che controllano la generazione di mappe normali.</span><span class="sxs-lookup"><span data-stu-id="c4685-120">One or more [D3DX\_NORMALMAP](d3dx-normalmap.md) flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="c4685-121">*Canale* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c4685-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4685-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4685-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4685-123">Un flag [CHANNEL \_ D3DX](d3dx-channel.md) che specifica l'origine delle informazioni sull'altezza.</span><span class="sxs-lookup"><span data-stu-id="c4685-123">One [D3DX\_CHANNEL](d3dx-channel.md) flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="c4685-124">*Ampiezza* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c4685-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4685-125">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4685-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4685-126">Moltiplicatore di valori costante che aumenta (o diminuisce) i valori nella mappa normale.</span><span class="sxs-lookup"><span data-stu-id="c4685-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="c4685-127">I valori più elevati in genere rendono le dossi più visibili, i valori più bassi in genere rendono le dossi meno visibili.</span><span class="sxs-lookup"><span data-stu-id="c4685-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4685-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4685-128">Return value</span></span>

<span data-ttu-id="c4685-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4685-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4685-130">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c4685-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c4685-131">Se la funzione ha esito negativo, il valore restituito può essere il seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="c4685-131">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4685-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4685-132">Remarks</span></span>

<span data-ttu-id="c4685-133">Questo metodo calcola la normale usando la differenza centrale con una dimensione del kernel di 3x3.</span><span class="sxs-lookup"><span data-stu-id="c4685-133">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="c4685-134">Il denominatore differenze centrale usato è 2.0.</span><span class="sxs-lookup"><span data-stu-id="c4685-134">The central differencing denominator used is 2.0.</span></span> <span data-ttu-id="c4685-135">I canali RGB nella destinazione contengono componenti parziali (x,y,z) della normale.</span><span class="sxs-lookup"><span data-stu-id="c4685-135">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4685-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4685-136">Requirements</span></span>



| <span data-ttu-id="c4685-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4685-137">Requirement</span></span> | <span data-ttu-id="c4685-138">Valore</span><span class="sxs-lookup"><span data-stu-id="c4685-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4685-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4685-139">Header</span></span><br/>  | <dl> <span data-ttu-id="c4685-140"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="c4685-140"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c4685-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4685-141">Library</span></span><br/> | <dl> <span data-ttu-id="c4685-142"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4685-142"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c4685-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4685-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4685-144">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="c4685-144">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
