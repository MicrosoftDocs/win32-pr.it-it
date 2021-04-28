---
description: "Funzione D3DXCreateEffectCompilerFromFile: crea un compilatore di effetti da una descrizione dell'effetto ASCII."
ms.assetid: 87438a1e-4149-42ef-aa7a-9f0549eb7982
title: Funzione D3DXCreateEffectCompilerFromFile (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 0c054b31b1ab70d1378c794be13058204b994ee2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087979"
---
# <a name="d3dxcreateeffectcompilerfromfile-function"></a><span data-ttu-id="cc909-103">Funzione D3DXCreateEffectCompilerFromFile</span><span class="sxs-lookup"><span data-stu-id="cc909-103">D3DXCreateEffectCompilerFromFile function</span></span>

<span data-ttu-id="cc909-104">Crea un compilatore di effetti da una descrizione dell'effetto ASCII.</span><span class="sxs-lookup"><span data-stu-id="cc909-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc909-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc909-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompilerFromFile(
  _In_        LPCTSTR              pSrcFile,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="cc909-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc909-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc909-107">*pSrcFile* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="cc909-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc909-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc909-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc909-109">Puntatore al nome file.</span><span class="sxs-lookup"><span data-stu-id="cc909-109">Pointer to the filename.</span></span> <span data-ttu-id="cc909-110">Questo parametro supporta entrambe le stringhe Unicode e ANSI.</span><span class="sxs-lookup"><span data-stu-id="cc909-110">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="cc909-111">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="cc909-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="cc909-112">*pDefines* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="cc909-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc909-113">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="cc909-113">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="cc909-114">Matrice facoltativa **con terminazione NULL** di [**strutture D3DXMACRO**](d3dxmacro.md) che descrivono le definizioni del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="cc909-114">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="cc909-115">Questo valore può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="cc909-115">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cc909-116">*pInclude* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="cc909-116">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc909-117">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="cc909-117">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="cc909-118">Puntatore a interfaccia [**facoltativo, ID3DXInclude,**](id3dxinclude.md)da usare per la gestione \# delle direttive include.</span><span class="sxs-lookup"><span data-stu-id="cc909-118">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="cc909-119">Se questo valore è **NULL,** include verrà rispettato durante la compilazione da un file o causerà un errore durante la compilazione \# da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="cc909-119">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="cc909-120">*Flag* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="cc909-120">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc909-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cc909-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="cc909-122">Opzioni di compilazione identificate da vari flag (vedere [Flag D3DXSHADER](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="cc909-122">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="cc909-123">Il compilatore HLSL Direct3D 10 è ora l'impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="cc909-123">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="cc909-124">Per [informazioni dettagliate, vedere Effect-Compiler Tool](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="cc909-124">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="cc909-125">*ppEffectCompiler* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="cc909-125">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc909-126">Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc909-126">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="cc909-127">Indirizzo di un puntatore a [**un'interfaccia ID3DXEffectCompiler,**](id3dxeffectcompiler.md) contenente il compilatore dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="cc909-127">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="cc909-128">*ppParseErrors* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="cc909-128">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc909-129">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="cc909-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="cc909-130">Indirizzo di un puntatore a [**un'interfaccia ID3DXBuffer,**](id3dxbuffer.md) contenente eventuali messaggi di errore che si sono verificati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="cc909-130">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="cc909-131">Questo parametro può essere impostato su **NULL per ignorare** i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="cc909-131">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc909-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc909-132">Return value</span></span>

<span data-ttu-id="cc909-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cc909-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cc909-134">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cc909-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cc909-135">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="cc909-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc909-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc909-136">Remarks</span></span>

<span data-ttu-id="cc909-137">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="cc909-137">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="cc909-138">In caso contrario, il tipo di dati LPCTSTR viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="cc909-138">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="cc909-139">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="cc909-139">The compiler setting also determines the function version.</span></span> <span data-ttu-id="cc909-140">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateEffectCompilerFromFileW.</span><span class="sxs-lookup"><span data-stu-id="cc909-140">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromFileW.</span></span> <span data-ttu-id="cc909-141">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateEffectCompilerFromFileA perché vengono usate stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="cc909-141">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc909-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc909-142">Requirements</span></span>



| <span data-ttu-id="cc909-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc909-143">Requirement</span></span> | <span data-ttu-id="cc909-144">Valore</span><span class="sxs-lookup"><span data-stu-id="cc909-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc909-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc909-145">Header</span></span><br/>  | <dl> <span data-ttu-id="cc909-146"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="cc909-146"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="cc909-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="cc909-147">Library</span></span><br/> | <dl> <span data-ttu-id="cc909-148"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc909-148"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cc909-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc909-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc909-150">Funzioni di effetto</span><span class="sxs-lookup"><span data-stu-id="cc909-150">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="cc909-151">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="cc909-151">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="cc909-152">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="cc909-152">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
