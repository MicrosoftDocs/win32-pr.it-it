---
description: Crea un compilatore di effetti dalla descrizione di un effetto ASCII.
ms.assetid: 96e883f4-4055-4b8b-940a-164bbf893af4
title: Funzione D3DXCreateEffectCompiler (D3DX9Effect. h)
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
ms.openlocfilehash: 513b11ba12abe05126c122f8bc9bfcfa978df3fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762281"
---
# <a name="d3dxcreateeffectcompiler-function"></a><span data-ttu-id="b7dfd-103">D3DXCreateEffectCompiler (funzione)</span><span class="sxs-lookup"><span data-stu-id="b7dfd-103">D3DXCreateEffectCompiler function</span></span>

<span data-ttu-id="b7dfd-104">Crea un compilatore di effetti dalla descrizione di un effetto ASCII.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7dfd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b7dfd-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="b7dfd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b7dfd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7dfd-107">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7dfd-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7dfd-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7dfd-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7dfd-109">Puntatore a un buffer contenente una descrizione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-109">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="b7dfd-110">*SrcDataLen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7dfd-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7dfd-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7dfd-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7dfd-112">Lunghezza, in byte, dei dati effettivi.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-112">Length, in bytes, of the effect data.</span></span>

</dd> <dt>

<span data-ttu-id="b7dfd-113">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7dfd-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7dfd-114">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="b7dfd-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="b7dfd-115">Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) che descrivono le definizioni del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-115">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="b7dfd-116">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b7dfd-117">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7dfd-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7dfd-118">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="b7dfd-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="b7dfd-119">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="b7dfd-120">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="b7dfd-121">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b7dfd-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7dfd-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b7dfd-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b7dfd-123">Opzioni di compilazione identificate da vari flag (vedere [flag D3DXSHADER](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="b7dfd-123">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="b7dfd-124">Il compilatore Direct3D 10 HLSL è ora il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="b7dfd-125">Per informazioni dettagliate, vedere [strumento del compilatore di effetti](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="b7dfd-125">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="b7dfd-126">*ppEffectCompiler* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b7dfd-126">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7dfd-127">Tipo: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="b7dfd-127">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="b7dfd-128">Indirizzo di un puntatore a un'interfaccia [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) contenente il compilatore di effetti.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-128">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="b7dfd-129">*ppParseErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b7dfd-129">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7dfd-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b7dfd-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="b7dfd-131">Indirizzo di un puntatore a un'interfaccia [**ID3DXBuffer**](id3dxbuffer.md) contenente i messaggi di errore che si sono verificati durante la compilazione.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="b7dfd-132">Questo parametro può essere impostato su **null** per ignorare i messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-132">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7dfd-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b7dfd-133">Return value</span></span>

<span data-ttu-id="b7dfd-134">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b7dfd-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b7dfd-135">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b7dfd-136">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="b7dfd-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7dfd-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7dfd-137">Requirements</span></span>



| <span data-ttu-id="b7dfd-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7dfd-138">Requirement</span></span> | <span data-ttu-id="b7dfd-139">Valore</span><span class="sxs-lookup"><span data-stu-id="b7dfd-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7dfd-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7dfd-140">Header</span></span><br/>  | <dl> <span data-ttu-id="b7dfd-141"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7dfd-141"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b7dfd-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="b7dfd-142">Library</span></span><br/> | <dl> <span data-ttu-id="b7dfd-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7dfd-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b7dfd-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7dfd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7dfd-145">Funzioni effetto</span><span class="sxs-lookup"><span data-stu-id="b7dfd-145">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="b7dfd-146">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="b7dfd-146">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="b7dfd-147">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="b7dfd-147">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
