---
description: Creare un processore di dati asincrono per uno shader.
ms.assetid: e23290fa-ccd7-4703-ae6b-4fffe352875e
title: Funzione D3DX10CreateAsyncCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 1fa6a558efd56917832da3280df2aad4ac400def
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234979"
---
# <a name="d3dx10createasynccompilerprocessor-function"></a><span data-ttu-id="71e38-103">D3DX10CreateAsyncCompilerProcessor (funzione)</span><span class="sxs-lookup"><span data-stu-id="71e38-103">D3DX10CreateAsyncCompilerProcessor function</span></span>

<span data-ttu-id="71e38-104">Creare un processore di dati asincrono per uno shader.</span><span class="sxs-lookup"><span data-stu-id="71e38-104">Create an asynchronous-data processor for a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="71e38-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71e38-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D10_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="71e38-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="71e38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71e38-107">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71e38-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e38-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71e38-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71e38-109">Stringa che contiene il nome file dello shader.</span><span class="sxs-lookup"><span data-stu-id="71e38-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="71e38-110">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71e38-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e38-111">Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="71e38-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="71e38-112">Matrice con terminazione NULL delle macro dello shader (vedere [**la \_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="71e38-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="71e38-113">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71e38-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e38-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="71e38-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="71e38-115">Puntatore a un'interfaccia di inclusione (vedere [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="71e38-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="71e38-116">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="71e38-116">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="71e38-117">*pFunctionName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71e38-117">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e38-118">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71e38-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71e38-119">Nome della funzione del punto di ingresso dello shader in cui inizia l'esecuzione dello shader.</span><span class="sxs-lookup"><span data-stu-id="71e38-119">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="71e38-120">Quando si compila un effetto, **D3DX10CreateAsyncCompilerProcessor** ignora *pFunctionName*; si consiglia di impostare *pFunctionName* su **null** perché è consigliabile impostare un parametro puntatore su **null** se la funzione chiamata non lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="71e38-120">When you compile an effect, **D3DX10CreateAsyncCompilerProcessor** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="71e38-121">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71e38-121">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e38-122">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71e38-122">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71e38-123">Stringa che specifica il [profilo dello shader](../direct3dhlsl/dx-graphics-hlsl-models.md) o il modello dello shader.</span><span class="sxs-lookup"><span data-stu-id="71e38-123">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="71e38-124">*Flags1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71e38-124">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e38-125">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71e38-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71e38-126">[Flag di compilazione shader](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="71e38-126">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="71e38-127">*Flags2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71e38-127">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e38-128">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="71e38-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="71e38-129">[Flag di compilazione effetto](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="71e38-129">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="71e38-130">Quando si compila uno shader e non un file di effetto, **D3DX10CreateAsyncCompilerProcessor** ignora *Flags2*; si consiglia di impostare *Flags2* su zero perché è consigliabile impostare un parametro puntatore su **null** se la funzione chiamata non lo utilizzerà.</span><span class="sxs-lookup"><span data-stu-id="71e38-130">When you compile a shader and not an effect file, **D3DX10CreateAsyncCompilerProcessor** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="71e38-131">*ppCompiledShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="71e38-131">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71e38-132">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="71e38-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="71e38-133">Indirizzo di un puntatore all'effetto compilato (vedere l' [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="71e38-133">Address of a pointer to the compiled effect (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="71e38-134">*ppErrorBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="71e38-134">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71e38-135">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="71e38-135">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="71e38-136">Indirizzo di un puntatore per la compilazione degli errori (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="71e38-136">Address of a pointer to compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="71e38-137">*ppDataProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="71e38-137">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71e38-138">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="71e38-138">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="71e38-139">Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="71e38-139">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71e38-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71e38-140">Return value</span></span>

<span data-ttu-id="71e38-141">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="71e38-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="71e38-142">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="71e38-142">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="71e38-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71e38-143">Requirements</span></span>



| <span data-ttu-id="71e38-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="71e38-144">Requirement</span></span> | <span data-ttu-id="71e38-145">Valore</span><span class="sxs-lookup"><span data-stu-id="71e38-145">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="71e38-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71e38-146">Header</span></span><br/> | <dl> <span data-ttu-id="71e38-147"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="71e38-147"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71e38-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71e38-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71e38-149">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="71e38-149">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
