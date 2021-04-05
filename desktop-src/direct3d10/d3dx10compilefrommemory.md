---
description: Nota invece di usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore dalla riga di comando o l'API D3DCompile. Compilare uno shader o un effetto caricato in memoria.
ms.assetid: c6458d82-a649-402c-8180-5b7320f9fdb0
title: Funzione D3DX10CompileFromMemory (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: fbb4a716df4a893ea122e7badfd6faad536aacce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969477"
---
# <a name="d3dx10compilefrommemory-function"></a><span data-ttu-id="7ee3e-104">D3DX10CompileFromMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="7ee3e-104">D3DX10CompileFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="7ee3e-105">Invece di usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore da riga di comando o l'API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="7ee3e-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="7ee3e-106">Compilare uno shader o un effetto caricato in memoria.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-106">Compile a shader or an effect that is loaded in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ee3e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ee3e-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="7ee3e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ee3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ee3e-109">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ee3e-109">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ee3e-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ee3e-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ee3e-111">Puntatore allo shader in memoria.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-111">Pointer to the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="7ee3e-112">*SrcDataLen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ee3e-112">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ee3e-113">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ee3e-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ee3e-114">Dimensioni dello shader in memoria.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-114">Size of the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="7ee3e-115">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ee3e-115">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ee3e-116">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ee3e-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ee3e-117">Nome del file che contiene il codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-117">The name of the file that contains the shader code.</span></span>

</dd> <dt>

<span data-ttu-id="7ee3e-118">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ee3e-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ee3e-119">Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="7ee3e-119">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="7ee3e-120">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-120">Optional.</span></span> <span data-ttu-id="7ee3e-121">Puntatore a una matrice di definizioni di macro (vedere la [**\_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="7ee3e-121">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="7ee3e-122">L'ultima struttura della matrice funge da carattere di terminazione e deve avere tutti i membri impostati su 0.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-122">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="7ee3e-123">Se non viene usato, impostare *pDefines* su **null**.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-123">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7ee3e-124">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ee3e-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ee3e-125">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="7ee3e-125">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="7ee3e-126">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-126">Optional.</span></span> <span data-ttu-id="7ee3e-127">Puntatore a un'interfaccia di [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) per la gestione dei file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-127">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="7ee3e-128">Se si imposta su **null** , verrà generato un errore di compilazione se uno shader contiene un' \# inclusione.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-128">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="7ee3e-129">*pFunctionName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ee3e-129">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ee3e-130">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ee3e-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ee3e-131">Nome della funzione del punto di ingresso dello shader in cui inizia l'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-131">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="7ee3e-132">Quando si compila un effetto, **D3DX10CompileFromMemory** ignora *pFunctionName*; si consiglia di impostare *pFunctionName* su **null** perché è consigliabile impostare un parametro puntatore su **null** se la funzione chiamata non lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-132">When you compile an effect, **D3DX10CompileFromMemory** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="7ee3e-133">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ee3e-133">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ee3e-134">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ee3e-134">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ee3e-135">Stringa che specifica il modello di shader; può essere qualsiasi profilo in [Shader Model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)o [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="7ee3e-135">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ee3e-136">*Flags1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ee3e-136">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ee3e-137">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ee3e-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ee3e-138">[Flag di compilazione shader](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="7ee3e-138">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="7ee3e-139">*Flags2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ee3e-139">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ee3e-140">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ee3e-140">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ee3e-141">[Flag di compilazione effetto](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7ee3e-141">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="7ee3e-142">Quando si compila uno shader e non un file di effetto, **D3DX10CompileFromMemory** ignora *Flags2*; si consiglia di impostare *Flags2* su zero, perché è consigliabile impostare un parametro non di puntatore su zero se la funzione chiamata non lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-142">When you compile a shader and not an effect file, **D3DX10CompileFromMemory** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="7ee3e-143">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ee3e-143">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ee3e-144">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="7ee3e-144">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="7ee3e-145">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="7ee3e-145">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="7ee3e-146">Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-146">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="7ee3e-147">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7ee3e-147">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ee3e-148">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="7ee3e-148">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="7ee3e-149">Puntatore a un' [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) che contiene lo shader compilato, nonché tutte le informazioni di debug e tabella di simboli incorporate.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-149">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="7ee3e-150">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7ee3e-150">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ee3e-151">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="7ee3e-151">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="7ee3e-152">Puntatore a un' [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) contenente un elenco di errori e avvisi che si sono verificati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-152">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="7ee3e-153">Questi errori e avvisi sono identici a quelli dell'output di debug di un debugger.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-153">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="7ee3e-154">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7ee3e-154">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ee3e-155">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="7ee3e-155">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="7ee3e-156">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-156">A pointer to the return value.</span></span> <span data-ttu-id="7ee3e-157">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-157">May be **NULL**.</span></span> <span data-ttu-id="7ee3e-158">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="7ee3e-158">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ee3e-159">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ee3e-159">Return value</span></span>

<span data-ttu-id="7ee3e-160">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ee3e-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ee3e-161">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7ee3e-161">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ee3e-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ee3e-162">Requirements</span></span>



| <span data-ttu-id="7ee3e-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ee3e-163">Requirement</span></span> | <span data-ttu-id="7ee3e-164">Valore</span><span class="sxs-lookup"><span data-stu-id="7ee3e-164">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ee3e-165">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ee3e-165">Header</span></span><br/> | <dl> <span data-ttu-id="7ee3e-166"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ee3e-166"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ee3e-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ee3e-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ee3e-168">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="7ee3e-168">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
