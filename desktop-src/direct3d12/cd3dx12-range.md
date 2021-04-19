---
title: Struttura CD3DX12_RANGE (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura di intervallo D3D12.
ms.assetid: 5D5192BF-D14C-487B-A214-F8428E82AF0E
keywords:
- Struttura CD3DX12_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b6b92cd24a981d48252f5ad457f7ac0320e2d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323570"
---
# <a name="cd3dx12_range-structure"></a><span data-ttu-id="cdb0e-104">\_Struttura dell'intervallo CD3DX12</span><span class="sxs-lookup"><span data-stu-id="cdb0e-104">CD3DX12\_RANGE structure</span></span>

<span data-ttu-id="cdb0e-105">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**\_ intervallo D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .</span><span class="sxs-lookup"><span data-stu-id="cdb0e-105">A helper structure to enable easy initialization of a [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdb0e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cdb0e-106">Syntax</span></span>


```C++
struct CD3DX12_RANGE  : public D3D12_RANGE{
   CD3DX12_RANGE();
   explicit CD3DX12_RANGE(const D3D12_RANGE &o);
   CD3DX12_RANGE(SIZE_T begin, SIZE_T end);
   operator const D3D12_RANGE&() const;
};
```



## <a name="members"></a><span data-ttu-id="cdb0e-107">Members</span><span class="sxs-lookup"><span data-stu-id="cdb0e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="cdb0e-108">**\_Intervallo CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="cdb0e-108">**CD3DX12\_RANGE()**</span></span>
</dt> <dd>

<span data-ttu-id="cdb0e-109">Crea una nuova istanza non inizializzata di un intervallo di CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="cdb0e-109">Creates a new, uninitialized, instance of a CD3DX12\_RANGE.</span></span>

</dd> <dt>

<span data-ttu-id="cdb0e-110">**intervallo CD3DX12 esplicito \_ (const D3D12 \_ Range &o)**</span><span class="sxs-lookup"><span data-stu-id="cdb0e-110">**explicit CD3DX12\_RANGE(const D3D12\_RANGE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="cdb0e-111">Crea una nuova istanza di un intervallo di CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura di [**\_ intervallo D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .</span><span class="sxs-lookup"><span data-stu-id="cdb0e-111">Creates a new instance of a CD3DX12\_RANGE, initialized with the contents of another [**D3D12\_RANGE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cdb0e-112">**\_Intervallo CD3DX12 (size \_ t begin, Size \_ t end)**</span><span class="sxs-lookup"><span data-stu-id="cdb0e-112">**CD3DX12\_RANGE(SIZE\_T begin, SIZE\_T end)**</span></span>
</dt> <dd>

<span data-ttu-id="cdb0e-113">Crea una nuova istanza di un intervallo di CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="cdb0e-113">Creates a new instance of a CD3DX12\_RANGE, initializing the following parameters:</span></span>

<span data-ttu-id="cdb0e-114">DIMENSIONI \_ T Begin</span><span class="sxs-lookup"><span data-stu-id="cdb0e-114">SIZE\_T begin</span></span>

<span data-ttu-id="cdb0e-115">DIMENSIONI \_ T End</span><span class="sxs-lookup"><span data-stu-id="cdb0e-115">SIZE\_T end</span></span>

</dd> <dt>

<span data-ttu-id="cdb0e-116">**operatore const D3D12 \_ RANGE& () const**</span><span class="sxs-lookup"><span data-stu-id="cdb0e-116">**operator const D3D12\_RANGE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="cdb0e-117">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="cdb0e-117">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cdb0e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdb0e-118">Requirements</span></span>



| <span data-ttu-id="cdb0e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdb0e-119">Requirement</span></span> | <span data-ttu-id="cdb0e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="cdb0e-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb0e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cdb0e-121">Header</span></span><br/> | <dl> <span data-ttu-id="cdb0e-122"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdb0e-122"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdb0e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdb0e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdb0e-124">**\_Intervallo D3D12**</span><span class="sxs-lookup"><span data-stu-id="cdb0e-124">**D3D12\_RANGE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)
</dt> <dt>

[<span data-ttu-id="cdb0e-125">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="cdb0e-125">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





