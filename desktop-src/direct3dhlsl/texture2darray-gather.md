---
title: 'Metodi di raccolta Texture2DArray:: Texture2DArray'
description: Campiona un Texture2DArray e restituisce tutti e quattro i componenti.
ms.assetid: eea1dd00-0061-4601-a218-979eb0ecd36d
keywords:
- Metodi gather HLSL
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: cd10959490a85583cab01814f9cdb012859317a4
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104981023"
---
# <a name="texture2darraygather-methods"></a><span data-ttu-id="4890f-104">Metodi Texture2DArray:: Gather</span><span class="sxs-lookup"><span data-stu-id="4890f-104">Texture2DArray::Gather methods</span></span>

<span data-ttu-id="4890f-105">Restituisce i quattro valori Texel di un [**Texture2DArray**](sm5-object-texture2darray.md) che verrebbero usati in un'operazione di filtro bi-lineare.</span><span class="sxs-lookup"><span data-stu-id="4890f-105">Returns the four texel values of a [**Texture2DArray**](sm5-object-texture2darray.md) that would be used in a bi-linear filtering operation.</span></span>

<span data-ttu-id="4890f-106">Per ulteriori informazioni sulla descrizione dell'istruzione DXBC sottostante, vedere la documentazione su [gather4](./gather4--sm5---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="4890f-106">See the documentation on [gather4](./gather4--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="4890f-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="4890f-107">Overload list</span></span>



| <span data-ttu-id="4890f-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="4890f-108">Method</span></span>                                                                | <span data-ttu-id="4890f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4890f-109">Description</span></span>                                                                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4890f-110">**Raccolta (S, float, int)**</span><span class="sxs-lookup"><span data-stu-id="4890f-110">**Gather(S,float,int)**</span></span>](sm5-object-texture2darray-gather.md)        | <span data-ttu-id="4890f-111">Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.</span><span class="sxs-lookup"><span data-stu-id="4890f-111">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span><br/>                                 |
| [<span data-ttu-id="4890f-112">**Raccolta (S, float, int, uint)**</span><span class="sxs-lookup"><span data-stu-id="4890f-112">**Gather(S,float,int,uint)**</span></span>](t2darray-gather-s-float-int-uint-.md)  | <span data-ttu-id="4890f-113">Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtraggio bilineare, insieme allo stato del mapping dei riquadri.</span><span class="sxs-lookup"><span data-stu-id="4890f-113">Returns the four texel values that would be used in a bi-linear filtering operation, along with tile-mapping status.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4890f-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4890f-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4890f-115">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4890f-115">Texture2DArray</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

