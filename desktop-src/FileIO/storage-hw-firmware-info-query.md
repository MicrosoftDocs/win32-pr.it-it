---
description: 'STORAGE_HW_FIRMWARE_INFO_QUERY: questa struttura contiene informazioni sul firmware del dispositivo.'
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: STORAGE_HW_FIRMWARE_INFO_QUERY struttura (Winioctl.h)
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
ms.openlocfilehash: ffda37d918406a696a29a9bf2903424523c3b830
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119399"
---
# <a name="storage_hw_firmware_info_query-structure"></a><span data-ttu-id="c4c01-103">STRUTTURA DI \_ QUERY DELLE INFORMAZIONI SUL FIRMWARE \_ \_ HW DI \_ ARCHIVIAZIONE</span><span class="sxs-lookup"><span data-stu-id="c4c01-103">STORAGE\_HW\_FIRMWARE\_INFO\_QUERY structure</span></span>

<span data-ttu-id="c4c01-104">Questa struttura contiene informazioni sul firmware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4c01-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4c01-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4c01-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a><span data-ttu-id="c4c01-106">Members</span><span class="sxs-lookup"><span data-stu-id="c4c01-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c4c01-107">**Versione**</span><span class="sxs-lookup"><span data-stu-id="c4c01-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="c4c01-108">Versione di questa struttura .</span><span class="sxs-lookup"><span data-stu-id="c4c01-108">The version of this structure.</span></span> <span data-ttu-id="c4c01-109">Deve essere impostato su sizeof(STORAGE \_ HW \_ FIRMWARE INFO \_ \_ QUERY)</span><span class="sxs-lookup"><span data-stu-id="c4c01-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO\_QUERY)</span></span>

</dd> <dt>

<span data-ttu-id="c4c01-110">**Size**</span><span class="sxs-lookup"><span data-stu-id="c4c01-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="c4c01-111">Dimensione di questa struttura come buffer.</span><span class="sxs-lookup"><span data-stu-id="c4c01-111">The size of this structure as a buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c4c01-112">**Flag**</span><span class="sxs-lookup"><span data-stu-id="c4c01-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="c4c01-113">Flag associati alla query.</span><span class="sxs-lookup"><span data-stu-id="c4c01-113">The flags associated with the query.</span></span> <span data-ttu-id="c4c01-114">Di seguito sono riportati i flag che possono essere impostati in questo membro.</span><span class="sxs-lookup"><span data-stu-id="c4c01-114">The following are flags that can be set in this member.</span></span>



| <span data-ttu-id="c4c01-115">Flag</span><span class="sxs-lookup"><span data-stu-id="c4c01-115">Flag</span></span>                                             | <span data-ttu-id="c4c01-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4c01-116">Description</span></span>                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c01-117">CONTROLLER DEL \_ FLAG DI RICHIESTA DEL FIRMWARE HW DI \_ \_ \_ \_ ARCHIVIAZIONE</span><span class="sxs-lookup"><span data-stu-id="c4c01-117">STORAGE\_HW\_FIRMWARE\_REQUEST\_FLAG\_CONTROLLER</span></span> | <span data-ttu-id="c4c01-118">Indica che la destinazione della richiesta è diversa dalla mano o dall'oggetto del dispositivo stesso.</span><span class="sxs-lookup"><span data-stu-id="c4c01-118">Indicates that the target of the request other than the device hand/object itself.</span></span> |



 

</dd> <dt>

<span data-ttu-id="c4c01-119">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="c4c01-119">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="c4c01-120">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="c4c01-120">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4c01-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4c01-121">Requirements</span></span>



| <span data-ttu-id="c4c01-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4c01-122">Requirement</span></span> | <span data-ttu-id="c4c01-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c4c01-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c01-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4c01-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c4c01-125">Windows 10 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c4c01-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="c4c01-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4c01-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c4c01-127">Solo app desktop di Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="c4c01-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="c4c01-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4c01-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4c01-129"><dt>Winioctl.h.h (incluso Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4c01-129"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4c01-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4c01-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4c01-131">**ATTIVAZIONE DEL FIRMWARE DI ARCHIVIAZIONE IOCTL \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c4c01-131">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="c4c01-132">**ATTIVAZIONE \_ FIRMWARE HW \_ DI \_ ARCHIVIAZIONE**</span><span class="sxs-lookup"><span data-stu-id="c4c01-132">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="c4c01-133">**DOWNLOAD DEL FIRMWARE DI ARCHIVIAZIONE IOCTL \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c4c01-133">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="c4c01-134">**DOWNLOAD DEL \_ FIRMWARE HW \_ DI \_ ARCHIVIAZIONE**</span><span class="sxs-lookup"><span data-stu-id="c4c01-134">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="c4c01-135">**IOCTL STORAGE FIRMWARE GET INFO (OTTENERE INFORMAZIONI \_ SUL FIRMWARE DI ARCHIVIAZIONE IOCTL) \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c4c01-135">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="c4c01-136">**STORAGE \_ HW FIRMWARE INFO (INFORMAZIONI SUL FIRMWARE HW \_ \_ DI ARCHIVIAZIONE)**</span><span class="sxs-lookup"><span data-stu-id="c4c01-136">**STORAGE\_HW\_FIRMWARE\_INFO**</span></span>](storage-hw-firmware-info.md)
</dt> <dt>

[<span data-ttu-id="c4c01-137">**INFORMAZIONI \_ DELLO SLOT DEL FIRMWARE HW DI \_ \_ \_ ARCHIVIAZIONE**</span><span class="sxs-lookup"><span data-stu-id="c4c01-137">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




