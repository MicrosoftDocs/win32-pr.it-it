---
description: Compila uno shader da un effetto che contiene una o più funzioni.
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: 'Metodo ID3DXEffectCompiler:: CompileShader (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 375646202e102623053c179398329ad2286e6c1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323081"
---
# <a name="id3dxeffectcompilercompileshader-method"></a><span data-ttu-id="e4811-103">Metodo ID3DXEffectCompiler:: CompileShader</span><span class="sxs-lookup"><span data-stu-id="e4811-103">ID3DXEffectCompiler::CompileShader method</span></span>

<span data-ttu-id="e4811-104">Compila uno shader da un effetto che contiene una o più funzioni.</span><span class="sxs-lookup"><span data-stu-id="e4811-104">Compiles a shader from an effect that contains one or more functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4811-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4811-105">Syntax</span></span>


```C++
HRESULT CompileShader(
  [in]          D3DXHANDLE          hFunction,
  [in]          LPCSTR              pTarget,
  [in]          DWORD               Flags,
  [out, retval] LPD3DXBUFFER        *ppShader,
  [out, retval] LPD3DXBUFFER        *ppErrorMsgs,
  [out]         LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="e4811-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4811-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4811-107">*hFunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4811-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4811-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e4811-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e4811-109">Identificatore univoco della funzione da compilare.</span><span class="sxs-lookup"><span data-stu-id="e4811-109">Unique identifier to the function to be compiled.</span></span> <span data-ttu-id="e4811-110">Questo valore non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="e4811-110">This value must not be **NULL**.</span></span> <span data-ttu-id="e4811-111">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="e4811-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4811-112">*PTarget* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4811-112">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4811-113">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4811-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4811-114">Puntatore a un profilo dello shader che determina il set di istruzioni dello shader.</span><span class="sxs-lookup"><span data-stu-id="e4811-114">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="e4811-115">Per un elenco dei profili disponibili, vedere [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="e4811-115">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="e4811-116">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4811-116">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4811-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4811-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4811-118">Opzioni di compilazione identificate da diversi flag.</span><span class="sxs-lookup"><span data-stu-id="e4811-118">Compile options identified by various flags.</span></span> <span data-ttu-id="e4811-119">Il compilatore Direct3D 10 HLSL è ora il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="e4811-119">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="e4811-120">Per informazioni dettagliate, vedere [flag D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="e4811-120">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="e4811-121">*ppShader* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e4811-121">*ppShader* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e4811-122">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4811-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e4811-123">Buffer contenente lo shader compilato.</span><span class="sxs-lookup"><span data-stu-id="e4811-123">Buffer containing the compiled shader.</span></span> <span data-ttu-id="e4811-124">Lo shader del compilatore è una matrice di DWORD.</span><span class="sxs-lookup"><span data-stu-id="e4811-124">The compiler shader is an array of DWORDs.</span></span> <span data-ttu-id="e4811-125">Per ulteriori informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="e4811-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4811-126">*ppErrorMsgs* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e4811-126">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e4811-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4811-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e4811-128">Buffer contenente almeno il primo messaggio di errore di compilazione che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="e4811-128">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="e4811-129">Sono inclusi gli errori del compilatore degli effetti e gli errori di compilazione del linguaggio di alto livello.</span><span class="sxs-lookup"><span data-stu-id="e4811-129">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="e4811-130">Per ulteriori informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="e4811-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="e4811-131">*ppConstantTable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e4811-131">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4811-132">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4811-132">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="e4811-133">Restituisce un'interfaccia [**ID3DXConstantTable**](id3dxconstanttable.md) che può essere utilizzata per accedere alle costanti dello shader.</span><span class="sxs-lookup"><span data-stu-id="e4811-133">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="e4811-134">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="e4811-134">This value can be **NULL**.</span></span> <span data-ttu-id="e4811-135">Se l'applicazione viene compilata con un indirizzo di grandi dimensioni (ovvero si usa l'opzione del linker/LARGEADDRESSAWARE per gestire gli indirizzi maggiori di 2 GB), non è possibile usare questo parametro e deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="e4811-135">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="e4811-136">È invece necessario utilizzare la funzione [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) per recuperare la tabella delle costanti shader incorporata all'interno dello shader.</span><span class="sxs-lookup"><span data-stu-id="e4811-136">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="e4811-137">In questa chiamata **D3DXGetShaderConstantTableEx** è necessario passare il flag **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parametro *Flags* per specificare di accedere a un massimo di 4 GB di spazio degli indirizzi virtuali.</span><span class="sxs-lookup"><span data-stu-id="e4811-137">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4811-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4811-138">Return value</span></span>

<span data-ttu-id="e4811-139">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e4811-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e4811-140">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e4811-140">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="e4811-141">Se gli argomenti non sono validi, il metodo restituirà D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e4811-141">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="e4811-142">Se il metodo ha esito negativo, il valore restituito sarà E avrà \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="e4811-142">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4811-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4811-143">Remarks</span></span>

<span data-ttu-id="e4811-144">È possibile specificare le destinazioni per i vertex shader, i pixel shader e le funzioni di riempimento della trama.</span><span class="sxs-lookup"><span data-stu-id="e4811-144">Targets can be specified for vertex shaders, pixel shaders, and texture fill functions.</span></span>



|                       |                                                                       |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="e4811-145">Destinazioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="e4811-145">Vertex shader targets</span></span> | <span data-ttu-id="e4811-146">vs \_ 1 \_ , vs \_ 2 \_ 0, vs \_ 2 \_ SW, vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e4811-146">vs\_1\_1, vs\_2\_0, vs\_2\_sw, vs\_3\_0</span></span>                               |
| <span data-ttu-id="e4811-147">Destinazioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="e4811-147">Pixel shader targets</span></span>  | <span data-ttu-id="e4811-148">PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4, PS \_ 2 \_ 0, PS \_ 2 \_ SW, PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e4811-148">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4, ps\_2\_0, ps\_2\_sw, ps\_3\_0</span></span> |
| <span data-ttu-id="e4811-149">Destinazioni riempimento trama</span><span class="sxs-lookup"><span data-stu-id="e4811-149">Texture fill targets</span></span>  | <span data-ttu-id="e4811-150">TX \_ 0, TX \_ 1</span><span class="sxs-lookup"><span data-stu-id="e4811-150">tx\_0, tx\_1</span></span>                                                          |



 

<span data-ttu-id="e4811-151">Questo metodo compila uno shader da una funzione scritta in un linguaggio simile a C.</span><span class="sxs-lookup"><span data-stu-id="e4811-151">This method compiles a shader from a function that is written in a C-like language.</span></span> <span data-ttu-id="e4811-152">Per ulteriori informazioni, vedere [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="e4811-152">For more information, see [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4811-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4811-153">Requirements</span></span>



| <span data-ttu-id="e4811-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4811-154">Requirement</span></span> | <span data-ttu-id="e4811-155">Valore</span><span class="sxs-lookup"><span data-stu-id="e4811-155">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4811-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4811-156">Header</span></span><br/>  | <dl> <span data-ttu-id="e4811-157"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4811-157"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e4811-158">Libreria</span><span class="sxs-lookup"><span data-stu-id="e4811-158">Library</span></span><br/> | <dl> <span data-ttu-id="e4811-159"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4811-159"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e4811-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4811-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4811-161">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="e4811-161">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="e4811-162">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="e4811-162">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
