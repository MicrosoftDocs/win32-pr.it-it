---
title: Struttura CD3DX12_RANGE_UINT64 (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una struttura D3D12 dell' \_ intervallo \_ UInt64.
ms.assetid: 789A2C46-B7D4-462E-9C10-69FD63D27491
keywords:
- Struttura CD3DX12_RANGE_UINT64
topic_type:
- apiref
api_name:
- CD3DX12_RANGE_UINT64
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c408197afb1254cae922c402939f6f169708d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323571"
---
# <a name="cd3dx12_range_uint64-structure"></a><span data-ttu-id="8713d-104">Struttura CD3DX12 dell' \_ intervallo \_ UInt64</span><span class="sxs-lookup"><span data-stu-id="8713d-104">CD3DX12\_RANGE\_UINT64 structure</span></span>

<span data-ttu-id="8713d-105">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura [**D3D12 dell' \_ intervallo \_ UInt64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) .</span><span class="sxs-lookup"><span data-stu-id="8713d-105">A helper structure to enable easy initialization of a [**D3D12\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8713d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8713d-106">Syntax</span></span>


```C++
struct CD3DX12_RANGE_UINT64  : public D3D12_RANGE_UINT64{
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64();
  CD3DX12_RANGE_UINT64 explicit CD3DX12_RANGE_UINT64(const D3D12_RANGE_UINT64 &o);
  CD3DX12_RANGE_UINT64 CD3DX12_RANGE_UINT64(UINT64 begin, UINT64 end);
                       operator const D3D12_RANGE_UINT64&() const;
};
```



## <a name="members"></a><span data-ttu-id="8713d-107">Members</span><span class="sxs-lookup"><span data-stu-id="8713d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8713d-108">**\_Intervallo CD3DX12 \_ UInt64 ()**</span><span class="sxs-lookup"><span data-stu-id="8713d-108">**CD3DX12\_RANGE\_UINT64()**</span></span>
</dt> <dd>

<span data-ttu-id="8713d-109">Crea una nuova istanza non inizializzata di un \_ intervallo CD3DX12 \_ UInt64.</span><span class="sxs-lookup"><span data-stu-id="8713d-109">Creates a new, uninitialized, instance of a CD3DX12\_RANGE\_UINT64.</span></span>

</dd> <dt>

<span data-ttu-id="8713d-110">**intervallo CD3DX12 esplicito \_ \_ UInt64 (const D3D12 \_ Range \_ UInt64 &o)**</span><span class="sxs-lookup"><span data-stu-id="8713d-110">**explicit CD3DX12\_RANGE\_UINT64(const D3D12\_RANGE\_UINT64 &o)**</span></span>
</dt> <dd>

<span data-ttu-id="8713d-111">Crea una nuova istanza di un intervallo di CD3DX12 \_ \_ UInt64, inizializzato con i valori copiati da un [**\_ intervallo D3D12 \_ UInt64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) struttura.</span><span class="sxs-lookup"><span data-stu-id="8713d-111">Creates a new instance of a CD3DX12\_RANGE\_UINT64, initialized with values copied from a [**D3D12\_RANGE\_UINT64**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8713d-112">**CD3DX12 \_ Range \_ UINT64 (UInt64 Begin, UInt64 end)**</span><span class="sxs-lookup"><span data-stu-id="8713d-112">**CD3DX12\_RANGE\_UINT64(UINT64 begin, UINT64 end)**</span></span>
</dt> <dd>

<span data-ttu-id="8713d-113">Crea una nuova istanza di un DESC1 di CD3DX12 \_ Depth \_ stencil \_ , inizializzata con i valori passati nell'elenco di parametri.</span><span class="sxs-lookup"><span data-stu-id="8713d-113">Creates a new instance of a CD3DX12\_DEPTH\_STENCIL\_DESC1, initialized with the values passed in the parameter list.</span></span>

</dd> <dt>

<span data-ttu-id="8713d-114">**operatore const D3D12 \_ Range \_ UInt64& () const**</span><span class="sxs-lookup"><span data-stu-id="8713d-114">**operator const D3D12\_RANGE\_UINT64&() const**</span></span>
</dt> <dd>

<span data-ttu-id="8713d-115">Conversione implicita in una \_ struttura D3D12 dell'intervallo \_ UInt64.</span><span class="sxs-lookup"><span data-stu-id="8713d-115">Implicit conversion to a D3D12\_RANGE\_UINT64 structure.</span></span> <span data-ttu-id="8713d-116">Poiché l' \_ intervallo \_ di D3D12 UInt64 è il tipo sottostante dell'intervallo di CD3DX12 \_ \_ UInt64, l'oggetto viene semplicemente restituito come \_ riferimento a un intervallo const D3D12 \_ a se stesso.</span><span class="sxs-lookup"><span data-stu-id="8713d-116">Because D3D12\_RANGE\_UINT64 is the underlying type of CD3DX12\_RANGE\_UINT64, the object is simply returned as a const D3D12\_RANGE\_UINT64 reference to itself.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8713d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8713d-117">Requirements</span></span>



| <span data-ttu-id="8713d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8713d-118">Requirement</span></span> | <span data-ttu-id="8713d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="8713d-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8713d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8713d-120">Header</span></span><br/> | <dl> <span data-ttu-id="8713d-121"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8713d-121"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8713d-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8713d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8713d-123">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="8713d-123">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="8713d-124">**\_Intervallo D3D12 \_ UInt64**</span><span class="sxs-lookup"><span data-stu-id="8713d-124">**D3D12\_RANGE\_UINT64**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range_uint64)
</dt> </dl>

 

 





