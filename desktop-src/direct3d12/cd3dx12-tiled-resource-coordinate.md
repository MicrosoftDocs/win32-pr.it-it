---
title: Struttura CD3DX12_TILED_RESOURCE_COORDINATE (D3dx12. h)
description: Struttura helper per consentire l'inizializzazione semplificata di una \_ \_ struttura di coordinate delle risorse affiancate D3D12 \_ .
ms.assetid: B337ED04-E2C6-4B89-80F1-92C0854A6AF2
keywords:
- Struttura CD3DX12_TILED_RESOURCE_COORDINATE
topic_type:
- apiref
api_name:
- CD3DX12_TILED_RESOURCE_COORDINATE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 281afeab8d1172e9cae749512612129dd001161b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322186"
---
# <a name="cd3dx12_tiled_resource_coordinate-structure"></a><span data-ttu-id="971b9-104">\_ \_ Struttura delle coordinate delle risorse CD3DX12 affiancata \_</span><span class="sxs-lookup"><span data-stu-id="971b9-104">CD3DX12\_TILED\_RESOURCE\_COORDINATE structure</span></span>

<span data-ttu-id="971b9-105">Struttura helper per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ \_ coordinate delle risorse affiancate D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .</span><span class="sxs-lookup"><span data-stu-id="971b9-105">A helper structure to enable easy initialization of a [**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="971b9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="971b9-106">Syntax</span></span>


```C++
struct CD3DX12_TILED_RESOURCE_COORDINATE  : public D3D12_TILED_RESOURCE_COORDINATE{
   CD3DX12_TILED_RESOURCE_COORDINATE();
   explicit CD3DX12_TILED_RESOURCE_COORDINATE(const D3D12_TILED_RESOURCE_COORDINATE &o);
   CD3DX12_TILED_RESOURCE_COORDINATE(UINT x, UINT y, UINT z, UINT subresource);
   operator const D3D12_TILED_RESOURCE_COORDINATE&() const;
};
```



## <a name="members"></a><span data-ttu-id="971b9-107">Members</span><span class="sxs-lookup"><span data-stu-id="971b9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="971b9-108">**\_Coordinata di risorsa affiancata CD3DX12 \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="971b9-108">**CD3DX12\_TILED\_RESOURCE\_COORDINATE()**</span></span>
</dt> <dd>

<span data-ttu-id="971b9-109">Crea una nuova istanza non inizializzata di una \_ \_ coordinata di risorsa CD3DX12 affiancata \_ .</span><span class="sxs-lookup"><span data-stu-id="971b9-109">Creates a new, uninitialized, instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE.</span></span>

</dd> <dt>

<span data-ttu-id="971b9-110">**\_coordinata della risorsa affiancata CD3DX12 esplicita \_ \_ (const D3D12 di \_ risorse affiancate \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="971b9-110">**explicit CD3DX12\_TILED\_RESOURCE\_COORDINATE(const D3D12\_TILED\_RESOURCE\_COORDINATE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="971b9-111">Crea una nuova istanza di una \_ \_ coordinata di risorsa CD3DX12 affiancata \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ \_ coordinate della risorsa affiancata D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) .</span><span class="sxs-lookup"><span data-stu-id="971b9-111">Creates a new instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE, initialized with the contents of another [**D3D12\_TILED\_RESOURCE\_COORDINATE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate) structure.</span></span>

</dd> <dt>

<span data-ttu-id="971b9-112">**\_Coordinata di risorsa affiancata CD3DX12 \_ \_ (UINT x, UINT y, UINT z, uint subresource)**</span><span class="sxs-lookup"><span data-stu-id="971b9-112">**CD3DX12\_TILED\_RESOURCE\_COORDINATE(UINT x, UINT y, UINT z, UINT subresource)**</span></span>
</dt> <dd>

<span data-ttu-id="971b9-113">Crea una nuova istanza di una \_ \_ coordinata di risorsa CD3DX12 affiancata \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="971b9-113">Creates a new instance of a CD3DX12\_TILED\_RESOURCE\_COORDINATE, initializing the following parameters:</span></span>

<span data-ttu-id="971b9-114">UINT x</span><span class="sxs-lookup"><span data-stu-id="971b9-114">UINT x</span></span>

<span data-ttu-id="971b9-115">UINT y</span><span class="sxs-lookup"><span data-stu-id="971b9-115">UINT y</span></span>

<span data-ttu-id="971b9-116">UINT z</span><span class="sxs-lookup"><span data-stu-id="971b9-116">UINT z</span></span>

<span data-ttu-id="971b9-117">Sottorisorsa UINT</span><span class="sxs-lookup"><span data-stu-id="971b9-117">UINT subresource</span></span>

</dd> <dt>

<span data-ttu-id="971b9-118">**operatore const \_ D3D12 \_ \_ coordinata delle risorse& () const**</span><span class="sxs-lookup"><span data-stu-id="971b9-118">**operator const D3D12\_TILED\_RESOURCE\_COORDINATE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="971b9-119">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="971b9-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="971b9-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="971b9-120">Requirements</span></span>



| <span data-ttu-id="971b9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="971b9-121">Requirement</span></span> | <span data-ttu-id="971b9-122">Valore</span><span class="sxs-lookup"><span data-stu-id="971b9-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="971b9-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="971b9-123">Header</span></span><br/> | <dl> <span data-ttu-id="971b9-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="971b9-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="971b9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="971b9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="971b9-126">**\_Coordinata risorse D3D12 affiancata \_ \_**</span><span class="sxs-lookup"><span data-stu-id="971b9-126">**D3D12\_TILED\_RESOURCE\_COORDINATE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tiled_resource_coordinate)
</dt> <dt>

[<span data-ttu-id="971b9-127">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="971b9-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





