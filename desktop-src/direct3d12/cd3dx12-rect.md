---
title: Struttura CD3DX12_RECT (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura Rect D3D12.
ms.assetid: FBF01294-1448-4D9A-BA6B-27D5D59C2958
keywords:
- Struttura CD3DX12_RECT
topic_type:
- apiref
api_name:
- CD3DX12_RECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d8c133f14b531433ceb2239377ea85ba212af
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322217"
---
# <a name="cd3dx12_rect-structure"></a><span data-ttu-id="40679-104">\_Struttura Rect CD3DX12</span><span class="sxs-lookup"><span data-stu-id="40679-104">CD3DX12\_RECT structure</span></span>

<span data-ttu-id="40679-105">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura [**\_ Rect D3D12**](d3d12-rect.md) .</span><span class="sxs-lookup"><span data-stu-id="40679-105">A helper structure to enable easy initialization of a [**D3D12\_RECT**](d3d12-rect.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="40679-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40679-106">Syntax</span></span>


```C++
struct CD3DX12_RECT  : public D3D12_RECT{
   CD3DX12_RECT();
   explicit CD3DX12_RECT(const D3D12_RECT& o);
   explicit CD3DX12_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom);
   ~CD3DX12_RECT();
   operator const D3D12_RECT&() const;
};
```



## <a name="members"></a><span data-ttu-id="40679-107">Members</span><span class="sxs-lookup"><span data-stu-id="40679-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="40679-108">**CD3DX12 \_ Rect ()**</span><span class="sxs-lookup"><span data-stu-id="40679-108">**CD3DX12\_RECT()**</span></span>
</dt> <dd>

<span data-ttu-id="40679-109">Crea una nuova istanza non inizializzata di un \_ rettangolo CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="40679-109">Creates a new, uninitialized, instance of a CD3DX12\_RECT.</span></span>

</dd> <dt>

<span data-ttu-id="40679-110">**Explicit CD3DX12 \_ Rect (const D3D12 \_ Rect& o)**</span><span class="sxs-lookup"><span data-stu-id="40679-110">**explicit CD3DX12\_RECT(const D3D12\_RECT& o)**</span></span>
</dt> <dd>

<span data-ttu-id="40679-111">Crea una nuova istanza di un oggetto CD3DX12 \_ Rect, inizializzato con il contenuto di un'altra struttura [**\_ Rect di D3D12**](d3d12-rect.md) .</span><span class="sxs-lookup"><span data-stu-id="40679-111">Creates a new instance of a CD3DX12\_RECT, initialized with the contents of another [**D3D12\_RECT**](d3d12-rect.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="40679-112">**Rect CD3DX12 esplicito \_ (Long Left, Long Top, Long Right, Long Bottom)**</span><span class="sxs-lookup"><span data-stu-id="40679-112">**explicit CD3DX12\_RECT(LONG Left, LONG Top, LONG Right, LONG Bottom)**</span></span>
</dt> <dd>

<span data-ttu-id="40679-113">Crea una nuova istanza di un oggetto CD3DX12 \_ Rect, inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="40679-113">Creates a new instance of a CD3DX12\_RECT, initializing the following parameters:</span></span>

<span data-ttu-id="40679-114">LONG Left</span><span class="sxs-lookup"><span data-stu-id="40679-114">LONG Left</span></span>

<span data-ttu-id="40679-115">Inizio lungo</span><span class="sxs-lookup"><span data-stu-id="40679-115">LONG Top</span></span>

<span data-ttu-id="40679-116">LUNGO a destra</span><span class="sxs-lookup"><span data-stu-id="40679-116">LONG Right</span></span>

<span data-ttu-id="40679-117">LUNGO in basso</span><span class="sxs-lookup"><span data-stu-id="40679-117">LONG Bottom</span></span>

</dd> <dt>

<span data-ttu-id="40679-118">**~ CD3DX12 \_ Rect ()**</span><span class="sxs-lookup"><span data-stu-id="40679-118">**~CD3DX12\_RECT()**</span></span>
</dt> <dd>

<span data-ttu-id="40679-119">Elimina un'istanza di un CD3DX12 \_ Rect.</span><span class="sxs-lookup"><span data-stu-id="40679-119">Destroys an instance of a CD3DX12\_RECT.</span></span>

</dd> <dt>

<span data-ttu-id="40679-120">**operatore const D3D12 \_ RECT& () const**</span><span class="sxs-lookup"><span data-stu-id="40679-120">**operator const D3D12\_RECT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="40679-121">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="40679-121">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40679-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40679-122">Requirements</span></span>



| <span data-ttu-id="40679-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="40679-123">Requirement</span></span> | <span data-ttu-id="40679-124">Valore</span><span class="sxs-lookup"><span data-stu-id="40679-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="40679-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40679-125">Header</span></span><br/> | <dl> <span data-ttu-id="40679-126"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="40679-126"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40679-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40679-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40679-128">**D3D12 \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="40679-128">**D3D12\_RECT**</span></span>](d3d12-rect.md)
</dt> <dt>

[<span data-ttu-id="40679-129">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="40679-129">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





