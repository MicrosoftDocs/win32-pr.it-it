---
title: Struttura CD3DX12_BOX (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di D3D12 \_ box.
ms.assetid: 7E1A352C-D664-4538-BA78-91493980559D
keywords:
- Struttura CD3DX12_BOX
topic_type:
- apiref
api_name:
- CD3DX12_BOX
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.topic: reference
ms.localizationpriority: low
ms.date: 05/31/2018
ms.openlocfilehash: c689c9bfe611651248280f7536bd91a9f4d003d4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322282"
---
# <a name="cd3dx12_box-structure"></a><span data-ttu-id="b3780-104">\_Struttura CD3DX12 box</span><span class="sxs-lookup"><span data-stu-id="b3780-104">CD3DX12\_BOX structure</span></span>

<span data-ttu-id="b3780-105">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**D3D12 \_ Box**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .</span><span class="sxs-lookup"><span data-stu-id="b3780-105">A helper structure to enable easy initialization of a [**D3D12\_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3780-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3780-106">Syntax</span></span>


```C++
struct CD3DX12_BOX  : public D3D12_BOX{
   CD3DX12_BOX();
   explicit CD3DX12_BOX(const D3D12_BOX& o);
   explicit CD3DX12_BOX(LONG Left, LONG Right);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom);
   explicit CD3DX12_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back);
   ~CD3DX12_BOX();
   operator const D3D12_BOX&() const;
};
```



## <a name="members"></a><span data-ttu-id="b3780-107">Members</span><span class="sxs-lookup"><span data-stu-id="b3780-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b3780-108">**CD3DX12 \_ Box ()**</span><span class="sxs-lookup"><span data-stu-id="b3780-108">**CD3DX12\_BOX()**</span></span>
</dt> <dd>

<span data-ttu-id="b3780-109">Crea una nuova istanza non inizializzata di una \_ casella CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="b3780-109">Creates a new, uninitialized, instance of a CD3DX12\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="b3780-110">**casella CD3DX12 esplicita \_ (const D3D12 \_ Box& o)**</span><span class="sxs-lookup"><span data-stu-id="b3780-110">**explicit CD3DX12\_BOX(const D3D12\_BOX& o)**</span></span>
</dt> <dd>

<span data-ttu-id="b3780-111">Crea una nuova istanza di una \_ casella CD3DX12, inizializzata con il contenuto di un'altra struttura di [**\_ caselle di D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) .</span><span class="sxs-lookup"><span data-stu-id="b3780-111">Creates a new instance of a CD3DX12\_BOX, initialized with the contents of another [**D3D12\_BOX**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b3780-112">**casella CD3DX12 esplicita \_ (Long Left, Long Right)**</span><span class="sxs-lookup"><span data-stu-id="b3780-112">**explicit CD3DX12\_BOX(LONG Left, LONG Right)**</span></span>
</dt> <dd>

<span data-ttu-id="b3780-113">Crea una nuova istanza di una \_ casella CD3DX12, inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3780-113">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="b3780-114">LONG Left</span><span class="sxs-lookup"><span data-stu-id="b3780-114">LONG Left</span></span>

<span data-ttu-id="b3780-115">LUNGO a destra</span><span class="sxs-lookup"><span data-stu-id="b3780-115">LONG Right</span></span>

</dd> <dt>

<span data-ttu-id="b3780-116">**casella CD3DX12 esplicita \_ (Long Left, Long Top, Long Right, Long Bottom)**</span><span class="sxs-lookup"><span data-stu-id="b3780-116">**explicit CD3DX12\_BOX(LONG Left, LONG Top, LONG Right, LONG Bottom)**</span></span>
</dt> <dd>

<span data-ttu-id="b3780-117">Crea una nuova istanza di una \_ casella CD3DX12, inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3780-117">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="b3780-118">LONG Left</span><span class="sxs-lookup"><span data-stu-id="b3780-118">LONG Left</span></span>

<span data-ttu-id="b3780-119">Inizio lungo</span><span class="sxs-lookup"><span data-stu-id="b3780-119">LONG Top</span></span>

<span data-ttu-id="b3780-120">LUNGO a destra</span><span class="sxs-lookup"><span data-stu-id="b3780-120">LONG Right</span></span>

<span data-ttu-id="b3780-121">LUNGO in basso</span><span class="sxs-lookup"><span data-stu-id="b3780-121">LONG Bottom</span></span>

</dd> <dt>

<span data-ttu-id="b3780-122">**casella CD3DX12 esplicita \_ (Long Left, Long Top, Long Front, Long Right, Long Bottom, Long back)**</span><span class="sxs-lookup"><span data-stu-id="b3780-122">**explicit CD3DX12\_BOX(LONG Left, LONG Top, LONG Front, LONG Right, LONG Bottom, LONG Back)**</span></span>
</dt> <dd>

<span data-ttu-id="b3780-123">Crea una nuova istanza di una \_ casella CD3DX12, inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3780-123">Creates a new instance of a CD3DX12\_BOX, initializing the following parameters:</span></span>

<span data-ttu-id="b3780-124">LONG Left</span><span class="sxs-lookup"><span data-stu-id="b3780-124">LONG Left</span></span>

<span data-ttu-id="b3780-125">Inizio lungo</span><span class="sxs-lookup"><span data-stu-id="b3780-125">LONG Top</span></span>

<span data-ttu-id="b3780-126">LUNGO Front</span><span class="sxs-lookup"><span data-stu-id="b3780-126">LONG Front</span></span>

<span data-ttu-id="b3780-127">LUNGO a destra</span><span class="sxs-lookup"><span data-stu-id="b3780-127">LONG Right</span></span>

<span data-ttu-id="b3780-128">LUNGO in basso</span><span class="sxs-lookup"><span data-stu-id="b3780-128">LONG Bottom</span></span>

<span data-ttu-id="b3780-129">LONG back</span><span class="sxs-lookup"><span data-stu-id="b3780-129">LONG Back</span></span>

</dd> <dt>

<span data-ttu-id="b3780-130">**~ CD3DX12 \_ Box ()**</span><span class="sxs-lookup"><span data-stu-id="b3780-130">**~CD3DX12\_BOX()**</span></span>
</dt> <dd>

<span data-ttu-id="b3780-131">Elimina un'istanza di una casella CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="b3780-131">Destroys an instance of a CD3DX12\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="b3780-132">**operatore const D3D12 \_ BOX& () const**</span><span class="sxs-lookup"><span data-stu-id="b3780-132">**operator const D3D12\_BOX&() const**</span></span>
</dt> <dd>

<span data-ttu-id="b3780-133">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="b3780-133">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3780-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3780-134">Requirements</span></span>



| <span data-ttu-id="b3780-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3780-135">Requirement</span></span> | <span data-ttu-id="b3780-136">Valore</span><span class="sxs-lookup"><span data-stu-id="b3780-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b3780-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3780-137">Header</span></span><br/> | <dl> <span data-ttu-id="b3780-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3780-138"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3780-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3780-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3780-140">**\_Casella D3D12**</span><span class="sxs-lookup"><span data-stu-id="b3780-140">**D3D12\_BOX**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_box)
</dt> <dt>

[<span data-ttu-id="b3780-141">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="b3780-141">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





