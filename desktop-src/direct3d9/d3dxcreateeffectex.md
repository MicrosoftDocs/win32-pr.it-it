---
description: Crea un effetto da una descrizione di effetto ASCII o binario. Questa funzione è una versione estesa di D3DXCreateEffect che consente a un'applicazione di controllare quali parametri vengono ignorati dal sistema di effetti.
ms.assetid: b08f727e-6061-4e78-8243-08c4ccab342d
title: Funzione D3DXCreateEffectEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 979b09f852e692b4c25414607f79cd8792342755
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322903"
---
# <a name="d3dxcreateeffectex-function"></a><span data-ttu-id="7be1c-104">D3DXCreateEffectEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="7be1c-104">D3DXCreateEffectEx function</span></span>

<span data-ttu-id="7be1c-105">Crea un effetto da una descrizione di effetto ASCII o binario.</span><span class="sxs-lookup"><span data-stu-id="7be1c-105">Creates an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="7be1c-106">Questa funzione è una versione estesa di [**D3DXCreateEffect**](d3dxcreateeffect.md) che consente a un'applicazione di controllare quali parametri vengono ignorati dal sistema di effetti.</span><span class="sxs-lookup"><span data-stu-id="7be1c-106">This function is an extended version of [**D3DXCreateEffect**](d3dxcreateeffect.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="7be1c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7be1c-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="7be1c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7be1c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7be1c-109">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7be1c-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7be1c-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7be1c-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7be1c-111">Puntatore al dispositivo che creerà l'effetto.</span><span class="sxs-lookup"><span data-stu-id="7be1c-111">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="7be1c-112">Vedere [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="7be1c-112">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="7be1c-113">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7be1c-113">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7be1c-114">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7be1c-114">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7be1c-115">Puntatore a un buffer contenente una descrizione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="7be1c-115">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="7be1c-116">*SrcDataLen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7be1c-116">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7be1c-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7be1c-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7be1c-118">Lunghezza in byte dei dati effettivi.</span><span class="sxs-lookup"><span data-stu-id="7be1c-118">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7be1c-119">*pDefines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7be1c-119">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7be1c-120">Tipo: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="7be1c-120">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="7be1c-121">Matrice facoltativa con terminazione **null** di strutture [**D3DXMACRO**](d3dxmacro.md) che descrivono le definizioni del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="7be1c-121">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="7be1c-122">Questo valore può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="7be1c-122">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7be1c-123">*pInclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7be1c-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7be1c-124">Tipo: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="7be1c-124">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="7be1c-125">Puntatore a interfaccia facoltativo, [**ID3DXInclude**](id3dxinclude.md), da usare per la gestione delle \# direttive include.</span><span class="sxs-lookup"><span data-stu-id="7be1c-125">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="7be1c-126">Se questo valore è **null**, le \# inclusioni verranno rispettate durante la compilazione da un file o genereranno un errore quando vengono compilate da una risorsa o da una memoria.</span><span class="sxs-lookup"><span data-stu-id="7be1c-126">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="7be1c-127">*pSkipConstants* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7be1c-127">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7be1c-128">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7be1c-128">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7be1c-129">Una stringa di parametri effetti che verrà ignorata dal sistema di effetti.</span><span class="sxs-lookup"><span data-stu-id="7be1c-129">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="7be1c-130">La stringa deve essere con terminazione **null** e deve contenere il nome di ogni costante gestita dall'applicazione separata da un punto e virgola.</span><span class="sxs-lookup"><span data-stu-id="7be1c-130">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="7be1c-131">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7be1c-131">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7be1c-132">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7be1c-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7be1c-133">Se *pSrcData* contiene un effetto di testo, i flag possono essere una combinazione di flag [D3DXSHADER](d3dxshader-flags.md) e flag [D3DXFX](d3dxfx.md) ; in caso contrario, *pSrcData* contiene un effetto binario e gli unici flag rispettati sono i flag D3DXFX.</span><span class="sxs-lookup"><span data-stu-id="7be1c-133">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="7be1c-134">Il compilatore Direct3D 10 HLSL è ora il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="7be1c-134">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="7be1c-135">Per informazioni dettagliate, vedere [strumento del compilatore di effetti](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="7be1c-135">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="7be1c-136">*pPool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7be1c-136">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7be1c-137">Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="7be1c-137">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="7be1c-138">Puntatore a un oggetto [**ID3DXEffectPool**](id3dxeffectpool.md) da utilizzare per i parametri condivisi.</span><span class="sxs-lookup"><span data-stu-id="7be1c-138">Pointer to an [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="7be1c-139">Se questo valore è **null**, non verrà condiviso alcun parametro.</span><span class="sxs-lookup"><span data-stu-id="7be1c-139">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="7be1c-140">*ppEffect* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7be1c-140">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7be1c-141">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="7be1c-141">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="7be1c-142">Restituisce un puntatore a un'interfaccia [**ID3DXEffect**](id3dxeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="7be1c-142">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7be1c-143">*ppCompilationErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7be1c-143">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7be1c-144">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7be1c-144">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7be1c-145">Restituisce un buffer contenente un elenco di errori di compilazione.</span><span class="sxs-lookup"><span data-stu-id="7be1c-145">Returns a buffer containing a list of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7be1c-146">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7be1c-146">Return value</span></span>

<span data-ttu-id="7be1c-147">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7be1c-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7be1c-148">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7be1c-148">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7be1c-149">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="7be1c-149">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7be1c-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="7be1c-150">Remarks</span></span>

<span data-ttu-id="7be1c-151">Questa funzione è una versione estesa di [**D3DXCreateEffect**](d3dxcreateeffect.md) che consente a un'applicazione di specificare quali costanti di effetto verranno gestite dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7be1c-151">This function is an extended version of [**D3DXCreateEffect**](d3dxcreateeffect.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="7be1c-152">Una costante gestita dall'applicazione viene ignorata dal sistema di effetti.</span><span class="sxs-lookup"><span data-stu-id="7be1c-152">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="7be1c-153">In altre condizioni, l'applicazione è responsabile dell'inizializzazione della costante, nonché del salvataggio e del ripristino dello stato quando appropriato.</span><span class="sxs-lookup"><span data-stu-id="7be1c-153">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="7be1c-154">Questa funzione controlla ogni costante in pSkipConstants per vedere quanto segue:</span><span class="sxs-lookup"><span data-stu-id="7be1c-154">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="7be1c-155">È associato a un registro costante.</span><span class="sxs-lookup"><span data-stu-id="7be1c-155">It is bound to a constant register.</span></span>
-   <span data-ttu-id="7be1c-156">Viene usato solo nel codice shader HLSL.</span><span class="sxs-lookup"><span data-stu-id="7be1c-156">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="7be1c-157">Se una costante viene denominata nella stringa non presente nell'effetto, viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="7be1c-157">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7be1c-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7be1c-158">Requirements</span></span>



| <span data-ttu-id="7be1c-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="7be1c-159">Requirement</span></span> | <span data-ttu-id="7be1c-160">Valore</span><span class="sxs-lookup"><span data-stu-id="7be1c-160">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be1c-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7be1c-161">Header</span></span><br/>  | <dl> <span data-ttu-id="7be1c-162"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="7be1c-162"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7be1c-163">Libreria</span><span class="sxs-lookup"><span data-stu-id="7be1c-163">Library</span></span><br/> | <dl> <span data-ttu-id="7be1c-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7be1c-164"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7be1c-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7be1c-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7be1c-166">Funzioni effetto</span><span class="sxs-lookup"><span data-stu-id="7be1c-166">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="7be1c-167">**D3DXCreateEffectFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="7be1c-167">**D3DXCreateEffectFromFileEx**</span></span>](d3dxcreateeffectfromfileex.md)
</dt> <dt>

[<span data-ttu-id="7be1c-168">**D3DXCreateEffectFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="7be1c-168">**D3DXCreateEffectFromResourceEx**</span></span>](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
