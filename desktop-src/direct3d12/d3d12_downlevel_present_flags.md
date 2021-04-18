---
title: Enumerazione D3D12_DOWNLEVEL_PRESENT_FLAGS
description: Flag passati al metodo ID3D12CommandQueueDownlevel::P reinviate.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
topic_type:
- APIRef
api_name:
- D3D12_DOWNLEVEL_PRESENT_FLAGS
api_type:
- HeaderDef
ms.openlocfilehash: 1ce1536945748bae09fc7a0981c14c076fc6394e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322181"
---
# <a name="d3d12_downlevel_present_flags-enumeration"></a><span data-ttu-id="7f28b-103">\_ \_ Enumerazione flag presenti di livello inferiore D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="7f28b-103">D3D12\_DOWNLEVEL\_PRESENT\_FLAGS enumeration</span></span>

<span data-ttu-id="7f28b-104">Flag passati alla funzione [**ID3D12CommandQueueDownlevel::P reinviato**](id3d12commandqueuedownlevel-present.md) per modificare il comportamento.</span><span class="sxs-lookup"><span data-stu-id="7f28b-104">Flags passed to the [**ID3D12CommandQueueDownlevel::Present**](id3d12commandqueuedownlevel-present.md) function to modify behavior.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f28b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f28b-105">Syntax</span></span>

```cpp
enum D3D12_DOWNLEVEL_PRESENT_FLAGS
{
    D3D12_DOWNLEVEL_PRESENT_FLAG_NONE = 0,
    D3D12_DOWNLEVEL_PRESENT_FLAG_WAIT_FOR_VBLANK = 1
};
```

## <a name="constants"></a><span data-ttu-id="7f28b-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="7f28b-106">Constants</span></span>

<span data-ttu-id="7f28b-107">**D3D12 \_ il \_ flag presente di livello inferiore \_ \_ None**</span><span class="sxs-lookup"><span data-stu-id="7f28b-107">**D3D12\_DOWNLEVEL\_PRESENT\_FLAG\_NONE**</span></span>

<span data-ttu-id="7f28b-108">Non è stata selezionata alcuna opzione.</span><span class="sxs-lookup"><span data-stu-id="7f28b-108">No options selected.</span></span>

<span data-ttu-id="7f28b-109">**Il \_ \_ flag presente D3D12 di livello inferiore \_ attende il \_ \_ \_ VBLANK**</span><span class="sxs-lookup"><span data-stu-id="7f28b-109">**D3D12\_DOWNLEVEL\_PRESENT\_FLAG\_WAIT\_FOR\_VBLANK**</span></span>

<span data-ttu-id="7f28b-110">L'operazione **corrente** non verrà eseguita fino a quando non si verifica un vsync dall'ultima volta in cui si **presenta** ed.</span><span class="sxs-lookup"><span data-stu-id="7f28b-110">The **Present** operation won't be done until a VSync has occurred since the last time you **Present** ed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f28b-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f28b-111">Requirements</span></span>

| <span data-ttu-id="7f28b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f28b-112">Requirement</span></span> | <span data-ttu-id="7f28b-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7f28b-113">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="7f28b-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f28b-114">Header</span></span> | <span data-ttu-id="7f28b-115">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="7f28b-115">d3d12downlevel.h</span></span> |
| <span data-ttu-id="7f28b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="7f28b-116">DLL</span></span>    | <span data-ttu-id="7f28b-117">D3D12.dll (solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="7f28b-117">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="7f28b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f28b-118">See also</span></span>
* [<span data-ttu-id="7f28b-119">ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="7f28b-119">ID3D12CommandQueueDownlevel</span></span>](id3d12commandqueuedownlevel.md)
* [<span data-ttu-id="7f28b-120">Enumerazioni Direct3D 12 su Windows 7</span><span class="sxs-lookup"><span data-stu-id="7f28b-120">Direct3D 12 On Windows 7 enumerations</span></span>](direct3d-12on7-enumerations.md)
* [<span data-ttu-id="7f28b-121">Guida di riferimento a Direct3D 12 per Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="7f28b-121">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="7f28b-122">Direct3D 12 in Windows 7</span><span class="sxs-lookup"><span data-stu-id="7f28b-122">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
