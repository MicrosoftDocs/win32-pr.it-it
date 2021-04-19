---
title: Struttura CD3DX12_VIEWPORT (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura del viewport D3D12.
ms.assetid: 1A824F54-596B-450E-A191-B60FBBBB60ED
keywords:
- Struttura CD3DX12_VIEWPORT
topic_type:
- apiref
api_name:
- CD3DX12_VIEWPORT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da29adc50b62bd645070d9667bec1e5c7ce7ab15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323551"
---
# <a name="cd3dx12_viewport-structure"></a><span data-ttu-id="5926d-104">\_Struttura del viewport CD3DX12</span><span class="sxs-lookup"><span data-stu-id="5926d-104">CD3DX12\_VIEWPORT structure</span></span>

<span data-ttu-id="5926d-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="5926d-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5926d-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="5926d-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5926d-107">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura del [**\_ viewport D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) .</span><span class="sxs-lookup"><span data-stu-id="5926d-107">A helper structure to enable easy initialization of a [**D3D12\_VIEWPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="5926d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5926d-108">Syntax</span></span>


```C++
struct CD3DX12_VIEWPORT  : public D3D12_VIEWPORT{
   CD3DX12_VIEWPORT();
   explicit CD3DX12_VIEWPORT(const D3D12_VIEWPORT& o);
   explicit CD3DX12_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   explicit CD3DX12_VIEWPORT(ID3D12Resource* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   ~CD3DX12_VIEWPORT();
   operator const D3D12_VIEWPORT&() const;
};
```



## <a name="members"></a><span data-ttu-id="5926d-109">Members</span><span class="sxs-lookup"><span data-stu-id="5926d-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="5926d-110">**\_Viewport CD3DX12 ()**</span><span class="sxs-lookup"><span data-stu-id="5926d-110">**CD3DX12\_VIEWPORT()**</span></span>
</dt> <dd>

<span data-ttu-id="5926d-111">Crea una nuova istanza non inizializzata di un \_ viewport CD3DX12.</span><span class="sxs-lookup"><span data-stu-id="5926d-111">Creates a new, uninitialized, instance of a CD3DX12\_VIEWPORT.</span></span>

</dd> <dt>

<span data-ttu-id="5926d-112">**Viewport CD3DX12 esplicito \_ (const D3D12 \_ viewport& o)**</span><span class="sxs-lookup"><span data-stu-id="5926d-112">**explicit CD3DX12\_VIEWPORT(const D3D12\_VIEWPORT& o)**</span></span>
</dt> <dd>

<span data-ttu-id="5926d-113">Crea una nuova istanza di un \_ viewport CD3DX12, inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="5926d-113">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="5926d-114">& o del viewport const D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="5926d-114">const D3D12\_VIEWPORT& o</span></span>

</dd> <dt>

<span data-ttu-id="5926d-115">**Viewport CD3DX12 esplicito \_ (float topLeftX, float a sinistra, float width, float height, float minDepth = D3D12 \_ Min \_ Depth, float MaxDepth = D3D12 \_ Max \_ Depth)**</span><span class="sxs-lookup"><span data-stu-id="5926d-115">**explicit CD3DX12\_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12\_MIN\_DEPTH, FLOAT maxDepth = D3D12\_MAX\_DEPTH)**</span></span>
</dt> <dd>

<span data-ttu-id="5926d-116">Crea una nuova istanza di un \_ viewport CD3DX12, inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="5926d-116">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="5926d-117">FLOAT topLeftX</span><span class="sxs-lookup"><span data-stu-id="5926d-117">FLOAT topLeftX</span></span>

<span data-ttu-id="5926d-118">FLOAT a sinistra</span><span class="sxs-lookup"><span data-stu-id="5926d-118">FLOAT topLeftY</span></span>

<span data-ttu-id="5926d-119">Larghezza FLOAT</span><span class="sxs-lookup"><span data-stu-id="5926d-119">FLOAT width</span></span>

<span data-ttu-id="5926d-120">Altezza FLOAT</span><span class="sxs-lookup"><span data-stu-id="5926d-120">FLOAT height</span></span>

<span data-ttu-id="5926d-121">FLOAT minDepth = D3D12 \_ Min \_ Depth</span><span class="sxs-lookup"><span data-stu-id="5926d-121">FLOAT minDepth = D3D12\_MIN\_DEPTH</span></span>

<span data-ttu-id="5926d-122">FLOAT maxDepth = \_ profondità massima \_ D3D12</span><span class="sxs-lookup"><span data-stu-id="5926d-122">FLOAT maxDepth = D3D12\_MAX\_DEPTH</span></span>

</dd> <dt>

<span data-ttu-id="5926d-123">**Viewport CD3DX12 esplicito \_ (ID3D12Resource \* PreSource, uint mipSlice = 0, float topLeftX = 0,0 f, float-Lefty = 0,0 f, float MINDEPTH = D3D12 \_ Min \_ Depth, float MaxDepth = D3D12 \_ Max \_ Depth)**</span><span class="sxs-lookup"><span data-stu-id="5926d-123">**explicit CD3DX12\_VIEWPORT(ID3D12Resource\* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12\_MIN\_DEPTH, FLOAT maxDepth = D3D12\_MAX\_DEPTH)**</span></span>
</dt> <dd>

<span data-ttu-id="5926d-124">Crea una nuova istanza di un \_ viewport CD3DX12, inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="5926d-124">Creates a new instance of a CD3DX12\_VIEWPORT, initializing the following parameters:</span></span>

<span data-ttu-id="5926d-125">Preorigine ID3D12Resource \*</span><span class="sxs-lookup"><span data-stu-id="5926d-125">ID3D12Resource\* pResource</span></span>

<span data-ttu-id="5926d-126">UINT mipSlice = 0</span><span class="sxs-lookup"><span data-stu-id="5926d-126">UINT mipSlice = 0</span></span>

<span data-ttu-id="5926d-127">FLOAT topLeftX = 0,0 f</span><span class="sxs-lookup"><span data-stu-id="5926d-127">FLOAT topLeftX = 0.0f</span></span>

<span data-ttu-id="5926d-128">FLOAT in uscita = 0,0 f</span><span class="sxs-lookup"><span data-stu-id="5926d-128">FLOAT topLeftY = 0.0f</span></span>

<span data-ttu-id="5926d-129">FLOAT minDepth = D3D12 \_ Min \_ Depth</span><span class="sxs-lookup"><span data-stu-id="5926d-129">FLOAT minDepth = D3D12\_MIN\_DEPTH</span></span>

<span data-ttu-id="5926d-130">FLOAT maxDepth = \_ profondità massima \_ D3D12</span><span class="sxs-lookup"><span data-stu-id="5926d-130">FLOAT maxDepth = D3D12\_MAX\_DEPTH</span></span>

</dd> <dt>

<span data-ttu-id="5926d-131">**Viewport ~ CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="5926d-131">**~CD3DX12\_VIEWPORT()**</span></span>
</dt> <dd>

<span data-ttu-id="5926d-132">Elimina un'istanza di un viewport D3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="5926d-132">Destroys an instance of a D3DX12\_VIEWPORT.</span></span>

</dd> <dt>

<span data-ttu-id="5926d-133">**operatore const D3D12 \_ VIEWPORT& () const**</span><span class="sxs-lookup"><span data-stu-id="5926d-133">**operator const D3D12\_VIEWPORT&() const**</span></span>
</dt> <dd>

<span data-ttu-id="5926d-134">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="5926d-134">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5926d-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5926d-135">Requirements</span></span>



| <span data-ttu-id="5926d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5926d-136">Requirement</span></span> | <span data-ttu-id="5926d-137">Valore</span><span class="sxs-lookup"><span data-stu-id="5926d-137">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5926d-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5926d-138">Header</span></span><br/> | <dl> <span data-ttu-id="5926d-139"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="5926d-139"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5926d-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5926d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5926d-141">**\_Viewport D3D12**</span><span class="sxs-lookup"><span data-stu-id="5926d-141">**D3D12\_VIEWPORT**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)
</dt> <dt>

[<span data-ttu-id="5926d-142">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="5926d-142">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





