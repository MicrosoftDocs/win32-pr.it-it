---
description: Questa struttura contiene informazioni sul firmware del dispositivo.
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: Struttura STORAGE_HW_FIRMWARE_INFO_QUERY (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO_QUERY
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: c5c4294a733a57a6735691a134f997189736def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312352"
---
# <a name="storage_hw_firmware_info_query-structure"></a><span data-ttu-id="2648f-103">\_Struttura di \_ \_ query per informazioni sul firmware HW di archiviazione \_</span><span class="sxs-lookup"><span data-stu-id="2648f-103">STORAGE\_HW\_FIRMWARE\_INFO\_QUERY structure</span></span>

<span data-ttu-id="2648f-104">Questa struttura contiene informazioni sul firmware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2648f-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="2648f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2648f-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a><span data-ttu-id="2648f-106">Members</span><span class="sxs-lookup"><span data-stu-id="2648f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2648f-107">**Versione**</span><span class="sxs-lookup"><span data-stu-id="2648f-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="2648f-108">Versione della struttura.</span><span class="sxs-lookup"><span data-stu-id="2648f-108">The version of this structure.</span></span> <span data-ttu-id="2648f-109">Deve essere impostato su sizeof (query di \_ informazioni sul firmware HW di archiviazione \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="2648f-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO\_QUERY)</span></span>

</dd> <dt>

<span data-ttu-id="2648f-110">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="2648f-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="2648f-111">Dimensioni di questa struttura come un buffer.</span><span class="sxs-lookup"><span data-stu-id="2648f-111">The size of this structure as a buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2648f-112">**Flag**</span><span class="sxs-lookup"><span data-stu-id="2648f-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="2648f-113">Flag associati alla query.</span><span class="sxs-lookup"><span data-stu-id="2648f-113">The flags associated with the query.</span></span> <span data-ttu-id="2648f-114">Di seguito sono riportati i flag che è possibile impostare in questo membro.</span><span class="sxs-lookup"><span data-stu-id="2648f-114">The following are flags that can be set in this member.</span></span>



| <span data-ttu-id="2648f-115">Flag</span><span class="sxs-lookup"><span data-stu-id="2648f-115">Flag</span></span>                                             | <span data-ttu-id="2648f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2648f-116">Description</span></span>                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2648f-117">\_controller del \_ \_ flag di richiesta del firmware HW \_ di \_ archiviazione</span><span class="sxs-lookup"><span data-stu-id="2648f-117">STORAGE\_HW\_FIRMWARE\_REQUEST\_FLAG\_CONTROLLER</span></span> | <span data-ttu-id="2648f-118">Indica che la destinazione della richiesta è diversa dalla mano/oggetto del dispositivo stesso.</span><span class="sxs-lookup"><span data-stu-id="2648f-118">Indicates that the target of the request other than the device hand/object itself.</span></span> |



 

</dd> <dt>

<span data-ttu-id="2648f-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="2648f-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="2648f-120">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="2648f-120">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2648f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2648f-121">Requirements</span></span>



| <span data-ttu-id="2648f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2648f-122">Requirement</span></span> | <span data-ttu-id="2648f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="2648f-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2648f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2648f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2648f-125">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2648f-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="2648f-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2648f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2648f-127">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="2648f-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="2648f-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2648f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2648f-129"><dt>Winioctl. h. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2648f-129"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2648f-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2648f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2648f-131">**\_attivazione del \_ firmware di archiviazione IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="2648f-131">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="2648f-132">**\_attivazione del \_ firmware \_ HW di archiviazione**</span><span class="sxs-lookup"><span data-stu-id="2648f-132">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="2648f-133">**\_download del \_ firmware di archiviazione IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="2648f-133">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="2648f-134">**\_download del \_ firmware \_ HW di archiviazione**</span><span class="sxs-lookup"><span data-stu-id="2648f-134">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="2648f-135">**\_informazioni sul \_ firmware di archiviazione \_ IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="2648f-135">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="2648f-136">**\_informazioni sul \_ firmware \_ HW di archiviazione**</span><span class="sxs-lookup"><span data-stu-id="2648f-136">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="2648f-137">**\_informazioni sugli \_ slot del firmware HW \_ di archiviazione \_**</span><span class="sxs-lookup"><span data-stu-id="2648f-137">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




