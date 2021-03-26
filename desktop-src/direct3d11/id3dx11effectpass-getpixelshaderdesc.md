---
title: Metodo ID3DX11EffectPass GetPixelShaderDesc (D3dx11effect. h)
description: Ottenere una descrizione del pixel shader.
ms.assetid: 5772f197-7ac5-4492-9a41-eedb1a8b22c9
keywords:
- Metodo GetPixelShaderDesc Direct3D 11
- Metodo GetPixelShaderDesc Direct3D 11, interfaccia ID3DX11EffectPass
- Interfaccia ID3DX11EffectPass Direct3D 11, metodo GetPixelShaderDesc
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetPixelShaderDesc
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c04479a58eed0aa94616f0ffc092f17d52d9af4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982247"
---
# <a name="id3dx11effectpassgetpixelshaderdesc-method"></a><span data-ttu-id="a88bf-106">Metodo ID3DX11EffectPass:: GetPixelShaderDesc</span><span class="sxs-lookup"><span data-stu-id="a88bf-106">ID3DX11EffectPass::GetPixelShaderDesc method</span></span>

<span data-ttu-id="a88bf-107">Ottenere una descrizione del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="a88bf-107">Get a pixel-shader description.</span></span>

## <a name="syntax"></a><span data-ttu-id="a88bf-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a88bf-108">Syntax</span></span>


```C++
HRESULT GetPixelShaderDesc(
   D3DX11_PASS_SHADER_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="a88bf-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a88bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a88bf-110">*pDesc*</span><span class="sxs-lookup"><span data-stu-id="a88bf-110">*pDesc*</span></span> 
</dt> <dd>

<span data-ttu-id="a88bf-111">Tipo: **[ **D3DX11 \_ pass \_ shader \_ desc**](d3dx11-pass-shader-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="a88bf-111">Type: **[**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)\***</span></span>

<span data-ttu-id="a88bf-112">Puntatore a una descrizione di pixel shader (vedere [**D3DX11 \_ pass \_ shader \_ desc**](d3dx11-pass-shader-desc.md)).</span><span class="sxs-lookup"><span data-stu-id="a88bf-112">A pointer to a pixel-shader description (see [**D3DX11\_PASS\_SHADER\_DESC**](d3dx11-pass-shader-desc.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a88bf-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a88bf-113">Return value</span></span>

<span data-ttu-id="a88bf-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a88bf-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a88bf-115">Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a88bf-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a88bf-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a88bf-116">Remarks</span></span>

<span data-ttu-id="a88bf-117">Un passaggio di effetto può contenere le assegnazioni dello stato di rendering e le assegnazioni degli oggetti shader.</span><span class="sxs-lookup"><span data-stu-id="a88bf-117">An effect pass can contain render state assignments and shader object assignments.</span></span>

> [!Note]  
> <span data-ttu-id="a88bf-118">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="a88bf-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a88bf-119">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="a88bf-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a88bf-120">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a88bf-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a88bf-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a88bf-121">Requirements</span></span>



| <span data-ttu-id="a88bf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a88bf-122">Requirement</span></span> | <span data-ttu-id="a88bf-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a88bf-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a88bf-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a88bf-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a88bf-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a88bf-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a88bf-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="a88bf-126">Library</span></span><br/> | <dl> <span data-ttu-id="a88bf-127"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="a88bf-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a88bf-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a88bf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a88bf-129">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="a88bf-129">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

 





