---
description: Nota invece di usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore dalla riga di comando o l'API D3DCompile. Compilare uno shader o un effetto da una risorsa.
ms.assetid: d291e47d-e04f-4e2d-9d05-9aef8e4fcf7e
title: Funzione D3DX10CompileFromResource (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 6b698700804ca767c953343e6d5a5e540ca77555
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322428"
---
# <a name="d3dx10compilefromresource-function"></a><span data-ttu-id="c9a31-104">D3DX10CompileFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="c9a31-104">D3DX10CompileFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="c9a31-105">Invece di usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore da riga di comando o l'API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="c9a31-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="c9a31-106">Compilare uno shader o un effetto da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="c9a31-106">Compile a shader or an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a31-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9a31-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromResource(
  _In_        HMODULE            hSrcModule,
  _In_        LPCTSTR            pSrcResource,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
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



## <a name="parameters"></a><span data-ttu-id="c9a31-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9a31-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a31-109">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9a31-109">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a31-110">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9a31-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9a31-111">Handle per il modulo della risorsa contenente lo shader.</span><span class="sxs-lookup"><span data-stu-id="c9a31-111">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="c9a31-112">HMODULE può essere ottenuto con la [funzione GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="c9a31-112">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="c9a31-113">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9a31-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a31-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9a31-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9a31-115">Nome della risorsa contenente lo shader.</span><span class="sxs-lookup"><span data-stu-id="c9a31-115">Name of the resource containing the shader.</span></span> <span data-ttu-id="c9a31-116">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="c9a31-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="c9a31-117">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="c9a31-117">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="c9a31-118">*pSrcFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9a31-118">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a31-119">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9a31-119">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9a31-120">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c9a31-120">Optional.</span></span> <span data-ttu-id="c9a31-121">Nome del file di effetto, che viene usato solo per i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="c9a31-121">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="c9a31-122">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="c9a31-122">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c9a31-123">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9a31-123">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a31-124">Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="c9a31-124">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="c9a31-125">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c9a31-125">Optional.</span></span> <span data-ttu-id="c9a31-126">Puntatore a una matrice di definizioni di macro (vedere la [**\_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="c9a31-126">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="c9a31-127">L'ultima struttura della matrice funge da carattere di terminazione e deve avere tutti i membri impostati su 0.</span><span class="sxs-lookup"><span data-stu-id="c9a31-127">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="c9a31-128">Se non viene usato, impostare *pDefines* su **null**.</span><span class="sxs-lookup"><span data-stu-id="c9a31-128">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c9a31-129">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9a31-129">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a31-130">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="c9a31-130">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="c9a31-131">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c9a31-131">Optional.</span></span> <span data-ttu-id="c9a31-132">Puntatore a un'interfaccia di [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) per la gestione dei file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="c9a31-132">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="c9a31-133">Se si imposta su **null** , verrà generato un errore di compilazione se uno shader contiene un' \# inclusione.</span><span class="sxs-lookup"><span data-stu-id="c9a31-133">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="c9a31-134">*pFunctionName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9a31-134">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a31-135">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9a31-135">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9a31-136">Nome della funzione del punto di ingresso dello shader in cui inizia l'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="c9a31-136">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="c9a31-137">Quando si compila un effetto, **D3DX10CompileFromResource** ignora *pFunctionName*; si consiglia di impostare *pFunctionName* su **null** perché è consigliabile impostare un parametro puntatore su **null** se la funzione chiamata non lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="c9a31-137">When you compile an effect, **D3DX10CompileFromResource** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="c9a31-138">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9a31-138">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a31-139">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9a31-139">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9a31-140">Stringa che specifica il modello di shader; può essere qualsiasi profilo in [Shader Model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)o [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="c9a31-140">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9a31-141">*Flags1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9a31-141">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a31-142">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9a31-142">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9a31-143">[Flag di compilazione shader](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="c9a31-143">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="c9a31-144">*Flags2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9a31-144">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a31-145">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9a31-145">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c9a31-146">[Flag di compilazione effetto](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c9a31-146">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="c9a31-147">Quando si compila uno shader e non un file di effetto, **D3DX10CompileFromResource** ignora *Flags2*; si consiglia di impostare *Flags2* su zero, perché è consigliabile impostare un parametro non di puntatore su zero se la funzione chiamata non lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="c9a31-147">When you compile a shader and not an effect file, **D3DX10CompileFromResource** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="c9a31-148">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9a31-148">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a31-149">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9a31-149">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="c9a31-150">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="c9a31-150">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="c9a31-151">Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="c9a31-151">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="c9a31-152">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c9a31-152">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a31-153">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c9a31-153">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c9a31-154">Puntatore a un' [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) che contiene lo shader compilato, nonché tutte le informazioni di debug e tabella di simboli incorporate.</span><span class="sxs-lookup"><span data-stu-id="c9a31-154">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="c9a31-155">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c9a31-155">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a31-156">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c9a31-156">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c9a31-157">Puntatore a un' [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) contenente un elenco di errori e avvisi che si sono verificati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="c9a31-157">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="c9a31-158">Questi errori e avvisi sono identici a quelli dell'output di debug di un debugger.</span><span class="sxs-lookup"><span data-stu-id="c9a31-158">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="c9a31-159">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c9a31-159">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a31-160">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="c9a31-160">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="c9a31-161">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="c9a31-161">A pointer to the return value.</span></span> <span data-ttu-id="c9a31-162">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="c9a31-162">May be **NULL**.</span></span> <span data-ttu-id="c9a31-163">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="c9a31-163">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9a31-164">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9a31-164">Return value</span></span>

<span data-ttu-id="c9a31-165">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c9a31-165">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c9a31-166">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c9a31-166">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9a31-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9a31-167">Requirements</span></span>



| <span data-ttu-id="c9a31-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9a31-168">Requirement</span></span> | <span data-ttu-id="c9a31-169">Valore</span><span class="sxs-lookup"><span data-stu-id="c9a31-169">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a31-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9a31-170">Header</span></span><br/> | <dl> <span data-ttu-id="c9a31-171"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9a31-171"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9a31-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9a31-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a31-173">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="c9a31-173">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
