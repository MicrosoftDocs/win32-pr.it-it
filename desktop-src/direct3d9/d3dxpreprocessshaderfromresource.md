---
description: Pre-elabora una risorsa shader senza eseguire la compilazione. Questo consente di risolvere tutte le \# definizioni e le \# inclusioni, fornendo uno shader autonomo per la successiva compilazione.
ms.assetid: a00c2db9-d7ba-48ab-80e3-dc20774e1b1e
title: Funzione D3DXPreprocessShaderFromResource (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c45073d0b84ef6fb33d378c4c18f862f55c6b84a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354654"
---
# <a name="d3dxpreprocessshaderfromresource-function"></a><span data-ttu-id="04461-104">D3DXPreprocessShaderFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="04461-104">D3DXPreprocessShaderFromResource function</span></span>

<span data-ttu-id="04461-105">Pre-elabora una risorsa shader senza eseguire la compilazione.</span><span class="sxs-lookup"><span data-stu-id="04461-105">Preprocesses a shader resource without performing compilation.</span></span> <span data-ttu-id="04461-106">Questo consente di risolvere tutte le \# definizioni e le \# inclusioni, fornendo uno shader autonomo per la successiva compilazione.</span><span class="sxs-lookup"><span data-stu-id="04461-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="04461-107">Invece di usare questa funzione legacy, è consigliabile usare l'API [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) .</span><span class="sxs-lookup"><span data-stu-id="04461-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="04461-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04461-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCSTR        pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="04461-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="04461-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04461-110">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04461-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04461-111">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04461-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04461-112">Handle per il modulo che include la risorsa shader.</span><span class="sxs-lookup"><span data-stu-id="04461-112">Handle to the module that holds the shader resource.</span></span> <span data-ttu-id="04461-113">Se questo valore è **null**, verrà usato il modulo corrente.</span><span class="sxs-lookup"><span data-stu-id="04461-113">If this value is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="04461-114">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04461-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04461-115">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="04461-115">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="04461-116">Stringa che rappresenta il nome della risorsa nel modulo.</span><span class="sxs-lookup"><span data-stu-id="04461-116">String that represents the name of the resource in the module.</span></span>

</dd> <dt>

<span data-ttu-id="04461-117">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04461-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04461-118">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="04461-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="04461-119">Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) .</span><span class="sxs-lookup"><span data-stu-id="04461-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="04461-120">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="04461-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="04461-121">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04461-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04461-122">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="04461-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="04461-123">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="04461-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="04461-124">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="04461-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="04461-125">*ppShaderText* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="04461-125">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04461-126">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="04461-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="04461-127">Restituisce un buffer contenente un'unica stringa di grandi dimensioni che rappresenta il flusso del token formattato risultante.</span><span class="sxs-lookup"><span data-stu-id="04461-127">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="04461-128">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="04461-128">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04461-129">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="04461-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="04461-130">Restituisce un buffer contenente un elenco di errori e avvisi che sono stati rilevati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="04461-130">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="04461-131">Si tratta degli stessi messaggi visualizzati dal debugger durante l'esecuzione in modalità di debug.</span><span class="sxs-lookup"><span data-stu-id="04461-131">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="04461-132">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="04461-132">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04461-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04461-133">Return value</span></span>

<span data-ttu-id="04461-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="04461-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="04461-135">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="04461-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="04461-136">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="04461-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="04461-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04461-137">Requirements</span></span>



| <span data-ttu-id="04461-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="04461-138">Requirement</span></span> | <span data-ttu-id="04461-139">Valore</span><span class="sxs-lookup"><span data-stu-id="04461-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="04461-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04461-140">Header</span></span><br/>  | <dl> <span data-ttu-id="04461-141"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="04461-141"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="04461-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="04461-142">Library</span></span><br/> | <dl> <span data-ttu-id="04461-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04461-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="04461-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04461-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04461-145">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="04461-145">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="04461-146">**D3DXPreprocessShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="04461-146">**D3DXPreprocessShaderFromFile**</span></span>](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="04461-147">**D3DXPreprocessShader**</span><span class="sxs-lookup"><span data-stu-id="04461-147">**D3DXPreprocessShader**</span></span>](d3dxpreprocessshader.md)
</dt> </dl>

 

 
