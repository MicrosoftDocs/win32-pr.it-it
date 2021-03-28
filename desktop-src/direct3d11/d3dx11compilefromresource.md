---
title: Funzione D3DX11CompileFromResource (D3DX11async. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Nota invece di usare questa funzione, è consigliabile usare le funzioni delle risorse, quindi compilare offline usando il Fxc.exe compilatore della riga di comando o usare una delle API di compilazione HLSL, ad esempio l'API D3DCompile. Compilare uno shader o un effetto da una risorsa.
ms.assetid: ececa469-f5e3-4cb3-befe-0ed1a5a57671
keywords:
- Funzione D3DX11CompileFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CompileFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b26eeb825a1d3b6bcda9f77eae24c99c3cec168b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969438"
---
# <a name="d3dx11compilefromresource-function"></a><span data-ttu-id="a13ba-106">D3DX11CompileFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="a13ba-106">D3DX11CompileFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="a13ba-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a13ba-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="a13ba-108">Invece di usare questa funzione, è consigliabile usare le [funzioni di risorsa](/windows/desktop/menurc/resources-functions), quindi compilare offline usando il Fxc.exe compilatore della riga di comando o usare una delle API di compilazione HLSL, ad esempio l'API [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="a13ba-108">Instead of using this function, we recommend that you use [resource functions](/windows/desktop/menurc/resources-functions), then compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) API.</span></span>

 

<span data-ttu-id="a13ba-109">Compilare uno shader o un effetto da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="a13ba-109">Compile a shader or an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="a13ba-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a13ba-110">Syntax</span></span>


```C++
HRESULT D3DX11CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
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



## <a name="parameters"></a><span data-ttu-id="a13ba-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="a13ba-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a13ba-112">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a13ba-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13ba-113">Tipo: **[ **hmodule**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a13ba-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a13ba-114">Handle per il modulo della risorsa contenente lo shader.</span><span class="sxs-lookup"><span data-stu-id="a13ba-114">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="a13ba-115">HMODULE può essere ottenuto con la [funzione GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="a13ba-115">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="a13ba-116">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a13ba-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13ba-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a13ba-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a13ba-118">Nome della risorsa contenente lo shader.</span><span class="sxs-lookup"><span data-stu-id="a13ba-118">Name of the resource containing the shader.</span></span> <span data-ttu-id="a13ba-119">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="a13ba-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="a13ba-120">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="a13ba-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="a13ba-121">*pSrcFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a13ba-121">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13ba-122">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a13ba-122">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a13ba-123">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a13ba-123">Optional.</span></span> <span data-ttu-id="a13ba-124">Nome del file di effetto, che viene usato solo per i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="a13ba-124">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="a13ba-125">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="a13ba-125">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a13ba-126">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a13ba-126">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13ba-127">Tipo: **const [**D3D10 \_ shader \_ macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="a13ba-127">Type: **const [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="a13ba-128">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a13ba-128">Optional.</span></span> <span data-ttu-id="a13ba-129">Puntatore a una matrice di definizioni di macro (vedere [**D3D10 \_ shader \_ macro**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="a13ba-129">Pointer to an array of macro definitions (see [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="a13ba-130">L'ultima struttura della matrice funge da carattere di terminazione e deve avere tutti i membri impostati su 0.</span><span class="sxs-lookup"><span data-stu-id="a13ba-130">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="a13ba-131">Se non viene usato, impostare *pDefines* su **null**.</span><span class="sxs-lookup"><span data-stu-id="a13ba-131">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a13ba-132">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a13ba-132">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13ba-133">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="a13ba-133">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="a13ba-134">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a13ba-134">Optional.</span></span> <span data-ttu-id="a13ba-135">Puntatore a un'interfaccia per la gestione dei file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="a13ba-135">Pointer to an interface for handling include files.</span></span> <span data-ttu-id="a13ba-136">Se si imposta su **null** , verrà generato un errore di compilazione se uno shader contiene un' \# inclusione.</span><span class="sxs-lookup"><span data-stu-id="a13ba-136">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="a13ba-137">*pFunctionName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a13ba-137">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13ba-138">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a13ba-138">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a13ba-139">Nome della funzione del punto di ingresso dello shader in cui inizia l'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="a13ba-139">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="a13ba-140">Quando si compila un effetto, **D3DX11CompileFromResource** ignora *pFunctionName*; si consiglia di impostare *pFunctionName* su **null** perché è consigliabile impostare un parametro puntatore su **null** se la funzione chiamata non lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="a13ba-140">When you compile an effect, **D3DX11CompileFromResource** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="a13ba-141">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a13ba-141">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13ba-142">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a13ba-142">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a13ba-143">Stringa che specifica il modello di shader; può essere qualsiasi profilo in Shader Model 2, Shader Model 3, Shader Model 4 o Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="a13ba-143">A string that specifies the shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="a13ba-144">Il profilo può essere anche per il tipo di effetto (ad esempio, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="a13ba-144">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="a13ba-145">*Flags1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a13ba-145">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13ba-146">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a13ba-146">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a13ba-147">Flag di [**compilazione**](/windows/desktop/direct3dhlsl/d3dcompile-constants)shader.</span><span class="sxs-lookup"><span data-stu-id="a13ba-147">Shader [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-constants).</span></span>

</dd> <dt>

<span data-ttu-id="a13ba-148">*Flags2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a13ba-148">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13ba-149">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a13ba-149">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a13ba-150">[**Flag di compilazione**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants)effetto.</span><span class="sxs-lookup"><span data-stu-id="a13ba-150">Effect [**compile flags**](/windows/desktop/direct3dhlsl/d3dcompile-effect-constants).</span></span> <span data-ttu-id="a13ba-151">Quando si compila uno shader e non un file di effetto, **D3DX11CompileFromResource** ignora *Flags2*; si consiglia di impostare *Flags2* su zero, perché è consigliabile impostare un parametro non di puntatore su zero se la funzione chiamata non lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="a13ba-151">When you compile a shader and not an effect file, **D3DX11CompileFromResource** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="a13ba-152">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a13ba-152">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a13ba-153">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="a13ba-153">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="a13ba-154">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="a13ba-154">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="a13ba-155">Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="a13ba-155">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="a13ba-156">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a13ba-156">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a13ba-157">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="a13ba-157">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="a13ba-158">Puntatore alla memoria che contiene lo shader compilato, nonché tutte le informazioni di debug e tabella di simboli incorporate.</span><span class="sxs-lookup"><span data-stu-id="a13ba-158">A pointer to memory which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="a13ba-159">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a13ba-159">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a13ba-160">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="a13ba-160">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="a13ba-161">Puntatore alla memoria contenente un elenco di errori e avvisi che si sono verificati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="a13ba-161">A pointer to memory which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="a13ba-162">Questi errori e avvisi sono identici a quelli dell'output di debug di un debugger.</span><span class="sxs-lookup"><span data-stu-id="a13ba-162">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="a13ba-163">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a13ba-163">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a13ba-164">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="a13ba-164">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="a13ba-165">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="a13ba-165">A pointer to the return value.</span></span> <span data-ttu-id="a13ba-166">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="a13ba-166">May be **NULL**.</span></span> <span data-ttu-id="a13ba-167">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="a13ba-167">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a13ba-168">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a13ba-168">Return value</span></span>

<span data-ttu-id="a13ba-169">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a13ba-169">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a13ba-170">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a13ba-170">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

<span data-ttu-id="a13ba-171">**D3DX11CompileFromResource** restituisce E \_ INVALIDARG se si fornisce un valore diverso da **null** al parametro *pHResult* quando si fornisce **null** al parametro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="a13ba-171">**D3DX11CompileFromResource** returns E\_INVALIDARG if you supply non-**NULL** to the *pHResult* parameter when you supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="a13ba-172">Per ulteriori informazioni su questa situazione, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a13ba-172">For more information about this situation, see Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="a13ba-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="a13ba-173">Remarks</span></span>

<span data-ttu-id="a13ba-174">Per ulteriori informazioni su **D3DX11CompileFromResource**, vedere [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="a13ba-174">For more information about **D3DX11CompileFromResource**, see [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile).</span></span>

<span data-ttu-id="a13ba-175">È necessario fornire **null** al parametro *pHResult* se si fornisce anche **null** al parametro *pPump* .</span><span class="sxs-lookup"><span data-stu-id="a13ba-175">You must supply **NULL** to the *pHResult* parameter if you also supply **NULL** to the *pPump* parameter.</span></span> <span data-ttu-id="a13ba-176">In caso contrario, non sarà possibile creare uno shader usando il codice dello shader compilato restituito da **D3DX11CompileFromResource** nella memoria a cui punta il parametro *ppShader* .</span><span class="sxs-lookup"><span data-stu-id="a13ba-176">Otherwise, you cannot subsequently create a shader by using the compiled shader code that **D3DX11CompileFromResource** returns in the memory that the *ppShader* parameter points to.</span></span> <span data-ttu-id="a13ba-177">Per creare uno shader dal codice dello shader rispettato, chiamare uno dei seguenti metodi di interfaccia [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) :</span><span class="sxs-lookup"><span data-stu-id="a13ba-177">To create a shader from complied shader code, you call one of the following [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface methods:</span></span>

-   [<span data-ttu-id="a13ba-178">**CreateComputeShader**</span><span class="sxs-lookup"><span data-stu-id="a13ba-178">**CreateComputeShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createcomputeshader)
-   [<span data-ttu-id="a13ba-179">**CreateDomainShader**</span><span class="sxs-lookup"><span data-stu-id="a13ba-179">**CreateDomainShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [<span data-ttu-id="a13ba-180">**CreateGeometryShader**</span><span class="sxs-lookup"><span data-stu-id="a13ba-180">**CreateGeometryShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [<span data-ttu-id="a13ba-181">**CreateGeometryShaderWithStreamOutput**</span><span class="sxs-lookup"><span data-stu-id="a13ba-181">**CreateGeometryShaderWithStreamOutput**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [<span data-ttu-id="a13ba-182">**CreateHullShader**</span><span class="sxs-lookup"><span data-stu-id="a13ba-182">**CreateHullShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [<span data-ttu-id="a13ba-183">**CreatePixelShader**</span><span class="sxs-lookup"><span data-stu-id="a13ba-183">**CreatePixelShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createpixelshader)
-   [<span data-ttu-id="a13ba-184">**CreateVertexShader**</span><span class="sxs-lookup"><span data-stu-id="a13ba-184">**CreateVertexShader**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

<span data-ttu-id="a13ba-185">Inoltre, se si fornisce un valore non **null** a *pHResult* quando si fornisce **null** a *pPump*, **D3DX11CompileFromResource** restituisce il codice di \_ errore E INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="a13ba-185">In addition, if you supply a non-**NULL** value to *pHResult* when you supply **NULL** to *pPump*, **D3DX11CompileFromResource** returns the E\_INVALIDARG error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a13ba-186">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a13ba-186">Requirements</span></span>



| <span data-ttu-id="a13ba-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="a13ba-187">Requirement</span></span> | <span data-ttu-id="a13ba-188">Valore</span><span class="sxs-lookup"><span data-stu-id="a13ba-188">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a13ba-189">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a13ba-189">Header</span></span><br/>  | <dl> <span data-ttu-id="a13ba-190"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="a13ba-190"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="a13ba-191">Libreria</span><span class="sxs-lookup"><span data-stu-id="a13ba-191">Library</span></span><br/> | <dl> <span data-ttu-id="a13ba-192"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a13ba-192"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a13ba-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a13ba-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a13ba-194">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="a13ba-194">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

