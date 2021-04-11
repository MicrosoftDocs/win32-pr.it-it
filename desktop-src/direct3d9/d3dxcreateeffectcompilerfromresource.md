---
description: Crea un ID3DXEffectCompiler da una descrizione dell'effetto ASCII.
ms.assetid: 041e0a3f-3dc6-4cc3-8380-d4a79a3f647a
title: Funzione D3DXCreateEffectCompilerFromResource (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1a3dabe0a2690c84e125af6d321397cbe3765f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235067"
---
# <a name="d3dxcreateeffectcompilerfromresource-function"></a><span data-ttu-id="b1acc-103">D3DXCreateEffectCompilerFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="b1acc-103">D3DXCreateEffectCompilerFromResource function</span></span>

<span data-ttu-id="b1acc-104">Crea un [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) da una descrizione dell'effetto ASCII.</span><span class="sxs-lookup"><span data-stu-id="b1acc-104">Creates an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1acc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1acc-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompilerFromResource(
  _In_        HMODULE              hSrcModule,
  _In_        LPCTSTR              pSrcResource,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="b1acc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1acc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1acc-107">*hSrcModule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1acc-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1acc-108">Tipo: **[ **hmodule**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1acc-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1acc-109">Handle per un modulo che contiene la descrizione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b1acc-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="b1acc-110">Se questo parametro è **null**, verrà usato il modulo corrente.</span><span class="sxs-lookup"><span data-stu-id="b1acc-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="b1acc-111">*pSrcResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1acc-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1acc-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1acc-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1acc-113">Puntatore alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="b1acc-113">Pointer to the resource.</span></span> <span data-ttu-id="b1acc-114">Questo parametro supporta sia stringhe Unicode che ANSI.</span><span class="sxs-lookup"><span data-stu-id="b1acc-114">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="b1acc-115">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b1acc-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b1acc-116">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1acc-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1acc-117">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="b1acc-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="b1acc-118">Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) che descrivono le definizioni del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="b1acc-118">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="b1acc-119">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="b1acc-119">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b1acc-120">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1acc-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1acc-121">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="b1acc-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="b1acc-122">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="b1acc-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="b1acc-123">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="b1acc-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="b1acc-124">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1acc-124">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1acc-125">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1acc-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1acc-126">Opzioni di compilazione identificate da vari flag (vedere [flag D3DXSHADER](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="b1acc-126">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="b1acc-127">Il compilatore Direct3D 10 HLSL è ora il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b1acc-127">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="b1acc-128">Per informazioni dettagliate, vedere [strumento del compilatore di effetti](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="b1acc-128">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="b1acc-129">*ppEffectCompiler* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b1acc-129">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1acc-130">Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1acc-130">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="b1acc-131">Indirizzo di un puntatore a un'interfaccia [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) contenente il compilatore di effetti.</span><span class="sxs-lookup"><span data-stu-id="b1acc-131">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="b1acc-132">*ppParseErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b1acc-132">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1acc-133">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b1acc-133">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b1acc-134">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) contenente tutti i messaggi di errore verificatisi durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="b1acc-134">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="b1acc-135">Questo parametro può essere impostato su **null** per ignorare i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="b1acc-135">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1acc-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1acc-136">Return value</span></span>

<span data-ttu-id="b1acc-137">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1acc-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1acc-138">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b1acc-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b1acc-139">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="b1acc-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1acc-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1acc-140">Remarks</span></span>

<span data-ttu-id="b1acc-141">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="b1acc-141">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="b1acc-142">In caso contrario, il tipo di dati LPCTSTR viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="b1acc-142">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="b1acc-143">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="b1acc-143">The compiler setting also determines the function version.</span></span> <span data-ttu-id="b1acc-144">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateEffectCompilerFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="b1acc-144">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromResourceW.</span></span> <span data-ttu-id="b1acc-145">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateEffectCompilerFromResourceA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="b1acc-145">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1acc-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1acc-146">Requirements</span></span>



| <span data-ttu-id="b1acc-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1acc-147">Requirement</span></span> | <span data-ttu-id="b1acc-148">Valore</span><span class="sxs-lookup"><span data-stu-id="b1acc-148">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1acc-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1acc-149">Header</span></span><br/>  | <dl> <span data-ttu-id="b1acc-150"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1acc-150"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b1acc-151">Libreria</span><span class="sxs-lookup"><span data-stu-id="b1acc-151">Library</span></span><br/> | <dl> <span data-ttu-id="b1acc-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1acc-152"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b1acc-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1acc-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1acc-154">Funzioni effetto</span><span class="sxs-lookup"><span data-stu-id="b1acc-154">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="b1acc-155">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="b1acc-155">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="b1acc-156">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="b1acc-156">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> </dl>

 

 
