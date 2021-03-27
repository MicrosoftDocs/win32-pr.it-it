---
title: Funzione D3DX11PreprocessShaderFromFile (D3DX11async. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Si noti invece di usare questa funzione, è consigliabile usare l'API D3DPreprocess. Creare uno shader da un file senza compilarlo.
ms.assetid: aab08efd-b6b0-44e5-bd68-f32c242d9e94
keywords:
- Funzione D3DX11PreprocessShaderFromFile Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1987ef25688e83a48059805f79af4dc8a88c1ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982319"
---
# <a name="d3dx11preprocessshaderfromfile-function"></a><span data-ttu-id="c43bf-106">D3DX11PreprocessShaderFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="c43bf-106">D3DX11PreprocessShaderFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="c43bf-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="c43bf-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="c43bf-108">Invece di usare questa funzione, è consigliabile usare l'API [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="c43bf-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="c43bf-109">Creare uno shader da un file senza compilarlo.</span><span class="sxs-lookup"><span data-stu-id="c43bf-109">Create a shader from a file without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="c43bf-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c43bf-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="c43bf-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="c43bf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c43bf-112">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c43bf-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c43bf-113">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c43bf-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c43bf-114">Nome del file shader.</span><span class="sxs-lookup"><span data-stu-id="c43bf-114">Name of the shader file.</span></span>

</dd> <dt>

<span data-ttu-id="c43bf-115">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c43bf-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c43bf-116">Tipo: **const d3d11 \_ shader \_ macro \***</span><span class="sxs-lookup"><span data-stu-id="c43bf-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="c43bf-117">Matrice con terminazione NULL delle macro dello shader; impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="c43bf-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="c43bf-118">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c43bf-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c43bf-119">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="c43bf-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="c43bf-120">Puntatore a un'interfaccia di inclusione. impostare su **null** per specificare che non è presente alcun file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="c43bf-120">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="c43bf-121">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c43bf-121">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c43bf-122">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="c43bf-122">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="c43bf-123">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="c43bf-123">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="c43bf-124">Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="c43bf-124">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="c43bf-125">*ppShaderText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c43bf-125">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c43bf-126">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c43bf-126">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c43bf-127">Puntatore alla memoria che contiene lo shader non compilato.</span><span class="sxs-lookup"><span data-stu-id="c43bf-127">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="c43bf-128">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c43bf-128">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c43bf-129">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c43bf-129">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c43bf-130">Indirizzo di un puntatore alla memoria che contiene gli errori di creazione dell'effetto, se presenti.</span><span class="sxs-lookup"><span data-stu-id="c43bf-130">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c43bf-131">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c43bf-131">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c43bf-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="c43bf-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="c43bf-133">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="c43bf-133">A pointer to the return value.</span></span> <span data-ttu-id="c43bf-134">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="c43bf-134">May be **NULL**.</span></span> <span data-ttu-id="c43bf-135">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="c43bf-135">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c43bf-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c43bf-136">Return value</span></span>

<span data-ttu-id="c43bf-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c43bf-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c43bf-138">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c43bf-138">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c43bf-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c43bf-139">Requirements</span></span>



| <span data-ttu-id="c43bf-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c43bf-140">Requirement</span></span> | <span data-ttu-id="c43bf-141">Valore</span><span class="sxs-lookup"><span data-stu-id="c43bf-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c43bf-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c43bf-142">Header</span></span><br/>  | <dl> <span data-ttu-id="c43bf-143"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="c43bf-143"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="c43bf-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="c43bf-144">Library</span></span><br/> | <dl> <span data-ttu-id="c43bf-145"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c43bf-145"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c43bf-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c43bf-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c43bf-147">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="c43bf-147">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

