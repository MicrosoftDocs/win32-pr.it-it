---
description: Creare un effetto dalla descrizione di un effetto ASCII o binario.
ms.assetid: 8385512c-e93d-4c07-b353-87717eb58bcd
title: Funzione D3DXCreateEffectFromResource (D3DX9Effect. h)
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
ms.openlocfilehash: 36db2c82debc542301ba44d4baa74ecaaf01245e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323256"
---
# <a name="d3dxcreateeffectfromresource-function"></a><span data-ttu-id="47e76-103">D3DXCreateEffectFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="47e76-103">D3DXCreateEffectFromResource function</span></span>

<span data-ttu-id="47e76-104">Creare un effetto dalla descrizione di un effetto ASCII o binario.</span><span class="sxs-lookup"><span data-stu-id="47e76-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="47e76-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47e76-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="47e76-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="47e76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47e76-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47e76-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e76-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="47e76-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="47e76-109">Puntatore al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="47e76-109">Pointer to the device.</span></span>

</dd> <dt>

<span data-ttu-id="47e76-110">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47e76-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e76-111">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47e76-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47e76-112">Handle per un modulo che contiene la descrizione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="47e76-112">Handle to a module containing the effect description.</span></span> <span data-ttu-id="47e76-113">Se questo parametro è **null**, verrà usato il modulo corrente.</span><span class="sxs-lookup"><span data-stu-id="47e76-113">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="47e76-114">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47e76-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e76-115">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47e76-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47e76-116">Puntatore alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="47e76-116">Pointer to the resource.</span></span> <span data-ttu-id="47e76-117">Questo parametro supporta sia stringhe Unicode che ANSI.</span><span class="sxs-lookup"><span data-stu-id="47e76-117">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="47e76-118">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="47e76-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="47e76-119">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47e76-119">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e76-120">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="47e76-120">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="47e76-121">Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) che descrivono le definizioni del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="47e76-121">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="47e76-122">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="47e76-122">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="47e76-123">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47e76-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e76-124">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="47e76-124">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="47e76-125">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="47e76-125">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="47e76-126">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="47e76-126">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="47e76-127">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47e76-127">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e76-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47e76-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47e76-129">Se *hSrcModule* contiene un effetto di testo, i flag possono essere una combinazione di flag [D3DXSHADER](d3dxshader-flags.md) e flag [D3DXFX](d3dxfx.md) ; in caso contrario, *hSrcModule* contiene un effetto binario e gli unici flag rispettati sono i flag D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="47e76-129">If *hSrcModule* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *hSrcModule* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="47e76-130">Il compilatore Direct3D 10 HLSL è ora il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="47e76-130">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="47e76-131">Per informazioni dettagliate, vedere [strumento del compilatore di effetti](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="47e76-131">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="47e76-132">*pPool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47e76-132">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47e76-133">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="47e76-133">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="47e76-134">Puntatore a un oggetto [**ID3DXEffectPool**](id3dxeffectpool.md) da utilizzare per i parametri condivisi.</span><span class="sxs-lookup"><span data-stu-id="47e76-134">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="47e76-135">Se questo valore è **null**, non verrà condiviso alcun parametro.</span><span class="sxs-lookup"><span data-stu-id="47e76-135">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="47e76-136">*ppEffect* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="47e76-136">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47e76-137">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="47e76-137">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="47e76-138">Restituisce un buffer contenente l'effetto compilato.</span><span class="sxs-lookup"><span data-stu-id="47e76-138">Returns a buffer containing the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="47e76-139">*ppCompilationErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="47e76-139">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47e76-140">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="47e76-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="47e76-141">Restituisce un buffer contenente un elenco di errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="47e76-141">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47e76-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47e76-142">Return value</span></span>

<span data-ttu-id="47e76-143">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="47e76-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="47e76-144">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="47e76-144">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="47e76-145">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="47e76-145">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="47e76-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="47e76-146">Remarks</span></span>

<span data-ttu-id="47e76-147">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="47e76-147">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="47e76-148">In caso contrario, il tipo di dati LPCTSTR viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="47e76-148">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="47e76-149">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="47e76-149">The compiler setting also determines the function version.</span></span> <span data-ttu-id="47e76-150">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateEffectFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="47e76-150">If Unicode is defined, the function call resolves to D3DXCreateEffectFromResourceW.</span></span> <span data-ttu-id="47e76-151">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateEffectFromResourceA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="47e76-151">Otherwise, the function call resolves to D3DXCreateEffectFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="47e76-152">D3DXCreateEffectFromResource carica i dati da una risorsa di tipo RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="47e76-152">D3DXCreateEffectFromResource loads data from a resource of type RT\_RCDATA.</span></span> <span data-ttu-id="47e76-153">Per ulteriori informazioni sulle risorse di Windows, vedere MSDN.</span><span class="sxs-lookup"><span data-stu-id="47e76-153">See MSDN for more information about Windows resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="47e76-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47e76-154">Requirements</span></span>



| <span data-ttu-id="47e76-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="47e76-155">Requirement</span></span> | <span data-ttu-id="47e76-156">Valore</span><span class="sxs-lookup"><span data-stu-id="47e76-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="47e76-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47e76-157">Header</span></span><br/>  | <dl> <span data-ttu-id="47e76-158"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="47e76-158"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="47e76-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="47e76-159">Library</span></span><br/> | <dl> <span data-ttu-id="47e76-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47e76-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="47e76-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47e76-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47e76-162">Funzioni effetto</span><span class="sxs-lookup"><span data-stu-id="47e76-162">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="47e76-163">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="47e76-163">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="47e76-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="47e76-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
