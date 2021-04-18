---
description: Crea un compilatore di effetti dalla descrizione di un effetto ASCII.
ms.assetid: 87438a1e-4149-42ef-aa7a-9f0549eb7982
title: Funzione D3DXCreateEffectCompilerFromFile (D3DX9Effect. h)
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
ms.openlocfilehash: fe27683078f77d7d444bd3a763fc326e749f7517
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322904"
---
# <a name="d3dxcreateeffectcompilerfromfile-function"></a><span data-ttu-id="b6c24-103">D3DXCreateEffectCompilerFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="b6c24-103">D3DXCreateEffectCompilerFromFile function</span></span>

<span data-ttu-id="b6c24-104">Crea un compilatore di effetti dalla descrizione di un effetto ASCII.</span><span class="sxs-lookup"><span data-stu-id="b6c24-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c24-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6c24-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="b6c24-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6c24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6c24-107">*pSrcFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6c24-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c24-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6c24-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6c24-109">Puntatore al nome file.</span><span class="sxs-lookup"><span data-stu-id="b6c24-109">Pointer to the filename.</span></span> <span data-ttu-id="b6c24-110">Questo parametro supporta sia stringhe Unicode che ANSI.</span><span class="sxs-lookup"><span data-stu-id="b6c24-110">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="b6c24-111">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b6c24-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b6c24-112">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6c24-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c24-113">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="b6c24-113">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="b6c24-114">Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) che descrivono le definizioni del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="b6c24-114">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="b6c24-115">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="b6c24-115">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b6c24-116">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6c24-116">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c24-117">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="b6c24-117">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="b6c24-118">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="b6c24-118">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="b6c24-119">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="b6c24-119">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="b6c24-120">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b6c24-120">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c24-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b6c24-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b6c24-122">Opzioni di compilazione identificate da vari flag (vedere [flag D3DXSHADER](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="b6c24-122">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="b6c24-123">Il compilatore Direct3D 10 HLSL è ora il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b6c24-123">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="b6c24-124">Per informazioni dettagliate, vedere [strumento del compilatore di effetti](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="b6c24-124">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="b6c24-125">*ppEffectCompiler* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b6c24-125">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c24-126">Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="b6c24-126">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="b6c24-127">Indirizzo di un puntatore a un'interfaccia [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) contenente il compilatore di effetti.</span><span class="sxs-lookup"><span data-stu-id="b6c24-127">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="b6c24-128">*ppParseErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b6c24-128">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6c24-129">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b6c24-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b6c24-130">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) contenente tutti i messaggi di errore verificatisi durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="b6c24-130">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="b6c24-131">Questo parametro può essere impostato su **null** per ignorare i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="b6c24-131">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6c24-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6c24-132">Return value</span></span>

<span data-ttu-id="b6c24-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b6c24-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b6c24-134">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b6c24-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b6c24-135">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="b6c24-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6c24-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6c24-136">Remarks</span></span>

<span data-ttu-id="b6c24-137">Se le impostazioni del compilatore richiedono Unicode, il tipo di dati LPCTSTR viene risolto in LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="b6c24-137">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="b6c24-138">In caso contrario, il tipo di dati LPCTSTR viene risolto in LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="b6c24-138">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="b6c24-139">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="b6c24-139">The compiler setting also determines the function version.</span></span> <span data-ttu-id="b6c24-140">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXCreateEffectCompilerFromFileW.</span><span class="sxs-lookup"><span data-stu-id="b6c24-140">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromFileW.</span></span> <span data-ttu-id="b6c24-141">In caso contrario, la chiamata di funzione viene risolta in D3DXCreateEffectCompilerFromFileA perché vengono utilizzate le stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="b6c24-141">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6c24-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6c24-142">Requirements</span></span>



| <span data-ttu-id="b6c24-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6c24-143">Requirement</span></span> | <span data-ttu-id="b6c24-144">Valore</span><span class="sxs-lookup"><span data-stu-id="b6c24-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c24-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6c24-145">Header</span></span><br/>  | <dl> <span data-ttu-id="b6c24-146"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6c24-146"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b6c24-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="b6c24-147">Library</span></span><br/> | <dl> <span data-ttu-id="b6c24-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6c24-148"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b6c24-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6c24-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c24-150">Funzioni effetto</span><span class="sxs-lookup"><span data-stu-id="b6c24-150">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="b6c24-151">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="b6c24-151">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="b6c24-152">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="b6c24-152">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
