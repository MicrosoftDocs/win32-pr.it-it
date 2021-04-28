---
description: "Funzione D3DXCreateEffectFromResource: crea un effetto da una descrizione dell'effetto ASCII o binario."
ms.assetid: 8385512c-e93d-4c07-b353-87717eb58bcd
title: Funzione D3DXCreateEffectFromResource (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f2a84d2da1f3ca88a117c0150e7b27485838c300
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107689"
---
# <a name="d3dxcreateeffectfromresource-function"></a><span data-ttu-id="3e3f4-103">Funzione D3DXCreateEffectFromResource</span><span class="sxs-lookup"><span data-stu-id="3e3f4-103">D3DXCreateEffectFromResource function</span></span>

<span data-ttu-id="3e3f4-104">Creare un effetto da una descrizione dell'effetto ASCII o binario.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e3f4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e3f4-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromResource(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="3e3f4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e3f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e3f4-107">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3e3f4-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f4-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="3e3f4-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="3e3f4-109">Puntatore al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-109">Pointer to the device.</span></span>

</dd> <dt>

<span data-ttu-id="3e3f4-110">*hSrcModule* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3e3f4-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f4-111">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e3f4-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e3f4-112">Handle per un modulo contenente la descrizione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-112">Handle to a module containing the effect description.</span></span> <span data-ttu-id="3e3f4-113">Se questo parametro è **NULL,** verrà usato il modulo corrente.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-113">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="3e3f4-114">*pSrcResource* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3e3f4-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f4-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e3f4-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e3f4-116">Puntatore alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-116">Pointer to the resource.</span></span> <span data-ttu-id="3e3f4-117">Questo parametro supporta sia stringhe Unicode che ANSI.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-117">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="3e3f4-118">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3e3f4-119">*pDefines* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3e3f4-119">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f4-120">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="3e3f4-120">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="3e3f4-121">Matrice facoltativa **con terminazione NULL** di strutture [**D3DXMACRO**](d3dxmacro.md) che descrivono le definizioni del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-121">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="3e3f4-122">Questo valore può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="3e3f4-122">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3e3f4-123">*pInclude* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3e3f4-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f4-124">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="3e3f4-124">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="3e3f4-125">Puntatore a interfaccia [**facoltativo, ID3DXInclude,**](id3dxinclude.md)da usare per la gestione \# delle direttive include.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-125">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="3e3f4-126">Se questo valore è **NULL,** include verrà rispettato durante la compilazione da un file o causerà un errore durante la compilazione \# da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-126">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="3e3f4-127">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3e3f4-127">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f4-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3e3f4-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3e3f4-129">Se *hSrcModule contiene* un effetto di testo, i flag possono essere una combinazione di flag [D3DXSHADER](d3dxshader-flags.md) e [D3DXFX;](d3dxfx.md) In caso contrario, *hSrcModule contiene* un effetto binario e gli unici flag rispettati sono i flag D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-129">If *hSrcModule* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *hSrcModule* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="3e3f4-130">Il compilatore HLSL Direct3D 10 è ora l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-130">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="3e3f4-131">Per [informazioni dettagliate, vedere Strumento di compilazione effetti.](../direct3dtools/fxc.md)</span><span class="sxs-lookup"><span data-stu-id="3e3f4-131">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="3e3f4-132">*pPool* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="3e3f4-132">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f4-133">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="3e3f4-133">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="3e3f4-134">Puntatore a [**un oggetto ID3DXEffectPool**](id3dxeffectpool.md) da usare per i parametri condivisi.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-134">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="3e3f4-135">Se questo valore è **NULL,** non verrà condiviso alcun parametro.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-135">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="3e3f4-136">*ppEffect* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="3e3f4-136">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f4-137">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e3f4-137">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="3e3f4-138">Restituisce un buffer contenente l'effetto compilato.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-138">Returns a buffer containing the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="3e3f4-139">*ppCompilationErrors* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="3e3f4-139">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e3f4-140">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3e3f4-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3e3f4-141">Restituisce un buffer contenente un elenco di errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-141">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e3f4-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e3f4-142">Return value</span></span>

<span data-ttu-id="3e3f4-143">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3e3f4-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3e3f4-144">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-144">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3e3f4-145">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-145">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e3f4-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e3f4-146">Remarks</span></span>

<span data-ttu-id="3e3f4-147">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-147">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="3e3f4-148">In caso contrario, il tipo di dati LPCTSTR viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-148">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="3e3f4-149">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-149">The compiler setting also determines the function version.</span></span> <span data-ttu-id="3e3f4-150">Se unicode è definito, la chiamata di funzione viene risolta in D3DXCreateEffectFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-150">If Unicode is defined, the function call resolves to D3DXCreateEffectFromResourceW.</span></span> <span data-ttu-id="3e3f4-151">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateEffectFromResourceA perché vengono usate stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-151">Otherwise, the function call resolves to D3DXCreateEffectFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="3e3f4-152">D3DXCreateEffectFromResource carica i dati da una risorsa di tipo RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-152">D3DXCreateEffectFromResource loads data from a resource of type RT\_RCDATA.</span></span> <span data-ttu-id="3e3f4-153">Per altre informazioni sulle risorse di Windows, vedere MSDN.</span><span class="sxs-lookup"><span data-stu-id="3e3f4-153">See MSDN for more information about Windows resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e3f4-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e3f4-154">Requirements</span></span>



| <span data-ttu-id="3e3f4-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e3f4-155">Requirement</span></span> | <span data-ttu-id="3e3f4-156">Valore</span><span class="sxs-lookup"><span data-stu-id="3e3f4-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e3f4-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e3f4-157">Header</span></span><br/>  | <dl> <span data-ttu-id="3e3f4-158"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="3e3f4-158"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="3e3f4-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="3e3f4-159">Library</span></span><br/> | <dl> <span data-ttu-id="3e3f4-160"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e3f4-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3e3f4-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e3f4-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e3f4-162">Funzioni degli effetti</span><span class="sxs-lookup"><span data-stu-id="3e3f4-162">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="3e3f4-163">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="3e3f4-163">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="3e3f4-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="3e3f4-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
