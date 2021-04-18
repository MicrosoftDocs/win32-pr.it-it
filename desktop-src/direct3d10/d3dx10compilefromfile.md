---
description: Nota invece di usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore dalla riga di comando o l'API D3DCompile. Compilare uno shader o un effetto da un file.
ms.assetid: b0ca0b6a-3ff0-49ee-83de-14c4686a7104
title: Funzione D3DX10CompileFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CompileFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 571f8123a9834c95ecca6043c3495fb18fbaca47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323379"
---
# <a name="d3dx10compilefromfile-function"></a><span data-ttu-id="b1dcc-104">D3DX10CompileFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="b1dcc-104">D3DX10CompileFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="b1dcc-105">Invece di usare questa funzione legacy, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore da riga di comando o l'API [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) .</span><span class="sxs-lookup"><span data-stu-id="b1dcc-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

<span data-ttu-id="b1dcc-106">Compilare uno shader o un effetto da un file.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-106">Compile a shader or an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1dcc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1dcc-107">Syntax</span></span>


```C++
HRESULT D3DX10CompileFromFile(
  _In_        LPCTSTR            pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="b1dcc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1dcc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1dcc-109">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1dcc-109">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dcc-110">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1dcc-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1dcc-111">Nome del file che contiene il codice dello shader.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-111">The name of the file that contains the shader code.</span></span> <span data-ttu-id="b1dcc-112">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-112">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="b1dcc-113">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-113">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="b1dcc-114">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1dcc-114">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dcc-115">Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="b1dcc-115">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="b1dcc-116">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-116">Optional.</span></span> <span data-ttu-id="b1dcc-117">Puntatore a una matrice di definizioni di macro (vedere la [**\_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span><span class="sxs-lookup"><span data-stu-id="b1dcc-117">Pointer to an array of macro definitions (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)).</span></span> <span data-ttu-id="b1dcc-118">L'ultima struttura della matrice funge da carattere di terminazione e deve avere tutti i membri impostati su 0.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-118">The last structure in the array serves as a terminator and must have all members set to 0.</span></span> <span data-ttu-id="b1dcc-119">Se non viene usato, impostare *pDefines* su **null**.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-119">If not used, set *pDefines* to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b1dcc-120">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1dcc-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dcc-121">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="b1dcc-121">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="b1dcc-122">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-122">Optional.</span></span> <span data-ttu-id="b1dcc-123">Puntatore a un'interfaccia di [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) per la gestione dei file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-123">Pointer to an [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85)) interface for handling include files.</span></span> <span data-ttu-id="b1dcc-124">Se si imposta su **null** , verrà generato un errore di compilazione se uno shader contiene un' \# inclusione.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-124">Setting this to **NULL** will cause a compile error if a shader contains a \#include.</span></span>

</dd> <dt>

<span data-ttu-id="b1dcc-125">*pFunctionName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1dcc-125">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dcc-126">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1dcc-126">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1dcc-127">Nome della funzione del punto di ingresso dello shader in cui inizia l'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-127">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="b1dcc-128">Quando si compila un effetto, **D3DX10CompileFromFile** ignora *pFunctionName*; si consiglia di impostare *pFunctionName* su **null** perché è consigliabile impostare un parametro puntatore su **null** se la funzione chiamata non lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-128">When you compile an effect, **D3DX10CompileFromFile** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="b1dcc-129">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1dcc-129">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dcc-130">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1dcc-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1dcc-131">Stringa che specifica il modello di shader; può essere qualsiasi profilo in [Shader Model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [Shader Model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md)o [Shader Model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="b1dcc-131">A string that specifies the shader model; can be any profile in [shader model 2](../direct3dhlsl/dx-graphics-hlsl-sm2.md), [shader model 3](../direct3dhlsl/dx-graphics-hlsl-sm3.md), or [shader model 4](../direct3dhlsl/dx-graphics-hlsl-sm4.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1dcc-132">*Flags1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1dcc-132">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dcc-133">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1dcc-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1dcc-134">[Flag di compilazione shader](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="b1dcc-134">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="b1dcc-135">*Flags2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1dcc-135">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dcc-136">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1dcc-136">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1dcc-137">[Flag di compilazione effetto](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b1dcc-137">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="b1dcc-138">Quando si compila uno shader e non un file di effetto, **D3DX10CompileFromFile** ignora *Flags2*; si consiglia di impostare *Flags2* su zero, perché è consigliabile impostare un parametro non di puntatore su zero se la funzione chiamata non lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-138">When you compile a shader and not an effect file, **D3DX10CompileFromFile** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="b1dcc-139">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1dcc-139">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dcc-140">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1dcc-140">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="b1dcc-141">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="b1dcc-141">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="b1dcc-142">Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-142">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="b1dcc-143">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b1dcc-143">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dcc-144">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="b1dcc-144">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="b1dcc-145">Puntatore a un' [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) che contiene lo shader compilato, nonché tutte le informazioni di debug e tabella di simboli incorporate.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-145">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains the compiled shader, as well as any embedded debug and symbol-table information.</span></span>

</dd> <dt>

<span data-ttu-id="b1dcc-146">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b1dcc-146">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dcc-147">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="b1dcc-147">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="b1dcc-148">Puntatore a un' [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) contenente un elenco di errori e avvisi che si sono verificati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-148">A pointer to an [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob) which contains a listing of errors and warnings that occurred during compilation.</span></span> <span data-ttu-id="b1dcc-149">Questi errori e avvisi sono identici a quelli dell'output di debug di un debugger.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-149">These errors and warnings are identical to the debug output from a debugger.</span></span>

</dd> <dt>

<span data-ttu-id="b1dcc-150">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b1dcc-150">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1dcc-151">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="b1dcc-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="b1dcc-152">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-152">A pointer to the return value.</span></span> <span data-ttu-id="b1dcc-153">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-153">May be **NULL**.</span></span> <span data-ttu-id="b1dcc-154">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="b1dcc-154">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1dcc-155">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1dcc-155">Return value</span></span>

<span data-ttu-id="b1dcc-156">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1dcc-156">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1dcc-157">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b1dcc-157">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1dcc-158">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="b1dcc-158">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b1dcc-159">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1dcc-159">Requirements</span></span>



| <span data-ttu-id="b1dcc-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1dcc-160">Requirement</span></span> | <span data-ttu-id="b1dcc-161">Valore</span><span class="sxs-lookup"><span data-stu-id="b1dcc-161">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1dcc-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1dcc-162">Header</span></span><br/> | <dl> <span data-ttu-id="b1dcc-163"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1dcc-163"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1dcc-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1dcc-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1dcc-165">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="b1dcc-165">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
