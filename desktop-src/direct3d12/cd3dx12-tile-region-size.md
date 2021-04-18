---
title: Struttura CD3DX12_TILE_REGION_SIZE (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ struttura di dimensioni dell'area del riquadro D3D12 \_ \_ .
ms.assetid: 07D2D8DE-C35C-48EE-8E9E-36545B60C594
keywords:
- Struttura CD3DX12_TILE_REGION_SIZE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_REGION_SIZE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f64046f2a7efa32af8b43adbcf7349f43b6ec3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322196"
---
# <a name="cd3dx12_tile_region_size-structure"></a><span data-ttu-id="9634b-104">\_Struttura delle \_ dimensioni dell'area del riquadro CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="9634b-104">CD3DX12\_TILE\_REGION\_SIZE structure</span></span>

<span data-ttu-id="9634b-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ dimensioni dell' \_ area \_ del riquadro D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .</span><span class="sxs-lookup"><span data-stu-id="9634b-105">A helper structure to enable easy initialization of a [**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9634b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9634b-106">Syntax</span></span>


```C++
struct CD3DX12_TILE_REGION_SIZE  : public D3D12_TILE_REGION_SIZE{
   CD3DX12_TILE_REGION_SIZE();
   explicit CD3DX12_TILE_REGION_SIZE(const D3D12_TILE_REGION_SIZE &o);
   CD3DX12_TILE_REGION_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth);
   operator const D3D12_TILE_REGION_SIZE&() const;
};
```



## <a name="members"></a><span data-ttu-id="9634b-107">Members</span><span class="sxs-lookup"><span data-stu-id="9634b-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9634b-108">**\_ \_ Dimensioni area riquadro CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="9634b-108">**CD3DX12\_TILE\_REGION\_SIZE()**</span></span>
</dt> <dd>

<span data-ttu-id="9634b-109">Crea una nuova istanza non inizializzata di una \_ dimensione dell'area del riquadro CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9634b-109">Creates a new, uninitialized, instance of a CD3DX12\_TILE\_REGION\_SIZE.</span></span>

</dd> <dt>

<span data-ttu-id="9634b-110">**dimensioni dell'area del riquadro CD3DX12 esplicite \_ \_ \_ (const D3D12 \_ dimensioni dell' \_ area \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="9634b-110">**explicit CD3DX12\_TILE\_REGION\_SIZE(const D3D12\_TILE\_REGION\_SIZE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="9634b-111">Crea una nuova istanza di una \_ dimensione dell'area del riquadro CD3DX12 \_ \_ , inizializzata con il contenuto di un'altra struttura di dimensioni dell' [**\_ area della sezione \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) .</span><span class="sxs-lookup"><span data-stu-id="9634b-111">Creates a new instance of a CD3DX12\_TILE\_REGION\_SIZE, initialized with the contents of another [**D3D12\_TILE\_REGION\_SIZE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9634b-112">**\_Dimensioni area del riquadro CD3DX12 \_ \_ (uint NumTiles, bool useBox, uint width, UINT16 Height, UInt16 Depth)**</span><span class="sxs-lookup"><span data-stu-id="9634b-112">**CD3DX12\_TILE\_REGION\_SIZE(UINT numTiles, BOOL useBox, UINT width, UINT16 height, UINT16 depth)**</span></span>
</dt> <dd>

<span data-ttu-id="9634b-113">Crea una nuova istanza di una \_ dimensione dell'area del riquadro CD3DX12 \_ \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="9634b-113">Creates a new instance of a CD3DX12\_TILE\_REGION\_SIZE, initializing the following parameters:</span></span>

<span data-ttu-id="9634b-114">NumTiles UINT</span><span class="sxs-lookup"><span data-stu-id="9634b-114">UINT numTiles</span></span>

<span data-ttu-id="9634b-115">BOOL useBox</span><span class="sxs-lookup"><span data-stu-id="9634b-115">BOOL useBox</span></span>

<span data-ttu-id="9634b-116">Lunghezza UINT</span><span class="sxs-lookup"><span data-stu-id="9634b-116">UINT width</span></span>

<span data-ttu-id="9634b-117">Altezza UINT16</span><span class="sxs-lookup"><span data-stu-id="9634b-117">UINT16 height</span></span>

<span data-ttu-id="9634b-118">Profondità UINT16</span><span class="sxs-lookup"><span data-stu-id="9634b-118">UINT16 depth</span></span>

</dd> <dt>

<span data-ttu-id="9634b-119">**operator const \_ D3D12 \_ dimensioni area del riquadro \_& () const**</span><span class="sxs-lookup"><span data-stu-id="9634b-119">**operator const D3D12\_TILE\_REGION\_SIZE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="9634b-120">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="9634b-120">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9634b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9634b-121">Requirements</span></span>



| <span data-ttu-id="9634b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9634b-122">Requirement</span></span> | <span data-ttu-id="9634b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="9634b-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9634b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9634b-124">Header</span></span><br/> | <dl> <span data-ttu-id="9634b-125"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="9634b-125"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9634b-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9634b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9634b-127">**\_ \_ Dimensioni area del riquadro D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="9634b-127">**D3D12\_TILE\_REGION\_SIZE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_region_size)
</dt> <dt>

[<span data-ttu-id="9634b-128">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="9634b-128">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





