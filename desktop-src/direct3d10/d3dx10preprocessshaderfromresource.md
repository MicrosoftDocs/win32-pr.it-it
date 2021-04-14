---
description: Nota invece di usare questa funzione legacy, è consigliabile usare l'API D3DPreprocess. Creare uno shader da una risorsa senza compilarlo.
ms.assetid: ca93e208-7627-4bf5-ab83-d4e906e149eb
title: Funzione D3DX10PreprocessShaderFromResource (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 81a9f272cb0769d4313a4375f98bdc25b9e403e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104402034"
---
# <a name="d3dx10preprocessshaderfromresource-function"></a><span data-ttu-id="30a95-104">D3DX10PreprocessShaderFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="30a95-104">D3DX10PreprocessShaderFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="30a95-105">Invece di usare questa funzione legacy, è consigliabile usare l'API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="30a95-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="30a95-106">Creare uno shader da una risorsa senza compilarlo.</span><span class="sxs-lookup"><span data-stu-id="30a95-106">Create a shader from a resource without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="30a95-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30a95-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="30a95-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="30a95-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30a95-109">*hmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30a95-109">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a95-110">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30a95-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30a95-111">Handle per il modulo della risorsa contenente lo shader.</span><span class="sxs-lookup"><span data-stu-id="30a95-111">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="30a95-112">HMODULE può essere ottenuto con la [funzione GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span><span class="sxs-lookup"><span data-stu-id="30a95-112">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="30a95-113">*origine* \[ dati in\]</span><span class="sxs-lookup"><span data-stu-id="30a95-113">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a95-114">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30a95-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30a95-115">Nome della risorsa in hModule lato contenente lo shader.</span><span class="sxs-lookup"><span data-stu-id="30a95-115">The name of the resource in side hModule containing the shader.</span></span> <span data-ttu-id="30a95-116">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="30a95-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="30a95-117">In caso contrario, il tipo di dati viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="30a95-117">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="30a95-118">*pSrcFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30a95-118">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a95-119">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="30a95-119">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="30a95-120">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="30a95-120">Optional.</span></span> <span data-ttu-id="30a95-121">Nome del file di effetto, che viene usato solo per i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="30a95-121">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="30a95-122">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="30a95-122">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="30a95-123">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30a95-123">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a95-124">Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="30a95-124">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="30a95-125">Matrice con terminazione NULL delle macro dello shader (vedere [**la \_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="30a95-125">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="30a95-126">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30a95-126">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a95-127">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="30a95-127">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="30a95-128">Puntatore a un'interfaccia di inclusione (vedere [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); impostare su **null** per specificare che non è presente alcun file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="30a95-128">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="30a95-129">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30a95-129">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a95-130">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="30a95-130">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="30a95-131">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="30a95-131">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="30a95-132">Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="30a95-132">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="30a95-133">*ppShaderText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="30a95-133">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30a95-134">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="30a95-134">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="30a95-135">Puntatore alla memoria (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene lo shader non compilato.</span><span class="sxs-lookup"><span data-stu-id="30a95-135">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="30a95-136">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="30a95-136">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30a95-137">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="30a95-137">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="30a95-138">Indirizzo di un puntatore alla memoria (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene gli errori di creazione degli effetti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="30a95-138">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30a95-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30a95-139">Return value</span></span>

<span data-ttu-id="30a95-140">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30a95-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30a95-141">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="30a95-141">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30a95-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30a95-142">Requirements</span></span>



| <span data-ttu-id="30a95-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="30a95-143">Requirement</span></span> | <span data-ttu-id="30a95-144">Valore</span><span class="sxs-lookup"><span data-stu-id="30a95-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30a95-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30a95-145">Header</span></span><br/>  | <dl> <span data-ttu-id="30a95-146"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="30a95-146"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="30a95-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="30a95-147">Library</span></span><br/> | <dl> <span data-ttu-id="30a95-148"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30a95-148"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30a95-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30a95-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a95-150">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="30a95-150">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
