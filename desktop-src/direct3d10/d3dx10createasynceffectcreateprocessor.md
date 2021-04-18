---
description: Creare un pool di effetti in modo asincrono.
ms.assetid: 50c55751-26de-4002-9a89-8e5ab59dda79
title: Funzione D3DX10CreateAsyncEffectCreateProcessor (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectCreateProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 573efc51214031afe66f6cfd552bbda634d15142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322422"
---
# <a name="d3dx10createasynceffectcreateprocessor-function"></a><span data-ttu-id="ac22f-103">D3DX10CreateAsyncEffectCreateProcessor (funzione)</span><span class="sxs-lookup"><span data-stu-id="ac22f-103">D3DX10CreateAsyncEffectCreateProcessor function</span></span>

<span data-ttu-id="ac22f-104">Creare un pool di effetti in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="ac22f-104">Create an effect pool asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac22f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac22f-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectCreateProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _In_        ID3D10Device         *pDevice,
  _In_        ID3D10EffectPool     *pPool,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="ac22f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac22f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac22f-107">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac22f-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac22f-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac22f-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac22f-109">Stringa che contiene il nome file dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="ac22f-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="ac22f-110">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac22f-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac22f-111">Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="ac22f-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="ac22f-112">Matrice con terminazione NULL delle macro dello shader (vedere [**la \_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="ac22f-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="ac22f-113">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac22f-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac22f-114">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="ac22f-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="ac22f-115">Puntatore a un'interfaccia di inclusione (vedere [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); impostare su **null** per specificare che non è presente alcun file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="ac22f-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="ac22f-116">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac22f-116">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac22f-117">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac22f-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac22f-118">Stringa che specifica il [profilo dello shader](../direct3dhlsl/dx-graphics-hlsl-models.md) o il modello dello shader.</span><span class="sxs-lookup"><span data-stu-id="ac22f-118">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="ac22f-119">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac22f-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac22f-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac22f-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac22f-121">Opzioni di compilazione HLSL (vedere [flag shader](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="ac22f-121">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ac22f-122">*FXFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac22f-122">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac22f-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac22f-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac22f-124">Opzioni di compilazione degli effetti (vedere [flag di compilazione ed effetto](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="ac22f-124">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ac22f-125">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac22f-125">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac22f-126">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="ac22f-126">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="ac22f-127">Un puntatore al dispositivo (vedere [**interfaccia ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) che utilizzerà le risorse.</span><span class="sxs-lookup"><span data-stu-id="ac22f-127">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="ac22f-128">*pPool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac22f-128">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac22f-129">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="ac22f-129">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="ac22f-130">Puntatore a un pool di effetti (vedere [**interfaccia ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) per la condivisione di variabili tra effetti.</span><span class="sxs-lookup"><span data-stu-id="ac22f-130">A pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="ac22f-131">*ppErrorBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ac22f-131">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac22f-132">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="ac22f-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="ac22f-133">Indirizzo di un puntatore alla memoria (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene gli errori di compilazione degli effetti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="ac22f-133">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="ac22f-134">*ppProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ac22f-134">*ppProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac22f-135">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ac22f-135">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="ac22f-136">Indirizzo di un puntatore al processore di dati asincrono (vedere [**interfaccia ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="ac22f-136">The address of a pointer to the asynchronous-data processor (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac22f-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac22f-137">Return value</span></span>

<span data-ttu-id="ac22f-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ac22f-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ac22f-139">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ac22f-139">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac22f-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac22f-140">Requirements</span></span>



| <span data-ttu-id="ac22f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac22f-141">Requirement</span></span> | <span data-ttu-id="ac22f-142">Valore</span><span class="sxs-lookup"><span data-stu-id="ac22f-142">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac22f-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac22f-143">Header</span></span><br/> | <dl> <span data-ttu-id="ac22f-144"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac22f-144"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac22f-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac22f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac22f-146">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="ac22f-146">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
