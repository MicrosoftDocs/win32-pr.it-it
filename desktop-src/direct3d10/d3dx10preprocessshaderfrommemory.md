---
description: Nota invece di usare questa funzione legacy, è consigliabile usare l'API D3DPreprocess. Creare uno shader dalla memoria senza compilarlo.
ms.assetid: 099bc010-1269-4833-8a96-a7c78ed48206
title: Funzione D3DX10PreprocessShaderFromMemory (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10PreprocessShaderFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d06e46a5cd6b86420543b380f74273be032c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762221"
---
# <a name="d3dx10preprocessshaderfrommemory-function"></a><span data-ttu-id="1ae18-104">D3DX10PreprocessShaderFromMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="1ae18-104">D3DX10PreprocessShaderFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="1ae18-105">Invece di usare questa funzione legacy, è consigliabile usare l'API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="1ae18-105">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

<span data-ttu-id="1ae18-106">Creare uno shader dalla memoria senza compilarlo.</span><span class="sxs-lookup"><span data-stu-id="1ae18-106">Create a shader from memory without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ae18-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ae18-107">Syntax</span></span>


```C++
HRESULT D3DX10PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="1ae18-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ae18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ae18-109">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae18-109">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae18-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ae18-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ae18-111">Puntatore alla memoria contenente lo shader.</span><span class="sxs-lookup"><span data-stu-id="1ae18-111">Pointer to the memory containing the shader.</span></span>

</dd> <dt>

<span data-ttu-id="1ae18-112">*SrcDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae18-112">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae18-113">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ae18-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ae18-114">Dimensioni dello shader.</span><span class="sxs-lookup"><span data-stu-id="1ae18-114">Size of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="1ae18-115">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae18-115">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae18-116">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ae18-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ae18-117">Nome dello shader.</span><span class="sxs-lookup"><span data-stu-id="1ae18-117">Name of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="1ae18-118">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae18-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae18-119">Tipo: **const [**D3D \_ shader \_ macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="1ae18-119">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="1ae18-120">Matrice con terminazione NULL delle macro dello shader (vedere [**la \_ \_ macro dello shader D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); impostare su **null** per specificare nessuna macro.</span><span class="sxs-lookup"><span data-stu-id="1ae18-120">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="1ae18-121">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae18-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae18-122">Tipo: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="1ae18-122">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="1ae18-123">Puntatore a un'interfaccia di inclusione (vedere [**interfaccia ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); impostare su **null** per specificare che non è presente alcun file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="1ae18-123">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="1ae18-124">*pPump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae18-124">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae18-125">Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ae18-125">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="1ae18-126">Puntatore a un'interfaccia della pompa di thread (vedere [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="1ae18-126">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="1ae18-127">Utilizzare **null** per specificare che questa funzione non deve essere restituita finché non viene completata.</span><span class="sxs-lookup"><span data-stu-id="1ae18-127">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="1ae18-128">*ppShaderText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1ae18-128">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae18-129">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="1ae18-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="1ae18-130">Puntatore alla memoria (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene lo shader non compilato.</span><span class="sxs-lookup"><span data-stu-id="1ae18-130">A pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="1ae18-131">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1ae18-131">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae18-132">Tipo: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="1ae18-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="1ae18-133">Indirizzo di un puntatore alla memoria (vedere [**interfaccia ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene gli errori di creazione degli effetti, se presenti.</span><span class="sxs-lookup"><span data-stu-id="1ae18-133">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect-creation errors, if any occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ae18-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ae18-134">Return value</span></span>

<span data-ttu-id="1ae18-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1ae18-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1ae18-136">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="1ae18-136">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ae18-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ae18-137">Requirements</span></span>



| <span data-ttu-id="1ae18-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ae18-138">Requirement</span></span> | <span data-ttu-id="1ae18-139">Valore</span><span class="sxs-lookup"><span data-stu-id="1ae18-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae18-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ae18-140">Header</span></span><br/>  | <dl> <span data-ttu-id="1ae18-141"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ae18-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ae18-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="1ae18-142">Library</span></span><br/> | <dl> <span data-ttu-id="1ae18-143"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ae18-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ae18-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ae18-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae18-145">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="1ae18-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
