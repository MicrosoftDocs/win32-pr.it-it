---
description: Creare un effetto dalla descrizione di un effetto ASCII o binario.
ms.assetid: 1cbd91f2-3cda-4770-a3c5-b1e6702628d1
title: Funzione D3DXCreateEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 3d5ac013617368ba4d702815d79aa411ea2988b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322905"
---
# <a name="d3dxcreateeffect-function"></a><span data-ttu-id="4a65f-103">D3DXCreateEffect (funzione)</span><span class="sxs-lookup"><span data-stu-id="4a65f-103">D3DXCreateEffect function</span></span>

<span data-ttu-id="4a65f-104">Creare un effetto dalla descrizione di un effetto ASCII o binario.</span><span class="sxs-lookup"><span data-stu-id="4a65f-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a65f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a65f-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="4a65f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a65f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a65f-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a65f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a65f-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="4a65f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="4a65f-109">Puntatore al dispositivo che creerà l'effetto.</span><span class="sxs-lookup"><span data-stu-id="4a65f-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="4a65f-110">Vedere [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="4a65f-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="4a65f-111">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a65f-111">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a65f-112">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a65f-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4a65f-113">Puntatore a un buffer contenente una descrizione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="4a65f-113">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="4a65f-114">*SrcDataLen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a65f-114">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a65f-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a65f-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4a65f-116">Lunghezza in byte dei dati effettivi.</span><span class="sxs-lookup"><span data-stu-id="4a65f-116">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4a65f-117">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a65f-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a65f-118">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="4a65f-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="4a65f-119">Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) che descrivono le definizioni del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="4a65f-119">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="4a65f-120">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="4a65f-120">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4a65f-121">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a65f-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a65f-122">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="4a65f-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="4a65f-123">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="4a65f-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="4a65f-124">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="4a65f-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="4a65f-125">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a65f-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a65f-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4a65f-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4a65f-127">Se *pSrcData* contiene un effetto di testo, i flag possono essere una combinazione di flag [D3DXSHADER](d3dxshader-flags.md) e flag [D3DXFX](d3dxfx.md) ; in caso contrario, *pSrcData* contiene un effetto binario e gli unici flag rispettati sono i flag D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="4a65f-127">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="4a65f-128">Il compilatore Direct3D 10 HLSL è ora il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="4a65f-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="4a65f-129">Per informazioni dettagliate, vedere [strumento del compilatore di effetti](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="4a65f-129">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="4a65f-130">*pPool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a65f-130">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a65f-131">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="4a65f-131">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="4a65f-132">Puntatore a un oggetto [**ID3DXEffectPool**](id3dxeffectpool.md) da utilizzare per i parametri condivisi.</span><span class="sxs-lookup"><span data-stu-id="4a65f-132">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="4a65f-133">Se questo valore è **null**, non verrà condiviso alcun parametro.</span><span class="sxs-lookup"><span data-stu-id="4a65f-133">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="4a65f-134">*ppEffect* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4a65f-134">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a65f-135">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="4a65f-135">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="4a65f-136">Restituisce un puntatore a un'interfaccia [**ID3DXEffect**](id3dxeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="4a65f-136">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="4a65f-137">*ppCompilationErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4a65f-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a65f-138">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="4a65f-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="4a65f-139">Restituisce un buffer contenente un elenco di errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="4a65f-139">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a65f-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a65f-140">Return value</span></span>

<span data-ttu-id="4a65f-141">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4a65f-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4a65f-142">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4a65f-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4a65f-143">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="4a65f-143">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a65f-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a65f-144">Requirements</span></span>



| <span data-ttu-id="4a65f-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a65f-145">Requirement</span></span> | <span data-ttu-id="4a65f-146">Valore</span><span class="sxs-lookup"><span data-stu-id="4a65f-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a65f-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4a65f-147">Header</span></span><br/>  | <dl> <span data-ttu-id="4a65f-148"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a65f-148"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="4a65f-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="4a65f-149">Library</span></span><br/> | <dl> <span data-ttu-id="4a65f-150"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a65f-150"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4a65f-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a65f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a65f-152">Funzioni effetto</span><span class="sxs-lookup"><span data-stu-id="4a65f-152">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="4a65f-153">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="4a65f-153">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="4a65f-154">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="4a65f-154">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
