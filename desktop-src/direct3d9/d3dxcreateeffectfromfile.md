---
description: "Funzione D3DXCreateEffectFromFile: creare un effetto da una descrizione dell'effetto ASCII o binario."
ms.assetid: b5868ba3-0869-46f7-804f-3103358a3ef5
title: Funzione D3DXCreateEffectFromFile (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d8b2afdd1e8008bc8e03efa670e5a4b37b6dc9f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094319"
---
# <a name="d3dxcreateeffectfromfile-function"></a><span data-ttu-id="9c631-103">Funzione D3DXCreateEffectFromFile</span><span class="sxs-lookup"><span data-stu-id="9c631-103">D3DXCreateEffectFromFile function</span></span>

<span data-ttu-id="9c631-104">Creare un effetto da una descrizione dell'effetto ASCII o binario.</span><span class="sxs-lookup"><span data-stu-id="9c631-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c631-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c631-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromFile(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="9c631-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c631-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c631-107">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9c631-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c631-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="9c631-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="9c631-109">Puntatore al dispositivo che creerà l'effetto.</span><span class="sxs-lookup"><span data-stu-id="9c631-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="9c631-110">Vedere [**IDirect3DDevice9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)</span><span class="sxs-lookup"><span data-stu-id="9c631-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="9c631-111">*pSrcFile* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9c631-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c631-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c631-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c631-113">Puntatore al nome file.</span><span class="sxs-lookup"><span data-stu-id="9c631-113">Pointer to the filename.</span></span> <span data-ttu-id="9c631-114">Questo parametro supporta sia stringhe Unicode che ANSI.</span><span class="sxs-lookup"><span data-stu-id="9c631-114">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="9c631-115">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="9c631-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9c631-116">*pDefines* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9c631-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c631-117">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="9c631-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="9c631-118">Matrice facoltativa di definizioni di macro del preprocessore con terminazione NULL.</span><span class="sxs-lookup"><span data-stu-id="9c631-118">Optional NULL-terminated array of preprocessor macro definitions.</span></span> <span data-ttu-id="9c631-119">Vedere [**D3DXMACRO**](d3dxmacro.md).</span><span class="sxs-lookup"><span data-stu-id="9c631-119">See [**D3DXMACRO**](d3dxmacro.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c631-120">*pInclude* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9c631-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c631-121">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="9c631-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="9c631-122">Puntatore a interfaccia [**facoltativo, ID3DXInclude,**](id3dxinclude.md)da usare per la gestione \# delle direttive include.</span><span class="sxs-lookup"><span data-stu-id="9c631-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="9c631-123">Se questo valore è **NULL,** include verrà rispettato durante la compilazione da un file o causerà un errore durante la compilazione \# da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="9c631-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="9c631-124">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9c631-124">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c631-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9c631-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9c631-126">Se *pSrcFile contiene* un effetto di testo, i flag possono essere una combinazione di flag [D3DXSHADER](d3dxshader-flags.md) e [flag D3DXFX;](d3dxfx.md) In caso contrario, *pSrcFile* contiene un effetto binario e gli unici flag rispettati sono i flag D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="9c631-126">If *pSrcFile* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcFile* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="9c631-127">Il compilatore HLSL Direct3D 10 è ora l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="9c631-127">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="9c631-128">Per [informazioni dettagliate, vedere Effect-Compiler Tool](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="9c631-128">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="9c631-129">*pPool* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="9c631-129">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c631-130">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="9c631-130">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="9c631-131">Puntatore a [**un oggetto ID3DXEffectPool**](id3dxeffectpool.md) da usare per i parametri condivisi.</span><span class="sxs-lookup"><span data-stu-id="9c631-131">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="9c631-132">Se questo valore è **NULL,** non verrà condiviso alcun parametro.</span><span class="sxs-lookup"><span data-stu-id="9c631-132">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="9c631-133">*ppEffect* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="9c631-133">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c631-134">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c631-134">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="9c631-135">Restituisce un puntatore a un buffer contenente l'effetto compilato.</span><span class="sxs-lookup"><span data-stu-id="9c631-135">Returns a pointer to a buffer containing the compiled effect.</span></span> <span data-ttu-id="9c631-136">Vedere [**ID3DXEffect.**](id3dxeffect.md)</span><span class="sxs-lookup"><span data-stu-id="9c631-136">See [**ID3DXEffect**](id3dxeffect.md).</span></span>

</dd> <dt>

<span data-ttu-id="9c631-137">*ppCompilationErrors* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="9c631-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c631-138">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9c631-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9c631-139">Restituisce un puntatore a un buffer contenente un elenco di errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="9c631-139">Returns a pointer to a buffer containing a listing of compile errors.</span></span> <span data-ttu-id="9c631-140">Vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="9c631-140">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c631-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c631-141">Return value</span></span>

<span data-ttu-id="9c631-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9c631-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9c631-143">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9c631-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9c631-144">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9c631-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c631-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c631-145">Remarks</span></span>

<span data-ttu-id="9c631-146">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="9c631-146">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="9c631-147">In caso contrario, il tipo di dati LPCTSTR viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="9c631-147">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="9c631-148">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="9c631-148">The compiler setting also determines the function version.</span></span> <span data-ttu-id="9c631-149">Se unicode è definito, la chiamata di funzione viene risolta in D3DXCreateEffectFromFileW.</span><span class="sxs-lookup"><span data-stu-id="9c631-149">If Unicode is defined, the function call resolves to D3DXCreateEffectFromFileW.</span></span> <span data-ttu-id="9c631-150">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateEffectFromFileA perché vengono usate stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="9c631-150">Otherwise, the function call resolves to D3DXCreateEffectFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c631-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c631-151">Requirements</span></span>



| <span data-ttu-id="9c631-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c631-152">Requirement</span></span> | <span data-ttu-id="9c631-153">Valore</span><span class="sxs-lookup"><span data-stu-id="9c631-153">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c631-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9c631-154">Header</span></span><br/>  | <dl> <span data-ttu-id="9c631-155"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="9c631-155"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="9c631-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="9c631-156">Library</span></span><br/> | <dl> <span data-ttu-id="9c631-157"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="9c631-157"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9c631-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c631-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c631-159">Funzioni degli effetti</span><span class="sxs-lookup"><span data-stu-id="9c631-159">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="9c631-160">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="9c631-160">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="9c631-161">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="9c631-161">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
