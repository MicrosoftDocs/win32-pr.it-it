---
title: Funzione D3DX11CreateAsyncShaderPreprocessProcessor (D3DX11async. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni. Creare un elaboratore di dati per uno shader in modo asincrono.
ms.assetid: a7e9754b-acc1-49d0-bd8e-b116bc3c7e3a
keywords:
- Funzione D3DX11CreateAsyncShaderPreprocessProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderPreprocessProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e58b267f186e5fd0104b10e9f9423f407aaf13
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969436"
---
# <a name="d3dx11createasyncshaderpreprocessprocessor-function"></a><span data-ttu-id="6aab7-106">D3DX11CreateAsyncShaderPreprocessProcessor (funzione)</span><span class="sxs-lookup"><span data-stu-id="6aab7-106">D3DX11CreateAsyncShaderPreprocessProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="6aab7-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="6aab7-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="6aab7-108">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="6aab7-108">See Remarks.</span></span>

 

<span data-ttu-id="6aab7-109">Creare un elaboratore di dati per uno shader in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="6aab7-109">Create a data processor for a shader asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aab7-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6aab7-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncShaderPreprocessProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _Out_       ID3D10Blob           **ppShaderText,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="6aab7-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="6aab7-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aab7-112">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6aab7-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aab7-113">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6aab7-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6aab7-114">Stringa che contiene il nome file dello shader.</span><span class="sxs-lookup"><span data-stu-id="6aab7-114">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="6aab7-115">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6aab7-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aab7-116">Tipo: **const d3d11 \_ shader \_ macro \***</span><span class="sxs-lookup"><span data-stu-id="6aab7-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="6aab7-117">Matrice con terminazione NULL delle macro dello shader; impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="6aab7-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="6aab7-118">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6aab7-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aab7-119">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="6aab7-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="6aab7-120">Puntatore a un'interfaccia di inclusione. impostare su **null** per specificare che non è presente alcun file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="6aab7-120">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="6aab7-121">*ppShaderText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6aab7-121">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aab7-122">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="6aab7-122">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="6aab7-123">Indirizzo di un puntatore a un buffer contenente il testo ASCII dello shader.</span><span class="sxs-lookup"><span data-stu-id="6aab7-123">Address of a pointer to a buffer that contains the ASCII text of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="6aab7-124">*ppErrorBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6aab7-124">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aab7-125">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="6aab7-125">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="6aab7-126">Indirizzo di un puntatore a un buffer che contiene errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="6aab7-126">Address of a pointer to a buffer that contains compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="6aab7-127">*ppDataProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6aab7-127">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aab7-128">Tipo: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6aab7-128">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="6aab7-129">Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX11DataProcessor**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="6aab7-129">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aab7-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6aab7-130">Return value</span></span>

<span data-ttu-id="6aab7-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6aab7-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6aab7-132">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6aab7-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6aab7-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="6aab7-133">Remarks</span></span>

<span data-ttu-id="6aab7-134">Non è presente alcuna implementazione del caricatore asincrono al di fuori di D3DX 10 e D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="6aab7-134">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="6aab7-135">Per le app di Windows Store, gli esempi di DirectX (ad esempio, l' [esempio di esercitazione Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) includono il modulo **BasicLoader** che usa il modello di programmazione asincrona Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="6aab7-135">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="6aab7-136">Per le applicazioni desktop Win32, è possibile utilizzare il [runtime di concorrenza](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) per implementare un modello simile a quello del Windows Runtime modello di programmazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="6aab7-136">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="6aab7-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6aab7-137">Requirements</span></span>



| <span data-ttu-id="6aab7-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="6aab7-138">Requirement</span></span> | <span data-ttu-id="6aab7-139">Valore</span><span class="sxs-lookup"><span data-stu-id="6aab7-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6aab7-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6aab7-140">Header</span></span><br/>  | <dl> <span data-ttu-id="6aab7-141"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="6aab7-141"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="6aab7-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="6aab7-142">Library</span></span><br/> | <dl> <span data-ttu-id="6aab7-143"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6aab7-143"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6aab7-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6aab7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aab7-145">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="6aab7-145">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

