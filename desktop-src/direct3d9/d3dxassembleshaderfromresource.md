---
description: Assembla uno shader.
ms.assetid: a0d31b15-db79-4aa8-afd8-fa1e20c61725
title: Funzione D3DXAssembleShaderFromResource (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5e748764eec94ea1f555c225c34680392610c9f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323549"
---
# <a name="d3dxassembleshaderfromresource-function"></a><span data-ttu-id="5beb1-103">D3DXAssembleShaderFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="5beb1-103">D3DXAssembleShaderFromResource function</span></span>

<span data-ttu-id="5beb1-104">Assembla uno shader.</span><span class="sxs-lookup"><span data-stu-id="5beb1-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="5beb1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5beb1-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCTSTR       pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="5beb1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5beb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5beb1-107">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5beb1-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5beb1-108">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5beb1-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5beb1-109">Handle per un modulo che contiene la descrizione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="5beb1-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="5beb1-110">Se questo parametro è **null**, verrà usato il modulo corrente.</span><span class="sxs-lookup"><span data-stu-id="5beb1-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="5beb1-111">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5beb1-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5beb1-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5beb1-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5beb1-113">Puntatore a una stringa che specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5beb1-113">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="5beb1-114">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="5beb1-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="5beb1-115">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="5beb1-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="5beb1-116">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="5beb1-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5beb1-117">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5beb1-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5beb1-118">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="5beb1-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="5beb1-119">Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="5beb1-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="5beb1-120">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="5beb1-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5beb1-121">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5beb1-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5beb1-122">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="5beb1-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="5beb1-123">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="5beb1-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="5beb1-124">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="5beb1-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="5beb1-125">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5beb1-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5beb1-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5beb1-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5beb1-127">Opzioni di compilazione identificate da diversi flag.</span><span class="sxs-lookup"><span data-stu-id="5beb1-127">Compile options identified by various flags.</span></span> <span data-ttu-id="5beb1-128">Il compilatore Direct3D 10 HLSL è ora il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="5beb1-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="5beb1-129">Per informazioni dettagliate, vedere [flag D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="5beb1-129">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="5beb1-130">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5beb1-130">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5beb1-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5beb1-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="5beb1-132">Restituisce un buffer contenente lo shader creato.</span><span class="sxs-lookup"><span data-stu-id="5beb1-132">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="5beb1-133">Questo buffer contiene il codice dello shader compilato, nonché tutte le informazioni di debug e di tabella dei simboli incorporate.</span><span class="sxs-lookup"><span data-stu-id="5beb1-133">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="5beb1-134">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5beb1-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5beb1-135">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5beb1-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="5beb1-136">Restituisce un buffer contenente un elenco di errori e avvisi che sono stati rilevati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="5beb1-136">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="5beb1-137">Si tratta degli stessi messaggi visualizzati dal debugger durante l'esecuzione in modalità di debug.</span><span class="sxs-lookup"><span data-stu-id="5beb1-137">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="5beb1-138">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="5beb1-138">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5beb1-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5beb1-139">Return value</span></span>

<span data-ttu-id="5beb1-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5beb1-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5beb1-141">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5beb1-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5beb1-142">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="5beb1-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5beb1-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="5beb1-143">Remarks</span></span>

<span data-ttu-id="5beb1-144">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="5beb1-144">The compiler setting also determines the function version.</span></span> <span data-ttu-id="5beb1-145">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXAssembleShaderFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="5beb1-145">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromResourceW.</span></span> <span data-ttu-id="5beb1-146">In caso contrario, la chiamata di funzione viene risolta in D3DXAssembleShaderFromResourceA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="5beb1-146">Otherwise, the function call resolves to D3DXAssembleShaderFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="5beb1-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5beb1-147">Requirements</span></span>



| <span data-ttu-id="5beb1-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="5beb1-148">Requirement</span></span> | <span data-ttu-id="5beb1-149">Valore</span><span class="sxs-lookup"><span data-stu-id="5beb1-149">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5beb1-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5beb1-150">Header</span></span><br/>  | <dl> <span data-ttu-id="5beb1-151"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5beb1-151"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5beb1-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="5beb1-152">Library</span></span><br/> | <dl> <span data-ttu-id="5beb1-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5beb1-153"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5beb1-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5beb1-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5beb1-155">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="5beb1-155">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="5beb1-156">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="5beb1-156">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="5beb1-157">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="5beb1-157">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
