---
title: Enumerazione VMVirtualPCEvent (VPCCOMInterfaces. h)
description: Specifica gli eventi di Windows Virtual PC.
ms.assetid: 3b239cd0-d922-42de-8bcc-51f625c0d8b0
keywords:
- VMVirtualPCEvent enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMVirtualPCEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4de7ecb639d0b62165dec691d522bed8116670c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048752"
---
# <a name="vmvirtualpcevent-enumeration"></a><span data-ttu-id="1370a-104">Enumerazione VMVirtualPCEvent</span><span class="sxs-lookup"><span data-stu-id="1370a-104">VMVirtualPCEvent enumeration</span></span>

<span data-ttu-id="1370a-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1370a-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1370a-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1370a-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1370a-107">Specifica gli eventi di Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="1370a-107">Specifies the Windows Virtual PC events.</span></span>

## <a name="syntax"></a><span data-ttu-id="1370a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1370a-108">Syntax</span></span>


```C++
typedef enum  { 
  vmVirtualPCEvent_VMStateChange  = 2,
  vmVirtualPCEvent_EventLogged    = 3
} VMVirtualPCEvent;
```



## <a name="constants"></a><span data-ttu-id="1370a-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="1370a-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1370a-110"><span id="vmVirtualPCEvent_VMStateChange"></span><span id="vmvirtualpcevent_vmstatechange"></span><span id="VMVIRTUALPCEVENT_VMSTATECHANGE"></span>**\_VMStateChange vmVirtualPCEvent**</span><span class="sxs-lookup"><span data-stu-id="1370a-110"><span id="vmVirtualPCEvent_VMStateChange"></span><span id="vmvirtualpcevent_vmstatechange"></span><span id="VMVIRTUALPCEVENT_VMSTATECHANGE"></span>**vmVirtualPCEvent\_VMStateChange**</span></span>
</dt> <dd>

<span data-ttu-id="1370a-111">Lo stato di una macchina virtuale è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="1370a-111">A virtual machine's state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="1370a-112"><span id="vmVirtualPCEvent_EventLogged"></span><span id="vmvirtualpcevent_eventlogged"></span><span id="VMVIRTUALPCEVENT_EVENTLOGGED"></span>**\_EventLogged vmVirtualPCEvent**</span><span class="sxs-lookup"><span data-stu-id="1370a-112"><span id="vmVirtualPCEvent_EventLogged"></span><span id="vmvirtualpcevent_eventlogged"></span><span id="VMVIRTUALPCEVENT_EVENTLOGGED"></span>**vmVirtualPCEvent\_EventLogged**</span></span>
</dt> <dd>

<span data-ttu-id="1370a-113">Virtual PC ha registrato un evento.</span><span class="sxs-lookup"><span data-stu-id="1370a-113">Virtual PC has logged an event.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1370a-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1370a-114">Requirements</span></span>



| <span data-ttu-id="1370a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1370a-115">Requirement</span></span> | <span data-ttu-id="1370a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1370a-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1370a-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1370a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1370a-118">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1370a-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1370a-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1370a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1370a-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1370a-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1370a-121">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="1370a-121">End of client support</span></span><br/>    | <span data-ttu-id="1370a-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1370a-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1370a-123">Prodotto</span><span class="sxs-lookup"><span data-stu-id="1370a-123">Product</span></span><br/>                  | <span data-ttu-id="1370a-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1370a-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1370a-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1370a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1370a-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1370a-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1370a-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1370a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1370a-128">**IVMVirtualPCEvents**</span><span class="sxs-lookup"><span data-stu-id="1370a-128">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

