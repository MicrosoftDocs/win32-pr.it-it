---
description: Creare un processore di dati asincrono per un effetto.
ms.assetid: 90a0dcd1-e495-4068-9f28-e2645370b984
title: Funzione D3DX10CreateAsyncEffectCompilerProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 9e1e5716228537d505adc4f48179ec7027b57198
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322949"
---
# <a name="d3dx10createasynceffectcompilerprocessor-function"></a><span data-ttu-id="b8a34-103">D3DX10CreateAsyncEffectCompilerProcessor (funzione)</span><span class="sxs-lookup"><span data-stu-id="b8a34-103">D3DX10CreateAsyncEffectCompilerProcessor function</span></span>

<span data-ttu-id="b8a34-104">Creare un processore di dati asincrono per un effetto.</span><span class="sxs-lookup"><span data-stu-id="b8a34-104">Create an asynchronous-data processor for an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a34-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8a34-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="b8a34-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8a34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8a34-107">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8a34-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8a34-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8a34-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8a34-109">Stringa che contiene il nome file dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b8a34-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="b8a34-110">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8a34-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8a34-111">Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="b8a34-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="b8a34-112">Matrice con terminazione NULL delle macro dello shader (vedere [**la \_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="b8a34-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="b8a34-113">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8a34-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8a34-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="b8a34-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="b8a34-115">Puntatore a un'interfaccia di inclusione (vedere [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="b8a34-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="b8a34-116">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b8a34-116">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b8a34-117">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8a34-117">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8a34-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8a34-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8a34-119">[Opzioni di compilazione HLSL](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b8a34-119">[HLSL compile options](d3d10-graphics-reference-effect-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="b8a34-120">*FXFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8a34-120">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8a34-121">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b8a34-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b8a34-122">[Opzioni di compilazione effetto](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="b8a34-122">[Effect compile options](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b8a34-123">*ppCompiledShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b8a34-123">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8a34-124">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="b8a34-124">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="b8a34-125">Indirizzo di un puntatore al buffer (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene l'effetto compilato.</span><span class="sxs-lookup"><span data-stu-id="b8a34-125">Address of a pointer to buffer (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="b8a34-126">*ppErrorBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b8a34-126">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8a34-127">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="b8a34-127">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="b8a34-128">Indirizzo di un puntatore a un buffer (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="b8a34-128">Address of a pointer to a buffer (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="b8a34-129">*ppDataProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b8a34-129">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b8a34-130">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b8a34-130">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="b8a34-131">Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="b8a34-131">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8a34-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8a34-132">Return value</span></span>

<span data-ttu-id="b8a34-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b8a34-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b8a34-134">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b8a34-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8a34-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8a34-135">Requirements</span></span>



| <span data-ttu-id="b8a34-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8a34-136">Requirement</span></span> | <span data-ttu-id="b8a34-137">Valore</span><span class="sxs-lookup"><span data-stu-id="b8a34-137">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a34-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8a34-138">Header</span></span><br/> | <dl> <span data-ttu-id="b8a34-139"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8a34-139"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8a34-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8a34-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a34-141">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="b8a34-141">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
