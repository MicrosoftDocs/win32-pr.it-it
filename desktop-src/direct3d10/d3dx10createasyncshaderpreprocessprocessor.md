---
description: Creare un elaboratore di dati per uno shader in modo asincrono.
ms.assetid: f5521e55-5f20-422d-979e-98b70efd3b13
title: Funzione D3DX10CreateAsyncShaderPreprocessProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderPreprocessProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 14afdb899d99b7c0278d3042fbc9a108f446c692
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323316"
---
# <a name="d3dx10createasyncshaderpreprocessprocessor-function"></a><span data-ttu-id="d9e20-103">D3DX10CreateAsyncShaderPreprocessProcessor (funzione)</span><span class="sxs-lookup"><span data-stu-id="d9e20-103">D3DX10CreateAsyncShaderPreprocessProcessor function</span></span>

<span data-ttu-id="d9e20-104">Creare un elaboratore di dati per uno shader in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="d9e20-104">Create a data processor for a shader asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9e20-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9e20-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderPreprocessProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _Out_       ID3D10Blob           **ppShaderText,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="d9e20-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9e20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9e20-107">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9e20-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e20-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d9e20-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d9e20-109">Stringa che contiene il nome file dello shader.</span><span class="sxs-lookup"><span data-stu-id="d9e20-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="d9e20-110">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9e20-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e20-111">Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="d9e20-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="d9e20-112">Matrice con terminazione NULL delle macro dello shader (vedere [**la \_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="d9e20-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="d9e20-113">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9e20-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e20-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="d9e20-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="d9e20-115">Puntatore a un'interfaccia di inclusione (vedere [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); impostare su **null** per specificare che non è presente alcun file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="d9e20-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="d9e20-116">*ppShaderText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d9e20-116">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e20-117">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d9e20-117">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d9e20-118">Indirizzo di un puntatore a un buffer contenente il testo ASCII dello shader (vedere l' [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="d9e20-118">Address of a pointer to a buffer that contains the ASCII text of the shader (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="d9e20-119">*ppErrorBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d9e20-119">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e20-120">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="d9e20-120">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="d9e20-121">Indirizzo di un puntatore a un buffer che contiene errori di compilazione (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="d9e20-121">Address of a pointer to a buffer that contains compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="d9e20-122">*ppDataProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d9e20-122">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9e20-123">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d9e20-123">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="d9e20-124">Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="d9e20-124">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9e20-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9e20-125">Return value</span></span>

<span data-ttu-id="d9e20-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d9e20-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d9e20-127">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d9e20-127">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9e20-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9e20-128">Requirements</span></span>



| <span data-ttu-id="d9e20-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9e20-129">Requirement</span></span> | <span data-ttu-id="d9e20-130">Valore</span><span class="sxs-lookup"><span data-stu-id="d9e20-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9e20-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9e20-131">Header</span></span><br/> | <dl> <span data-ttu-id="d9e20-132"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9e20-132"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9e20-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9e20-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9e20-134">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="d9e20-134">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
