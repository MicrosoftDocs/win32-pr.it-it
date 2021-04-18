---
title: Struttura CD3DX12_SUBRESOURCE_RANGE_UINT64 (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura della SOTTORISORSA D3D12 \_ \_ .
ms.assetid: 607A60ED-98D2-4A77-9A7A-6B54342EA101
keywords:
- Struttura CD3DX12_SUBRESOURCE_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2aea83d993c0c7b58ded8d0b92374d1dcbacdcc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322199"
---
# <a name="cd3dx12_subresource_range_uint64-structure"></a><span data-ttu-id="f9e82-104">\_ \_ Struttura UInt64 della SOTTOrisorsa CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="f9e82-104">CD3DX12\_SUBRESOURCE\_RANGE\_UINT64 structure</span></span>

<span data-ttu-id="f9e82-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura della [**\_ sottorisorsa \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="f9e82-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9e82-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9e82-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_RANGE_UINT64  : public D3D12_SUBRESOURCE_RANGE_UINT64{
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64();
  CD3DX12_SUBRESOURCE_RANGE_UINT64 explicit CD3DX12_SUBRESOURCE_RANGE_UINT64(const D3D12_SUBRESOURCE_RANGE_UINT64 &o);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, const D3D12_RANGE_UINT64& range);
  CD3DX12_SUBRESOURCE_RANGE_UINT64 CD3DX12_SUBRESOURCE_RANGE_UINT64(UINT subresource, UINT64 begin, UINT64 end);
                                   operator const D3D12_SUBRESOURCE_RANGE_UINT64&() const;
};
```



## <a name="members"></a><span data-ttu-id="f9e82-107">Members</span><span class="sxs-lookup"><span data-stu-id="f9e82-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="f9e82-108">**CD3DX12 \_ intervallo di sottorisorse \_ \_ UInt64 ()**</span><span class="sxs-lookup"><span data-stu-id="f9e82-108">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64()**</span></span>
</dt> <dd>

<span data-ttu-id="f9e82-109">Crea un'istanza nuova, non inizializzata, di un \_ intervallo di SOTTORISORSA CD3DX12 \_ \_ UInt64.</span><span class="sxs-lookup"><span data-stu-id="f9e82-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_RANGE\_UINT64.</span></span>

</dd> <dt>

<span data-ttu-id="f9e82-110">**intervallo di \_ SOTTORISORSA CD3DX12 esplicito \_ \_ UInt64 (const D3D12 \_ subresource \_ Range \_ UInt64 &o)**</span><span class="sxs-lookup"><span data-stu-id="f9e82-110">**explicit CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(const D3D12\_SUBRESOURCE\_RANGE\_UINT64 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="f9e82-111">Crea una nuova istanza di un \_ intervallo della SOTTORISORSA CD3DX12 \_ \_ , inizializzato con i valori copiati da una struttura di un [**intervallo di \_ sottorisorse di D3D12 \_ \_ UInt64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="f9e82-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_RANGE\_UINT64, initialized with values copied from a [**D3D12\_SUBRESOURCE\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f9e82-112">**Intervallo \_ di SOTTORISORSE CD3DX12 \_ \_ UInt64 (uint subresource, const D3D12 \_ Range \_ UInt64& Range)**</span><span class="sxs-lookup"><span data-stu-id="f9e82-112">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(UINT subresource, const D3D12\_RANGE\_UINT64& range)**</span></span>
</dt> <dd>

<span data-ttu-id="f9e82-113">Crea una nuova istanza di un DESC1 di CD3DX12 \_ Depth \_ stencil \_ , inizializzata con i valori passati nell'elenco di parametri.</span><span class="sxs-lookup"><span data-stu-id="f9e82-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="f9e82-114">**\_Intervallo della SOTTORISORSA CD3DX12 \_ \_ UInt64 (uint subresource, UINT64 Begin, UInt64 end)**</span><span class="sxs-lookup"><span data-stu-id="f9e82-114">**CD3DX12\_SUBRESOURCE\_RANGE\_UINT64(UINT subresource, UINT64 begin, UINT64 end)**</span></span>
</dt> <dd>

<span data-ttu-id="f9e82-115">Crea una nuova istanza di un DESC1 di CD3DX12 \_ Depth \_ stencil \_ , inizializzata con i valori passati nell'elenco di parametri.</span><span class="sxs-lookup"><span data-stu-id="f9e82-115">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="f9e82-116">**operator const D3D12- \_ intervallo di sottorisorse \_ \_ UInt64& () const**</span><span class="sxs-lookup"><span data-stu-id="f9e82-116">**operator const D3D12\_SUBRESOURCE\_RANGE\_UINT64&() const**</span></span>
</dt> <dd>

<span data-ttu-id="f9e82-117">Conversione implicita in una \_ struttura di intervallo di SOTTORISORSE D3D12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f9e82-117">Implicit conversion to a D3D12\_SUBRESOURCE\_RANGE\_UINT64 structure.</span></span> <span data-ttu-id="f9e82-118">Poiché l' \_ intervallo della SOTTORISORSA D3D12 \_ \_ UInt64 è il tipo sottostante dell' \_ intervallo della sottorisorsa CD3DX12 \_ \_ UInt64, l'oggetto viene semplicemente restituito come un riferimento const D3D12 \_ Depth \_ stencil \_ DESC1 a se stesso.</span><span class="sxs-lookup"><span data-stu-id="f9e82-118">Because D3D12\_SUBRESOURCE\_RANGE\_UINT64 is the underlying type of CD3DX12\_SUBRESOURCE\_RANGE\_UINT64, the object is simply returned as a const D3D12\_DEPTH\_STENCIL\_DESC1 reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9e82-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9e82-119">Requirements</span></span>



| <span data-ttu-id="f9e82-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9e82-120">Requirement</span></span> | <span data-ttu-id="f9e82-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f9e82-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e82-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9e82-122">Header</span></span><br/> | <dl> <span data-ttu-id="f9e82-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9e82-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9e82-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9e82-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9e82-125">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="f9e82-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="f9e82-126">**D3D12 \_ intervallo di sottorisorse \_ \_ UInt64**</span><span class="sxs-lookup"><span data-stu-id="f9e82-126">**D3D12\_SUBRESOURCE\_RANGE\_UINT64**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_range_uint64)
</dt> </dl>

 

 





