---
description: Creare un effetto dalla memoria.
ms.assetid: 6903a695-bb87-45fe-9913-25beeaf17233
title: Funzione D3DX10CreateEffectFromMemory (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 03cbbc70e633f8289f99e094602cb1a912b711c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322944"
---
# <a name="d3dx10createeffectfrommemory-function"></a><span data-ttu-id="1ae7f-103">D3DX10CreateEffectFromMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="1ae7f-103">D3DX10CreateEffectFromMemory function</span></span>

<span data-ttu-id="1ae7f-104">Creare un effetto dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-104">Create an effect from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ae7f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ae7f-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromMemory(
  _In_        LPCVOID            pData,
  _In_        SIZE_T             DataLength,
  _In_        LPCSTR             pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3D10EffectPool   *pEffectPool,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Effect       **ppEffect,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="1ae7f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ae7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ae7f-107">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae7f-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae7f-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ae7f-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ae7f-109">Puntatore all'effetto in memoria.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-109">Pointer to the effect in memory.</span></span>

</dd> <dt>

<span data-ttu-id="1ae7f-110">*DataLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae7f-110">*DataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae7f-111">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ae7f-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ae7f-112">Dimensioni dell'effetto in memoria.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-112">Size of the effect in memory.</span></span>

</dd> <dt>

<span data-ttu-id="1ae7f-113">*pSrcFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae7f-113">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae7f-114">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ae7f-114">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ae7f-115">Nome del file degli effetti in memoria.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-115">Name of the effect file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="1ae7f-116">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae7f-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae7f-117">Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="1ae7f-117">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="1ae7f-118">Matrice con terminazione NULL delle macro dello shader (vedere [**la \_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-118">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="1ae7f-119">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae7f-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae7f-120">Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="1ae7f-120">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="1ae7f-121">Puntatore a un'interfaccia di inclusione (vedere [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="1ae7f-121">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="1ae7f-122">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1ae7f-123">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae7f-123">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae7f-124">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ae7f-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ae7f-125">Stringa che specifica il [profilo dello shader](../direct3dhlsl/dx-graphics-hlsl-models.md)o il modello dello shader.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-125">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="1ae7f-126">*HLSLFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae7f-126">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae7f-127">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ae7f-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ae7f-128">Opzioni di compilazione HLSL ( [vedere \_ costanti shader D3D10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="1ae7f-128">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1ae7f-129">*FXFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae7f-129">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae7f-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ae7f-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ae7f-131">Opzioni di compilazione degli effetti (vedere [ \_ costanti degli effetti D3D10](d3d10-effect.md)).</span><span class="sxs-lookup"><span data-stu-id="1ae7f-131">Effect compile options (see [D3D10\_EFFECT Constants](d3d10-effect.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1ae7f-132">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae7f-132">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae7f-133">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="1ae7f-133">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="1ae7f-134">Un puntatore al dispositivo (vedere [**interfaccia ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) che utilizzerà le risorse.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-134">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="1ae7f-135">*pEffectPool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae7f-135">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae7f-136">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="1ae7f-136">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="1ae7f-137">Puntatore a un pool di effetti (vedere [**interfaccia ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) per la condivisione di variabili tra effetti.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-137">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="1ae7f-138">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae7f-138">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae7f-139">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ae7f-139">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="1ae7f-140">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="1ae7f-140">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="1ae7f-141">Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-141">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="1ae7f-142">*ppEffect* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1ae7f-142">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae7f-143">Tipo: **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="1ae7f-143">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="1ae7f-144">Indirizzo di un puntatore all'effetto (vedere [**interfaccia ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) che viene creato.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-144">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="1ae7f-145">*ppErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1ae7f-145">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae7f-146">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="1ae7f-146">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="1ae7f-147">Indirizzo di un puntatore alla memoria (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene gli errori di compilazione degli effetti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-147">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="1ae7f-148">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1ae7f-148">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae7f-149">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="1ae7f-149">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="1ae7f-150">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-150">A pointer to the return value.</span></span> <span data-ttu-id="1ae7f-151">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-151">May be **NULL**.</span></span> <span data-ttu-id="1ae7f-152">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="1ae7f-152">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ae7f-153">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ae7f-153">Return value</span></span>

<span data-ttu-id="1ae7f-154">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1ae7f-154">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1ae7f-155">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1ae7f-155">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ae7f-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ae7f-156">Requirements</span></span>



| <span data-ttu-id="1ae7f-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ae7f-157">Requirement</span></span> | <span data-ttu-id="1ae7f-158">Valore</span><span class="sxs-lookup"><span data-stu-id="1ae7f-158">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae7f-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ae7f-159">Header</span></span><br/> | <dl> <span data-ttu-id="1ae7f-160"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ae7f-160"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ae7f-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ae7f-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae7f-162">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="1ae7f-162">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
