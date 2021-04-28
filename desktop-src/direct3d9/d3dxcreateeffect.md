---
description: "Funzione D3DXCreateEffect: creare un effetto da una descrizione dell'effetto ASCII o binario."
ms.assetid: 1cbd91f2-3cda-4770-a3c5-b1e6702628d1
title: Funzione D3DXCreateEffect (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6821375dfc672d4937c335cf85dab12ba31b726c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115779"
---
# <a name="d3dxcreateeffect-function"></a><span data-ttu-id="a7fa4-103">Funzione D3DXCreateEffect</span><span class="sxs-lookup"><span data-stu-id="a7fa4-103">D3DXCreateEffect function</span></span>

<span data-ttu-id="a7fa4-104">Creare un effetto da una descrizione dell'effetto ASCII o binario.</span><span class="sxs-lookup"><span data-stu-id="a7fa4-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7fa4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7fa4-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="a7fa4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7fa4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7fa4-107">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a7fa4-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fa4-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a7fa4-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a7fa4-109">Puntatore al dispositivo che creerà l'effetto.</span><span class="sxs-lookup"><span data-stu-id="a7fa4-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="a7fa4-110">Vedere [**IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)</span><span class="sxs-lookup"><span data-stu-id="a7fa4-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="a7fa4-111">*pSrcData* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a7fa4-111">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fa4-112">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7fa4-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a7fa4-113">Puntatore a un buffer contenente una descrizione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="a7fa4-113">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="a7fa4-114">*SrcDataLen* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a7fa4-114">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fa4-115">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7fa4-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a7fa4-116">Lunghezza in byte dei dati dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="a7fa4-116">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a7fa4-117">*pDefines* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a7fa4-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fa4-118">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="a7fa4-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="a7fa4-119">Matrice facoltativa **con terminazione NULL** di [**strutture D3DXMACRO**](d3dxmacro.md) che descrivono le definizioni del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="a7fa4-119">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="a7fa4-120">Questo valore può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="a7fa4-120">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a7fa4-121">*pInclude* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a7fa4-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fa4-122">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="a7fa4-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="a7fa4-123">Puntatore a interfaccia [**facoltativo, ID3DXInclude,**](id3dxinclude.md)da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="a7fa4-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="a7fa4-124">Se questo valore è **NULL,** le include verranno rispettate durante la compilazione da un file o causeranno un errore durante la compilazione \# da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="a7fa4-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="a7fa4-125">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a7fa4-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fa4-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7fa4-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a7fa4-127">Se *pSrcData contiene* un effetto di testo, i flag possono essere una combinazione di flag [D3DXSHADER](d3dxshader-flags.md) e [flag D3DXFX;](d3dxfx.md) In caso contrario, *pSrcData* contiene un effetto binario e gli unici flag rispettati sono i flag D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="a7fa4-127">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="a7fa4-128">Il compilatore HLSL Direct3D 10 è ora l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a7fa4-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="a7fa4-129">Per [informazioni dettagliate, vedere Effect-Compiler Tool](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="a7fa4-129">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="a7fa4-130">*pPool* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a7fa4-130">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fa4-131">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="a7fa4-131">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="a7fa4-132">Puntatore a [**un oggetto ID3DXEffectPool**](id3dxeffectpool.md) da usare per i parametri condivisi.</span><span class="sxs-lookup"><span data-stu-id="a7fa4-132">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="a7fa4-133">Se questo valore è **NULL,** non verrà condiviso alcun parametro.</span><span class="sxs-lookup"><span data-stu-id="a7fa4-133">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="a7fa4-134">*ppEffect* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="a7fa4-134">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fa4-135">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="a7fa4-135">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="a7fa4-136">Restituisce un puntatore a [**un'interfaccia ID3DXEffect.**](id3dxeffect.md)</span><span class="sxs-lookup"><span data-stu-id="a7fa4-136">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a7fa4-137">*ppCompilationErrors* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="a7fa4-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fa4-138">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a7fa4-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a7fa4-139">Restituisce un buffer contenente un elenco di errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="a7fa4-139">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7fa4-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7fa4-140">Return value</span></span>

<span data-ttu-id="a7fa4-141">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a7fa4-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a7fa4-142">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a7fa4-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a7fa4-143">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a7fa4-143">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7fa4-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7fa4-144">Requirements</span></span>



| <span data-ttu-id="a7fa4-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7fa4-145">Requirement</span></span> | <span data-ttu-id="a7fa4-146">Valore</span><span class="sxs-lookup"><span data-stu-id="a7fa4-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7fa4-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7fa4-147">Header</span></span><br/>  | <dl> <span data-ttu-id="a7fa4-148"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="a7fa4-148"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="a7fa4-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="a7fa4-149">Library</span></span><br/> | <dl> <span data-ttu-id="a7fa4-150"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7fa4-150"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a7fa4-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7fa4-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7fa4-152">Funzioni degli effetti</span><span class="sxs-lookup"><span data-stu-id="a7fa4-152">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="a7fa4-153">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="a7fa4-153">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="a7fa4-154">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="a7fa4-154">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
