---
description: Creare un pool di effetti da un effetto in memoria.
ms.assetid: 634bcb23-a73f-4493-b805-e2aa5420fa2a
title: Funzione D3DX10CreateEffectPoolFromMemory (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 7dc93b7e73f336e75432debfe9bde6659ea4707c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322417"
---
# <a name="d3dx10createeffectpoolfrommemory-function"></a><span data-ttu-id="25e4b-103">D3DX10CreateEffectPoolFromMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="25e4b-103">D3DX10CreateEffectPoolFromMemory function</span></span>

<span data-ttu-id="25e4b-104">Creare un pool di effetti da un effetto in memoria.</span><span class="sxs-lookup"><span data-stu-id="25e4b-104">Create an effect pool from an effect in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="25e4b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25e4b-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromMemory(
  _In_        LPCVOID            pData,
  _In_        SIZE_T             DataLength,
  _In_        LPCSTR             pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10EffectPool   **ppEffectPool,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="25e4b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="25e4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25e4b-107">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25e4b-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25e4b-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25e4b-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25e4b-109">Puntatore all'effetto.</span><span class="sxs-lookup"><span data-stu-id="25e4b-109">A pointer to the effect.</span></span>

</dd> <dt>

<span data-ttu-id="25e4b-110">*DataLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25e4b-110">*DataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25e4b-111">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25e4b-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25e4b-112">Dimensione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="25e4b-112">The size of the effect.</span></span>

</dd> <dt>

<span data-ttu-id="25e4b-113">*pSrcFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25e4b-113">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25e4b-114">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25e4b-114">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25e4b-115">Nome del file di effetti.</span><span class="sxs-lookup"><span data-stu-id="25e4b-115">The name of the effect file.</span></span>

</dd> <dt>

<span data-ttu-id="25e4b-116">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25e4b-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25e4b-117">Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="25e4b-117">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="25e4b-118">Matrice con terminazione NULL delle macro dello shader (vedere [**la \_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="25e4b-118">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="25e4b-119">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25e4b-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25e4b-120">Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="25e4b-120">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="25e4b-121">Puntatore a un'interfaccia di inclusione (vedere [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="25e4b-121">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="25e4b-122">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="25e4b-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="25e4b-123">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25e4b-123">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25e4b-124">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25e4b-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25e4b-125">Stringa che specifica il [profilo dello shader](../direct3dhlsl/dx-graphics-hlsl-models.md)o il modello dello shader.</span><span class="sxs-lookup"><span data-stu-id="25e4b-125">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="25e4b-126">*HLSLFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25e4b-126">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25e4b-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25e4b-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25e4b-128">Opzioni di compilazione HLSL ( [vedere \_ costanti shader D3D10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="25e4b-128">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="25e4b-129">*FXFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25e4b-129">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25e4b-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25e4b-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25e4b-131">Opzioni di compilazione degli effetti (vedere [flag di compilazione ed effetto](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="25e4b-131">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="25e4b-132">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25e4b-132">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25e4b-133">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="25e4b-133">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="25e4b-134">Un puntatore al dispositivo (vedere [**interfaccia ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) che utilizzerà le risorse.</span><span class="sxs-lookup"><span data-stu-id="25e4b-134">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="25e4b-135">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25e4b-135">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25e4b-136">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="25e4b-136">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="25e4b-137">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="25e4b-137">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="25e4b-138">Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="25e4b-138">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="25e4b-139">*ppEffectPool* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="25e4b-139">*ppEffectPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25e4b-140">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="25e4b-140">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="25e4b-141">Indirizzo di un puntatore al pool di effetti (vedere [**interfaccia ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="25e4b-141">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="25e4b-142">*ppErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="25e4b-142">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25e4b-143">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="25e4b-143">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="25e4b-144">Indirizzo di un puntatore alla memoria (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene gli errori di compilazione degli effetti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="25e4b-144">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="25e4b-145">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="25e4b-145">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25e4b-146">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="25e4b-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="25e4b-147">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="25e4b-147">A pointer to the return value.</span></span> <span data-ttu-id="25e4b-148">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="25e4b-148">May be **NULL**.</span></span> <span data-ttu-id="25e4b-149">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="25e4b-149">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25e4b-150">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25e4b-150">Return value</span></span>

<span data-ttu-id="25e4b-151">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25e4b-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25e4b-152">Restituisce uno dei seguenti [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="25e4b-152">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25e4b-153">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25e4b-153">Requirements</span></span>



| <span data-ttu-id="25e4b-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="25e4b-154">Requirement</span></span> | <span data-ttu-id="25e4b-155">Valore</span><span class="sxs-lookup"><span data-stu-id="25e4b-155">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="25e4b-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25e4b-156">Header</span></span><br/> | <dl> <span data-ttu-id="25e4b-157"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="25e4b-157"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25e4b-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25e4b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25e4b-159">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="25e4b-159">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
