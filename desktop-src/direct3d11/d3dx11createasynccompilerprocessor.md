---
title: Funzione D3DX11CreateAsyncCompilerProcessor (D3DX11async. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni. Creare un processore di dati asincrono per uno shader.
ms.assetid: 90756ac3-946d-49fa-9f97-70dc5da812c6
keywords:
- Funzione D3DX11CreateAsyncCompilerProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncCompilerProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533e487e65640b8c17a0ff8d061388e8b5a6c0f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996050"
---
# <a name="d3dx11createasynccompilerprocessor-function"></a><span data-ttu-id="a64ce-106">D3DX11CreateAsyncCompilerProcessor (funzione)</span><span class="sxs-lookup"><span data-stu-id="a64ce-106">D3DX11CreateAsyncCompilerProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="a64ce-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a64ce-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="a64ce-108">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a64ce-108">See Remarks.</span></span>

 

<span data-ttu-id="a64ce-109">Creare un processore di dati asincrono per uno shader.</span><span class="sxs-lookup"><span data-stu-id="a64ce-109">Create an asynchronous-data processor for a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="a64ce-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a64ce-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="a64ce-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="a64ce-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a64ce-112">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a64ce-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a64ce-113">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a64ce-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a64ce-114">Stringa che contiene il nome file dello shader.</span><span class="sxs-lookup"><span data-stu-id="a64ce-114">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="a64ce-115">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a64ce-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a64ce-116">Tipo: **const d3d11 \_ shader \_ macro \***</span><span class="sxs-lookup"><span data-stu-id="a64ce-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="a64ce-117">Matrice con terminazione NULL delle macro dello shader; impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="a64ce-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="a64ce-118">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a64ce-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a64ce-119">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="a64ce-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="a64ce-120">Puntatore a un'interfaccia di inclusione.</span><span class="sxs-lookup"><span data-stu-id="a64ce-120">A pointer to an include interface.</span></span> <span data-ttu-id="a64ce-121">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a64ce-121">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a64ce-122">*pFunctionName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a64ce-122">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a64ce-123">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a64ce-123">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a64ce-124">Nome della funzione del punto di ingresso dello shader in cui inizia l'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="a64ce-124">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="a64ce-125">Quando si compila un effetto, **D3DX11CreateAsyncCompilerProcessor** ignora *pFunctionName*; si consiglia di impostare *pFunctionName* su **null** perché è consigliabile impostare un parametro puntatore su **null** se la funzione chiamata non lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="a64ce-125">When you compile an effect, **D3DX11CreateAsyncCompilerProcessor** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it..</span></span>

</dd> <dt>

<span data-ttu-id="a64ce-126">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a64ce-126">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a64ce-127">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a64ce-127">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a64ce-128">Stringa che specifica il profilo dello shader o il modello dello shader; può essere qualsiasi profilo in Shader Model 2, Shader Model 3, Shader Model 4 o Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="a64ce-128">A string that specifies the shader profile or shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="a64ce-129">Il profilo può essere anche per il tipo di effetto (ad esempio, FX \_ 4 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="a64ce-129">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="a64ce-130">*Flags1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a64ce-130">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a64ce-131">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a64ce-131">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a64ce-132">Flag di compilazione shader.</span><span class="sxs-lookup"><span data-stu-id="a64ce-132">Shader compile flags.</span></span>

</dd> <dt>

<span data-ttu-id="a64ce-133">*Flags2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a64ce-133">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a64ce-134">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a64ce-134">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a64ce-135">Flag di compilazione effetto.</span><span class="sxs-lookup"><span data-stu-id="a64ce-135">Effect compile flags.</span></span> <span data-ttu-id="a64ce-136">Quando si compila uno shader e non un file di effetto, **D3DX11CreateAsyncCompilerProcessor** ignora *Flags2*; si consiglia di impostare *Flags2* su zero, perché è consigliabile impostare un parametro non di puntatore su zero se la funzione chiamata non lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="a64ce-136">When you compile a shader and not an effect file, **D3DX11CreateAsyncCompilerProcessor** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="a64ce-137">*ppCompiledShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a64ce-137">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a64ce-138">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="a64ce-138">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="a64ce-139">Indirizzo di un puntatore all'effetto compilato.</span><span class="sxs-lookup"><span data-stu-id="a64ce-139">Address of a pointer to the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="a64ce-140">*ppErrorBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a64ce-140">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a64ce-141">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="a64ce-141">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="a64ce-142">Indirizzo di un puntatore per la compilazione degli errori.</span><span class="sxs-lookup"><span data-stu-id="a64ce-142">Address of a pointer to compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="a64ce-143">*ppDataProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a64ce-143">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a64ce-144">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a64ce-144">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="a64ce-145">Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="a64ce-145">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a64ce-146">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a64ce-146">Return value</span></span>

<span data-ttu-id="a64ce-147">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a64ce-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a64ce-148">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a64ce-148">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a64ce-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="a64ce-149">Remarks</span></span>

<span data-ttu-id="a64ce-150">Non è presente alcuna implementazione del caricatore asincrono al di fuori di D3DX 10 e D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="a64ce-150">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="a64ce-151">Per le app di Windows Store, gli esempi di DirectX (ad esempio, l' [esempio di esercitazione Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) includono il modulo **BasicLoader** che usa il modello di programmazione asincrona Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="a64ce-151">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="a64ce-152">Per le applicazioni desktop Win32, è possibile utilizzare il [runtime di concorrenza](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) per implementare un modello simile a quello del Windows Runtime modello di programmazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="a64ce-152">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="a64ce-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a64ce-153">Requirements</span></span>



| <span data-ttu-id="a64ce-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="a64ce-154">Requirement</span></span> | <span data-ttu-id="a64ce-155">Valore</span><span class="sxs-lookup"><span data-stu-id="a64ce-155">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a64ce-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a64ce-156">Header</span></span><br/>  | <dl> <span data-ttu-id="a64ce-157"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="a64ce-157"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="a64ce-158">Libreria</span><span class="sxs-lookup"><span data-stu-id="a64ce-158">Library</span></span><br/> | <dl> <span data-ttu-id="a64ce-159"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a64ce-159"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a64ce-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a64ce-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a64ce-161">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="a64ce-161">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

