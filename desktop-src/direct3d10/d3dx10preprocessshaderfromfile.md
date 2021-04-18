---
description: Nota invece di usare questa funzione legacy, è consigliabile usare l'API D3DPreprocess. Creare uno shader da un file senza compilarlo.
ms.assetid: 9f609aa5-5ee7-45fb-9693-69de130b6cc0
title: Funzione D3DX10PreprocessShaderFromFile (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e6222febd378b262d9fb9e87a6224968c2d04038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323168"
---
# <a name="d3dx10preprocessshaderfromfile-function"></a><span data-ttu-id="9878c-104">D3DX10PreprocessShaderFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="9878c-104">D3DX10PreprocessShaderFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="9878c-105">Invece di usare questa funzione legacy, è consigliabile usare l'API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="9878c-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="9878c-106">Creare uno shader da un file senza compilarlo.</span><span class="sxs-lookup"><span data-stu-id="9878c-106">Create a shader from a file without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="9878c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9878c-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="9878c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9878c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9878c-109">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9878c-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9878c-110">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9878c-110">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9878c-111">Nome del file shader.</span><span class="sxs-lookup"><span data-stu-id="9878c-111">Name of the shader file.</span></span>

</dd> <dt>

<span data-ttu-id="9878c-112">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9878c-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9878c-113">Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="9878c-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="9878c-114">Matrice con terminazione NULL delle macro dello shader (vedere [**la \_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="9878c-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="9878c-115">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9878c-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9878c-116">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="9878c-116">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="9878c-117">Puntatore a un'interfaccia di inclusione (vedere [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); impostare su **null** per specificare che non è presente alcun file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="9878c-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="9878c-118">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9878c-118">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9878c-119">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="9878c-119">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="9878c-120">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="9878c-120">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="9878c-121">Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="9878c-121">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="9878c-122">*ppShaderText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9878c-122">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9878c-123">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="9878c-123">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="9878c-124">Puntatore alla memoria (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene lo shader non compilato.</span><span class="sxs-lookup"><span data-stu-id="9878c-124">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="9878c-125">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9878c-125">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9878c-126">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="9878c-126">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="9878c-127">Indirizzo di un puntatore alla memoria (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene gli errori di creazione degli effetti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="9878c-127">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9878c-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9878c-128">Return value</span></span>

<span data-ttu-id="9878c-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9878c-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9878c-130">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9878c-130">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9878c-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9878c-131">Requirements</span></span>



| <span data-ttu-id="9878c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9878c-132">Requirement</span></span> | <span data-ttu-id="9878c-133">Valore</span><span class="sxs-lookup"><span data-stu-id="9878c-133">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9878c-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9878c-134">Header</span></span><br/> | <dl> <span data-ttu-id="9878c-135"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="9878c-135"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9878c-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9878c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9878c-137">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="9878c-137">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
