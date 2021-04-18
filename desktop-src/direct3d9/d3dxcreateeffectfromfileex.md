---
description: Creare un effetto dalla descrizione di un effetto ASCII o binario. Questa funzione è una versione estesa di D3DXCreateEffectFromFile che consente a un'applicazione di controllare quali parametri vengono ignorati dal sistema di effetti.
ms.assetid: 963caa1e-bc1a-4d4b-bdb1-50b17d8b4132
title: Funzione D3DXCreateEffectFromFileEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFileEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b3d97c5aa23dd0711cfb00585e5b8ba7d410fc02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323259"
---
# <a name="d3dxcreateeffectfromfileex-function"></a><span data-ttu-id="21f8e-104">D3DXCreateEffectFromFileEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="21f8e-104">D3DXCreateEffectFromFileEx function</span></span>

<span data-ttu-id="21f8e-105">Creare un effetto dalla descrizione di un effetto ASCII o binario.</span><span class="sxs-lookup"><span data-stu-id="21f8e-105">Create an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="21f8e-106">Questa funzione è una versione estesa di [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) che consente a un'applicazione di controllare quali parametri vengono ignorati dal sistema di effetti.</span><span class="sxs-lookup"><span data-stu-id="21f8e-106">This function is an extended version of [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="21f8e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21f8e-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromFileEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="21f8e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="21f8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21f8e-109">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f8e-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f8e-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="21f8e-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="21f8e-111">Puntatore al dispositivo che creerà l'effetto.</span><span class="sxs-lookup"><span data-stu-id="21f8e-111">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="21f8e-112">Vedere [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="21f8e-112">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="21f8e-113">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f8e-113">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f8e-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21f8e-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21f8e-115">Puntatore al nome file.</span><span class="sxs-lookup"><span data-stu-id="21f8e-115">Pointer to the filename.</span></span> <span data-ttu-id="21f8e-116">Questo parametro supporta sia stringhe Unicode che ANSI.</span><span class="sxs-lookup"><span data-stu-id="21f8e-116">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="21f8e-117">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="21f8e-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="21f8e-118">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f8e-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f8e-119">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="21f8e-119">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="21f8e-120">Matrice facoltativa con terminazione NULL di definizioni di macro del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="21f8e-120">Optional NULL-terminated array of preprocessor macro definitions.</span></span> <span data-ttu-id="21f8e-121">Vedere [**D3DXMACRO**](d3dxmacro.md).</span><span class="sxs-lookup"><span data-stu-id="21f8e-121">See [**D3DXMACRO**](d3dxmacro.md).</span></span>

</dd> <dt>

<span data-ttu-id="21f8e-122">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f8e-122">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f8e-123">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="21f8e-123">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="21f8e-124">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="21f8e-124">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="21f8e-125">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="21f8e-125">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="21f8e-126">*pSkipConstants* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f8e-126">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f8e-127">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21f8e-127">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21f8e-128">Una stringa di parametri effetti che verrà ignorata dal sistema di effetti.</span><span class="sxs-lookup"><span data-stu-id="21f8e-128">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="21f8e-129">La stringa deve essere con terminazione **null** e deve contenere il nome di ogni costante gestita dall'applicazione separata da un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="21f8e-129">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="21f8e-130">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f8e-130">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f8e-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21f8e-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21f8e-132">Se *pSrcFile* contiene un effetto di testo, i flag possono essere una combinazione di flag [D3DXSHADER](d3dxshader-flags.md) e flag [D3DXFX](d3dxfx.md) ; in caso contrario, *pSrcFile* contiene un effetto binario e gli unici flag rispettati sono i flag D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="21f8e-132">If *pSrcFile* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcFile* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="21f8e-133">Il compilatore Direct3D 10 HLSL è ora il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="21f8e-133">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="21f8e-134">Per informazioni dettagliate, vedere [strumento del compilatore di effetti](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="21f8e-134">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="21f8e-135">*pPool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f8e-135">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f8e-136">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="21f8e-136">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="21f8e-137">Puntatore a un oggetto [**ID3DXEffectPool**](id3dxeffectpool.md) da utilizzare per i parametri condivisi.</span><span class="sxs-lookup"><span data-stu-id="21f8e-137">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="21f8e-138">Se questo valore è **null**, non verrà condiviso alcun parametro.</span><span class="sxs-lookup"><span data-stu-id="21f8e-138">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="21f8e-139">*ppEffect* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="21f8e-139">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21f8e-140">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="21f8e-140">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="21f8e-141">Restituisce un puntatore a un buffer contenente l'effetto compilato.</span><span class="sxs-lookup"><span data-stu-id="21f8e-141">Returns a pointer to a buffer containing the compiled effect.</span></span> <span data-ttu-id="21f8e-142">Vedere [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="21f8e-142">See [**ID3DXEffect**](id3dxeffect.md).</span></span>

</dd> <dt>

<span data-ttu-id="21f8e-143">*ppCompilationErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="21f8e-143">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21f8e-144">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="21f8e-144">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="21f8e-145">Restituisce un puntatore a un buffer contenente un elenco di errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="21f8e-145">Returns a pointer to a buffer containing a listing of compile errors.</span></span> <span data-ttu-id="21f8e-146">Vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="21f8e-146">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21f8e-147">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21f8e-147">Return value</span></span>

<span data-ttu-id="21f8e-148">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21f8e-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21f8e-149">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="21f8e-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="21f8e-150">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="21f8e-150">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="21f8e-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="21f8e-151">Remarks</span></span>

<span data-ttu-id="21f8e-152">Questa funzione è una versione estesa di [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) che consente a un'applicazione di specificare quali costanti di effetto verranno gestite dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="21f8e-152">This function is an extended version of [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="21f8e-153">Una costante gestita dall'applicazione viene ignorata dal sistema di effetti.</span><span class="sxs-lookup"><span data-stu-id="21f8e-153">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="21f8e-154">In altre condizioni, l'applicazione è responsabile dell'inizializzazione della costante, nonché del salvataggio e del ripristino dello stato quando appropriato.</span><span class="sxs-lookup"><span data-stu-id="21f8e-154">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="21f8e-155">Questa funzione controlla ogni costante in pSkipConstants per vedere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="21f8e-155">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="21f8e-156">È associato a un registro costante.</span><span class="sxs-lookup"><span data-stu-id="21f8e-156">It is bound to a constant register.</span></span>
-   <span data-ttu-id="21f8e-157">Viene usato solo nel codice shader HLSL.</span><span class="sxs-lookup"><span data-stu-id="21f8e-157">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="21f8e-158">Se una costante viene denominata nella stringa non presente nell'effetto, viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="21f8e-158">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

<span data-ttu-id="21f8e-159">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="21f8e-159">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="21f8e-160">In caso contrario, il tipo di dati LPCTSTR viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="21f8e-160">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="21f8e-161">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="21f8e-161">The compiler setting also determines the function version.</span></span> <span data-ttu-id="21f8e-162">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateEffectFromFileW.</span><span class="sxs-lookup"><span data-stu-id="21f8e-162">If Unicode is defined, the function call resolves to D3DXCreateEffectFromFileW.</span></span> <span data-ttu-id="21f8e-163">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateEffectFromFileA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="21f8e-163">Otherwise, the function call resolves to D3DXCreateEffectFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="21f8e-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21f8e-164">Requirements</span></span>



| <span data-ttu-id="21f8e-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="21f8e-165">Requirement</span></span> | <span data-ttu-id="21f8e-166">Valore</span><span class="sxs-lookup"><span data-stu-id="21f8e-166">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="21f8e-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21f8e-167">Header</span></span><br/>  | <dl> <span data-ttu-id="21f8e-168"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="21f8e-168"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="21f8e-169">Libreria</span><span class="sxs-lookup"><span data-stu-id="21f8e-169">Library</span></span><br/> | <dl> <span data-ttu-id="21f8e-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21f8e-170"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="21f8e-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21f8e-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21f8e-172">Funzioni effetto</span><span class="sxs-lookup"><span data-stu-id="21f8e-172">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="21f8e-173">**D3DXCreateEffectEx**</span><span class="sxs-lookup"><span data-stu-id="21f8e-173">**D3DXCreateEffectEx**</span></span>](d3dxcreateeffectex.md)
</dt> <dt>

[<span data-ttu-id="21f8e-174">**D3DXCreateEffectFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="21f8e-174">**D3DXCreateEffectFromResourceEx**</span></span>](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
