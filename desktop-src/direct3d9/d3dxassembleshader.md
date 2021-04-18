---
description: Assembla uno shader.
ms.assetid: 24c3dcae-9397-4856-b072-0ae340157bf9
title: Funzione D3DXAssembleShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7268d394021c7dc1be665f8ed8781a827d1fcdb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322892"
---
# <a name="d3dxassembleshader-function"></a><span data-ttu-id="82284-103">D3DXAssembleShader (funzione)</span><span class="sxs-lookup"><span data-stu-id="82284-103">D3DXAssembleShader function</span></span>

<span data-ttu-id="82284-104">Assembla uno shader.</span><span class="sxs-lookup"><span data-stu-id="82284-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="82284-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82284-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShader(
  _In_        LPCSTR        pSrcData,
  _In_        UINT          SrcDataLen,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="82284-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="82284-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82284-107">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82284-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82284-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82284-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82284-109">Puntatore a un buffer di memoria che contiene i dati dello shader.</span><span class="sxs-lookup"><span data-stu-id="82284-109">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="82284-110">*SrcDataLen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82284-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82284-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82284-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82284-112">Lunghezza in byte dei dati effettivi.</span><span class="sxs-lookup"><span data-stu-id="82284-112">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="82284-113">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82284-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82284-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="82284-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="82284-115">Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="82284-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="82284-116">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="82284-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="82284-117">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82284-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82284-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="82284-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="82284-119">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="82284-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="82284-120">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="82284-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="82284-121">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82284-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82284-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82284-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82284-123">Opzioni di compilazione identificate da diversi flag.</span><span class="sxs-lookup"><span data-stu-id="82284-123">Compile options identified by various flags.</span></span> <span data-ttu-id="82284-124">Il compilatore Direct3D 10 HLSL è ora il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="82284-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="82284-125">Per informazioni dettagliate, vedere [flag D3DXSHADER](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="82284-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="82284-126">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="82284-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82284-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="82284-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="82284-128">Restituisce un buffer contenente lo shader creato.</span><span class="sxs-lookup"><span data-stu-id="82284-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="82284-129">Questo buffer contiene il codice dello shader compilato, nonché tutte le informazioni di debug e di tabella dei simboli incorporate.</span><span class="sxs-lookup"><span data-stu-id="82284-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="82284-130">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="82284-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82284-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="82284-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="82284-132">Restituisce un buffer contenente un elenco di errori e avvisi che sono stati rilevati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="82284-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="82284-133">Si tratta degli stessi messaggi visualizzati dal debugger durante l'esecuzione in modalità di debug.</span><span class="sxs-lookup"><span data-stu-id="82284-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="82284-134">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="82284-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82284-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82284-135">Return value</span></span>

<span data-ttu-id="82284-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="82284-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="82284-137">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="82284-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="82284-138">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="82284-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="82284-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82284-139">Requirements</span></span>



| <span data-ttu-id="82284-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="82284-140">Requirement</span></span> | <span data-ttu-id="82284-141">Valore</span><span class="sxs-lookup"><span data-stu-id="82284-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="82284-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82284-142">Header</span></span><br/>  | <dl> <span data-ttu-id="82284-143"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="82284-143"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="82284-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="82284-144">Library</span></span><br/> | <dl> <span data-ttu-id="82284-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82284-145"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="82284-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82284-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82284-147">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="82284-147">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="82284-148">**D3DXAssembleShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="82284-148">**D3DXAssembleShaderFromFile**</span></span>](d3dxassembleshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="82284-149">**D3DXAssembleShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="82284-149">**D3DXAssembleShaderFromResource**</span></span>](d3dxassembleshaderfromresource.md)
</dt> </dl>

 

 
