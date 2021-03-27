---
title: Metodo ID3DX11EffectVariable AsBlend (D3dx11effect. h)
description: Ottenere una variabile Effect-Blend.
ms.assetid: e9670d13-e006-408b-9cdf-352bcfa66a52
keywords:
- Metodo AsBlend Direct3D 11
- Metodo AsBlend Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo AsBlend
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsBlend
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f7e3d09a1299d00482e9a5cfbb75f563d4bba5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995921"
---
# <a name="id3dx11effectvariableasblend-method"></a><span data-ttu-id="c9f5f-106">Metodo ID3DX11EffectVariable:: AsBlend</span><span class="sxs-lookup"><span data-stu-id="c9f5f-106">ID3DX11EffectVariable::AsBlend method</span></span>

<span data-ttu-id="c9f5f-107">Ottenere una variabile Effect-Blend.</span><span class="sxs-lookup"><span data-stu-id="c9f5f-107">Get a effect-blend variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9f5f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9f5f-108">Syntax</span></span>


```C++
ID3DX11EffectBlendVariable* AsBlend();
```



## <a name="parameters"></a><span data-ttu-id="c9f5f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9f5f-109">Parameters</span></span>

<span data-ttu-id="c9f5f-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c9f5f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9f5f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9f5f-111">Return value</span></span>

<span data-ttu-id="c9f5f-112">Tipo: **[ **ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9f5f-112">Type: **[**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md)\***</span></span>

<span data-ttu-id="c9f5f-113">Puntatore a una variabile di Blend di effetto.</span><span class="sxs-lookup"><span data-stu-id="c9f5f-113">A pointer to an effect blend variable.</span></span> <span data-ttu-id="c9f5f-114">Vedere [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md).</span><span class="sxs-lookup"><span data-stu-id="c9f5f-114">See [**ID3DX11EffectBlendVariable**](id3dx11effectblendvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c9f5f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9f5f-115">Remarks</span></span>

<span data-ttu-id="c9f5f-116">AsBlend restituisce una versione della variabile Effect specializzata in una variabile Effect-Blend.</span><span class="sxs-lookup"><span data-stu-id="c9f5f-116">AsBlend returns a version of the effect variable that has been specialized to an effect-blend variable.</span></span> <span data-ttu-id="c9f5f-117">Analogamente a un cast, questa specializzazione restituirà un oggetto non valido se la variabile Effect non contiene dati di Blend di effetto.</span><span class="sxs-lookup"><span data-stu-id="c9f5f-117">Similar to a cast, this specialization will return an invalid object if the effect variable does not contain effect-blend data.</span></span>

<span data-ttu-id="c9f5f-118">Per verificare la validità dell'oggetto restituito, le applicazioni possono chiamare [**IsValid**](id3dx11effectvariable-isvalid.md).</span><span class="sxs-lookup"><span data-stu-id="c9f5f-118">Applications can test the returned object for validity by calling [**IsValid**](id3dx11effectvariable-isvalid.md).</span></span>

> [!Note]  
> <span data-ttu-id="c9f5f-119">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="c9f5f-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c9f5f-120">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="c9f5f-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c9f5f-121">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c9f5f-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c9f5f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9f5f-122">Requirements</span></span>



| <span data-ttu-id="c9f5f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9f5f-123">Requirement</span></span> | <span data-ttu-id="c9f5f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c9f5f-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9f5f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9f5f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c9f5f-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9f5f-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c9f5f-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="c9f5f-127">Library</span></span><br/> | <dl> <span data-ttu-id="c9f5f-128"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="c9f5f-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9f5f-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9f5f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9f5f-130">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="c9f5f-130">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





