---
description: Questa struttura contiene informazioni su uno slot in un dispositivo.
ms.assetid: 37475351-DE0F-4B80-B26B-1482FBCC16CD
title: Struttura STORAGE_HW_FIRMWARE_SLOT_INFO (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_SLOT_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: afb38e3dc866f31b6ada6797dcb611bce1ac81a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308214"
---
# <a name="storage_hw_firmware_slot_info-structure"></a><span data-ttu-id="991f5-103">\_Struttura di \_ \_ informazioni slot del firmware HW di archiviazione \_</span><span class="sxs-lookup"><span data-stu-id="991f5-103">STORAGE\_HW\_FIRMWARE\_SLOT\_INFO structure</span></span>

<span data-ttu-id="991f5-104">Questa struttura contiene informazioni su uno slot in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="991f5-104">This structure contains information about a slot on a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="991f5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="991f5-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_SLOT_INFO {
  DWORD Version;
  DWORD Size;
  BYTE  SlotNumber;
  BYTE  ReadOnly  :1;
  BYTE  Reserved0  :7;
  BYTE  Reserved1[6];
  BYTE  Revision[STORAGE_HW_FIRMWARE_REVISION_LENGTH];
} STORAGE_HW_FIRMWARE_SLOT_INFO, *PSTORAGE_HW_FIRMWARE_SLOT_INFO;
```



## <a name="members"></a><span data-ttu-id="991f5-106">Members</span><span class="sxs-lookup"><span data-stu-id="991f5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="991f5-107">**Versione**</span><span class="sxs-lookup"><span data-stu-id="991f5-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="991f5-108">Versione della struttura.</span><span class="sxs-lookup"><span data-stu-id="991f5-108">The version of this structure.</span></span> <span data-ttu-id="991f5-109">Deve essere impostato su sizeof ( \_ informazioni slot del firmware HW di archiviazione \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="991f5-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_SLOT\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="991f5-110">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="991f5-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="991f5-111">Dimensione della struttura.</span><span class="sxs-lookup"><span data-stu-id="991f5-111">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="991f5-112">**SlotNumber**</span><span class="sxs-lookup"><span data-stu-id="991f5-112">**SlotNumber**</span></span>
</dt> <dd>

<span data-ttu-id="991f5-113">Numero di slot dello slot.</span><span class="sxs-lookup"><span data-stu-id="991f5-113">The slot number of this slot.</span></span>

</dd> <dt>

<span data-ttu-id="991f5-114">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="991f5-114">**ReadOnly**</span></span>
</dt> <dd>

<span data-ttu-id="991f5-115">Indica se questo slot è di sola lettura o meno.</span><span class="sxs-lookup"><span data-stu-id="991f5-115">Indicates whether this slot is read-only or not.</span></span>

</dd> <dt>

<span data-ttu-id="991f5-116">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="991f5-116">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="991f5-117">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="991f5-117">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="991f5-118">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="991f5-118">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="991f5-119">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="991f5-119">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="991f5-120">**Revisione**</span><span class="sxs-lookup"><span data-stu-id="991f5-120">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="991f5-121">Revisione del firmware in questo slot.</span><span class="sxs-lookup"><span data-stu-id="991f5-121">The revision of the firmware on this slot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="991f5-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="991f5-122">Requirements</span></span>



| <span data-ttu-id="991f5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="991f5-123">Requirement</span></span> | <span data-ttu-id="991f5-124">Valore</span><span class="sxs-lookup"><span data-stu-id="991f5-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="991f5-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="991f5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="991f5-126">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="991f5-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="991f5-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="991f5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="991f5-128">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="991f5-128">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="991f5-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="991f5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="991f5-130"><dt>Winioctl. h. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="991f5-130"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="991f5-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="991f5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="991f5-132">**\_attivazione del \_ firmware di archiviazione IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="991f5-132">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="991f5-133">**\_attivazione del \_ firmware \_ HW di archiviazione**</span><span class="sxs-lookup"><span data-stu-id="991f5-133">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="991f5-134">**\_download del \_ firmware di archiviazione IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="991f5-134">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="991f5-135">**\_download del \_ firmware \_ HW di archiviazione**</span><span class="sxs-lookup"><span data-stu-id="991f5-135">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="991f5-136">**\_informazioni sul \_ firmware di archiviazione \_ IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="991f5-136">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="991f5-137">**\_informazioni sul \_ firmware \_ HW di archiviazione**</span><span class="sxs-lookup"><span data-stu-id="991f5-137">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="991f5-138">**\_query sulle \_ informazioni del firmware HW \_ di archiviazione \_**</span><span class="sxs-lookup"><span data-stu-id="991f5-138">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> </dl>

 

 




