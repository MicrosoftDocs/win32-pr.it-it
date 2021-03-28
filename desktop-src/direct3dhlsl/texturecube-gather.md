---
title: 'Metodi di raccolta TextureCube:: TextureCube'
description: "Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare. | Metodi di raccolta TextureCube:: TextureCube"
ms.assetid: 4891A62A-9D54-4F7E-92C2-9CDDF1453671
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
ms.openlocfilehash: ce58acc01ef87e6d53d829a5c84e7c9c0ff6afb9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981450"
---
# <a name="texturecubegather-methods"></a><span data-ttu-id="bf161-105">Metodi TextureCube:: Gather</span><span class="sxs-lookup"><span data-stu-id="bf161-105">TextureCube::Gather methods</span></span>

<span data-ttu-id="bf161-106">Restituisce i quattro valori Texel che verrebbero usati in un'operazione di filtro bi-lineare.</span><span class="sxs-lookup"><span data-stu-id="bf161-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

<span data-ttu-id="bf161-107">Per ulteriori informazioni sulla descrizione dell'istruzione DXBC sottostante, vedere la documentazione su [gather4](./gather4--sm5---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="bf161-107">See the documentation on [gather4](./gather4--sm5---asm-.md) for more information describing the underlying DXBC instruction.</span></span>

### <a name="overload-list"></a><span data-ttu-id="bf161-108">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="bf161-108">Overload list</span></span>



| <span data-ttu-id="bf161-109">Metodo</span><span class="sxs-lookup"><span data-stu-id="bf161-109">Method</span></span>                                                     | <span data-ttu-id="bf161-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf161-110">Description</span></span>                                                                                                              |
|:-----------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf161-111">**Raccolta (S, float)**</span><span class="sxs-lookup"><span data-stu-id="bf161-111">**Gather(S,float)**</span></span>](dx-graphics-hlsl-to-gather.md)      | <span data-ttu-id="bf161-112">Campiona una trama e restituisce i quattro campioni (solo per il componente rosso) usati per l'interpolazione bilineare.</span><span class="sxs-lookup"><span data-stu-id="bf161-112">Samples a texture and returns the four samples (red component only) that are used for bilinear interpolation.</span></span><br/> |
| [<span data-ttu-id="bf161-113">**Raccolta (S, float, uint)**</span><span class="sxs-lookup"><span data-stu-id="bf161-113">**Gather(S,float,uint)**</span></span>](tcube-gather-s-float-uint-.md) | <span data-ttu-id="bf161-114">Esegue il campionamento di una trama e restituisce tutti e quattro i componenti insieme allo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bf161-114">Samples a texture and returns all four components along with status about the operation.</span></span><br/>                      |



## <a name="see-also"></a><span data-ttu-id="bf161-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf161-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf161-116">**TextureCube**</span><span class="sxs-lookup"><span data-stu-id="bf161-116">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

