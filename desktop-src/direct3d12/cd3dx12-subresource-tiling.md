---
title: Struttura CD3DX12_SUBRESOURCE_TILING (D3dx12. h)
description: Struttura di supporto per consentire l'inizializzazione semplificata di una \_ struttura di affiancamento della SOTTORISORSA D3D12 \_ .
ms.assetid: 102E5E25-300B-40F2-A953-E40AD7EE61AD
keywords:
- Struttura CD3DX12_SUBRESOURCE_TILING
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_TILING
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07677c8a8367f58016a0236cf0b5558b852bef01
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322198"
---
# <a name="cd3dx12_subresource_tiling-structure"></a><span data-ttu-id="4c5ff-104">\_Struttura di affiancamento di SOTTORISORSE CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="4c5ff-104">CD3DX12\_SUBRESOURCE\_TILING structure</span></span>

<span data-ttu-id="4c5ff-105">Struttura di supporto per consentire l'inizializzazione semplificata di una struttura di [**\_ \_ affiancamento della sottorisorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .</span><span class="sxs-lookup"><span data-stu-id="4c5ff-105">A helper structure to enable easy initialization of a [**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c5ff-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c5ff-106">Syntax</span></span>


```C++
struct CD3DX12_SUBRESOURCE_TILING  : public D3D12_SUBRESOURCE_TILING{
   CD3DX12_SUBRESOURCE_TILING();
   explicit CD3DX12_SUBRESOURCE_TILING(const D3D12_SUBRESOURCE_TILING &o);
   CD3DX12_SUBRESOURCE_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource);
   operator const D3D12_SUBRESOURCE_TILING&() const;
};
```



## <a name="members"></a><span data-ttu-id="4c5ff-107">Members</span><span class="sxs-lookup"><span data-stu-id="4c5ff-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="4c5ff-108">**\_Affiancamento di SOTTORISORSE CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="4c5ff-108">**CD3DX12\_SUBRESOURCE\_TILING()**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ff-109">Crea una nuova istanza non inizializzata di un \_ affiancamento della SOTTORISORSA CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="4c5ff-109">Creates a new, uninitialized, instance of a CD3DX12\_SUBRESOURCE\_TILING.</span></span>

</dd> <dt>

<span data-ttu-id="4c5ff-110">**\_affiancamento della SOTTORISORSA CD3DX12 esplicita \_ (const D3D12 \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="4c5ff-110">**explicit CD3DX12\_SUBRESOURCE\_TILING(const D3D12\_SUBRESOURCE\_TILING &o)**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ff-111">Crea una nuova istanza di un \_ affiancamento della SOTTORISORSA CD3DX12 \_ , inizializzata con il contenuto di un'altra struttura di [**\_ \_ affiancamento della sottorisorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) .</span><span class="sxs-lookup"><span data-stu-id="4c5ff-111">Creates a new instance of a CD3DX12\_SUBRESOURCE\_TILING, initialized with the contents of another [**D3D12\_SUBRESOURCE\_TILING**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4c5ff-112">**CD3DX12 \_ subresource \_ affiancamento (uint WIDTHINTILES, UInt16 HEIGHTINTILES, UInt16 DEPTHINTILES, uint startTileIndexInOverallResource)**</span><span class="sxs-lookup"><span data-stu-id="4c5ff-112">**CD3DX12\_SUBRESOURCE\_TILING(UINT widthInTiles, UINT16 heightInTiles, UINT16 depthInTiles, UINT startTileIndexInOverallResource)**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ff-113">Crea una nuova istanza di un \_ affiancamento della SOTTORISORSA CD3DX12 \_ , inizializzando i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="4c5ff-113">Creates a new instance of a CD3DX12\_SUBRESOURCE\_TILING, initializing the following parameters:</span></span>

<span data-ttu-id="4c5ff-114">WidthInTiles UINT</span><span class="sxs-lookup"><span data-stu-id="4c5ff-114">UINT widthInTiles</span></span>

<span data-ttu-id="4c5ff-115">UINT16 heightInTiles</span><span class="sxs-lookup"><span data-stu-id="4c5ff-115">UINT16 heightInTiles</span></span>

<span data-ttu-id="4c5ff-116">UINT16 depthInTiles</span><span class="sxs-lookup"><span data-stu-id="4c5ff-116">UINT16 depthInTiles</span></span>

<span data-ttu-id="4c5ff-117">StartTileIndexInOverallResource UINT</span><span class="sxs-lookup"><span data-stu-id="4c5ff-117">UINT startTileIndexInOverallResource</span></span>

</dd> <dt>

<span data-ttu-id="4c5ff-118">**operatore const D3D12 \_ sottorisorse \_& () const**</span><span class="sxs-lookup"><span data-stu-id="4c5ff-118">**operator const D3D12\_SUBRESOURCE\_TILING&() const**</span></span>
</dt> <dd>

<span data-ttu-id="4c5ff-119">Definisce il & operatore pass-by-reference per il tipo di struttura padre.</span><span class="sxs-lookup"><span data-stu-id="4c5ff-119">Defines the & pass-by-reference operator for the parent structure type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4c5ff-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c5ff-120">Requirements</span></span>



| <span data-ttu-id="4c5ff-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c5ff-121">Requirement</span></span> | <span data-ttu-id="4c5ff-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4c5ff-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4c5ff-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c5ff-123">Header</span></span><br/> | <dl> <span data-ttu-id="4c5ff-124"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c5ff-124"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c5ff-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c5ff-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c5ff-126">**\_Affiancamento di SOTTORISORSE D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="4c5ff-126">**D3D12\_SUBRESOURCE\_TILING**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_tiling)
</dt> <dt>

[<span data-ttu-id="4c5ff-127">Strutture helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="4c5ff-127">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





