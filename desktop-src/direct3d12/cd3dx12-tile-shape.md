---
title: Struttura CD3DX12_TILE_SHAPE (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura di forma del riquadro D3D12 \_ .
ms.assetid: 0A5963F1-8CE5-4B03-B69F-83B2B801CC21
keywords:
- Struttura CD3DX12_TILE_SHAPE
topic_type:
- apiref
api_name:
- CD3DX12_TILE_SHAPE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 998a14e1bd4898d83d049ea50bc056abaeb68544
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322192"
---
# <a name="cd3dx12_tile_shape-structure"></a><span data-ttu-id="32ca1-104">\_ \_ Struttura forma sezione CD3DX12</span><span class="sxs-lookup"><span data-stu-id="32ca1-104">CD3DX12\_TILE\_SHAPE structure</span></span>

<span data-ttu-id="32ca1-105">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ forma del riquadro D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .</span><span class="sxs-lookup"><span data-stu-id="32ca1-105">A helper structure to enable easy initialization of a [**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="32ca1-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32ca1-106">Syntax</span></span>


```C++
struct CD3DX12_TILE_SHAPE  : public D3D12_TILE_SHAPE{
   CD3DX12_TILE_SHAPE();
   explicit CD3DX12_TILE_SHAPE(const D3D12_TILE_SHAPE &o);
   CD3DX12_TILE_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels);
   operator const D3D12_TILE_SHAPE&() const;
};
```



## <a name="members"></a><span data-ttu-id="32ca1-107">Members</span><span class="sxs-lookup"><span data-stu-id="32ca1-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="32ca1-108">**\_Forma riquadro CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="32ca1-108">**CD3DX12\_TILE\_SHAPE()**</span></span>
</dt> <dd>

<span data-ttu-id="32ca1-109">Crea una nuova istanza non inizializzata di una \_ forma affiancata CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="32ca1-109">Creates a new, uninitialized, instance of a CD3DX12\_TILE\_SHAPE.</span></span>

</dd> <dt>

<span data-ttu-id="32ca1-110">**forma riquadro CD3DX12 esplicita \_ \_ (const D3D12 \_ forma affiancata \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="32ca1-110">**explicit CD3DX12\_TILE\_SHAPE(const D3D12\_TILE\_SHAPE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="32ca1-111">Crea una nuova istanza di una \_ forma affiancata CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura della [**\_ \_ forma affiancata D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) .</span><span class="sxs-lookup"><span data-stu-id="32ca1-111">Creates a new instance of a CD3DX12\_TILE\_SHAPE, initialized with the contents of another [**D3D12\_TILE\_SHAPE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape) structure.</span></span>

</dd> <dt>

<span data-ttu-id="32ca1-112">**\_Forma riquadro CD3DX12 \_ (uint WIDTHINTEXELS, uint HEIGHTINTEXELS, uint depthInTexels)**</span><span class="sxs-lookup"><span data-stu-id="32ca1-112">**CD3DX12\_TILE\_SHAPE(UINT widthInTexels, UINT heightInTexels, UINT depthInTexels)**</span></span>
</dt> <dd>

<span data-ttu-id="32ca1-113">Crea una nuova istanza di una \_ forma affiancata CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="32ca1-113">Creates a new instance of a CD3DX12\_TILE\_SHAPE, initializing the following parameters:</span></span>

<span data-ttu-id="32ca1-114">WidthInTexels UINT</span><span class="sxs-lookup"><span data-stu-id="32ca1-114">UINT widthInTexels</span></span>

<span data-ttu-id="32ca1-115">HeightInTexels UINT</span><span class="sxs-lookup"><span data-stu-id="32ca1-115">UINT heightInTexels</span></span>

<span data-ttu-id="32ca1-116">DepthInTexels UINT</span><span class="sxs-lookup"><span data-stu-id="32ca1-116">UINT depthInTexels</span></span>

</dd> <dt>

<span data-ttu-id="32ca1-117">**operatore const \_ D3D12 \_ forma riquadro& () const**</span><span class="sxs-lookup"><span data-stu-id="32ca1-117">**operator const D3D12\_TILE\_SHAPE&() const**</span></span>
</dt> <dd>

<span data-ttu-id="32ca1-118">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="32ca1-118">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32ca1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32ca1-119">Requirements</span></span>



| <span data-ttu-id="32ca1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="32ca1-120">Requirement</span></span> | <span data-ttu-id="32ca1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="32ca1-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="32ca1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32ca1-122">Header</span></span><br/> | <dl> <span data-ttu-id="32ca1-123"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="32ca1-123"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32ca1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32ca1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32ca1-125">**\_Forma riquadro \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="32ca1-125">**D3D12\_TILE\_SHAPE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_tile_shape)
</dt> <dt>

[<span data-ttu-id="32ca1-126">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="32ca1-126">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





