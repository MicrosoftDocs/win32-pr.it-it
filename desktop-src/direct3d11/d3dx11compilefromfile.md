---
title: Funzione D3DX11CompileFromFile (D3DX11async. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di usare questa funzione, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore dalla riga di comando o una delle API di compilazione HLSL, ad esempio l'API D3DCompileFromFile. Compilare uno shader o un effetto da un file.
ms.assetid: 91a1a339-50da-4f86-9b55-6af246a60482
keywords:
- Funzione D3DX11CompileFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c9194eb54652304c220e5a4de0ee12a26ea1a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132374"
---
# <a name="d3dx11compilefromfile-function"></a><span data-ttu-id="74182-106">D3DX11CompileFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="74182-106">D3DX11CompileFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="74182-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="74182-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="74182-108">Invece di usare questa funzione, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore da riga di comando o una delle API di compilazione HLSL, ad esempio l'API [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) .</span><span class="sxs-lookup"><span data-stu-id="74182-108">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) API.</span></span>

 

<span data-ttu-id="74182-109">Compilare uno shader o un effetto da un file.</span><span class="sxs-lookup"><span data-stu-id="74182-109">Compile a shader or an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="74182-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74182-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="74182-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="74182-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74182-112">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74182-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74182-113">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="74182-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="74182-114">Nome del file che contiene il codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="74182-114">The name of the file that contains the shader code.</span></span> <span data-ttu-id="74182-115">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="74182-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="74182-116">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="74182-116">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="74182-117">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74182-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74182-118">Tipo: **const [**D3D10 \_ shader \_ macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="74182-118">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="74182-119">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="74182-119">Optional.</span></span> <span data-ttu-id="74182-120">Puntatore a una matrice di definizioni di macro (vedere [**D3D10 \_ shader \_ macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="74182-120">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="74182-121">L'ultima struttura della matrice funge da carattere di terminazione e deve avere tutti i membri impostati su 0.</span><span class="sxs-lookup"><span data-stu-id="74182-121">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="74182-122">Se non viene usato, impostare *pDefines* su **null**.</span><span class="sxs-lookup"><span data-stu-id="74182-122">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="74182-123">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74182-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74182-124">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="74182-124">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="74182-125">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="74182-125">Optional.</span></span> <span data-ttu-id="74182-126">Puntatore a un'interfaccia per la gestione dei file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="74182-126">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="74182-127">Se si imposta su **null** , verrà generato un errore di compilazione se uno shader contiene un' \# inclusione.</span><span class="sxs-lookup"><span data-stu-id="74182-127">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="74182-128">*pFunctionName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74182-128">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74182-129">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="74182-129">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="74182-130">Nome della funzione del punto di ingresso dello shader in cui inizia l'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="74182-130">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="74182-131">Quando si compila un effetto, **D3DX11CompileFromFile** ignora *pFunctionName*; si consiglia di impostare *pFunctionName* su **null** perché è consigliabile impostare un parametro puntatore su **null** se la funzione chiamata non lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="74182-131">When you compile an effect, **D3DX11CompileFromFile** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="74182-132">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74182-132">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74182-133">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="74182-133">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="74182-134">Stringa che specifica il modello di shader; può essere qualsiasi profilo in Shader Model 2, Shader Model 3, Shader Model 4 o Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="74182-134">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="74182-135">Il profilo può essere anche per il tipo di effetto (ad esempio, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="74182-135">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="74182-136">*Flags1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74182-136">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74182-137">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="74182-137">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="74182-138">Flag di [**compilazione**](/windows/desktop/direct3dhlsl/d3dcompile-constants)shader.</span><span class="sxs-lookup"><span data-stu-id="74182-138">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="74182-139">*Flags2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74182-139">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74182-140">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="74182-140">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="74182-141">[**Flag di compilazione**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)effetto.</span><span class="sxs-lookup"><span data-stu-id="74182-141">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="74182-142">Quando si compila uno shader e non un file di effetto, **D3DX11CompileFromFile** ignora *Flags2*; si consiglia di impostare *Flags2* su zero, perché è consigliabile impostare un parametro non di puntatore su zero se la funzione chiamata non lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="74182-142">When you compile a shader and not an effect file, **D3DX11CompileFromFile** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="74182-143">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74182-143">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74182-144">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="74182-144">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="74182-145">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="74182-145">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="74182-146">Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="74182-146">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="74182-147">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="74182-147">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74182-148">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="74182-148">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="74182-149">Puntatore alla memoria che contiene lo shader compilato, nonché tutte le informazioni di debug e tabella di simboli incorporate.</span><span class="sxs-lookup"><span data-stu-id="74182-149">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="74182-150">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="74182-150">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74182-151">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="74182-151">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="74182-152">Puntatore alla memoria contenente un elenco di errori e avvisi che si sono verificati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="74182-152">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="74182-153">Questi errori e avvisi sono identici a quelli dell'output di debug di un debugger.</span><span class="sxs-lookup"><span data-stu-id="74182-153">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="74182-154">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="74182-154">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74182-155">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="74182-155">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="74182-156">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="74182-156">A pointer to the return value.</span></span> <span data-ttu-id="74182-157">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="74182-157">May be **NULL**.</span></span> <span data-ttu-id="74182-158">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="74182-158">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74182-159">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74182-159">Return value</span></span>

<span data-ttu-id="74182-160">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74182-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74182-161">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="74182-161">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="74182-162">**D3DX11CompileFromFile** restituisce E \_ INVALIDARG se si fornisce un valore non **null** al parametro *pHResult* quando si fornisce **null** al parametro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="74182-162">**D3DX11CompileFromFile** returns E\_INVALIDARG if you supply a non-**NULL** value to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="74182-163">Per ulteriori informazioni su questa situazione, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="74182-163">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="74182-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="74182-164">Remarks</span></span>

<span data-ttu-id="74182-165">Per ulteriori informazioni su **D3DX11CompileFromFile**, vedere [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="74182-165">For more information about **D3DX11CompileFromFile**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="74182-166">È necessario fornire **null** al parametro *pHResult* se si fornisce anche **null** al parametro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="74182-166">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="74182-167">In caso contrario, non è possibile creare uno shader usando il codice dello shader compilato restituito da **D3DX11CompileFromFile** nella memoria a cui punta il parametro *ppShader* .</span><span class="sxs-lookup"><span data-stu-id="74182-167">Otherwise, you cannot create a shader by using the compiled shader code that **D3DX11CompileFromFile** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="74182-168">Per creare uno shader dal codice dello shader rispettato, chiamare uno dei seguenti metodi di interfaccia [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) :</span><span class="sxs-lookup"><span data-stu-id="74182-168">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="74182-169">**CreateComputeShader**</span><span class="sxs-lookup"><span data-stu-id="74182-169">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="74182-170">**CreateDomainShader**</span><span class="sxs-lookup"><span data-stu-id="74182-170">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="74182-171">**CreateGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="74182-171">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="74182-172">**CreateGeometryShaderWithStreamOutput**</span><span class="sxs-lookup"><span data-stu-id="74182-172">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="74182-173">**CreateHullShader**</span><span class="sxs-lookup"><span data-stu-id="74182-173">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="74182-174">**CreatePixelShader**</span><span class="sxs-lookup"><span data-stu-id="74182-174">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="74182-175">**CreateVertexShader**</span><span class="sxs-lookup"><span data-stu-id="74182-175">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="74182-176">Inoltre, se si fornisce un valore non **null** a *pHResult* quando si fornisce **null** a *pPump*, **D3DX11CompileFromFile** restituisce il codice di \_ errore E INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="74182-176">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromFile** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="74182-177">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74182-177">Requirements</span></span>



| <span data-ttu-id="74182-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="74182-178">Requirement</span></span> | <span data-ttu-id="74182-179">Valore</span><span class="sxs-lookup"><span data-stu-id="74182-179">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="74182-180">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74182-180">Header</span></span><br/>  | <dl> <span data-ttu-id="74182-181"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="74182-181"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="74182-182">Libreria</span><span class="sxs-lookup"><span data-stu-id="74182-182">Library</span></span><br/> | <dl> <span data-ttu-id="74182-183"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74182-183"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="74182-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74182-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74182-185">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="74182-185">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

