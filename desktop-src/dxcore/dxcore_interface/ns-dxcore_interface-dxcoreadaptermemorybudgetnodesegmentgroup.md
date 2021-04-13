---
title: DXCoreAdapterMemoryBudgetNodeSegmentGroup
description: Descrive un gruppo di segmenti di memoria per un adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c583b746b304232fc65c4281f67b0190b2d24c3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399168"
---
# <a name="dxcoreadaptermemorybudgetnodesegmentgroup-structure"></a><span data-ttu-id="bc19f-103">Struttura DXCoreAdapterMemoryBudgetNodeSegmentGroup</span><span class="sxs-lookup"><span data-stu-id="bc19f-103">DXCoreAdapterMemoryBudgetNodeSegmentGroup structure</span></span>

<span data-ttu-id="bc19f-104">Descrive un gruppo di segmenti di memoria per un adapter.</span><span class="sxs-lookup"><span data-stu-id="bc19f-104">Describes a memory segment group for an adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc19f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc19f-105">Syntax</span></span>

```cpp
struct DXCoreAdapterMemoryBudgetNodeSegmentGroup
{
  uint32_t nodeIndex;
  DXCoreSegmentGroup segmentGroup;
};
```

## <a name="members"></a><span data-ttu-id="bc19f-106">Members</span><span class="sxs-lookup"><span data-stu-id="bc19f-106">Members</span></span>

### <a name="nodeindex"></a><span data-ttu-id="bc19f-107">nodeIndex</span><span class="sxs-lookup"><span data-stu-id="bc19f-107">nodeIndex</span></span>

<span data-ttu-id="bc19f-108">Tipo: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="bc19f-108">Type: **uint32_t**</span></span>

<span data-ttu-id="bc19f-109">Specifica la scheda fisica del dispositivo per la quale vengono eseguite query sulle informazioni sulla memoria dell'adapter.</span><span class="sxs-lookup"><span data-stu-id="bc19f-109">Specifies the device's physical adapter for which the adapter memory information is queried.</span></span> <span data-ttu-id="bc19f-110">Per l'operazione a singolo adapter, impostare su zero.</span><span class="sxs-lookup"><span data-stu-id="bc19f-110">For single-adapter operation, set this to zero.</span></span> <span data-ttu-id="bc19f-111">Se sono presenti più nodi dell'adapter, impostarlo sull'indice del nodo (scheda fisica del dispositivo) per cui si desidera eseguire una query per le informazioni sulla memoria dell'adapter (vedere [sistemi a più schede](../../direct3d12/multi-engine.md)).</span><span class="sxs-lookup"><span data-stu-id="bc19f-111">If there are multiple adapter nodes, then set this to the index of the node (the device's physical adapter) for which you want to query for adapter memory information (see [Multi-adapter systems](../../direct3d12/multi-engine.md)).</span></span>

### <a name="segmentgroup"></a><span data-ttu-id="bc19f-112">segmentGroup</span><span class="sxs-lookup"><span data-stu-id="bc19f-112">segmentGroup</span></span>

<span data-ttu-id="bc19f-113">Tipo: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**</span><span class="sxs-lookup"><span data-stu-id="bc19f-113">Type: **[DXCoreSegmentGroup](./ne-dxcore_interface-dxcoresegmentgroup.md)**</span></span>

<span data-ttu-id="bc19f-114">Specifica il raggruppamento del segmento di memoria dell'adapter su cui si desidera eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="bc19f-114">Specifies the adapter memory segment grouping that you want to query about.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc19f-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc19f-115">See also</span></span>

[<span data-ttu-id="bc19f-116">Riferimento a DXCore</span><span class="sxs-lookup"><span data-stu-id="bc19f-116">DXCore Reference</span></span>](../dxcore-reference.md)

[<span data-ttu-id="bc19f-117">Uso di DXCore per enumerare gli adapter</span><span class="sxs-lookup"><span data-stu-id="bc19f-117">Using DXCore to enumerate adapters</span></span>](../dxcore-enum-adapters.md)

[<span data-ttu-id="bc19f-118">Sistemi con più adapter</span><span class="sxs-lookup"><span data-stu-id="bc19f-118">Multi-adapter systems</span></span>](../../direct3d12/multi-engine.md)