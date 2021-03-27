---
title: Funzione D3DX11CompileFromMemory (D3DX11async. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di usare questa funzione, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore dalla riga di comando o una delle API di compilazione HLSL, ad esempio l'API D3DCompile. Compilare uno shader o un effetto caricato in memoria.
ms.assetid: 3396560f-f411-4c66-9f22-03c0050c74b0
keywords:
- Funzione D3DX11CompileFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e10590c3db458a23bf4d52b6507146884630087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982358"
---
# <a name="d3dx11compilefrommemory-function"></a><span data-ttu-id="34ada-106">D3DX11CompileFromMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="34ada-106">D3DX11CompileFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="34ada-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="34ada-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="34ada-108">Invece di usare questa funzione, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore da riga di comando o una delle API di compilazione HLSL, ad esempio l'API [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="34ada-108">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API.</span></span>

 

<span data-ttu-id="34ada-109">Compilare uno shader o un effetto caricato in memoria.</span><span class="sxs-lookup"><span data-stu-id="34ada-109">Compile a shader or an effect that is loaded in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="34ada-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34ada-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataLen,
  _In_        LPCSTR             pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        LPCSTR             pFunctionName,
  _In_        LPCSTR             pProfile,
  _In_        UINT               Flags1,
  _In_        UINT               Flags2,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShader,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="34ada-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="34ada-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34ada-112">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34ada-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34ada-113">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="34ada-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="34ada-114">Puntatore allo shader in memoria.</span><span class="sxs-lookup"><span data-stu-id="34ada-114">Pointer to the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="34ada-115">*SrcDataLen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34ada-115">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34ada-116">Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="34ada-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="34ada-117">Dimensioni dello shader in memoria.</span><span class="sxs-lookup"><span data-stu-id="34ada-117">Size of the shader in memory.</span></span>

</dd> <dt>

<span data-ttu-id="34ada-118">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34ada-118">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34ada-119">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="34ada-119">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="34ada-120">Nome del file che contiene il codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="34ada-120">The name of the file that contains the shader code.</span></span>

</dd> <dt>

<span data-ttu-id="34ada-121">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34ada-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34ada-122">Tipo: **const [**D3D10 \_ shader \_ macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="34ada-122">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="34ada-123">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="34ada-123">Optional.</span></span> <span data-ttu-id="34ada-124">Puntatore a una matrice di definizioni di macro (vedere [**D3D10 \_ shader \_ macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="34ada-124">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="34ada-125">L'ultima struttura della matrice funge da carattere di terminazione e deve avere tutti i membri impostati su 0.</span><span class="sxs-lookup"><span data-stu-id="34ada-125">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="34ada-126">Se non viene usato, impostare *pDefines* su **null**.</span><span class="sxs-lookup"><span data-stu-id="34ada-126">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="34ada-127">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34ada-127">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34ada-128">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="34ada-128">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="34ada-129">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="34ada-129">Optional.</span></span> <span data-ttu-id="34ada-130">Puntatore a un'interfaccia per la gestione dei file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="34ada-130">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="34ada-131">Se si imposta su **null** , verrà generato un errore di compilazione se uno shader contiene un' \# inclusione.</span><span class="sxs-lookup"><span data-stu-id="34ada-131">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="34ada-132">*pFunctionName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34ada-132">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34ada-133">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="34ada-133">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="34ada-134">Nome della funzione del punto di ingresso dello shader in cui inizia l'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="34ada-134">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="34ada-135">Quando si compila un effetto, **D3DX11CompileFromMemory** ignora *pFunctionName*; si consiglia di impostare *pFunctionName* su **null** perché è consigliabile impostare un parametro puntatore su **null** se la funzione chiamata non lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="34ada-135">When you compile an effect, **D3DX11CompileFromMemory** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="34ada-136">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34ada-136">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34ada-137">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="34ada-137">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="34ada-138">Stringa che specifica il modello di shader; può essere qualsiasi profilo in Shader Model 2, Shader Model 3, Shader Model 4 o Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="34ada-138">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="34ada-139">Il profilo può essere anche per il tipo di effetto (ad esempio, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="34ada-139">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="34ada-140">*Flags1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34ada-140">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34ada-141">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="34ada-141">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="34ada-142">Flag di [**compilazione**](/windows/desktop/direct3dhlsl/d3dcompile-constants)shader.</span><span class="sxs-lookup"><span data-stu-id="34ada-142">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="34ada-143">*Flags2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34ada-143">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34ada-144">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="34ada-144">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="34ada-145">[**Flag di compilazione**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)effetto.</span><span class="sxs-lookup"><span data-stu-id="34ada-145">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="34ada-146">Quando si compila uno shader e non un file di effetto, **D3DX11CompileFromMemory** ignora *Flags2*; si consiglia di impostare *Flags2* su zero, perché è consigliabile impostare un parametro non di puntatore su zero se la funzione chiamata non lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="34ada-146">When you compile a shader and not an effect file, **D3DX11CompileFromMemory** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="34ada-147">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="34ada-147">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34ada-148">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="34ada-148">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="34ada-149">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="34ada-149">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="34ada-150">Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="34ada-150">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="34ada-151">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="34ada-151">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34ada-152">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="34ada-152">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="34ada-153">Puntatore alla memoria che contiene lo shader compilato, nonché tutte le informazioni di debug e tabella di simboli incorporate.</span><span class="sxs-lookup"><span data-stu-id="34ada-153">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="34ada-154">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="34ada-154">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34ada-155">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="34ada-155">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="34ada-156">Puntatore alla memoria contenente un elenco di errori e avvisi che si sono verificati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="34ada-156">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="34ada-157">Questi errori e avvisi sono identici a quelli dell'output di debug di un debugger.</span><span class="sxs-lookup"><span data-stu-id="34ada-157">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="34ada-158">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="34ada-158">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34ada-159">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="34ada-159">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="34ada-160">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="34ada-160">A pointer to the return value.</span></span> <span data-ttu-id="34ada-161">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="34ada-161">May be **NULL**.</span></span> <span data-ttu-id="34ada-162">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="34ada-162">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34ada-163">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34ada-163">Return value</span></span>

<span data-ttu-id="34ada-164">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="34ada-164">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="34ada-165">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="34ada-165">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="34ada-166">**D3DX11CompileFromMemory** restituisce E \_ INVALIDARG se si fornisce un valore diverso da **null** al parametro *pHResult* quando si fornisce **null** al parametro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="34ada-166">**D3DX11CompileFromMemory** returns E\_INVALIDARG if you supply non-**NULL** to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="34ada-167">Per ulteriori informazioni su questa situazione, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="34ada-167">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="34ada-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="34ada-168">Remarks</span></span>

<span data-ttu-id="34ada-169">Per ulteriori informazioni su **D3DX11CompileFromMemory**, vedere [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="34ada-169">For more information about **D3DX11CompileFromMemory**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="34ada-170">È necessario fornire **null** al parametro *pHResult* se si fornisce anche **null** al parametro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="34ada-170">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="34ada-171">In caso contrario, non sarà possibile creare uno shader usando il codice dello shader compilato restituito da **D3DX11CompileFromMemory** nella memoria a cui punta il parametro *ppShader* .</span><span class="sxs-lookup"><span data-stu-id="34ada-171">Otherwise, you cannot subsequently create a shader by using the compiled shader code that **D3DX11CompileFromMemory** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="34ada-172">Per creare uno shader dal codice dello shader rispettato, chiamare uno dei seguenti metodi di interfaccia [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) :</span><span class="sxs-lookup"><span data-stu-id="34ada-172">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="34ada-173">**CreateComputeShader**</span><span class="sxs-lookup"><span data-stu-id="34ada-173">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="34ada-174">**CreateDomainShader**</span><span class="sxs-lookup"><span data-stu-id="34ada-174">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="34ada-175">**CreateGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="34ada-175">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="34ada-176">**CreateGeometryShaderWithStreamOutput**</span><span class="sxs-lookup"><span data-stu-id="34ada-176">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="34ada-177">**CreateHullShader**</span><span class="sxs-lookup"><span data-stu-id="34ada-177">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="34ada-178">**CreatePixelShader**</span><span class="sxs-lookup"><span data-stu-id="34ada-178">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="34ada-179">**CreateVertexShader**</span><span class="sxs-lookup"><span data-stu-id="34ada-179">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="34ada-180">Inoltre, se si fornisce un valore non **null** a *pHResult* quando si fornisce **null** a *pPump*, **D3DX11CompileFromMemory** restituisce il codice di \_ errore E INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="34ada-180">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromMemory** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="34ada-181">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34ada-181">Requirements</span></span>



| <span data-ttu-id="34ada-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="34ada-182">Requirement</span></span> | <span data-ttu-id="34ada-183">Valore</span><span class="sxs-lookup"><span data-stu-id="34ada-183">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="34ada-184">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34ada-184">Header</span></span><br/>  | <dl> <span data-ttu-id="34ada-185"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="34ada-185"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="34ada-186">Libreria</span><span class="sxs-lookup"><span data-stu-id="34ada-186">Library</span></span><br/> | <dl> <span data-ttu-id="34ada-187"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="34ada-187"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="34ada-188">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34ada-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34ada-189">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="34ada-189">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

