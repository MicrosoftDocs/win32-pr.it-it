---
description: "Funzione D3DXCreateEffectCompiler: crea un compilatore di effetti da una descrizione dell'effetto ASCII."
ms.assetid: 96e883f4-4055-4b8b-940a-164bbf893af4
title: Funzione D3DXCreateEffectCompiler (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompiler
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 38ab58ed15609d468d25f4406353448e4fd6adb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115769"
---
# <a name="d3dxcreateeffectcompiler-function"></a><span data-ttu-id="7a22b-103">Funzione D3DXCreateEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="7a22b-103">D3DXCreateEffectCompiler function</span></span>

<span data-ttu-id="7a22b-104">Crea un compilatore di effetti da una descrizione dell'effetto ASCII.</span><span class="sxs-lookup"><span data-stu-id="7a22b-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a22b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a22b-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompiler(
  _In_        LPCSTR               pSrcData,
  _In_        UINT                 SrcDataLen,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="7a22b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a22b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a22b-107">*pSrcData* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7a22b-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a22b-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a22b-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7a22b-109">Puntatore a un buffer contenente una descrizione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="7a22b-109">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="7a22b-110">*SrcDataLen* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7a22b-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a22b-111">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a22b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7a22b-112">Lunghezza, in byte, dei dati dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="7a22b-112">Length, in bytes, of the effect data.</span></span>

</dd> <dt>

<span data-ttu-id="7a22b-113">*pDefines* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7a22b-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a22b-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="7a22b-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="7a22b-115">Matrice facoltativa **con terminazione NULL** di [**strutture D3DXMACRO**](d3dxmacro.md) che descrivono le definizioni del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="7a22b-115">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="7a22b-116">Questo valore può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="7a22b-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7a22b-117">*pInclude* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7a22b-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a22b-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="7a22b-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="7a22b-119">Puntatore a interfaccia [**facoltativo, ID3DXInclude,**](id3dxinclude.md)da usare per la gestione \# delle direttive include.</span><span class="sxs-lookup"><span data-stu-id="7a22b-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="7a22b-120">Se questo valore è **NULL,** include verrà rispettato durante la compilazione da un file o causerà un errore durante la compilazione \# da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="7a22b-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="7a22b-121">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7a22b-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a22b-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a22b-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7a22b-123">Opzioni di compilazione identificate da diversi flag (vedere [Flag D3DXSHADER).](d3dxshader-flags.md)</span><span class="sxs-lookup"><span data-stu-id="7a22b-123">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="7a22b-124">Il compilatore HLSL Direct3D 10 è ora l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7a22b-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="7a22b-125">Per [informazioni dettagliate, vedere Effect-Compiler Tool](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="7a22b-125">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="7a22b-126">*ppEffectCompiler* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="7a22b-126">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a22b-127">Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="7a22b-127">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="7a22b-128">Indirizzo di un puntatore a [**un'interfaccia ID3DXEffectCompiler**](id3dxeffectcompiler.md) contenente il compilatore dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="7a22b-128">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="7a22b-129">*ppParseErrors* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="7a22b-129">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a22b-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7a22b-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7a22b-131">Indirizzo di un puntatore a [**un'interfaccia ID3DXBuffer**](id3dxbuffer.md) contenente eventuali messaggi di errore che si sono verificati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="7a22b-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="7a22b-132">Questo parametro può essere impostato su **NULL per ignorare** i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="7a22b-132">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a22b-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a22b-133">Return value</span></span>

<span data-ttu-id="7a22b-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7a22b-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7a22b-135">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7a22b-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7a22b-136">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7a22b-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a22b-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a22b-137">Requirements</span></span>



| <span data-ttu-id="7a22b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a22b-138">Requirement</span></span> | <span data-ttu-id="7a22b-139">Valore</span><span class="sxs-lookup"><span data-stu-id="7a22b-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a22b-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a22b-140">Header</span></span><br/>  | <dl> <span data-ttu-id="7a22b-141"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="7a22b-141"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7a22b-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="7a22b-142">Library</span></span><br/> | <dl> <span data-ttu-id="7a22b-143"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a22b-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7a22b-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a22b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a22b-145">Funzioni di effetto</span><span class="sxs-lookup"><span data-stu-id="7a22b-145">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="7a22b-146">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="7a22b-146">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="7a22b-147">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="7a22b-147">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
