---
title: Enumerazione VMDVDDriveEvent (VPCCOMInterfaces. h)
description: Specifica gli eventi dell'unità DVD.
ms.assetid: 17126138-614f-42d9-937e-1aca9393557c
keywords:
- VMDVDDriveEvent enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMDVDDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 967fcd545c0ddd24d01c5dc779929ef4639c6736
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741394"
---
# <a name="vmdvddriveevent-enumeration"></a><span data-ttu-id="96f20-104">Enumerazione VMDVDDriveEvent</span><span class="sxs-lookup"><span data-stu-id="96f20-104">VMDVDDriveEvent enumeration</span></span>

<span data-ttu-id="96f20-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="96f20-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="96f20-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="96f20-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="96f20-107">Specifica gli eventi dell'unità DVD.</span><span class="sxs-lookup"><span data-stu-id="96f20-107">Specifies the DVD drive events.</span></span>

## <a name="syntax"></a><span data-ttu-id="96f20-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96f20-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDVDDriveEvent_OnInsert  = 1,
  vmDVDDriveEvent_OnEject   = 2
} VMDVDDriveEvent;
```



## <a name="constants"></a><span data-ttu-id="96f20-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="96f20-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="96f20-110"><span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**OnInsert vmDVDDriveEvent \_**</span><span class="sxs-lookup"><span data-stu-id="96f20-110"><span id="vmDVDDriveEvent_OnInsert"></span><span id="vmdvddriveevent_oninsert"></span><span id="VMDVDDRIVEEVENT_ONINSERT"></span>**vmDVDDriveEvent\_OnInsert**</span></span>
</dt> <dd>

<span data-ttu-id="96f20-111">Un'immagine ISO è collegata o un supporto reale viene inserito in un'unità host.</span><span class="sxs-lookup"><span data-stu-id="96f20-111">An ISO image is attached or real media is inserted into a host drive.</span></span>

</dd> <dt>

<span data-ttu-id="96f20-112"><span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**vmDVDDriveEvent \_ Oneject**</span><span class="sxs-lookup"><span data-stu-id="96f20-112"><span id="vmDVDDriveEvent_OnEject"></span><span id="vmdvddriveevent_oneject"></span><span id="VMDVDDRIVEEVENT_ONEJECT"></span>**vmDVDDriveEvent\_OnEject**</span></span>
</dt> <dd>

<span data-ttu-id="96f20-113">Il supporto è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="96f20-113">The media has been ejected.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96f20-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96f20-114">Requirements</span></span>



| <span data-ttu-id="96f20-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="96f20-115">Requirement</span></span> | <span data-ttu-id="96f20-116">Valore</span><span class="sxs-lookup"><span data-stu-id="96f20-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="96f20-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96f20-117">Minimum supported client</span></span><br/> | <span data-ttu-id="96f20-118">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="96f20-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96f20-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96f20-119">Minimum supported server</span></span><br/> | <span data-ttu-id="96f20-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="96f20-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="96f20-121">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="96f20-121">End of client support</span></span><br/>    | <span data-ttu-id="96f20-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="96f20-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="96f20-123">Prodotto</span><span class="sxs-lookup"><span data-stu-id="96f20-123">Product</span></span><br/>                  | <span data-ttu-id="96f20-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="96f20-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="96f20-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96f20-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="96f20-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="96f20-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96f20-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96f20-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96f20-128">**IVMDVDDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="96f20-128">**IVMDVDDriveEvents**</span></span>](ivmdvddriveevents.md)
</dt> </dl>

 

