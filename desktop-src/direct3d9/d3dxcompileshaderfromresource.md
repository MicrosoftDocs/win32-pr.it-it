---
description: 'Funzione D3DXCompileShaderFromResource: consente di compilare un file shader.'
ms.assetid: e944ae61-0c27-4795-8381-0ec9b3d8c3f4
title: Funzione D3DXCompileShaderFromResource (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de94754004cc42bcc6914d9513588a71a1a593dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115809"
---
# <a name="d3dxcompileshaderfromresource-function"></a><span data-ttu-id="4e7b3-103">Funzione D3DXCompileShaderFromResource</span><span class="sxs-lookup"><span data-stu-id="4e7b3-103">D3DXCompileShaderFromResource function</span></span>

<span data-ttu-id="4e7b3-104">Compilare un file shader.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="4e7b3-105">Anziché usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando Fxc.exe compilatore da riga di comando o usare l'API [**D3DCompile.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile)</span><span class="sxs-lookup"><span data-stu-id="4e7b3-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4e7b3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e7b3-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShaderFromResource(
  _In_        HMODULE             hSrcModule,
  _In_        LPCSTR              pSrcResource,
  _In_  const D3DXMACRO           *pDefines,
  _In_        LPD3DXINCLUDE       pInclude,
  _In_        LPCSTR              pFunctionName,
  _In_        LPCSTR              pProfile,
  _In_        DWORD               Flags,
  _Out_       LPD3DXBUFFER        *ppShader,
  _Out_       LPD3DXBUFFER        *ppErrorMsgs,
  _Out_       LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="4e7b3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e7b3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e7b3-108">*hSrcModule* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4e7b3-108">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7b3-109">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e7b3-109">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e7b3-110">Handle per un modulo contenente la descrizione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-110">Handle to a module containing the effect description.</span></span> <span data-ttu-id="4e7b3-111">Se questo parametro è **NULL,** verrà usato il modulo corrente.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-111">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="4e7b3-112">*pSrcResource* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4e7b3-112">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7b3-113">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e7b3-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e7b3-114">Puntatore a una stringa che specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-114">Pointer to a string that specifies the resource name.</span></span>

</dd> <dt>

<span data-ttu-id="4e7b3-115">*pDefines* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4e7b3-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7b3-116">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="4e7b3-116">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="4e7b3-117">Matrice facoltativa **con terminazione NULL** di [**strutture D3DXMACRO.**](d3dxmacro.md)</span><span class="sxs-lookup"><span data-stu-id="4e7b3-117">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="4e7b3-118">Questo valore può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="4e7b3-118">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4e7b3-119">*pInclude* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4e7b3-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7b3-120">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="4e7b3-120">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="4e7b3-121">Puntatore a interfaccia [**facoltativo, ID3DXInclude,**](id3dxinclude.md)da usare per la gestione \# delle direttive include.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-121">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="4e7b3-122">Se questo valore è **NULL,** include verrà rispettato durante la compilazione da un file o verrà generato un errore durante la compilazione \# da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-122">If this value is **NULL**, \#includes will either be honored when compiling from a file, or will error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="4e7b3-123">*pFunctionName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4e7b3-123">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7b3-124">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e7b3-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e7b3-125">Puntatore alla funzione del punto di ingresso dello shader da cui ha inizio l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-125">Pointer to the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="4e7b3-126">*pProfile* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4e7b3-126">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7b3-127">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e7b3-127">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e7b3-128">Puntatore a un profilo shader che determina il set di istruzioni dello shader.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-128">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="4e7b3-129">Per un elenco dei profili disponibili, vedere [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile.**](d3dxgetpixelshaderprofile.md)</span><span class="sxs-lookup"><span data-stu-id="4e7b3-129">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="4e7b3-130">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4e7b3-130">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7b3-131">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e7b3-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e7b3-132">Opzioni di compilazione identificate da vari flag.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-132">Compile options identified by various flags.</span></span> <span data-ttu-id="4e7b3-133">Il compilatore HLSL Direct3D 10 è ora l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-133">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="4e7b3-134">Per [informazioni dettagliate, vedere Flag D3DXSHADER.](d3dxshader-flags.md)</span><span class="sxs-lookup"><span data-stu-id="4e7b3-134">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="4e7b3-135">*ppShader* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="4e7b3-135">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7b3-136">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e7b3-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="4e7b3-137">Restituisce un buffer contenente lo shader creato.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-137">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="4e7b3-138">Questo buffer contiene il codice dello shader compilato, nonché eventuali informazioni incorporate sulla tabella di debug e simboli.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-138">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="4e7b3-139">*ppErrorMsgs* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="4e7b3-139">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7b3-140">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e7b3-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="4e7b3-141">Restituisce un buffer contenente un elenco di errori e avvisi rilevati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-141">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="4e7b3-142">Si tratta degli stessi messaggi visualizzati dal debugger durante l'esecuzione in modalità di debug.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-142">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="4e7b3-143">Questo valore può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="4e7b3-143">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4e7b3-144">*ppConstantTable* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="4e7b3-144">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e7b3-145">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="4e7b3-145">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="4e7b3-146">Restituisce [**un'interfaccia ID3DXConstantTable,**](id3dxconstanttable.md) che può essere usata per accedere alle costanti shader.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-146">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="4e7b3-147">Questo valore può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="4e7b3-147">This value can be **NULL**.</span></span> <span data-ttu-id="4e7b3-148">Se si compila l'applicazione come a conoscenza di indirizzi di grandi dimensioni, ovvero si usa l'opzione del linker /LARGEADDRESSAWARE per gestire indirizzi di dimensioni superiori a 2 GB, non è possibile usare questo parametro e impostarlo su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="4e7b3-148">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="4e7b3-149">È invece necessario usare la [**funzione D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) per recuperare la tabella costante shader incorporata all'interno dello shader.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-149">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="4e7b3-150">In questa chiamata **D3DXGetShaderConstantTableEx** è necessario passare il flag **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parametro *Flags* per specificare di accedere a un massimo di 4 GB di spazio degli indirizzi virtuali.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-150">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e7b3-151">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e7b3-151">Return value</span></span>

<span data-ttu-id="4e7b3-152">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4e7b3-152">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4e7b3-153">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-153">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4e7b3-154">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4e7b3-154">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e7b3-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e7b3-155">Requirements</span></span>



| <span data-ttu-id="4e7b3-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e7b3-156">Requirement</span></span> | <span data-ttu-id="4e7b3-157">Valore</span><span class="sxs-lookup"><span data-stu-id="4e7b3-157">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e7b3-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e7b3-158">Header</span></span><br/>  | <dl> <span data-ttu-id="4e7b3-159"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="4e7b3-159"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="4e7b3-160">Libreria</span><span class="sxs-lookup"><span data-stu-id="4e7b3-160">Library</span></span><br/> | <dl> <span data-ttu-id="4e7b3-161"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e7b3-161"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4e7b3-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e7b3-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e7b3-163">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="4e7b3-163">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="4e7b3-164">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="4e7b3-164">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="4e7b3-165">**D3DXCompileShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="4e7b3-165">**D3DXCompileShaderFromFile**</span></span>](d3dxcompileshaderfromfile.md)
</dt> </dl>

 

 
