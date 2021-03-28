---
title: Metodo ID3DX11EffectVariable AsUnorderedAccessView (D3dx11effect. h)
description: Ottenere una variabile di visualizzazione non ordinata.
ms.assetid: e8b7c104-09f7-4bfb-9980-a5603550b723
keywords:
- Metodo AsUnorderedAccessView Direct3D 11
- Metodo AsUnorderedAccessView Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo AsUnorderedAccessView
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b9ce7dbbc99ef16ef3290ec1ba3135a8d2cb05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762388"
---
# <a name="id3dx11effectvariableasunorderedaccessview-method"></a><span data-ttu-id="f4355-106">Metodo ID3DX11EffectVariable:: AsUnorderedAccessView</span><span class="sxs-lookup"><span data-stu-id="f4355-106">ID3DX11EffectVariable::AsUnorderedAccessView method</span></span>

<span data-ttu-id="f4355-107">Ottenere una variabile di visualizzazione non ordinata.</span><span class="sxs-lookup"><span data-stu-id="f4355-107">Get an unordered-access-view variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4355-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4355-108">Syntax</span></span>


```C++
ID3DX11EffectUnorderedAccessViewVariable* AsUnorderedAccessView();
```



## <a name="parameters"></a><span data-ttu-id="f4355-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4355-109">Parameters</span></span>

<span data-ttu-id="f4355-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f4355-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4355-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4355-111">Return value</span></span>

<span data-ttu-id="f4355-112">Tipo: **[ **ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***</span><span class="sxs-lookup"><span data-stu-id="f4355-112">Type: **[**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md)\***</span></span>

<span data-ttu-id="f4355-113">Puntatore a una variabile di visualizzazione di accesso non ordinato.</span><span class="sxs-lookup"><span data-stu-id="f4355-113">A pointer to an unordered-access-view variable.</span></span> <span data-ttu-id="f4355-114">Vedere [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md).</span><span class="sxs-lookup"><span data-stu-id="f4355-114">See [**ID3DX11EffectUnorderedAccessViewVariable**](id3dx11effectunorderedaccessviewvariable.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f4355-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4355-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f4355-116">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="f4355-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f4355-117">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="f4355-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f4355-118">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="f4355-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f4355-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4355-119">Requirements</span></span>



| <span data-ttu-id="f4355-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4355-120">Requirement</span></span> | <span data-ttu-id="f4355-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f4355-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4355-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4355-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f4355-123"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4355-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f4355-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="f4355-124">Library</span></span><br/> | <dl> <span data-ttu-id="f4355-125"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="f4355-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4355-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4355-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4355-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="f4355-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

 





