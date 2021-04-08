---
title: Enumerazione vmFloppyDriveEvent (VPCCOMInterfaces. h)
description: Specifica gli eventi dell'unità floppy.
ms.assetid: 31d0c748-609a-4e03-8b5c-0a17a2587242
keywords:
- vmFloppyDriveEvent enumerazione PC virtuale
topic_type:
- apiref
api_name:
- vmFloppyDriveEvent
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11b1485f91264713cf96a4f95cab8286261eea4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743079"
---
# <a name="vmfloppydriveevent-enumeration"></a><span data-ttu-id="8389e-104">Enumerazione vmFloppyDriveEvent</span><span class="sxs-lookup"><span data-stu-id="8389e-104">vmFloppyDriveEvent enumeration</span></span>

<span data-ttu-id="8389e-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8389e-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8389e-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8389e-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8389e-107">Specifica gli eventi dell'unità floppy.</span><span class="sxs-lookup"><span data-stu-id="8389e-107">Specifies the floppy drive events.</span></span>

## <a name="syntax"></a><span data-ttu-id="8389e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8389e-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDriveEvent_OnInsert  = 1,
  vmFloppyDriveEvent_OnEject   = 2
} vmFloppyDriveEvent;
```



## <a name="constants"></a><span data-ttu-id="8389e-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="8389e-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8389e-110"><span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**OnInsert vmFloppyDriveEvent \_**</span><span class="sxs-lookup"><span data-stu-id="8389e-110"><span id="vmFloppyDriveEvent_OnInsert"></span><span id="vmfloppydriveevent_oninsert"></span><span id="VMFLOPPYDRIVEEVENT_ONINSERT"></span>**vmFloppyDriveEvent\_OnInsert**</span></span>
</dt> <dd>

<span data-ttu-id="8389e-111">Un'immagine del disco floppy è collegata o un supporto reale viene inserito in un'unità host.</span><span class="sxs-lookup"><span data-stu-id="8389e-111">A floppy disk image is attached or real media is inserted into a host drive.</span></span>

</dd> <dt>

<span data-ttu-id="8389e-112"><span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**vmFloppyDriveEvent \_ Oneject**</span><span class="sxs-lookup"><span data-stu-id="8389e-112"><span id="vmFloppyDriveEvent_OnEject"></span><span id="vmfloppydriveevent_oneject"></span><span id="VMFLOPPYDRIVEEVENT_ONEJECT"></span>**vmFloppyDriveEvent\_OnEject**</span></span>
</dt> <dd>

<span data-ttu-id="8389e-113">Il supporto è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="8389e-113">Media has been ejected.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8389e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8389e-114">Requirements</span></span>



| <span data-ttu-id="8389e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8389e-115">Requirement</span></span> | <span data-ttu-id="8389e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8389e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8389e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8389e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8389e-118">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8389e-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8389e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8389e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8389e-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8389e-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8389e-121">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8389e-121">End of client support</span></span><br/>    | <span data-ttu-id="8389e-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8389e-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8389e-123">Prodotto</span><span class="sxs-lookup"><span data-stu-id="8389e-123">Product</span></span><br/>                  | <span data-ttu-id="8389e-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8389e-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8389e-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8389e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8389e-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8389e-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8389e-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8389e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8389e-128">**IVMFloppyDriveEvents**</span><span class="sxs-lookup"><span data-stu-id="8389e-128">**IVMFloppyDriveEvents**</span></span>](ivmfloppydriveevents.md)
</dt> </dl>

 

