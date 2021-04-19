---
title: Struttura CD3DX12_SUBRESOURCE_FOOTPRINT (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura footprint della SOTTORISORSA D3D12 \_ .
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- Struttura CD3DX12_SUBRESOURCE_FOOTPRINT
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_FOOTPRINT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab58e9a007d736222d9525d7a064456a1a9a7f14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322202"
---
# <a name="cd3dx12_subresource_footprint-structure"></a><span data-ttu-id="59769-104">\_Struttura del footprint della SOTTORISORSA CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="59769-104">CD3DX12\_SUBRESOURCE\_FOOTPRINT structure</span></span>

<span data-ttu-id="59769-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura [**\_ \_ footprint della sottorisorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .</span><span class="sxs-lookup"><span data-stu-id="59769-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="59769-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59769-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_FOOTPRINT  : public D3D12_SUBRESOURCE_FOOTPRINT{
   CD3DX12_SUBRESOURCE_FOOTPRINT();
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_SUBRESOURCE_FOOTPRINT &o);
   CD3DX12_SUBRESOURCE_FOOTPRINT(DXGI_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch);
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_RESOURCE_DESC& resDesc, UINT rowPitch);
   operator const D3D12_SUBRESOURCE_FOOTPRINT&() const;
};
```



## <a name="members"></a><span data-ttu-id="59769-107">Members</span><span class="sxs-lookup"><span data-stu-id="59769-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="59769-108">**\_Footprint delle sottorisorse CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="59769-108">**CD3DX12\_SUBRESOURCE\_FOOTPRINT()**</span></span>
</dt> <dd>

<span data-ttu-id="59769-109">Crea una nuova istanza non inizializzata di un \_ footprint della SOTTORISORSA CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="59769-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT.</span></span>

</dd> <dt>

<span data-ttu-id="59769-110">**footprint della \_ SOTTORISORSA CD3DX12 esplicita \_ (CONSt D3D12 \_ subresource \_ footprint &o)**</span><span class="sxs-lookup"><span data-stu-id="59769-110">**explicit CD3DX12\_SUBRESOURCE\_FOOTPRINT(const D3D12\_SUBRESOURCE\_FOOTPRINT &o)**</span></span>
</dt> <dd>

<span data-ttu-id="59769-111">Crea una nuova istanza di un \_ footprint della SOTTORISORSA CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura [**\_ \_ footprint della sottorisorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .</span><span class="sxs-lookup"><span data-stu-id="59769-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initialized with the contents of another [**D3D12\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) structure.</span></span>

</dd> <dt>

<span data-ttu-id="59769-112">**\_Footprint della SOTTORISORSA CD3DX12 \_ ( \_ formato DXGI, lunghezza UINT, altezza UINT, profondità uint, uint rowPitch)**</span><span class="sxs-lookup"><span data-stu-id="59769-112">**CD3DX12\_SUBRESOURCE\_FOOTPRINT(DXGI\_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch)**</span></span>
</dt> <dd>

<span data-ttu-id="59769-113">Crea una nuova istanza di un \_ footprint della SOTTORISORSA CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="59769-113">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initializing the following parameters:</span></span>

<span data-ttu-id="59769-114">[**DXGI \_ Formato formato**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="59769-114">[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) format</span></span>

<span data-ttu-id="59769-115">Lunghezza UINT</span><span class="sxs-lookup"><span data-stu-id="59769-115">UINT width</span></span>

<span data-ttu-id="59769-116">Altezza UINT</span><span class="sxs-lookup"><span data-stu-id="59769-116">UINT height</span></span>

<span data-ttu-id="59769-117">Profondità UINT</span><span class="sxs-lookup"><span data-stu-id="59769-117">UINT depth</span></span>

<span data-ttu-id="59769-118">RowPitch UINT</span><span class="sxs-lookup"><span data-stu-id="59769-118">UINT rowPitch</span></span>

</dd> <dt>

<span data-ttu-id="59769-119">**\_footprint delle sottorisorse CD3DX12 esplicito \_ (const D3D12 \_ Resource \_ desc& resDesc, uint rowPitch)**</span><span class="sxs-lookup"><span data-stu-id="59769-119">**explicit CD3DX12\_SUBRESOURCE\_FOOTPRINT(const D3D12\_RESOURCE\_DESC& resDesc, UINT rowPitch)**</span></span>
</dt> <dd>

<span data-ttu-id="59769-120">Crea una nuova istanza di un \_ footprint della SOTTORISORSA CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="59769-120">Creates a new instance of a CD3DX12\_SUBRESOURCE\_FOOTPRINT, initializing the following parameters:</span></span>

<span data-ttu-id="59769-121">[**D3D12 \_ \_Descrizione della risorsa**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc</span><span class="sxs-lookup"><span data-stu-id="59769-121">[**D3D12\_RESOURCE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc</span></span>

<span data-ttu-id="59769-122">RowPitch UINT</span><span class="sxs-lookup"><span data-stu-id="59769-122">UINT rowPitch</span></span>

</dd> <dt>

<span data-ttu-id="59769-123">**operatore const D3D12 \_ subresource \_ footprint& () const**</span><span class="sxs-lookup"><span data-stu-id="59769-123">**operator const D3D12\_SUBRESOURCE\_FOOTPRINT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="59769-124">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="59769-124">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="59769-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59769-125">Requirements</span></span>



| <span data-ttu-id="59769-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="59769-126">Requirement</span></span> | <span data-ttu-id="59769-127">Valore</span><span class="sxs-lookup"><span data-stu-id="59769-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="59769-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59769-128">Header</span></span><br/> | <dl> <span data-ttu-id="59769-129"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="59769-129"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59769-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59769-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59769-131">**\_Footprint delle sottorisorse D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="59769-131">**D3D12\_SUBRESOURCE\_FOOTPRINT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[<span data-ttu-id="59769-132">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="59769-132">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

