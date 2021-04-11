---
description: Creare un effetto da una risorsa.
ms.assetid: 239a3b14-9eea-4a0f-96b5-3959b7be3e19
title: Funzione D3DX10CreateEffectFromResource (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 6c5f7b7805e126f02c2658ddce6ec5029978de53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355099"
---
# <a name="d3dx10createeffectfromresource-function"></a><span data-ttu-id="aca13-103">D3DX10CreateEffectFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="aca13-103">D3DX10CreateEffectFromResource function</span></span>

<span data-ttu-id="aca13-104">Creare un effetto da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="aca13-104">Create an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="aca13-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aca13-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
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



## <a name="parameters"></a><span data-ttu-id="aca13-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aca13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aca13-107">*hmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aca13-107">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca13-108">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aca13-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aca13-109">Handle per il modulo della risorsa che contiene l'effetto.</span><span class="sxs-lookup"><span data-stu-id="aca13-109">A handle to the resource module containing the effect.</span></span> <span data-ttu-id="aca13-110">HMODULE può essere ottenuto con la [funzione GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="aca13-110">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="aca13-111">*origine* \[ dati in\]</span><span class="sxs-lookup"><span data-stu-id="aca13-111">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca13-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aca13-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aca13-113">Nome della risorsa in hModule.</span><span class="sxs-lookup"><span data-stu-id="aca13-113">Name of the resource in hModule.</span></span> <span data-ttu-id="aca13-114">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="aca13-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="aca13-115">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="aca13-115">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="aca13-116">*pSrcFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aca13-116">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca13-117">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aca13-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aca13-118">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="aca13-118">Optional.</span></span> <span data-ttu-id="aca13-119">Nome del file di effetto, che viene usato solo per i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="aca13-119">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="aca13-120">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="aca13-120">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aca13-121">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aca13-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca13-122">Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="aca13-122">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="aca13-123">Matrice con terminazione NULL delle macro dello shader (vedere [**la \_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="aca13-123">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="aca13-124">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aca13-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca13-125">Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="aca13-125">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="aca13-126">Puntatore a un'interfaccia di inclusione (vedere [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="aca13-126">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="aca13-127">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="aca13-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aca13-128">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aca13-128">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca13-129">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aca13-129">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aca13-130">Stringa che specifica il [profilo dello shader](../direct3dhlsl/dx-graphics-hlsl-models.md)o il modello dello shader.</span><span class="sxs-lookup"><span data-stu-id="aca13-130">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="aca13-131">*HLSLFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aca13-131">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca13-132">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aca13-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aca13-133">Opzioni di compilazione HLSL ( [vedere \_ costanti shader D3D10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="aca13-133">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="aca13-134">*FXFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aca13-134">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca13-135">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aca13-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aca13-136">Opzioni di compilazione degli effetti (vedere [flag di compilazione ed effetto](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="aca13-136">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="aca13-137">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aca13-137">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca13-138">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="aca13-138">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="aca13-139">Un puntatore al dispositivo (vedere [**interfaccia ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) che utilizzerà le risorse.</span><span class="sxs-lookup"><span data-stu-id="aca13-139">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="aca13-140">*pEffectPool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aca13-140">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca13-141">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="aca13-141">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="aca13-142">Puntatore a un pool di effetti (vedere [**interfaccia ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) per la condivisione di variabili tra effetti.</span><span class="sxs-lookup"><span data-stu-id="aca13-142">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="aca13-143">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aca13-143">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aca13-144">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="aca13-144">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="aca13-145">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="aca13-145">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="aca13-146">Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="aca13-146">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="aca13-147">*ppEffect* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="aca13-147">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aca13-148">Tipo: **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="aca13-148">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="aca13-149">Indirizzo di un puntatore all'effetto (vedere [**interfaccia ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) che viene creato.</span><span class="sxs-lookup"><span data-stu-id="aca13-149">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="aca13-150">*ppErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="aca13-150">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aca13-151">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="aca13-151">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="aca13-152">Indirizzo di un puntatore alla memoria (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene gli errori di compilazione degli effetti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="aca13-152">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="aca13-153">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="aca13-153">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aca13-154">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="aca13-154">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="aca13-155">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="aca13-155">A pointer to the return value.</span></span> <span data-ttu-id="aca13-156">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="aca13-156">May be **NULL**.</span></span> <span data-ttu-id="aca13-157">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="aca13-157">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aca13-158">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aca13-158">Return value</span></span>

<span data-ttu-id="aca13-159">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aca13-159">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aca13-160">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="aca13-160">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aca13-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aca13-161">Requirements</span></span>



| <span data-ttu-id="aca13-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="aca13-162">Requirement</span></span> | <span data-ttu-id="aca13-163">Valore</span><span class="sxs-lookup"><span data-stu-id="aca13-163">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aca13-164">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aca13-164">Header</span></span><br/> | <dl> <span data-ttu-id="aca13-165"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="aca13-165"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aca13-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aca13-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aca13-167">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="aca13-167">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
