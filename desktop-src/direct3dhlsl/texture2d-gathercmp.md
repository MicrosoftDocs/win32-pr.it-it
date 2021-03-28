---
title: 'Metodi di Texture2D:: Texture2D GatherCmp'
description: Campiona e confronta un Texture2D e restituisce tutti i componenti.
ms.assetid: d520b113-77af-486e-8d3d-8276f72df18f
keywords:
- Metodi GatherCmp HLSL
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: 18455f33ba97c9d5a0180a59e39891cd617a09af
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104981055"
---
# <a name="texture2dgathercmp-methods"></a><span data-ttu-id="ef589-104">Metodi Texture2D:: GatherCmp</span><span class="sxs-lookup"><span data-stu-id="ef589-104">Texture2D::GatherCmp methods</span></span>

<span data-ttu-id="ef589-105">Per quattro valori Texel di un [**Texture2D**](sm5-object-texture2d.md) che verrebbero usati in un'operazione di filtro bi-lineare, restituisce il confronto rispetto a un valore di confronto.</span><span class="sxs-lookup"><span data-stu-id="ef589-105">For four texel values of a [**Texture2D**](sm5-object-texture2d.md) that would be used in a bi-linear filtering operation, returns their comparison against a compare value.</span></span>

<span data-ttu-id="ef589-106">Per ulteriori informazioni sulla descrizione dell'istruzione DXBC sottostante, vedere la documentazione su [gather4_c](./gather4-c--sm5---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="ef589-106">See the documentation on [gather4_c](./gather4-c--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="ef589-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="ef589-107">Overload list</span></span>



| <span data-ttu-id="ef589-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="ef589-108">Method</span></span>                                                                             | <span data-ttu-id="ef589-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef589-109">Description</span></span>                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef589-110">**GatherCmp (S, float, float, int)**</span><span class="sxs-lookup"><span data-stu-id="ef589-110">**GatherCmp(S,float,float,int)**</span></span>](sm5-object-texture2d-gathercmp.md)             | <span data-ttu-id="ef589-111">Campiona e confronta una trama e restituisce tutti e quattro i componenti.</span><span class="sxs-lookup"><span data-stu-id="ef589-111">Samples and compares a texture and returns all four components.</span></span><br/>                                       |
| [<span data-ttu-id="ef589-112">**GatherCmp (S, float, float, int, uint)**</span><span class="sxs-lookup"><span data-stu-id="ef589-112">**GatherCmp(S,float,float,int,uint)**</span></span>](t2d-gathercmp-s-float-float-int-uint-.md) | <span data-ttu-id="ef589-113">Campiona e confronta una trama e restituisce tutti e quattro i componenti insieme allo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ef589-113">Samples and compares a texture and returns all four components along with status about the operation.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef589-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef589-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef589-115">Texture2D</span><span class="sxs-lookup"><span data-stu-id="ef589-115">Texture2D</span></span>](sm5-object-texture2d.md)
</dt> </dl>

 

