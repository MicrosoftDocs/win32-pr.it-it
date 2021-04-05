---
description: Creare un effetto dalla descrizione di un effetto ASCII o binario.
ms.assetid: b5868ba3-0869-46f7-804f-3103358a3ef5
title: Funzione D3DXCreateEffectFromFile (D3DX9Effect. h)
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
ms.openlocfilehash: f34d0cdb3ae19772f21d8307fffb395c4d1ac9ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762280"
---
# <a name="d3dxcreateeffectfromfile-function"></a><span data-ttu-id="3d937-103">D3DXCreateEffectFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="3d937-103">D3DXCreateEffectFromFile function</span></span>

<span data-ttu-id="3d937-104">Creare un effetto dalla descrizione di un effetto ASCII o binario.</span><span class="sxs-lookup"><span data-stu-id="3d937-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d937-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d937-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="3d937-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d937-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d937-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d937-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d937-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="3d937-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="3d937-109">Puntatore al dispositivo che creerà l'effetto.</span><span class="sxs-lookup"><span data-stu-id="3d937-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="3d937-110">Vedere [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="3d937-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="3d937-111">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d937-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d937-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3d937-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3d937-113">Puntatore al nome file.</span><span class="sxs-lookup"><span data-stu-id="3d937-113">Pointer to the filename.</span></span> <span data-ttu-id="3d937-114">Questo parametro supporta sia stringhe Unicode che ANSI.</span><span class="sxs-lookup"><span data-stu-id="3d937-114">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="3d937-115">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="3d937-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3d937-116">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d937-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d937-117">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="3d937-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="3d937-118">Matrice facoltativa con terminazione NULL di definizioni di macro del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="3d937-118">Optional NULL-terminated array of preprocessor macro definitions.</span></span> <span data-ttu-id="3d937-119">Vedere [**D3DXMACRO**](d3dxmacro.md).</span><span class="sxs-lookup"><span data-stu-id="3d937-119">See [**D3DXMACRO**](d3dxmacro.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d937-120">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d937-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d937-121">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="3d937-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="3d937-122">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="3d937-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="3d937-123">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="3d937-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="3d937-124">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d937-124">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d937-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3d937-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3d937-126">Se *pSrcFile* contiene un effetto di testo, i flag possono essere una combinazione di flag [D3DXSHADER](d3dxshader-flags.md) e flag [D3DXFX](d3dxfx.md) ; in caso contrario, *pSrcFile* contiene un effetto binario e gli unici flag rispettati sono i flag D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="3d937-126">If *pSrcFile* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcFile* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="3d937-127">Il compilatore Direct3D 10 HLSL è ora il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3d937-127">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="3d937-128">Per informazioni dettagliate, vedere [strumento del compilatore di effetti](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="3d937-128">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="3d937-129">*pPool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3d937-129">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d937-130">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="3d937-130">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="3d937-131">Puntatore a un oggetto [**ID3DXEffectPool**](id3dxeffectpool.md) da utilizzare per i parametri condivisi.</span><span class="sxs-lookup"><span data-stu-id="3d937-131">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="3d937-132">Se questo valore è **null**, non verrà condiviso alcun parametro.</span><span class="sxs-lookup"><span data-stu-id="3d937-132">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="3d937-133">*ppEffect* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3d937-133">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d937-134">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d937-134">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="3d937-135">Restituisce un puntatore a un buffer contenente l'effetto compilato.</span><span class="sxs-lookup"><span data-stu-id="3d937-135">Returns a pointer to a buffer containing the compiled effect.</span></span> <span data-ttu-id="3d937-136">Vedere [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="3d937-136">See [**ID3DXEffect**](id3dxeffect.md).</span></span>

</dd> <dt>

<span data-ttu-id="3d937-137">*ppCompilationErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3d937-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d937-138">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3d937-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3d937-139">Restituisce un puntatore a un buffer contenente un elenco di errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="3d937-139">Returns a pointer to a buffer containing a listing of compile errors.</span></span> <span data-ttu-id="3d937-140">Vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="3d937-140">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d937-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d937-141">Return value</span></span>

<span data-ttu-id="3d937-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3d937-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3d937-143">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3d937-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3d937-144">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="3d937-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d937-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d937-145">Remarks</span></span>

<span data-ttu-id="3d937-146">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="3d937-146">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="3d937-147">In caso contrario, il tipo di dati LPCTSTR viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="3d937-147">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="3d937-148">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="3d937-148">The compiler setting also determines the function version.</span></span> <span data-ttu-id="3d937-149">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateEffectFromFileW.</span><span class="sxs-lookup"><span data-stu-id="3d937-149">If Unicode is defined, the function call resolves to D3DXCreateEffectFromFileW.</span></span> <span data-ttu-id="3d937-150">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateEffectFromFileA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="3d937-150">Otherwise, the function call resolves to D3DXCreateEffectFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d937-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d937-151">Requirements</span></span>



| <span data-ttu-id="3d937-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d937-152">Requirement</span></span> | <span data-ttu-id="3d937-153">Valore</span><span class="sxs-lookup"><span data-stu-id="3d937-153">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d937-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d937-154">Header</span></span><br/>  | <dl> <span data-ttu-id="3d937-155"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d937-155"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="3d937-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="3d937-156">Library</span></span><br/> | <dl> <span data-ttu-id="3d937-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d937-157"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3d937-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d937-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d937-159">Funzioni effetto</span><span class="sxs-lookup"><span data-stu-id="3d937-159">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="3d937-160">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="3d937-160">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="3d937-161">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="3d937-161">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
