---
description: Creare un pool di effetti da un file di effetti.
ms.assetid: be738374-a91e-43d3-9cec-14882e6317ee
title: Funzione D3DX10CreateEffectPoolFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 418ea287b9bbf2021f3b2e5379b209cf87745a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322418"
---
# <a name="d3dx10createeffectpoolfromfile-function"></a><span data-ttu-id="12884-103">D3DX10CreateEffectPoolFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="12884-103">D3DX10CreateEffectPoolFromFile function</span></span>

<span data-ttu-id="12884-104">Creare un pool di effetti da un file di effetti.</span><span class="sxs-lookup"><span data-stu-id="12884-104">Create an effect pool from an effect file.</span></span>

## <a name="syntax"></a><span data-ttu-id="12884-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12884-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromFile(
  _In_        LPCTSTR            pFileName,
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



## <a name="parameters"></a><span data-ttu-id="12884-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="12884-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12884-107">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12884-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12884-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12884-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12884-109">Nome del file di effetto.</span><span class="sxs-lookup"><span data-stu-id="12884-109">The effect filename.</span></span> <span data-ttu-id="12884-110">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="12884-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="12884-111">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="12884-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="12884-112">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12884-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12884-113">Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="12884-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="12884-114">Matrice con terminazione NULL delle macro dello shader (vedere [**la \_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="12884-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="12884-115">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12884-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12884-116">Tipo: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="12884-116">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="12884-117">Puntatore a un'interfaccia di inclusione (vedere [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="12884-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="12884-118">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="12884-118">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="12884-119">*pProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12884-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12884-120">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12884-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12884-121">Stringa che specifica il [profilo dello shader](../direct3dhlsl/dx-graphics-hlsl-models.md)o il modello dello shader.</span><span class="sxs-lookup"><span data-stu-id="12884-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="12884-122">*HLSLFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12884-122">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12884-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12884-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12884-124">Opzioni di compilazione HLSL ( [vedere \_ costanti shader D3D10](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="12884-124">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="12884-125">*FXFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12884-125">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12884-126">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12884-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="12884-127">Opzioni di compilazione degli effetti (vedere [flag di compilazione ed effetto](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="12884-127">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="12884-128">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12884-128">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12884-129">Tipo: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="12884-129">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="12884-130">Un puntatore al dispositivo (vedere [**interfaccia ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) che utilizzerà le risorse.</span><span class="sxs-lookup"><span data-stu-id="12884-130">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="12884-131">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12884-131">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12884-132">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="12884-132">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="12884-133">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="12884-133">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="12884-134">Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="12884-134">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="12884-135">*ppEffectPool* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="12884-135">*ppEffectPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12884-136">Tipo: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="12884-136">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="12884-137">Indirizzo di un puntatore al pool di effetti (vedere [**interfaccia ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="12884-137">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="12884-138">*ppErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="12884-138">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12884-139">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="12884-139">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="12884-140">Indirizzo di un puntatore alla memoria (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene gli errori di compilazione degli effetti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="12884-140">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="12884-141">*pHResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="12884-141">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12884-142">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="12884-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="12884-143">Puntatore al valore restituito.</span><span class="sxs-lookup"><span data-stu-id="12884-143">A pointer to the return value.</span></span> <span data-ttu-id="12884-144">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="12884-144">May be **NULL**.</span></span> <span data-ttu-id="12884-145">Se *pPump* non è **null**, *pHResult* deve essere una posizione di memoria valida fino al completamento dell'esecuzione asincrona.</span><span class="sxs-lookup"><span data-stu-id="12884-145">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12884-146">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12884-146">Return value</span></span>

<span data-ttu-id="12884-147">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12884-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12884-148">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="12884-148">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="12884-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="12884-149">Remarks</span></span>

<span data-ttu-id="12884-150">Questo esempio crea un pool di effetti dall'effetto usato nell' [esempio BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="12884-150">This example creates an effect pool from the effect used in the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


```
   
// Create an effect pool from an effect in memory
ID3D10EffectPool * l_pEffectPool = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
WCHAR str[MAX_PATH];
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CreateEffectPoolFromFile( str, 
    NULL, NULL, D3D10_SHADER_ENABLE_STRICTNESS, 
    0, pd3dDevice, NULL, &l_pEffectPool,
    &l_pBlob_Errors );
```



## <a name="requirements"></a><span data-ttu-id="12884-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12884-151">Requirements</span></span>



| <span data-ttu-id="12884-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="12884-152">Requirement</span></span> | <span data-ttu-id="12884-153">Valore</span><span class="sxs-lookup"><span data-stu-id="12884-153">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="12884-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12884-154">Header</span></span><br/> | <dl> <span data-ttu-id="12884-155"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="12884-155"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12884-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12884-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12884-157">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="12884-157">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
