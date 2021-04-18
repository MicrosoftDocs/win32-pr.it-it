---
title: Struttura CD3DX12_PACKED_MIP_INFO (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di \_ una \_ struttura di informazioni MIP compresso D3D12 \_ .
ms.assetid: B3549D78-C354-48FC-A012-1F835DBD585E
keywords:
- Struttura CD3DX12_PACKED_MIP_INFO
topic_type:
- apiref
api_name:
- CD3DX12_PACKED_MIP_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4565bbac6189cffc5358213437463b4abc0322
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322260"
---
# <a name="cd3dx12_packed_mip_info-structure"></a><span data-ttu-id="6f60e-104">\_Struttura di \_ informazioni MIP compresso \_ CD3DX12</span><span class="sxs-lookup"><span data-stu-id="6f60e-104">CD3DX12\_PACKED\_MIP\_INFO structure</span></span>

<span data-ttu-id="6f60e-105">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ \_ informazioni MIP compresso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .</span><span class="sxs-lookup"><span data-stu-id="6f60e-105">A helper structure to enable easy initialization of a [**D3D12\_PACKED\_MIP\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f60e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6f60e-106">Syntax</span></span>


```C++
struct CD3DX12_PACKED_MIP_INFO  : public D3D12_PACKED_MIP_INFO{
   CD3DX12_PACKED_MIP_INFO();
   explicit CD3DX12_PACKED_MIP_INFO(const D3D12_PACKED_MIP_INFO &o);
   CD3DX12_PACKED_MIP_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource);
   operator const D3D12_PACKED_MIP_INFO&() const;
};
```



## <a name="members"></a><span data-ttu-id="6f60e-107">Members</span><span class="sxs-lookup"><span data-stu-id="6f60e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="6f60e-108">**\_ \_ Informazioni MIP compresse CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="6f60e-108">**CD3DX12\_PACKED\_MIP\_INFO()**</span></span>
</dt> <dd>

<span data-ttu-id="6f60e-109">Crea un'istanza nuova, non inizializzata, di un CD3DX12 \_ di \_ informazioni MIP compresso \_ .</span><span class="sxs-lookup"><span data-stu-id="6f60e-109">Creates a new, uninitialized, instance of a CD3DX12\_PACKED\_MIP\_INFO.</span></span>

</dd> <dt>

<span data-ttu-id="6f60e-110">**informazioni sul \_ MIP compresse CD3DX12 esplicite \_ \_ (const D3D12- \_ \_ informazioni MIP compresse \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="6f60e-110">**explicit CD3DX12\_PACKED\_MIP\_INFO(const D3D12\_PACKED\_MIP\_INFO &o)**</span></span>
</dt> <dd>

<span data-ttu-id="6f60e-111">Crea una nuova istanza di un' \_ \_ informazione MIP compressa CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ \_ informazioni MIP compresso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) .</span><span class="sxs-lookup"><span data-stu-id="6f60e-111">Creates a new instance of a CD3DX12\_PACKED\_MIP\_INFO, initialized with the contents of another [**D3D12\_PACKED\_MIP\_INFO**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6f60e-112">**\_ \_ Informazioni MIP compresse CD3DX12 \_ (UINT8 NumStandardMips, Uint8 NumPackedMips, UINT NumTilesForPackedMips, uint startTileIndexInOverallResource)**</span><span class="sxs-lookup"><span data-stu-id="6f60e-112">**CD3DX12\_PACKED\_MIP\_INFO(UINT8 numStandardMips, UINT8 numPackedMips, UINT numTilesForPackedMips, UINT startTileIndexInOverallResource)**</span></span>
</dt> <dd>

<span data-ttu-id="6f60e-113">Crea una nuova istanza di un CD3DX12 \_ di \_ dati MIP compresso \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="6f60e-113">Creates a new instance of a CD3DX12\_PACKED\_MIP\_INFO, initializing the following parameters:</span></span>

<span data-ttu-id="6f60e-114">NumStandardMips UINT8</span><span class="sxs-lookup"><span data-stu-id="6f60e-114">UINT8 numStandardMips</span></span>

<span data-ttu-id="6f60e-115">NumPackedMips UINT8</span><span class="sxs-lookup"><span data-stu-id="6f60e-115">UINT8 numPackedMips</span></span>

<span data-ttu-id="6f60e-116">NumTilesForPackedMips UINT</span><span class="sxs-lookup"><span data-stu-id="6f60e-116">UINT numTilesForPackedMips</span></span>

<span data-ttu-id="6f60e-117">StartTileIndexInOverallResource UINT</span><span class="sxs-lookup"><span data-stu-id="6f60e-117">UINT startTileIndexInOverallResource</span></span>

</dd> <dt>

<span data-ttu-id="6f60e-118">**operator const D3D12 \_ compresse di \_ \_ informazioni& () const**</span><span class="sxs-lookup"><span data-stu-id="6f60e-118">**operator const D3D12\_PACKED\_MIP\_INFO&() const**</span></span>
</dt> <dd>

<span data-ttu-id="6f60e-119">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="6f60e-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f60e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6f60e-120">Requirements</span></span>



| <span data-ttu-id="6f60e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f60e-121">Requirement</span></span> | <span data-ttu-id="6f60e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="6f60e-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6f60e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6f60e-123">Header</span></span><br/> | <dl> <span data-ttu-id="6f60e-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f60e-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f60e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6f60e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f60e-126">**\_ \_ Informazioni MIP compresse \_ D3D12**</span><span class="sxs-lookup"><span data-stu-id="6f60e-126">**D3D12\_PACKED\_MIP\_INFO**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_packed_mip_info)
</dt> <dt>

[<span data-ttu-id="6f60e-127">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="6f60e-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





