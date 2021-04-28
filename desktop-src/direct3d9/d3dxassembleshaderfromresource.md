---
description: 'Funzione D3DXAssembleShaderFromResource: assemblare uno shader.'
ms.assetid: a0d31b15-db79-4aa8-afd8-fa1e20c61725
title: Funzione D3DXAssembleShaderFromResource (D3DX9Shader.h)
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
ms.openlocfilehash: 78df978201df37269b7d33058effc16eadc9d16f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116018"
---
# <a name="d3dxassembleshaderfromresource-function"></a><span data-ttu-id="ea82a-103">Funzione D3DXAssembleShaderFromResource</span><span class="sxs-lookup"><span data-stu-id="ea82a-103">D3DXAssembleShaderFromResource function</span></span>

<span data-ttu-id="ea82a-104">Assemblare uno shader.</span><span class="sxs-lookup"><span data-stu-id="ea82a-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea82a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea82a-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="ea82a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea82a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea82a-107">*hSrcModule* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ea82a-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea82a-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea82a-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea82a-109">Handle per un modulo contenente la descrizione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="ea82a-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="ea82a-110">Se questo parametro è **NULL,** verrà usato il modulo corrente.</span><span class="sxs-lookup"><span data-stu-id="ea82a-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="ea82a-111">*pSrcResource* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ea82a-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea82a-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea82a-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea82a-113">Puntatore a una stringa che specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ea82a-113">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="ea82a-114">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="ea82a-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ea82a-115">In caso contrario, il tipo di dati stringa viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ea82a-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="ea82a-116">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ea82a-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ea82a-117">*pDefines* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ea82a-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea82a-118">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea82a-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="ea82a-119">Matrice facoltativa **con terminazione NULL** di [**strutture D3DXMACRO.**](d3dxmacro.md)</span><span class="sxs-lookup"><span data-stu-id="ea82a-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="ea82a-120">Questo valore può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="ea82a-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ea82a-121">*pInclude* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ea82a-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea82a-122">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="ea82a-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="ea82a-123">Puntatore a interfaccia [**facoltativo, ID3DXInclude,**](id3dxinclude.md)da usare per la gestione \# delle direttive include.</span><span class="sxs-lookup"><span data-stu-id="ea82a-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="ea82a-124">Se questo valore è **NULL,** le include verranno rispettate durante la compilazione da un file o causeranno un errore durante la compilazione \# da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="ea82a-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="ea82a-125">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="ea82a-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea82a-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea82a-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea82a-127">Opzioni di compilazione identificate da vari flag.</span><span class="sxs-lookup"><span data-stu-id="ea82a-127">Compile options identified by various flags.</span></span> <span data-ttu-id="ea82a-128">Il compilatore HLSL Direct3D 10 è ora l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ea82a-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="ea82a-129">Per [informazioni dettagliate, vedere Flag D3DXSHADER.](d3dxshader-flags.md)</span><span class="sxs-lookup"><span data-stu-id="ea82a-129">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="ea82a-130">*ppShader* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="ea82a-130">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea82a-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea82a-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ea82a-132">Restituisce un buffer contenente lo shader creato.</span><span class="sxs-lookup"><span data-stu-id="ea82a-132">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="ea82a-133">Questo buffer contiene il codice dello shader compilato, nonché eventuali informazioni incorporate sulla tabella di debug e simboli.</span><span class="sxs-lookup"><span data-stu-id="ea82a-133">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="ea82a-134">*ppErrorMsgs* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="ea82a-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea82a-135">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea82a-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ea82a-136">Restituisce un buffer contenente un elenco di errori e avvisi rilevati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="ea82a-136">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="ea82a-137">Si tratta degli stessi messaggi visualizzati dal debugger durante l'esecuzione in modalità di debug.</span><span class="sxs-lookup"><span data-stu-id="ea82a-137">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="ea82a-138">Questo valore può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="ea82a-138">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea82a-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea82a-139">Return value</span></span>

<span data-ttu-id="ea82a-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ea82a-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ea82a-141">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea82a-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ea82a-142">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ea82a-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea82a-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea82a-143">Remarks</span></span>

<span data-ttu-id="ea82a-144">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="ea82a-144">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ea82a-145">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXAssembleShaderFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="ea82a-145">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromResourceW.</span></span> <span data-ttu-id="ea82a-146">In caso contrario, la chiamata di funzione viene risolta in D3DXAssembleShaderFromResourceA perché vengono usate stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="ea82a-146">Otherwise, the function call resolves to D3DXAssembleShaderFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea82a-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea82a-147">Requirements</span></span>



| <span data-ttu-id="ea82a-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea82a-148">Requirement</span></span> | <span data-ttu-id="ea82a-149">Valore</span><span class="sxs-lookup"><span data-stu-id="ea82a-149">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea82a-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea82a-150">Header</span></span><br/>  | <dl> <span data-ttu-id="ea82a-151"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="ea82a-151"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ea82a-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="ea82a-152">Library</span></span><br/> | <dl> <span data-ttu-id="ea82a-153"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea82a-153"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ea82a-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea82a-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea82a-155">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="ea82a-155">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="ea82a-156">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="ea82a-156">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="ea82a-157">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="ea82a-157">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
