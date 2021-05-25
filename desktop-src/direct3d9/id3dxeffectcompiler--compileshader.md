---
description: Compila uno shader da un effetto che contiene una o più funzioni.
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: Metodo ID3DXEffectCompiler::CompileShader (D3DX9Effect.h)
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
ms.openlocfilehash: 3e8d1d72fccd5c4ad47d21d05ee46013860a7743
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343626"
---
# <a name="id3dxeffectcompilercompileshader-method"></a><span data-ttu-id="32c88-103">Metodo ID3DXEffectCompiler::CompileShader</span><span class="sxs-lookup"><span data-stu-id="32c88-103">ID3DXEffectCompiler::CompileShader method</span></span>

<span data-ttu-id="32c88-104">Compila uno shader da un effetto che contiene una o più funzioni.</span><span class="sxs-lookup"><span data-stu-id="32c88-104">Compiles a shader from an effect that contains one or more functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="32c88-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32c88-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="32c88-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="32c88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32c88-107">*hFunction* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="32c88-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32c88-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="32c88-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="32c88-109">Identificatore univoco della funzione da compilare.</span><span class="sxs-lookup"><span data-stu-id="32c88-109">Unique identifier to the function to be compiled.</span></span> <span data-ttu-id="32c88-110">Questo valore non deve essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="32c88-110">This value must not be **NULL**.</span></span> <span data-ttu-id="32c88-111">Vedere [Handle (Direct3D 9).](handles.md)</span><span class="sxs-lookup"><span data-stu-id="32c88-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="32c88-112">*pTarget* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="32c88-112">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32c88-113">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32c88-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="32c88-114">Puntatore a un profilo shader che determina il set di istruzioni dello shader.</span><span class="sxs-lookup"><span data-stu-id="32c88-114">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="32c88-115">Per un elenco dei profili disponibili, vedere [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) o [**D3DXGetPixelShaderProfile.**](d3dxgetpixelshaderprofile.md)</span><span class="sxs-lookup"><span data-stu-id="32c88-115">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="32c88-116">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="32c88-116">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32c88-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32c88-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="32c88-118">Opzioni di compilazione identificate da vari flag.</span><span class="sxs-lookup"><span data-stu-id="32c88-118">Compile options identified by various flags.</span></span> <span data-ttu-id="32c88-119">Il compilatore HLSL Direct3D 10 è ora l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="32c88-119">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="32c88-120">Per [informazioni dettagliate, vedere Flag D3DXSHADER.](d3dxshader-flags.md)</span><span class="sxs-lookup"><span data-stu-id="32c88-120">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="32c88-121">*ppShader* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="32c88-121">*ppShader* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="32c88-122">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="32c88-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="32c88-123">Buffer contenente lo shader compilato.</span><span class="sxs-lookup"><span data-stu-id="32c88-123">Buffer containing the compiled shader.</span></span> <span data-ttu-id="32c88-124">Lo shader del compilatore è una matrice di DWORD.</span><span class="sxs-lookup"><span data-stu-id="32c88-124">The compiler shader is an array of DWORDs.</span></span> <span data-ttu-id="32c88-125">Per altre informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="32c88-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="32c88-126">*ppErrorMsgs* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="32c88-126">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="32c88-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="32c88-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="32c88-128">Buffer contenente almeno il primo messaggio di errore di compilazione che si è verificato.</span><span class="sxs-lookup"><span data-stu-id="32c88-128">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="32c88-129">Sono inclusi gli errori del compilatore degli effetti e gli errori di compilazione del linguaggio di alto livello.</span><span class="sxs-lookup"><span data-stu-id="32c88-129">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="32c88-130">Per altre informazioni sull'accesso al buffer, vedere [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="32c88-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="32c88-131">*ppConstantTable* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="32c88-131">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="32c88-132">Tipo: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="32c88-132">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="32c88-133">Restituisce [**un'interfaccia ID3DXConstantTable,**](id3dxconstanttable.md) che può essere usata per accedere alle costanti shader.</span><span class="sxs-lookup"><span data-stu-id="32c88-133">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="32c88-134">Questo valore può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="32c88-134">This value can be **NULL**.</span></span> <span data-ttu-id="32c88-135">Se si compila l'applicazione come con supporto per gli indirizzi di grandi dimensioni, ovvero si usa l'opzione del linker /LARGEADDRESSAWARE per gestire indirizzi di dimensioni superiori a 2 GB, non è possibile usare questo parametro e impostarlo su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="32c88-135">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="32c88-136">È invece necessario usare la [**funzione D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) per recuperare la tabella costante dello shader incorporata all'interno dello shader.</span><span class="sxs-lookup"><span data-stu-id="32c88-136">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="32c88-137">In questa chiamata **D3DXGetShaderConstantTableEx** è necessario passare il flag **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** al parametro *Flags* per specificare di accedere a un massimo di 4 GB di spazio degli indirizzi virtuali.</span><span class="sxs-lookup"><span data-stu-id="32c88-137">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32c88-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32c88-138">Return value</span></span>

<span data-ttu-id="32c88-139">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="32c88-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="32c88-140">Se il metodo ha esito positivo, il valore restituito è S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="32c88-140">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="32c88-141">Se gli argomenti non sono validi, il metodo restituirà D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="32c88-141">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="32c88-142">Se il metodo ha esito negativo, il valore restituito sarà E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="32c88-142">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="32c88-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="32c88-143">Remarks</span></span>

<span data-ttu-id="32c88-144">Le destinazioni possono essere specificate per vertex shader, pixel shader e funzioni di riempimento della trama.</span><span class="sxs-lookup"><span data-stu-id="32c88-144">Targets can be specified for vertex shaders, pixel shaders, and texture fill functions.</span></span>



| <span data-ttu-id="32c88-145">Targets</span><span class="sxs-lookup"><span data-stu-id="32c88-145">Targets</span></span>                      | <span data-ttu-id="32c88-146">Funzioni</span><span class="sxs-lookup"><span data-stu-id="32c88-146">Functions</span></span>                                                                      |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="32c88-147">Destinazioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="32c88-147">Vertex shader targets</span></span> | <span data-ttu-id="32c88-148">vs \_ 1 \_ 1, vs \_ 2 \_ 0, vs \_ 2 \_ sw, vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="32c88-148">vs\_1\_1, vs\_2\_0, vs\_2\_sw, vs\_3\_0</span></span>                               |
| <span data-ttu-id="32c88-149">Destinazioni pixel shader</span><span class="sxs-lookup"><span data-stu-id="32c88-149">Pixel shader targets</span></span>  | <span data-ttu-id="32c88-150">ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4, ps \_ 2 \_ 0, ps \_ 2 \_ sw, ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="32c88-150">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4, ps\_2\_0, ps\_2\_sw, ps\_3\_0</span></span> |
| <span data-ttu-id="32c88-151">Destinazioni di riempimento della trama</span><span class="sxs-lookup"><span data-stu-id="32c88-151">Texture fill targets</span></span>  | <span data-ttu-id="32c88-152">tx \_ 0, tx \_ 1</span><span class="sxs-lookup"><span data-stu-id="32c88-152">tx\_0, tx\_1</span></span>                                                          |



 

<span data-ttu-id="32c88-153">Questo metodo compila uno shader da una funzione scritta in un linguaggio simile a C.</span><span class="sxs-lookup"><span data-stu-id="32c88-153">This method compiles a shader from a function that is written in a C-like language.</span></span> <span data-ttu-id="32c88-154">Per altre informazioni, vedere [HLSL.](../direct3dhlsl/dx-graphics-hlsl.md)</span><span class="sxs-lookup"><span data-stu-id="32c88-154">For more information, see [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32c88-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32c88-155">Requirements</span></span>



| <span data-ttu-id="32c88-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="32c88-156">Requirement</span></span> | <span data-ttu-id="32c88-157">Valore</span><span class="sxs-lookup"><span data-stu-id="32c88-157">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="32c88-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32c88-158">Header</span></span><br/>  | <dl> <span data-ttu-id="32c88-159"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="32c88-159"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="32c88-160">Libreria</span><span class="sxs-lookup"><span data-stu-id="32c88-160">Library</span></span><br/> | <dl> <span data-ttu-id="32c88-161"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="32c88-161"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="32c88-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32c88-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32c88-163">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="32c88-163">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="32c88-164">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="32c88-164">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
