---
description: Assembla uno shader.
ms.assetid: 2977b64a-b8cc-454b-8e28-291f6f2c6fc1
title: Funzione D3DXAssembleShaderFromFile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6e355f6ce51158f72757f771114346899557c59
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322891"
---
# <a name="d3dxassembleshaderfromfile-function"></a><span data-ttu-id="ab348-103">D3DXAssembleShaderFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="ab348-103">D3DXAssembleShaderFromFile function</span></span>

<span data-ttu-id="ab348-104">Assembla uno shader.</span><span class="sxs-lookup"><span data-stu-id="ab348-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab348-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab348-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShaderFromFile(
  _In_        LPCTSTR       pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="ab348-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab348-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab348-107">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab348-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab348-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab348-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab348-109">Puntatore a una stringa che specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="ab348-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="ab348-110">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="ab348-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ab348-111">In caso contrario, il tipo di dati String viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ab348-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="ab348-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ab348-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ab348-113">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab348-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab348-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="ab348-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="ab348-115">Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="ab348-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="ab348-116">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="ab348-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ab348-117">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab348-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab348-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="ab348-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="ab348-119">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="ab348-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="ab348-120">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="ab348-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="ab348-121">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab348-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab348-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab348-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab348-123">Opzioni di compilazione identificate da diversi flag.</span><span class="sxs-lookup"><span data-stu-id="ab348-123">Compile options identified by various flags.</span></span> <span data-ttu-id="ab348-124">Il compilatore Direct3D 10 HLSL è ora il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ab348-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="ab348-125">Per informazioni dettagliate, vedere [flag D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="ab348-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="ab348-126">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ab348-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab348-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab348-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ab348-128">Restituisce un buffer contenente lo shader creato.</span><span class="sxs-lookup"><span data-stu-id="ab348-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="ab348-129">Questo buffer contiene il codice dello shader compilato, nonché tutte le informazioni di debug e di tabella dei simboli incorporate.</span><span class="sxs-lookup"><span data-stu-id="ab348-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="ab348-130">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ab348-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab348-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab348-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ab348-132">Restituisce un buffer contenente un elenco di errori e avvisi che sono stati rilevati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="ab348-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="ab348-133">Si tratta degli stessi messaggi visualizzati dal debugger durante l'esecuzione in modalità di debug.</span><span class="sxs-lookup"><span data-stu-id="ab348-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="ab348-134">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="ab348-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab348-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab348-135">Return value</span></span>

<span data-ttu-id="ab348-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab348-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab348-137">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ab348-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ab348-138">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="ab348-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab348-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab348-139">Remarks</span></span>

<span data-ttu-id="ab348-140">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="ab348-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ab348-141">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXAssembleShaderFromFileW.</span><span class="sxs-lookup"><span data-stu-id="ab348-141">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromFileW.</span></span> <span data-ttu-id="ab348-142">In caso contrario, la chiamata di funzione viene risolta in D3DXAssembleShaderFromFileA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="ab348-142">Otherwise, the function call resolves to D3DXAssembleShaderFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab348-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab348-143">Requirements</span></span>



| <span data-ttu-id="ab348-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab348-144">Requirement</span></span> | <span data-ttu-id="ab348-145">Valore</span><span class="sxs-lookup"><span data-stu-id="ab348-145">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab348-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab348-146">Header</span></span><br/>  | <dl> <span data-ttu-id="ab348-147"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab348-147"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ab348-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="ab348-148">Library</span></span><br/> | <dl> <span data-ttu-id="ab348-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab348-149"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ab348-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab348-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab348-151">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="ab348-151">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="ab348-152">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="ab348-152">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="ab348-153">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="ab348-153">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
