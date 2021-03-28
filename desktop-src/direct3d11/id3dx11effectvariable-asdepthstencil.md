---
title: Metodo ID3DX11EffectVariable AsDepthStencil (D3dx11effect. h)
description: Ottenere una variabile di stencil Depth.
ms.assetid: 3526812b-6c43-492e-b529-12f61ecd20e3
keywords:
- Metodo AsDepthStencil Direct3D 11
- Metodo AsDepthStencil Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo AsDepthStencil
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsDepthStencil
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 980bd43f51d187252fab1872ba75d04f82820ef8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969402"
---
# <a name="id3dx11effectvariableasdepthstencil-method"></a><span data-ttu-id="2da0c-106">Metodo ID3DX11EffectVariable:: AsDepthStencil</span><span class="sxs-lookup"><span data-stu-id="2da0c-106">ID3DX11EffectVariable::AsDepthStencil method</span></span>

<span data-ttu-id="2da0c-107">Ottenere una variabile di stencil Depth.</span><span class="sxs-lookup"><span data-stu-id="2da0c-107">Get a depth-stencil variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="2da0c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2da0c-108">Syntax</span></span>


```C++
ID3DX11EffectDepthStencilVariable* AsDepthStencil();
```



## <a name="parameters"></a><span data-ttu-id="2da0c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2da0c-109">Parameters</span></span>

<span data-ttu-id="2da0c-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2da0c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2da0c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2da0c-111">Return value</span></span>

<span data-ttu-id="2da0c-112">Tipo: **[ **ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="2da0c-112">Type: **[**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md)\***</span></span>

<span data-ttu-id="2da0c-113">Puntatore a una variabile di stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="2da0c-113">A pointer to a depth-stencil variable.</span></span> <span data-ttu-id="2da0c-114">Vedere [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md).</span><span class="sxs-lookup"><span data-stu-id="2da0c-114">See [**ID3DX11EffectDepthStencilVariable**](id3dx11effectdepthstencilvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2da0c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="2da0c-115">Remarks</span></span>

<span data-ttu-id="2da0c-116">AsDepthStencil restituisce una versione della variabile Effect specializzata in una variabile di stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="2da0c-116">AsDepthStencil returns a version of the effect variable that has been specialized to a depth-stencil variable.</span></span> <span data-ttu-id="2da0c-117">Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile Effect non contiene dati di stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="2da0c-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain depth-stencil data.</span></span>

<span data-ttu-id="2da0c-118">Per verificare la validità dell'oggetto restituito, le applicazioni possono chiamare [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="2da0c-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="2da0c-119">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="2da0c-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="2da0c-120">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="2da0c-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="2da0c-121">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="2da0c-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2da0c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2da0c-122">Requirements</span></span>



| <span data-ttu-id="2da0c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2da0c-123">Requirement</span></span> | <span data-ttu-id="2da0c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="2da0c-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2da0c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2da0c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2da0c-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2da0c-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="2da0c-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="2da0c-127">Library</span></span><br/> | <dl> <span data-ttu-id="2da0c-128"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="2da0c-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2da0c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2da0c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da0c-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="2da0c-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





