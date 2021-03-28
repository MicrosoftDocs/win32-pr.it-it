---
title: Metodo ID3DX11EffectPass GetComputeShaderDesc (D3dx11effect. h)
description: Ottenere una descrizione del compute shader.
ms.assetid: 9c3a702f-2016-4b1a-a832-d1bb968aec2d
keywords:
- Metodo GetComputeShaderDesc Direct3D 11
- Metodo GetComputeShaderDesc Direct3D 11, interfaccia ID3DX11EffectPass
- Interfaccia ID3DX11EffectPass Direct3D 11, metodo GetComputeShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetComputeShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21cc13699553b0da60498209ddffd31a56607809
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969465"
---
# <a name="id3dx11effectpassgetcomputeshaderdesc-method"></a><span data-ttu-id="18bf0-106">Metodo ID3DX11EffectPass:: GetComputeShaderDesc</span><span class="sxs-lookup"><span data-stu-id="18bf0-106">ID3DX11EffectPass::GetComputeShaderDesc method</span></span>

<span data-ttu-id="18bf0-107">Ottenere una descrizione del compute shader.</span><span class="sxs-lookup"><span data-stu-id="18bf0-107">Get a compute-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="18bf0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18bf0-108">Syntax</span></span>


```C++
HRESULT GetComputeShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="18bf0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="18bf0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18bf0-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="18bf0-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="18bf0-111">Tipo: **[ **D3DX11 \_ pass \_ shader \_ desc**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="18bf0-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="18bf0-112">Puntatore a una descrizione del compute shader (vedere [**D3DX11 \_ pass \_ shader \_ desc**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="18bf0-112">A pointer to a compute-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18bf0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18bf0-113">Return value</span></span>

<span data-ttu-id="18bf0-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="18bf0-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="18bf0-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="18bf0-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="18bf0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="18bf0-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="18bf0-117">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="18bf0-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="18bf0-118">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="18bf0-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="18bf0-119">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="18bf0-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="18bf0-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18bf0-120">Requirements</span></span>



| <span data-ttu-id="18bf0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="18bf0-121">Requirement</span></span> | <span data-ttu-id="18bf0-122">Valore</span><span class="sxs-lookup"><span data-stu-id="18bf0-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18bf0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18bf0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="18bf0-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="18bf0-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="18bf0-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="18bf0-125">Library</span></span><br/> | <dl> <span data-ttu-id="18bf0-126"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="18bf0-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18bf0-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18bf0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18bf0-128">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="18bf0-128">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





