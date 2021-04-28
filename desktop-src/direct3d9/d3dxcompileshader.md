---
description: 'Funzione D3DXCompileShader: consente di compilare un file shader.'
ms.assetid: 9b19ab67-d5d5-482d-b3fe-ce20b64d7ad8
title: Funzione D3DXCompileShader (D3DX9Shader.h)
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
ms.openlocfilehash: b1f5e5f0f30714ed001438235e124341b8ce4d35
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115859"
---
# <a name="d3dxcompileshader-function"></a><span data-ttu-id="91371-103">Funzione D3DXCompileShader</span><span class="sxs-lookup"><span data-stu-id="91371-103">D3DXCompileShader function</span></span>

<span data-ttu-id="91371-104">Compilare un file shader.</span><span class="sxs-lookup"><span data-stu-id="91371-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="91371-105">Invece di usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando il Fxc.exe della riga di comando o l'API [**D3DCompile.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile)</span><span class="sxs-lookup"><span data-stu-id="91371-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="91371-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91371-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="91371-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="91371-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91371-108">*pSrcData* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="91371-108">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91371-109">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91371-109">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91371-110">Puntatore a una stringa che contiene lo shader.</span><span class="sxs-lookup"><span data-stu-id="91371-110">Pointer to a string that contains the shader.</span></span>

</dd> <dt>

<span data-ttu-id="91371-111">*srcDataLen* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="91371-111">*srcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91371-112">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91371-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91371-113">Lunghezza dei dati in byte.</span><span class="sxs-lookup"><span data-stu-id="91371-113">Length of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="91371-114">*pDefines* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="91371-114">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91371-115">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="91371-115">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="91371-116">Matrice facoltativa con terminazione **NULL** di [**strutture D3DXMACRO.**](d3dxmacro.md)</span><span class="sxs-lookup"><span data-stu-id="91371-116">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="91371-117">Questo valore può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="91371-117">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="91371-118">*pInclude* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="91371-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91371-119">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="91371-119">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="91371-120">Puntatore a interfaccia [**facoltativo, ID3DXInclude,**](id3dxinclude.md)da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="91371-120">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="91371-121">Se questo valore è **NULL,** le include verranno rispettate durante la compilazione da un file o causeranno un errore durante la compilazione \# da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="91371-121">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="91371-122">*pFunctionName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="91371-122">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91371-123">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91371-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91371-124">Puntatore a una stringa contenente il nome della funzione del punto di ingresso dello shader in cui ha inizio l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="91371-124">Pointer to a string that contains the name of the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="91371-125">*pProfile* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="91371-125">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91371-126">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91371-126">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91371-127">Puntatore a un profilo shader che determina il set di istruzioni shader.</span><span class="sxs-lookup"><span data-stu-id="91371-127">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="91371-128">Per un elenco dei profili disponibili, vedere [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile.**](d3dxgetpixelshaderprofile.md)</span><span class="sxs-lookup"><span data-stu-id="91371-128">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="91371-129">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="91371-129">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91371-130">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="91371-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="91371-131">Opzioni di compilazione identificate da vari flag.</span><span class="sxs-lookup"><span data-stu-id="91371-131">Compile options identified by various flags.</span></span> <span data-ttu-id="91371-132">Il compilatore HLSL Direct3D 10 è ora l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="91371-132">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="91371-133">Per [informazioni dettagliate, vedere Flag D3DXSHADER.](d3dxshader-flags.md)</span><span class="sxs-lookup"><span data-stu-id="91371-133">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="91371-134">*ppShader* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="91371-134">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91371-135">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="91371-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="91371-136">Restituisce un buffer contenente lo shader creato.</span><span class="sxs-lookup"><span data-stu-id="91371-136">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="91371-137">Questo buffer contiene il codice shader compilato, nonché le informazioni sulle tabelle di debug e simboli incorporate.</span><span class="sxs-lookup"><span data-stu-id="91371-137">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="91371-138">*ppErrorMsgs* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="91371-138">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91371-139">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="91371-139">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="91371-140">Restituisce un buffer contenente un elenco di errori e avvisi rilevati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="91371-140">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="91371-141">Si tratta degli stessi messaggi visualizzati dal debugger durante l'esecuzione in modalità di debug.</span><span class="sxs-lookup"><span data-stu-id="91371-141">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="91371-142">Questo valore può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="91371-142">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="91371-143">*ppConstantTable* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="91371-143">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91371-144">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="91371-144">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="91371-145">Restituisce [**un'interfaccia ID3DXConstantTable,**](id3dxconstanttable.md) che può essere usata per accedere alle costanti shader.</span><span class="sxs-lookup"><span data-stu-id="91371-145">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="91371-146">Questo valore può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="91371-146">This value can be **NULL**.</span></span> <span data-ttu-id="91371-147">Se si compila l'applicazione come a conoscenza di indirizzi di grandi dimensioni, ovvero si usa l'opzione del linker /LARGEADDRESSAWARE per gestire indirizzi di dimensioni superiori a 2 GB, non è possibile usare questo parametro e impostarlo su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="91371-147">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="91371-148">È invece necessario usare la [**funzione D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) per recuperare la tabella costante shader incorporata all'interno dello shader.</span><span class="sxs-lookup"><span data-stu-id="91371-148">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="91371-149">In questa chiamata **D3DXGetShaderConstantTableEx** è necessario passare il flag **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parametro *Flags* per specificare di accedere a un massimo di 4 GB di spazio degli indirizzi virtuali.</span><span class="sxs-lookup"><span data-stu-id="91371-149">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91371-150">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91371-150">Return value</span></span>

<span data-ttu-id="91371-151">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="91371-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="91371-152">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="91371-152">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="91371-153">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="91371-153">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="91371-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91371-154">Requirements</span></span>



| <span data-ttu-id="91371-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="91371-155">Requirement</span></span> | <span data-ttu-id="91371-156">Valore</span><span class="sxs-lookup"><span data-stu-id="91371-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="91371-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91371-157">Header</span></span><br/>  | <dl> <span data-ttu-id="91371-158"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="91371-158"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="91371-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="91371-159">Library</span></span><br/> | <dl> <span data-ttu-id="91371-160"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="91371-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="91371-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91371-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91371-162">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="91371-162">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="91371-163">**D3DXCompileShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="91371-163">**D3DXCompileShaderFromFile**</span></span>](d3dxcompileshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="91371-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="91371-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
