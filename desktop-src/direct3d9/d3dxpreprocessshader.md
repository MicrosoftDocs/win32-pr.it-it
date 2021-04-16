---
description: Pre-elabora uno shader senza eseguire la compilazione. Questo consente di risolvere tutte le \# definizioni e le \# inclusioni, fornendo uno shader autonomo per la successiva compilazione.
ms.assetid: d91258ed-6206-487a-aa81-e7c2bcea21ea
title: Funzione D3DXPreprocessShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 042cebe4e678ac1715a37ec3425ec0f21561797c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530853"
---
# <a name="d3dxpreprocessshader-function"></a><span data-ttu-id="53353-104">D3DXPreprocessShader (funzione)</span><span class="sxs-lookup"><span data-stu-id="53353-104">D3DXPreprocessShader function</span></span>

<span data-ttu-id="53353-105">Pre-elabora uno shader senza eseguire la compilazione.</span><span class="sxs-lookup"><span data-stu-id="53353-105">Preprocesses a shader without performing compilation.</span></span> <span data-ttu-id="53353-106">Questo consente di risolvere tutte le \# definizioni e le \# inclusioni, fornendo uno shader autonomo per la successiva compilazione.</span><span class="sxs-lookup"><span data-stu-id="53353-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="53353-107">Invece di usare questa funzione legacy, è consigliabile usare l'API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="53353-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="53353-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53353-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShader(
  _In_        LPCSTR        pSrcData,
  _In_        UINT          SrcDataSize,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="53353-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="53353-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53353-110">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53353-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53353-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53353-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53353-112">Puntatore a una stringa che contiene lo shader.</span><span class="sxs-lookup"><span data-stu-id="53353-112">Pointer to a string that contains the shader.</span></span>

</dd> <dt>

<span data-ttu-id="53353-113">*SrcDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53353-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53353-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53353-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53353-115">Lunghezza dei dati in byte.</span><span class="sxs-lookup"><span data-stu-id="53353-115">Length of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="53353-116">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53353-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53353-117">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="53353-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="53353-118">Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="53353-118">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="53353-119">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="53353-119">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="53353-120">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53353-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53353-121">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="53353-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="53353-122">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="53353-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="53353-123">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="53353-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="53353-124">*ppShaderText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="53353-124">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53353-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="53353-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="53353-126">Restituisce un buffer contenente un'unica stringa di grandi dimensioni che rappresenta il flusso del token formattato risultante.</span><span class="sxs-lookup"><span data-stu-id="53353-126">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="53353-127">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="53353-127">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53353-128">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="53353-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="53353-129">Restituisce un buffer contenente un elenco di errori e avvisi che sono stati rilevati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="53353-129">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="53353-130">Si tratta degli stessi messaggi visualizzati dal debugger durante l'esecuzione in modalità di debug.</span><span class="sxs-lookup"><span data-stu-id="53353-130">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="53353-131">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="53353-131">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53353-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53353-132">Return value</span></span>

<span data-ttu-id="53353-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="53353-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="53353-134">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="53353-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="53353-135">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="53353-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="53353-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53353-136">Requirements</span></span>



| <span data-ttu-id="53353-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="53353-137">Requirement</span></span> | <span data-ttu-id="53353-138">Valore</span><span class="sxs-lookup"><span data-stu-id="53353-138">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="53353-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53353-139">Header</span></span><br/>  | <dl> <span data-ttu-id="53353-140"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="53353-140"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="53353-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="53353-141">Library</span></span><br/> | <dl> <span data-ttu-id="53353-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53353-142"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="53353-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53353-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53353-144">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="53353-144">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="53353-145">**D3DXPreprocessShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="53353-145">**D3DXPreprocessShaderFromFile**</span></span>](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="53353-146">**D3DXPreprocessShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="53353-146">**D3DXPreprocessShaderFromResource**</span></span>](d3dxpreprocessshaderfromresource.md)
</dt> </dl>

 

 
