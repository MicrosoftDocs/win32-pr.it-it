---
title: Struttura CD3DX12_TEXTURE_COPY_LOCATION (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura del percorso di copia della trama D3D12 \_ \_ .
ms.assetid: 8BA93729-2FFB-4C09-88B0-779049BAF385
keywords:
- Struttura CD3DX12_TEXTURE_COPY_LOCATION
topic_type:
- apiref
api_name:
- CD3DX12_TEXTURE_COPY_LOCATION
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5143137f92e38662660588dd89a527f59644126
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322197"
---
# <a name="cd3dx12_texture_copy_location-structure"></a><span data-ttu-id="f9b6f-104">\_Struttura del \_ percorso della copia di trama CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="f9b6f-104">CD3DX12\_TEXTURE\_COPY\_LOCATION structure</span></span>

<span data-ttu-id="f9b6f-105">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura del [**\_ percorso di \_ Copia \_ della trama D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .</span><span class="sxs-lookup"><span data-stu-id="f9b6f-105">A helper structure to enable easy initialization of a [**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9b6f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9b6f-106">Syntax</span></span>


```C++
struct CD3DX12_TEXTURE_COPY_LOCATION  : public D3D12_TEXTURE_COPY_LOCATION{
   CD3DX12_TEXTURE_COPY_LOCATION();
   explicit CD3DX12_TEXTURE_COPY_LOCATION(const D3D12_TEXTURE_COPY_LOCATION &o);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, D3D12_PLACED_SUBRESOURCE_FOOTPRINT const& Footprint);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, UINT Sub);
};
```



## <a name="members"></a><span data-ttu-id="f9b6f-107">Members</span><span class="sxs-lookup"><span data-stu-id="f9b6f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f9b6f-108">**\_ \_ Percorso copia trama CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="f9b6f-108">**CD3DX12\_TEXTURE\_COPY\_LOCATION()**</span></span>
</dt> <dd>

<span data-ttu-id="f9b6f-109">Crea una nuova istanza non inizializzata di un \_ percorso di copia della trama CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f9b6f-109">Creates a new, uninitialized, instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION.</span></span>

</dd> <dt>

<span data-ttu-id="f9b6f-110">**\_percorso copia trama CD3DX12 esplicita \_ \_ (const D3D12 \_ texture \_ copy \_ location &o)**</span><span class="sxs-lookup"><span data-stu-id="f9b6f-110">**explicit CD3DX12\_TEXTURE\_COPY\_LOCATION(const D3D12\_TEXTURE\_COPY\_LOCATION &o)**</span></span>
</dt> <dd>

<span data-ttu-id="f9b6f-111">Crea una nuova istanza di un \_ percorso di copia di trama CD3DX12 \_ \_ , inizializzato con il contenuto di un'altra struttura del percorso di [**\_ copia della trama \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .</span><span class="sxs-lookup"><span data-stu-id="f9b6f-111">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initialized with the contents of another [**D3D12\_TEXTURE\_COPY\_LOCATION**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f9b6f-112">**\_ \_ Posizione copia trama CD3DX12 \_ (ID3D12Resource \* pRes)**</span><span class="sxs-lookup"><span data-stu-id="f9b6f-112">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes)**</span></span>
</dt> <dd>

<span data-ttu-id="f9b6f-113">Crea una nuova istanza di un \_ percorso di copia di trama CD3DX12 \_ \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="f9b6f-113">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="f9b6f-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes</span><span class="sxs-lookup"><span data-stu-id="f9b6f-114">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

</dd> <dt>

<span data-ttu-id="f9b6f-115">**\_Posizione della \_ copia di trama CD3DX12 \_ (ID3D12RESOURCE \* pRes, D3D12 \_ posto \_ footprint delle risorse subresource \_& footprint)**</span><span class="sxs-lookup"><span data-stu-id="f9b6f-115">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes, D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT const& Footprint)**</span></span>
</dt> <dd>

<span data-ttu-id="f9b6f-116">Crea una nuova istanza di un \_ percorso di copia di trama CD3DX12 \_ \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="f9b6f-116">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="f9b6f-117">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes</span><span class="sxs-lookup"><span data-stu-id="f9b6f-117">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

<span data-ttu-id="f9b6f-118">[**D3D12 \_ \_ \_ Footprint delle risorse SOTTOrisorse posizionate**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)& footprint</span><span class="sxs-lookup"><span data-stu-id="f9b6f-118">[**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) const& Footprint</span></span>

</dd> <dt>

<span data-ttu-id="f9b6f-119">**\_ \_ Percorso copia trama CD3DX12 \_ (ID3D12RESOURCE \* pRes, uint Sub)**</span><span class="sxs-lookup"><span data-stu-id="f9b6f-119">**CD3DX12\_TEXTURE\_COPY\_LOCATION(ID3D12Resource\* pRes, UINT Sub)**</span></span>
</dt> <dd>

<span data-ttu-id="f9b6f-120">Crea una nuova istanza di un \_ percorso di copia di trama CD3DX12 \_ \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="f9b6f-120">Creates a new instance of a CD3DX12\_TEXTURE\_COPY\_LOCATION, initializing the following parameters:</span></span>

<span data-ttu-id="f9b6f-121">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes</span><span class="sxs-lookup"><span data-stu-id="f9b6f-121">[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\* pRes</span></span>

<span data-ttu-id="f9b6f-122">Sub UINT</span><span class="sxs-lookup"><span data-stu-id="f9b6f-122">UINT Sub</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9b6f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9b6f-123">Requirements</span></span>



| <span data-ttu-id="f9b6f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9b6f-124">Requirement</span></span> | <span data-ttu-id="f9b6f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f9b6f-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f9b6f-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9b6f-126">Header</span></span><br/> | <dl> <span data-ttu-id="f9b6f-127"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9b6f-127"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9b6f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9b6f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9b6f-129">**\_ \_ Percorso copia trama \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="f9b6f-129">**D3D12\_TEXTURE\_COPY\_LOCATION**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
</dt> <dt>

[<span data-ttu-id="f9b6f-130">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="f9b6f-130">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





