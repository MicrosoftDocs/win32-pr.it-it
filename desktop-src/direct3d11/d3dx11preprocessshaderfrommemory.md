---
title: Funzione D3DX11PreprocessShaderFromMemory (D3DX11async. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Si noti invece di usare questa funzione, è consigliabile usare l'API D3DPreprocess. Creare uno shader dalla memoria senza compilarlo.
ms.assetid: 3c646914-9334-44fe-a8a0-b84d0dc1a16e
keywords:
- Funzione D3DX11PreprocessShaderFromMemory Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a94633270fe0f4e462e60915de862be8693daa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995990"
---
# <a name="d3dx11preprocessshaderfrommemory-function"></a><span data-ttu-id="fd6b2-106">D3DX11PreprocessShaderFromMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="fd6b2-106">D3DX11PreprocessShaderFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="fd6b2-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="fd6b2-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="fd6b2-108">Invece di usare questa funzione, è consigliabile usare l'API [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="fd6b2-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="fd6b2-109">Creare uno shader dalla memoria senza compilarlo.</span><span class="sxs-lookup"><span data-stu-id="fd6b2-109">Create a shader from memory without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd6b2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd6b2-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="fd6b2-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd6b2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd6b2-112">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd6b2-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6b2-113">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fd6b2-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fd6b2-114">Puntatore alla memoria contenente lo shader.</span><span class="sxs-lookup"><span data-stu-id="fd6b2-114">Pointer to the memory containing the shader.</span></span>

</dd> <dt>

<span data-ttu-id="fd6b2-115">*SrcDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd6b2-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6b2-116">Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fd6b2-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fd6b2-117">Dimensioni dello shader.</span><span class="sxs-lookup"><span data-stu-id="fd6b2-117">Size of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="fd6b2-118">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd6b2-118">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6b2-119">Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="fd6b2-119">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="fd6b2-120">Nome dello shader.</span><span class="sxs-lookup"><span data-stu-id="fd6b2-120">Name of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="fd6b2-121">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd6b2-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6b2-122">Tipo: **const d3d11 \_ shader \_ macro \***</span><span class="sxs-lookup"><span data-stu-id="fd6b2-122">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="fd6b2-123">Matrice con terminazione NULL delle macro dello shader; impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="fd6b2-123">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="fd6b2-124">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd6b2-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6b2-125">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="fd6b2-125">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="fd6b2-126">Puntatore a un'interfaccia di inclusione. impostare su **null** per specificare che non è presente alcun file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="fd6b2-126">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="fd6b2-127">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd6b2-127">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6b2-128">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd6b2-128">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="fd6b2-129">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="fd6b2-129">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="fd6b2-130">Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="fd6b2-130">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="fd6b2-131">*ppShaderText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fd6b2-131">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6b2-132">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="fd6b2-132">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="fd6b2-133">Puntatore alla memoria che contiene lo shader non compilato.</span><span class="sxs-lookup"><span data-stu-id="fd6b2-133">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="fd6b2-134">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fd6b2-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6b2-135">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="fd6b2-135">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="fd6b2-136">Indirizzo di un puntatore alla memoria che contiene gli errori di creazione dell'effetto, se presenti.</span><span class="sxs-lookup"><span data-stu-id="fd6b2-136">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="fd6b2-137">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fd6b2-137">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd6b2-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="fd6b2-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="fd6b2-139">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="fd6b2-139">A pointer to the return value.</span></span> <span data-ttu-id="fd6b2-140">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="fd6b2-140">May be **NULL**.</span></span> <span data-ttu-id="fd6b2-141">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="fd6b2-141">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd6b2-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd6b2-142">Return value</span></span>

<span data-ttu-id="fd6b2-143">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fd6b2-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fd6b2-144">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fd6b2-144">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd6b2-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd6b2-145">Requirements</span></span>



| <span data-ttu-id="fd6b2-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd6b2-146">Requirement</span></span> | <span data-ttu-id="fd6b2-147">Valore</span><span class="sxs-lookup"><span data-stu-id="fd6b2-147">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd6b2-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fd6b2-148">Header</span></span><br/>  | <dl> <span data-ttu-id="fd6b2-149"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd6b2-149"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="fd6b2-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="fd6b2-150">Library</span></span><br/> | <dl> <span data-ttu-id="fd6b2-151"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd6b2-151"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fd6b2-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd6b2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd6b2-153">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="fd6b2-153">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

