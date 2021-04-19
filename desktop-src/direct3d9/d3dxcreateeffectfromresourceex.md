---
description: Creare un effetto dalla descrizione di un effetto ASCII o binario. Si tratta di una versione estesa di D3DXCreateEffectFromResource che consente a un'applicazione di controllare quali parametri vengono ignorati dal sistema di effetti.
ms.assetid: 5937bdb1-750a-41f8-a49d-3643427f3e3c
title: Funzione D3DXCreateEffectFromResourceEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResourceEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d0ae7a0ee43f93019f3c4c1f6145b3d8aa0e4367
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323255"
---
# <a name="d3dxcreateeffectfromresourceex-function"></a><span data-ttu-id="2f7a1-104">D3DXCreateEffectFromResourceEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="2f7a1-104">D3DXCreateEffectFromResourceEx function</span></span>

<span data-ttu-id="2f7a1-105">Creare un effetto dalla descrizione di un effetto ASCII o binario.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-105">Create an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="2f7a1-106">Si tratta di una versione estesa di [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) che consente a un'applicazione di controllare quali parametri vengono ignorati dal sistema di effetti.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-106">This is an extended version of [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f7a1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f7a1-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromResourceEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="2f7a1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f7a1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f7a1-109">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f7a1-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f7a1-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2f7a1-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2f7a1-111">Puntatore al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-111">Pointer to the device.</span></span>

</dd> <dt>

<span data-ttu-id="2f7a1-112">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f7a1-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f7a1-113">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f7a1-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f7a1-114">Handle per un modulo che contiene la descrizione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-114">Handle to a module containing the effect description.</span></span> <span data-ttu-id="2f7a1-115">Se questo parametro è **null**, verrà usato il modulo corrente.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-115">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="2f7a1-116">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f7a1-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f7a1-117">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f7a1-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f7a1-118">Puntatore alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-118">Pointer to the resource.</span></span> <span data-ttu-id="2f7a1-119">Questo parametro supporta sia stringhe Unicode che ANSI.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-119">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="2f7a1-120">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2f7a1-121">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f7a1-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f7a1-122">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f7a1-122">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="2f7a1-123">Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) che descrivono le definizioni del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-123">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="2f7a1-124">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-124">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2f7a1-125">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f7a1-125">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f7a1-126">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="2f7a1-126">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="2f7a1-127">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-127">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="2f7a1-128">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-128">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="2f7a1-129">*pSkipConstants* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f7a1-129">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f7a1-130">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f7a1-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f7a1-131">Una stringa di parametri effetti che verrà ignorata dal sistema di effetti.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-131">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="2f7a1-132">La stringa deve essere con terminazione **null** e deve contenere il nome di ogni costante gestita dall'applicazione separata da un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-132">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="2f7a1-133">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f7a1-133">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f7a1-134">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f7a1-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f7a1-135">Se *pSrcResource* contiene un effetto di testo, i flag possono essere una combinazione di flag [D3DXSHADER](d3dxshader-flags.md) e flag [D3DXFX](d3dxfx.md) ; in caso contrario, *pSrcResource* contiene un effetto binario e gli unici flag rispettati sono i flag D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-135">If *pSrcResource* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcResource* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="2f7a1-136">Il compilatore Direct3D 10 HLSL è ora il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-136">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="2f7a1-137">Per informazioni dettagliate, vedere [strumento del compilatore di effetti](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="2f7a1-137">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="2f7a1-138">*pPool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f7a1-138">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f7a1-139">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="2f7a1-139">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="2f7a1-140">Puntatore a un oggetto [**ID3DXEffectPool**](id3dxeffectpool.md) da utilizzare per i parametri condivisi.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-140">Pointer to an [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="2f7a1-141">Se questo valore è **null**, non verrà condiviso alcun parametro.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-141">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="2f7a1-142">*ppEffect* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2f7a1-142">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f7a1-143">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f7a1-143">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="2f7a1-144">Restituisce un buffer contenente l'effetto compilato.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-144">Returns a buffer containing the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="2f7a1-145">*ppCompilationErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2f7a1-145">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f7a1-146">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f7a1-146">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="2f7a1-147">Restituisce un buffer contenente un elenco di errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-147">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f7a1-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f7a1-148">Return value</span></span>

<span data-ttu-id="2f7a1-149">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2f7a1-149">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2f7a1-150">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-150">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2f7a1-151">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-151">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f7a1-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f7a1-152">Remarks</span></span>

<span data-ttu-id="2f7a1-153">Questa funzione è una versione estesa di [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) che consente a un'applicazione di specificare quali costanti di effetto verranno gestite dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-153">This function is an extended version of [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="2f7a1-154">Una costante gestita dall'applicazione viene ignorata dal sistema di effetti.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-154">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="2f7a1-155">In altre condizioni, l'applicazione è responsabile dell'inizializzazione della costante, nonché del salvataggio e del ripristino dello stato quando appropriato.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-155">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="2f7a1-156">Questa funzione controlla ogni costante in pSkipConstants per vedere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="2f7a1-156">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="2f7a1-157">È associato a un registro costante.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-157">It is bound to a constant register.</span></span>
-   <span data-ttu-id="2f7a1-158">Viene usato solo nel codice shader HLSL.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-158">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="2f7a1-159">Se una costante viene denominata nella stringa non presente nell'effetto, viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-159">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

<span data-ttu-id="2f7a1-160">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-160">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="2f7a1-161">In caso contrario, il tipo di dati LPCTSTR viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-161">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="2f7a1-162">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-162">The compiler setting also determines the function version.</span></span> <span data-ttu-id="2f7a1-163">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateEffectFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-163">If Unicode is defined, the function call resolves to D3DXCreateEffectFromResourceW.</span></span> <span data-ttu-id="2f7a1-164">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateEffectFromResourceA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-164">Otherwise, the function call resolves to D3DXCreateEffectFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="2f7a1-165">D3DXCreateEffectFromResource carica i dati da una risorsa di tipo RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-165">D3DXCreateEffectFromResource loads data from a resource of type RT\_RCDATA.</span></span> <span data-ttu-id="2f7a1-166">Per ulteriori informazioni sulle risorse di Windows, vedere MSDN.</span><span class="sxs-lookup"><span data-stu-id="2f7a1-166">See MSDN for more information about Windows resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f7a1-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f7a1-167">Requirements</span></span>



| <span data-ttu-id="2f7a1-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f7a1-168">Requirement</span></span> | <span data-ttu-id="2f7a1-169">Valore</span><span class="sxs-lookup"><span data-stu-id="2f7a1-169">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f7a1-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f7a1-170">Header</span></span><br/>  | <dl> <span data-ttu-id="2f7a1-171"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f7a1-171"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2f7a1-172">Libreria</span><span class="sxs-lookup"><span data-stu-id="2f7a1-172">Library</span></span><br/> | <dl> <span data-ttu-id="2f7a1-173"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f7a1-173"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2f7a1-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f7a1-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f7a1-175">Funzioni effetto</span><span class="sxs-lookup"><span data-stu-id="2f7a1-175">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="2f7a1-176">**D3DXCreateEffectEx**</span><span class="sxs-lookup"><span data-stu-id="2f7a1-176">**D3DXCreateEffectEx**</span></span>](d3dxcreateeffectex.md)
</dt> <dt>

[<span data-ttu-id="2f7a1-177">**D3DXCreateEffectFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="2f7a1-177">**D3DXCreateEffectFromFileEx**</span></span>](d3dxcreateeffectfromfileex.md)
</dt> </dl>

 

 
