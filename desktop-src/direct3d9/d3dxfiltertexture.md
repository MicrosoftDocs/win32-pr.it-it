---
description: Filtra i livelli di mipmap di una trama.
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: Funzione D3DXFilterTexture (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFilterTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8a0d1c211b50379451c8b04830e9c97fe988137
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322696"
---
# <a name="d3dxfiltertexture-function"></a><span data-ttu-id="5271a-103">D3DXFilterTexture (funzione)</span><span class="sxs-lookup"><span data-stu-id="5271a-103">D3DXFilterTexture function</span></span>

<span data-ttu-id="5271a-104">Filtra i livelli di mipmap di una trama.</span><span class="sxs-lookup"><span data-stu-id="5271a-104">Filters mipmap levels of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="5271a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5271a-105">Syntax</span></span>


```C++
HRESULT D3DXFilterTexture(
  _In_        LPDIRECT3DBASETEXTURE9 pBaseTexture,
  _Out_ const PALETTEENTRY           *pPalette,
  _In_        UINT                   SrcLevel,
  _In_        DWORD                  MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="5271a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5271a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5271a-107">*pBaseTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5271a-107">*pBaseTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5271a-108">Tipo: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="5271a-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="5271a-109">Puntatore a un'interfaccia [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) che rappresenta l'oggetto trama da filtrare.</span><span class="sxs-lookup"><span data-stu-id="5271a-109">Pointer to an [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface that represents the texture object to filter.</span></span>

</dd> <dt>

<span data-ttu-id="5271a-110">*pPalette* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5271a-110">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5271a-111">Tipo: **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="5271a-111">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="5271a-112">Puntatore a una struttura [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) che rappresenta una tavolozza dei colori 256 da compilare o **null** per i formati nonpalettized.</span><span class="sxs-lookup"><span data-stu-id="5271a-112">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure that represents a 256-color palette to fill in, or **NULL** for nonpalettized formats.</span></span> <span data-ttu-id="5271a-113">Se non si specifica una tavolozza, viene fornita la tavolozza Direct3D predefinita, ovvero una tavolozza bianca completamente opaca.</span><span class="sxs-lookup"><span data-stu-id="5271a-113">If a palette is not specified, the default Direct3D palette (an all opaque white palette) is provided.</span></span> <span data-ttu-id="5271a-114">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="5271a-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5271a-115">*SrcLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5271a-115">*SrcLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5271a-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5271a-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5271a-117">Livello la cui immagine viene utilizzata per generare i livelli successivi.</span><span class="sxs-lookup"><span data-stu-id="5271a-117">Level whose image is used to generate the subsequent levels.</span></span> <span data-ttu-id="5271a-118">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare 0.</span><span class="sxs-lookup"><span data-stu-id="5271a-118">Specifying D3DX\_DEFAULT for this parameter is equivalent to specifying 0.</span></span>

</dd> <dt>

<span data-ttu-id="5271a-119">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5271a-119">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5271a-120">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5271a-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5271a-121">Combinazione di uno o più [ \_ filtri D3DX](d3dx-filter.md) che controllano la modalità di filtraggio del mipmap.</span><span class="sxs-lookup"><span data-stu-id="5271a-121">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the mipmap is filtered.</span></span> <span data-ttu-id="5271a-122">Specificare \_ il valore predefinito di D3DX per questo parametro equivale a specificare la \_ casella di filtro D3DX \_ se la dimensione della trama è una potenza di due e la \_ casella di filtro D3DX \_ \| D3DX \_ filtrare \_ in altro modo.</span><span class="sxs-lookup"><span data-stu-id="5271a-122">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5271a-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5271a-123">Return value</span></span>

<span data-ttu-id="5271a-124">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5271a-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5271a-125">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5271a-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5271a-126">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="5271a-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="5271a-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="5271a-127">Remarks</span></span>

<span data-ttu-id="5271a-128">Un filtro viene applicato in modo ricorsivo a ogni livello di trama per generare il livello di trama successivo.</span><span class="sxs-lookup"><span data-stu-id="5271a-128">A filter is recursively applied to each texture level to generate the next texture level.</span></span>

<span data-ttu-id="5271a-129">Se si scrive in una superficie non di livello zero della trama, il rettangolo modificato non verrà aggiornato.</span><span class="sxs-lookup"><span data-stu-id="5271a-129">Writing to a non-level-zero surface of the texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="5271a-130">Se viene chiamato **D3DXFilterTexture** e la superficie non è già sporca (si tratta di un problema improbabile in scenari di utilizzo normali), l'applicazione deve chiamare in modo esplicito [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sulla trama.</span><span class="sxs-lookup"><span data-stu-id="5271a-130">If **D3DXFilterTexture** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the texture.</span></span>

<span data-ttu-id="5271a-131">Le trame create nel pool predefinito ( \_ impostazione predefinita D3DPOOL) non possono essere usate con **D3DXFilterTexture** (a meno che non vengano create con D3DUSAGE \_ Dynamic) perché è necessaria un'operazione di blocco sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5271a-131">Textures created in the default pool (D3DPOOL\_DEFAULT) cannot be used with **D3DXFilterTexture** (unless created with D3DUSAGE\_DYNAMIC) because a lock operation is needed on the object.</span></span> <span data-ttu-id="5271a-132">Si noti che i blocchi non sono consentiti nelle trame del pool predefinito (a meno che non siano dinamici).</span><span class="sxs-lookup"><span data-stu-id="5271a-132">Note that locks are prohibited on textures in the default pool (unless they are dynamic).</span></span>

<span data-ttu-id="5271a-133">Per informazioni dettagliate su [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), vedere Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="5271a-133">For details on [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="5271a-134">Si noti che, a partire da DirectX 8,0, il membro peFlags della struttura **PaletteEntry** non funziona come documentato in Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="5271a-134">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="5271a-135">Il membro peFlags è ora il canale alfa per i formati pallettizzati a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="5271a-135">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="5271a-136">Esiste una sola funzione di filtro di trama, ma due macro che chiamano questo metodo.</span><span class="sxs-lookup"><span data-stu-id="5271a-136">There is only one texture filtering function, but two macros that call this method.</span></span>


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
```



## <a name="requirements"></a><span data-ttu-id="5271a-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5271a-137">Requirements</span></span>



| <span data-ttu-id="5271a-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="5271a-138">Requirement</span></span> | <span data-ttu-id="5271a-139">Valore</span><span class="sxs-lookup"><span data-stu-id="5271a-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5271a-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5271a-140">Header</span></span><br/>  | <dl> <span data-ttu-id="5271a-141"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="5271a-141"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="5271a-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="5271a-142">Library</span></span><br/> | <dl> <span data-ttu-id="5271a-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5271a-143"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5271a-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5271a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5271a-145">Funzioni di trama in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="5271a-145">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
