---
description: Compilare un file shader.
ms.assetid: 9b19ab67-d5d5-482d-b3fe-ce20b64d7ad8
title: Funzione D3DXCompileShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65dd9f74280abe7ee2fe427a4772b14b88742e97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354729"
---
# <a name="d3dxcompileshader-function"></a><span data-ttu-id="36d7f-103">D3DXCompileShader (funzione)</span><span class="sxs-lookup"><span data-stu-id="36d7f-103">D3DXCompileShader function</span></span>

<span data-ttu-id="36d7f-104">Compilare un file shader.</span><span class="sxs-lookup"><span data-stu-id="36d7f-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="36d7f-105">Invece di usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore da riga di comando o l'API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="36d7f-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="36d7f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36d7f-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShader(
  _In_        LPCSTR              pSrcData,
  _In_        UINT                srcDataLen,
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



## <a name="parameters"></a><span data-ttu-id="36d7f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="36d7f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36d7f-108">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36d7f-108">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d7f-109">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36d7f-109">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36d7f-110">Puntatore a una stringa che contiene lo shader.</span><span class="sxs-lookup"><span data-stu-id="36d7f-110">Pointer to a string that contains the shader.</span></span>

</dd> <dt>

<span data-ttu-id="36d7f-111">*srcDataLen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36d7f-111">*srcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d7f-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36d7f-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36d7f-113">Lunghezza dei dati in byte.</span><span class="sxs-lookup"><span data-stu-id="36d7f-113">Length of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="36d7f-114">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36d7f-114">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d7f-115">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="36d7f-115">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="36d7f-116">Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="36d7f-116">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="36d7f-117">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="36d7f-117">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="36d7f-118">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36d7f-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d7f-119">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="36d7f-119">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="36d7f-120">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="36d7f-120">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="36d7f-121">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="36d7f-121">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="36d7f-122">*pFunctionName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36d7f-122">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d7f-123">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36d7f-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36d7f-124">Puntatore a una stringa che contiene il nome della funzione del punto di ingresso dello shader in cui inizia l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="36d7f-124">Pointer to a string that contains the name of the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="36d7f-125">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36d7f-125">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d7f-126">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36d7f-126">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36d7f-127">Puntatore a un profilo dello shader che determina il set di istruzioni dello shader.</span><span class="sxs-lookup"><span data-stu-id="36d7f-127">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="36d7f-128">Per un elenco dei profili disponibili, vedere [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="36d7f-128">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="36d7f-129">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36d7f-129">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d7f-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36d7f-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36d7f-131">Opzioni di compilazione identificate da diversi flag.</span><span class="sxs-lookup"><span data-stu-id="36d7f-131">Compile options identified by various flags.</span></span> <span data-ttu-id="36d7f-132">Il compilatore Direct3D 10 HLSL è ora il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="36d7f-132">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="36d7f-133">Per informazioni dettagliate, vedere [flag D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="36d7f-133">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="36d7f-134">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="36d7f-134">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36d7f-135">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="36d7f-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="36d7f-136">Restituisce un buffer contenente lo shader creato.</span><span class="sxs-lookup"><span data-stu-id="36d7f-136">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="36d7f-137">Questo buffer contiene il codice dello shader compilato, nonché tutte le informazioni di debug e di tabella dei simboli incorporate.</span><span class="sxs-lookup"><span data-stu-id="36d7f-137">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="36d7f-138">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="36d7f-138">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36d7f-139">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="36d7f-139">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="36d7f-140">Restituisce un buffer contenente un elenco di errori e avvisi che sono stati rilevati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="36d7f-140">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="36d7f-141">Si tratta degli stessi messaggi visualizzati dal debugger durante l'esecuzione in modalità di debug.</span><span class="sxs-lookup"><span data-stu-id="36d7f-141">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="36d7f-142">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="36d7f-142">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="36d7f-143">*ppConstantTable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="36d7f-143">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36d7f-144">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="36d7f-144">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="36d7f-145">Restituisce un'interfaccia [**ID3DXConstantTable**](id3dxconstanttable.md) che può essere utilizzata per accedere alle costanti dello shader.</span><span class="sxs-lookup"><span data-stu-id="36d7f-145">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="36d7f-146">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="36d7f-146">This value can be **NULL**.</span></span> <span data-ttu-id="36d7f-147">Se l'applicazione viene compilata con un indirizzo di grandi dimensioni (ovvero si usa l'opzione del linker/LARGEADDRESSAWARE per gestire gli indirizzi maggiori di 2 GB), non è possibile usare questo parametro e deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="36d7f-147">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="36d7f-148">È invece necessario utilizzare la funzione [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) per recuperare la tabella delle costanti shader incorporata all'interno dello shader.</span><span class="sxs-lookup"><span data-stu-id="36d7f-148">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="36d7f-149">In questa chiamata **D3DXGetShaderConstantTableEx** è necessario passare il flag **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parametro *Flags* per specificare di accedere a un massimo di 4 GB di spazio degli indirizzi virtuali.</span><span class="sxs-lookup"><span data-stu-id="36d7f-149">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36d7f-150">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="36d7f-150">Return value</span></span>

<span data-ttu-id="36d7f-151">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="36d7f-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="36d7f-152">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="36d7f-152">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="36d7f-153">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="36d7f-153">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="36d7f-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36d7f-154">Requirements</span></span>



| <span data-ttu-id="36d7f-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="36d7f-155">Requirement</span></span> | <span data-ttu-id="36d7f-156">Valore</span><span class="sxs-lookup"><span data-stu-id="36d7f-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="36d7f-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36d7f-157">Header</span></span><br/>  | <dl> <span data-ttu-id="36d7f-158"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="36d7f-158"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="36d7f-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="36d7f-159">Library</span></span><br/> | <dl> <span data-ttu-id="36d7f-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36d7f-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="36d7f-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36d7f-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d7f-162">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="36d7f-162">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="36d7f-163">**D3DXCompileShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="36d7f-163">**D3DXCompileShaderFromFile**</span></span>](d3dxcompileshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="36d7f-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="36d7f-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
