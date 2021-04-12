---
description: Pre-elabora un file shader senza eseguire la compilazione. Questo consente di risolvere tutte le \# definizioni e le \# inclusioni, fornendo uno shader autonomo per la successiva compilazione.
ms.assetid: 1be68cc0-b4a3-41b4-b956-b96ed439be9e
title: Funzione D3DXPreprocessShaderFromFile (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba9cf35418bbbe6fe4b39341031fd1e056b27dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354779"
---
# <a name="d3dxpreprocessshaderfromfile-function"></a><span data-ttu-id="1aa57-104">D3DXPreprocessShaderFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="1aa57-104">D3DXPreprocessShaderFromFile function</span></span>

<span data-ttu-id="1aa57-105">Pre-elabora un file shader senza eseguire la compilazione.</span><span class="sxs-lookup"><span data-stu-id="1aa57-105">Preprocesses a shader file without performing compilation.</span></span> <span data-ttu-id="1aa57-106">Questo consente di risolvere tutte le \# definizioni e le \# inclusioni, fornendo uno shader autonomo per la successiva compilazione.</span><span class="sxs-lookup"><span data-stu-id="1aa57-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="1aa57-107">Invece di usare questa funzione legacy, è consigliabile usare l'API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="1aa57-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1aa57-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1aa57-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShaderFromFile(
  _In_        LPCSTR        pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="1aa57-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1aa57-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aa57-110">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1aa57-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa57-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1aa57-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1aa57-112">Puntatore a una stringa che specifica il nome del file dello shader.</span><span class="sxs-lookup"><span data-stu-id="1aa57-112">Pointer to a string that specifies the filename of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="1aa57-113">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1aa57-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa57-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="1aa57-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="1aa57-115">Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="1aa57-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="1aa57-116">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="1aa57-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1aa57-117">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1aa57-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa57-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="1aa57-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="1aa57-119">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="1aa57-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="1aa57-120">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="1aa57-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="1aa57-121">*ppShaderText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1aa57-121">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa57-122">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1aa57-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1aa57-123">Restituisce un buffer contenente un'unica stringa di grandi dimensioni che rappresenta il flusso del token formattato risultante.</span><span class="sxs-lookup"><span data-stu-id="1aa57-123">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="1aa57-124">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1aa57-124">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1aa57-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1aa57-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1aa57-126">Restituisce un buffer contenente un elenco di errori e avvisi che sono stati rilevati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="1aa57-126">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="1aa57-127">Si tratta degli stessi messaggi visualizzati dal debugger durante l'esecuzione in modalità di debug.</span><span class="sxs-lookup"><span data-stu-id="1aa57-127">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="1aa57-128">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="1aa57-128">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aa57-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1aa57-129">Return value</span></span>

<span data-ttu-id="1aa57-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1aa57-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1aa57-131">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1aa57-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1aa57-132">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="1aa57-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aa57-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1aa57-133">Requirements</span></span>



| <span data-ttu-id="1aa57-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1aa57-134">Requirement</span></span> | <span data-ttu-id="1aa57-135">Valore</span><span class="sxs-lookup"><span data-stu-id="1aa57-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa57-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1aa57-136">Header</span></span><br/>  | <dl> <span data-ttu-id="1aa57-137"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1aa57-137"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1aa57-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="1aa57-138">Library</span></span><br/> | <dl> <span data-ttu-id="1aa57-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1aa57-139"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1aa57-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1aa57-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aa57-141">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="1aa57-141">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="1aa57-142">**D3DXPreprocessShader**</span><span class="sxs-lookup"><span data-stu-id="1aa57-142">**D3DXPreprocessShader**</span></span>](d3dxpreprocessshader.md)
</dt> <dt>

[<span data-ttu-id="1aa57-143">**D3DXPreprocessShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="1aa57-143">**D3DXPreprocessShaderFromResource**</span></span>](d3dxpreprocessshaderfromresource.md)
</dt> </dl>

 

 
