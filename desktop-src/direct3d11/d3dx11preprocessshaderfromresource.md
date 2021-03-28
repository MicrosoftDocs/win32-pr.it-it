---
title: Funzione D3DX11PreprocessShaderFromResource (D3DX11async. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Si noti invece di usare questa funzione, è consigliabile usare l'API D3DPreprocess. Creare uno shader da una risorsa senza compilarlo.
ms.assetid: 13362ad6-f02e-4899-8962-4f7d4750ff69
keywords:
- Funzione D3DX11PreprocessShaderFromResource Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645d872e983cabbcd81aab05a59ee8f1f83cc403
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995987"
---
# <a name="d3dx11preprocessshaderfromresource-function"></a><span data-ttu-id="356db-106">D3DX11PreprocessShaderFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="356db-106">D3DX11PreprocessShaderFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="356db-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="356db-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="356db-108">Invece di usare questa funzione, è consigliabile usare l'API [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="356db-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="356db-109">Creare uno shader da una risorsa senza compilarlo.</span><span class="sxs-lookup"><span data-stu-id="356db-109">Create a shader from a resource without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="356db-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="356db-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="356db-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="356db-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="356db-112">*hmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="356db-112">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="356db-113">Tipo: **[ **hmodule**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="356db-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="356db-114">Handle per il modulo della risorsa contenente lo shader.</span><span class="sxs-lookup"><span data-stu-id="356db-114">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="356db-115">HMODULE può essere ottenuto con la [funzione GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="356db-115">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="356db-116">*origine* \[ dati in\]</span><span class="sxs-lookup"><span data-stu-id="356db-116">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="356db-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="356db-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="356db-118">Nome della risorsa in hModule lato contenente lo shader.</span><span class="sxs-lookup"><span data-stu-id="356db-118">The name of the resource in side hModule containing the shader.</span></span> <span data-ttu-id="356db-119">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="356db-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="356db-120">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="356db-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="356db-121">*pSrcFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="356db-121">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="356db-122">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="356db-122">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="356db-123">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="356db-123">Optional.</span></span> <span data-ttu-id="356db-124">Nome del file di effetto, che viene usato solo per i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="356db-124">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="356db-125">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="356db-125">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="356db-126">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="356db-126">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="356db-127">Tipo: **const d3d11 \_ shader \_ macro \***</span><span class="sxs-lookup"><span data-stu-id="356db-127">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="356db-128">Matrice con terminazione NULL delle macro dello shader; impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="356db-128">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="356db-129">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="356db-129">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="356db-130">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="356db-130">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="356db-131">Puntatore a un'interfaccia di inclusione. impostare su **null** per specificare che non è presente alcun file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="356db-131">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="356db-132">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="356db-132">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="356db-133">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="356db-133">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="356db-134">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="356db-134">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="356db-135">Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="356db-135">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="356db-136">*ppShaderText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="356db-136">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="356db-137">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="356db-137">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="356db-138">Puntatore alla memoria che contiene lo shader non compilato.</span><span class="sxs-lookup"><span data-stu-id="356db-138">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="356db-139">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="356db-139">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="356db-140">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="356db-140">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="356db-141">Indirizzo di un puntatore alla memoria che contiene gli errori di creazione dell'effetto, se presenti.</span><span class="sxs-lookup"><span data-stu-id="356db-141">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="356db-142">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="356db-142">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="356db-143">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="356db-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="356db-144">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="356db-144">A pointer to the return value.</span></span> <span data-ttu-id="356db-145">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="356db-145">May be **NULL**.</span></span> <span data-ttu-id="356db-146">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="356db-146">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="356db-147">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="356db-147">Return value</span></span>

<span data-ttu-id="356db-148">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="356db-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="356db-149">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="356db-149">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="356db-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="356db-150">Requirements</span></span>



| <span data-ttu-id="356db-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="356db-151">Requirement</span></span> | <span data-ttu-id="356db-152">Valore</span><span class="sxs-lookup"><span data-stu-id="356db-152">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="356db-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="356db-153">Header</span></span><br/>  | <dl> <span data-ttu-id="356db-154"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="356db-154"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="356db-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="356db-155">Library</span></span><br/> | <dl> <span data-ttu-id="356db-156"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="356db-156"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="356db-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="356db-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="356db-158">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="356db-158">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

