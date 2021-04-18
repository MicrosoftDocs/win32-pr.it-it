---
description: Compilare un file shader.
ms.assetid: 2ad6042f-3601-4f4a-9624-6319a3372355
title: Funzione D3DXCompileShaderFromFile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 865241142fa13ec9d34826bfe334c30b38ca78d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322877"
---
# <a name="d3dxcompileshaderfromfile-function"></a><span data-ttu-id="a3d55-103">D3DXCompileShaderFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="a3d55-103">D3DXCompileShaderFromFile function</span></span>

<span data-ttu-id="a3d55-104">Compilare un file shader.</span><span class="sxs-lookup"><span data-stu-id="a3d55-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="a3d55-105">Invece di usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore da riga di comando o l'API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="a3d55-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a3d55-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3d55-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShaderFromFile(
  _In_        LPCTSTR             pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="a3d55-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3d55-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3d55-108">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d55-108">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d55-109">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3d55-109">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3d55-110">Puntatore a una stringa che specifica il nome del file.</span><span class="sxs-lookup"><span data-stu-id="a3d55-110">Pointer to a string that specifies the filename.</span></span>

</dd> <dt>

<span data-ttu-id="a3d55-111">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d55-111">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d55-112">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3d55-112">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="a3d55-113">Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="a3d55-113">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="a3d55-114">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="a3d55-114">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a3d55-115">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d55-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d55-116">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="a3d55-116">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="a3d55-117">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="a3d55-117">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="a3d55-118">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="a3d55-118">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="a3d55-119">*pFunctionName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d55-119">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d55-120">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3d55-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3d55-121">Puntatore alla funzione del punto di ingresso dello shader in cui inizia l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a3d55-121">Pointer to the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="a3d55-122">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d55-122">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d55-123">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3d55-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3d55-124">Puntatore a un profilo dello shader che determina il set di istruzioni dello shader.</span><span class="sxs-lookup"><span data-stu-id="a3d55-124">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="a3d55-125">Per un elenco dei profili disponibili, vedere [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="a3d55-125">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="a3d55-126">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3d55-126">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d55-127">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3d55-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3d55-128">Opzioni di compilazione identificate da diversi flag.</span><span class="sxs-lookup"><span data-stu-id="a3d55-128">Compile options identified by various flags.</span></span> <span data-ttu-id="a3d55-129">Il compilatore Direct3D 10 HLSL è ora il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a3d55-129">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="a3d55-130">Per informazioni dettagliate, vedere [flag D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="a3d55-130">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="a3d55-131">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a3d55-131">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d55-132">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3d55-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a3d55-133">Restituisce un buffer contenente lo shader creato.</span><span class="sxs-lookup"><span data-stu-id="a3d55-133">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="a3d55-134">Questo buffer contiene il codice dello shader compilato, nonché tutte le informazioni di debug e di tabella dei simboli incorporate.</span><span class="sxs-lookup"><span data-stu-id="a3d55-134">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="a3d55-135">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a3d55-135">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d55-136">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3d55-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a3d55-137">Restituisce un buffer contenente un elenco di errori e avvisi che sono stati rilevati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="a3d55-137">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="a3d55-138">Si tratta degli stessi messaggi visualizzati dal debugger durante l'esecuzione in modalità di debug.</span><span class="sxs-lookup"><span data-stu-id="a3d55-138">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="a3d55-139">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="a3d55-139">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a3d55-140">*ppConstantTable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a3d55-140">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3d55-141">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="a3d55-141">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="a3d55-142">Restituisce un'interfaccia [**ID3DXConstantTable**](id3dxconstanttable.md) che può essere utilizzata per accedere alle costanti dello shader.</span><span class="sxs-lookup"><span data-stu-id="a3d55-142">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="a3d55-143">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="a3d55-143">This value can be **NULL**.</span></span> <span data-ttu-id="a3d55-144">Se l'applicazione viene compilata con un indirizzo di grandi dimensioni (ovvero si usa l'opzione del linker/LARGEADDRESSAWARE per gestire gli indirizzi maggiori di 2 GB), non è possibile usare questo parametro e deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="a3d55-144">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="a3d55-145">È invece necessario utilizzare la funzione [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) per recuperare la tabella delle costanti shader incorporata all'interno dello shader.</span><span class="sxs-lookup"><span data-stu-id="a3d55-145">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="a3d55-146">In questa chiamata **D3DXGetShaderConstantTableEx** è necessario passare il flag **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parametro *Flags* per specificare di accedere a un massimo di 4 GB di spazio degli indirizzi virtuali.</span><span class="sxs-lookup"><span data-stu-id="a3d55-146">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3d55-147">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3d55-147">Return value</span></span>

<span data-ttu-id="a3d55-148">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a3d55-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a3d55-149">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a3d55-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a3d55-150">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, e \_ NOTIMPL, e \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="a3d55-150">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_NOTIMPL, E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="a3d55-151">\_Se si usano gli shader 1,1 (vs \_ 1 \_ 1 e PS \_ 1 \_ 1), viene restituito E NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="a3d55-151">E\_NOTIMPL is returned if you're using 1.1 shaders (vs\_1\_1 and ps\_1\_1).</span></span>

## <a name="requirements"></a><span data-ttu-id="a3d55-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3d55-152">Requirements</span></span>



| <span data-ttu-id="a3d55-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3d55-153">Requirement</span></span> | <span data-ttu-id="a3d55-154">Valore</span><span class="sxs-lookup"><span data-stu-id="a3d55-154">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3d55-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3d55-155">Header</span></span><br/>  | <dl> <span data-ttu-id="a3d55-156"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3d55-156"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a3d55-157">Libreria</span><span class="sxs-lookup"><span data-stu-id="a3d55-157">Library</span></span><br/> | <dl> <span data-ttu-id="a3d55-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3d55-158"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a3d55-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3d55-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3d55-160">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="a3d55-160">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="a3d55-161">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="a3d55-161">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="a3d55-162">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="a3d55-162">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
