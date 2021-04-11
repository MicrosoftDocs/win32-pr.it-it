---
description: Creare un processore di dati asincrono per un pool di memoria.
ms.assetid: 3985a5e5-492e-4003-9d10-6e34620de69f
title: Funzione D3DX10CreateAsyncEffectPoolCreateProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectPoolCreateProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 32e7c60f28a823c624b3866a8cdd46db659f8a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235076"
---
# <a name="d3dx10createasynceffectpoolcreateprocessor-function"></a><span data-ttu-id="cfc57-103">D3DX10CreateAsyncEffectPoolCreateProcessor (funzione)</span><span class="sxs-lookup"><span data-stu-id="cfc57-103">D3DX10CreateAsyncEffectPoolCreateProcessor function</span></span>

<span data-ttu-id="cfc57-104">Creare un processore di dati asincrono per un pool di memoria.</span><span class="sxs-lookup"><span data-stu-id="cfc57-104">Create an asynchronous-data processor for a memory pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfc57-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cfc57-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectPoolCreateProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _In_        ID3D10Device         *pDevice,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="cfc57-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cfc57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfc57-107">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfc57-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc57-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfc57-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfc57-109">Stringa che contiene il nome file dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="cfc57-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="cfc57-110">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfc57-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc57-111">Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="cfc57-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="cfc57-112">Matrice con terminazione NULL delle macro dello shader (vedere [**la \_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="cfc57-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="cfc57-113">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfc57-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc57-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="cfc57-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="cfc57-115">Puntatore a un'interfaccia di inclusione (vedere [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); impostare su **null** per specificare che non è presente alcun file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="cfc57-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="cfc57-116">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfc57-116">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc57-117">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfc57-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfc57-118">Stringa che specifica il [profilo dello shader](../direct3dhlsl/dx-graphics-hlsl-models.md) o il modello dello shader.</span><span class="sxs-lookup"><span data-stu-id="cfc57-118">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="cfc57-119">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfc57-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc57-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfc57-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfc57-121">Opzioni di compilazione HLSL (vedere [flag shader](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="cfc57-121">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="cfc57-122">*FXFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfc57-122">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc57-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cfc57-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cfc57-124">Opzioni di compilazione degli effetti (vedere [flag di compilazione ed effetto](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="cfc57-124">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="cfc57-125">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfc57-125">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc57-126">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="cfc57-126">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="cfc57-127">Un puntatore al dispositivo (vedere [**interfaccia ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) che utilizzerà le risorse.</span><span class="sxs-lookup"><span data-stu-id="cfc57-127">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="cfc57-128">*ppErrorBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cfc57-128">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc57-129">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="cfc57-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="cfc57-130">Indirizzo di un puntatore alla memoria (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene gli errori di compilazione degli effetti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="cfc57-130">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="cfc57-131">*ppDataProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cfc57-131">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfc57-132">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cfc57-132">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="cfc57-133">Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="cfc57-133">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfc57-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cfc57-134">Return value</span></span>

<span data-ttu-id="cfc57-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cfc57-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cfc57-136">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="cfc57-136">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfc57-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfc57-137">Requirements</span></span>



| <span data-ttu-id="cfc57-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfc57-138">Requirement</span></span> | <span data-ttu-id="cfc57-139">Valore</span><span class="sxs-lookup"><span data-stu-id="cfc57-139">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfc57-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cfc57-140">Header</span></span><br/> | <dl> <span data-ttu-id="cfc57-141"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfc57-141"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfc57-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfc57-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfc57-143">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="cfc57-143">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
