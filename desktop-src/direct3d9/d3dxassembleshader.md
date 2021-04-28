---
description: 'Funzione D3DXAssembleShader: assemblare uno shader.'
ms.assetid: 24c3dcae-9397-4856-b072-0ae340157bf9
title: Funzione D3DXAssembleShader (D3DX9Shader.h)
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
ms.openlocfilehash: 891281ebc3db970ca61132fe49ba98531ca1d879
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116049"
---
# <a name="d3dxassembleshader-function"></a><span data-ttu-id="0f901-103">Funzione D3DXAssembleShader</span><span class="sxs-lookup"><span data-stu-id="0f901-103">D3DXAssembleShader function</span></span>

<span data-ttu-id="0f901-104">Assemblare uno shader.</span><span class="sxs-lookup"><span data-stu-id="0f901-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f901-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f901-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="0f901-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f901-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f901-107">*pSrcData* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0f901-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f901-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f901-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0f901-109">Puntatore a un buffer di memoria che contiene i dati dello shader.</span><span class="sxs-lookup"><span data-stu-id="0f901-109">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="0f901-110">*SrcDataLen* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0f901-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f901-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f901-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0f901-112">Lunghezza dei dati dell'effetto, in byte.</span><span class="sxs-lookup"><span data-stu-id="0f901-112">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0f901-113">*pDefines* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0f901-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f901-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="0f901-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="0f901-115">Matrice facoltativa con terminazione **NULL** di [**strutture D3DXMACRO.**](d3dxmacro.md)</span><span class="sxs-lookup"><span data-stu-id="0f901-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="0f901-116">Questo valore può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="0f901-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0f901-117">*pInclude* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0f901-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f901-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="0f901-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="0f901-119">Puntatore a interfaccia [**facoltativo, ID3DXInclude,**](id3dxinclude.md)da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="0f901-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="0f901-120">Se questo valore è **NULL,** le include verranno rispettate durante la compilazione da un file o causeranno un errore durante la compilazione \# da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="0f901-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="0f901-121">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0f901-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f901-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f901-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0f901-123">Opzioni di compilazione identificate da vari flag.</span><span class="sxs-lookup"><span data-stu-id="0f901-123">Compile options identified by various flags.</span></span> <span data-ttu-id="0f901-124">Il compilatore HLSL Direct3D 10 è ora l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0f901-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="0f901-125">Per [informazioni dettagliate, vedere Flag D3DXSHADER.](d3dxshader-flags.md)</span><span class="sxs-lookup"><span data-stu-id="0f901-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="0f901-126">*ppShader* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="0f901-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f901-127">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f901-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0f901-128">Restituisce un buffer contenente lo shader creato.</span><span class="sxs-lookup"><span data-stu-id="0f901-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="0f901-129">Questo buffer contiene il codice shader compilato, nonché le informazioni sulle tabelle di debug e simboli incorporate.</span><span class="sxs-lookup"><span data-stu-id="0f901-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="0f901-130">*ppErrorMsgs* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="0f901-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f901-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f901-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0f901-132">Restituisce un buffer contenente un elenco di errori e avvisi rilevati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="0f901-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="0f901-133">Si tratta degli stessi messaggi visualizzati dal debugger durante l'esecuzione in modalità di debug.</span><span class="sxs-lookup"><span data-stu-id="0f901-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="0f901-134">Questo valore può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="0f901-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f901-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f901-135">Return value</span></span>

<span data-ttu-id="0f901-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0f901-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0f901-137">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0f901-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0f901-138">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0f901-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f901-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f901-139">Requirements</span></span>



| <span data-ttu-id="0f901-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f901-140">Requirement</span></span> | <span data-ttu-id="0f901-141">Valore</span><span class="sxs-lookup"><span data-stu-id="0f901-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f901-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f901-142">Header</span></span><br/>  | <dl> <span data-ttu-id="0f901-143"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="0f901-143"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0f901-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="0f901-144">Library</span></span><br/> | <dl> <span data-ttu-id="0f901-145"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f901-145"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0f901-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f901-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f901-147">Funzioni shader</span><span class="sxs-lookup"><span data-stu-id="0f901-147">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="0f901-148">**D3DXAssembleShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="0f901-148">**D3DXAssembleShaderFromFile**</span></span>](d3dxassembleshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="0f901-149">**D3DXAssembleShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="0f901-149">**D3DXAssembleShaderFromResource**</span></span>](d3dxassembleshaderfromresource.md)
</dt> </dl>

 

 
