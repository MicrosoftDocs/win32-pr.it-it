---
description: Compilare uno shader e creare un elaboratore di dati in modo asincrono.
ms.assetid: 842db48b-51a7-4f32-8ea6-44247f2619b0
title: Funzione D3DX10CreateAsyncShaderCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 2a1cd663827cc32b868c9c6c9b74fbc3c21b8ee6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401946"
---
# <a name="d3dx10createasyncshadercompilerprocessor-function"></a><span data-ttu-id="2e026-103">D3DX10CreateAsyncShaderCompilerProcessor (funzione)</span><span class="sxs-lookup"><span data-stu-id="2e026-103">D3DX10CreateAsyncShaderCompilerProcessor function</span></span>

<span data-ttu-id="2e026-104">Compilare uno shader e creare un elaboratore di dati in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="2e026-104">Compile a shader and create a data processor asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e026-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e026-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="2e026-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e026-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e026-107">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e026-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e026-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e026-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e026-109">Stringa che contiene il nome file dello shader.</span><span class="sxs-lookup"><span data-stu-id="2e026-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="2e026-110">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e026-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e026-111">Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="2e026-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="2e026-112">Matrice con terminazione NULL delle macro dello shader (vedere [**la \_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="2e026-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="2e026-113">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e026-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e026-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="2e026-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="2e026-115">Puntatore a un'interfaccia di inclusione (vedere [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); impostare su **null** per specificare che non è presente alcun file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="2e026-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="2e026-116">*pFunctionName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e026-116">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e026-117">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e026-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e026-118">Nome della funzione del punto di ingresso per lo shader.</span><span class="sxs-lookup"><span data-stu-id="2e026-118">Name of the entry point function for the shader.</span></span>

</dd> <dt>

<span data-ttu-id="2e026-119">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e026-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e026-120">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e026-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e026-121">Stringa che specifica il [profilo dello shader](../direct3dhlsl/dx-graphics-hlsl-models.md) o il modello dello shader.</span><span class="sxs-lookup"><span data-stu-id="2e026-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="2e026-122">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2e026-122">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e026-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e026-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e026-124">Opzioni di compilazione HLSL (vedere [flag shader](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="2e026-124">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="2e026-125">*ppCompiledShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2e026-125">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e026-126">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="2e026-126">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="2e026-127">Indirizzo di un puntatore allo shader compilato.</span><span class="sxs-lookup"><span data-stu-id="2e026-127">Address of a pointer to the compiled shader.</span></span> <span data-ttu-id="2e026-128">Vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob).</span><span class="sxs-lookup"><span data-stu-id="2e026-128">See [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob).</span></span>

</dd> <dt>

<span data-ttu-id="2e026-129">*ppErrorBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2e026-129">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e026-130">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="2e026-130">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="2e026-131">Indirizzo di un puntatore a un buffer che contiene errori di compilazione (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="2e026-131">Address of a pointer to a buffer that contains compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="2e026-132">*ppDataProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2e026-132">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e026-133">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="2e026-133">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="2e026-134">Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="2e026-134">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e026-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e026-135">Return value</span></span>

<span data-ttu-id="2e026-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2e026-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2e026-137">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2e026-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e026-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e026-138">Requirements</span></span>



| <span data-ttu-id="2e026-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e026-139">Requirement</span></span> | <span data-ttu-id="2e026-140">Valore</span><span class="sxs-lookup"><span data-stu-id="2e026-140">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e026-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e026-141">Header</span></span><br/> | <dl> <span data-ttu-id="2e026-142"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e026-142"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e026-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e026-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e026-144">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="2e026-144">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
