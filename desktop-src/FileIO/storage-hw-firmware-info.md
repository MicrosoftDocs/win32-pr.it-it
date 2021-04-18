---
description: Questa struttura contiene informazioni sul firmware del dispositivo.
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: Struttura STORAGE_HW_FIRMWARE_INFO (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: 5d611df1708059b0ee636a64f55026caf8801fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316769"
---
# <a name="storage_hw_firmware_info-structure"></a><span data-ttu-id="29fdb-103">\_Struttura delle \_ informazioni del firmware HW di archiviazione \_</span><span class="sxs-lookup"><span data-stu-id="29fdb-103">STORAGE\_HW\_FIRMWARE\_INFO structure</span></span>

<span data-ttu-id="29fdb-104">Questa struttura contiene informazioni sul firmware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29fdb-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="29fdb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29fdb-105">Syntax</span></span>


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO {
  DWORD                         Version;
  DWORD                         Size;
  BYTE                          SupportUpgrade  :1;
  BYTE                          Reserved0  :7;
  BYTE                          SlotCount;
  BYTE                          ActiveSlot;
  BYTE                          PendingActivateSlot;
  BOOLEAN                       FirmwareShared;
  BYTE                          Reserved[3];
  DWORD                         ImagePayloadAlignment;
  DWORD                         ImagePayloadMaxSize;
  STORAGE_HW_FIRMWARE_SLOT_INFO Slot[ANYSIZE_ARRAY];
} STORAGE_HW_FIRMWARE_INFO, *PSTORAGE_HW_FIRMWARE_INFO;
```



## <a name="members"></a><span data-ttu-id="29fdb-106">Members</span><span class="sxs-lookup"><span data-stu-id="29fdb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="29fdb-107">**Versione**</span><span class="sxs-lookup"><span data-stu-id="29fdb-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="29fdb-108">Versione della struttura.</span><span class="sxs-lookup"><span data-stu-id="29fdb-108">The version of this structure.</span></span> <span data-ttu-id="29fdb-109">Deve essere impostato su sizeof (informazioni sul \_ firmware HW di archiviazione \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="29fdb-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="29fdb-110">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="29fdb-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="29fdb-111">Dimensione della struttura come buffer, incluso lo slot.</span><span class="sxs-lookup"><span data-stu-id="29fdb-111">The size of this structure as a buffer including slot.</span></span>

</dd> <dt>

<span data-ttu-id="29fdb-112">**SupportUpgrade**</span><span class="sxs-lookup"><span data-stu-id="29fdb-112">**SupportUpgrade**</span></span>
</dt> <dd>

<span data-ttu-id="29fdb-113">Indica che il firmware supporta un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="29fdb-113">Indicates that this firmware supports an upgrade.</span></span>

</dd> <dt>

<span data-ttu-id="29fdb-114">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="29fdb-114">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="29fdb-115">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="29fdb-115">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="29fdb-116">**SlotCount**</span><span class="sxs-lookup"><span data-stu-id="29fdb-116">**SlotCount**</span></span>
</dt> <dd>

<span data-ttu-id="29fdb-117">Il numero di slot del firmware nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29fdb-117">The number of firmware slots on the device.</span></span> <span data-ttu-id="29fdb-118">Si tratta della dimensione della matrice di slot.</span><span class="sxs-lookup"><span data-stu-id="29fdb-118">This is the dimension of the Slot array.</span></span>

> [!Note]  
> <span data-ttu-id="29fdb-119">Alcuni dispositivi possono archiviare più di un'immagine del firmware, se hanno più di 1 slot del firmware.</span><span class="sxs-lookup"><span data-stu-id="29fdb-119">Some devices can store more than 1 firmware image, if they have more than 1 firmware slot.</span></span>

 

</dd> <dt>

<span data-ttu-id="29fdb-120">**ActiveSlot**</span><span class="sxs-lookup"><span data-stu-id="29fdb-120">**ActiveSlot**</span></span>
</dt> <dd>

<span data-ttu-id="29fdb-121">Slot del firmware che contiene l'immagine del firmware attualmente attivo o in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="29fdb-121">The firmware slot containing the currently active/running firmware image.</span></span>

</dd> <dt>

<span data-ttu-id="29fdb-122">**PendingActivateSlot**</span><span class="sxs-lookup"><span data-stu-id="29fdb-122">**PendingActivateSlot**</span></span>
</dt> <dd>

<span data-ttu-id="29fdb-123">Slot del firmware in attesa di attivazione.</span><span class="sxs-lookup"><span data-stu-id="29fdb-123">The firmware slot that is pending activation.</span></span>

</dd> <dt>

<span data-ttu-id="29fdb-124">**FirmwareShared**</span><span class="sxs-lookup"><span data-stu-id="29fdb-124">**FirmwareShared**</span></span>
</dt> <dd>

<span data-ttu-id="29fdb-125">Indica che il firmware si applica sia al dispositivo che al controller/adattatore, ad esempio NVMe SSD.</span><span class="sxs-lookup"><span data-stu-id="29fdb-125">Indicates that the firmware applies to both the device and controller/adapter, e.g. NVMe SSD.</span></span>

</dd> <dt>

<span data-ttu-id="29fdb-126">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="29fdb-126">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="29fdb-127">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="29fdb-127">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="29fdb-128">**ImagePayloadAlignment**</span><span class="sxs-lookup"><span data-stu-id="29fdb-128">**ImagePayloadAlignment**</span></span>
</dt> <dd>

<span data-ttu-id="29fdb-129">Allineamento del payload dell'immagine, in numero di byte.</span><span class="sxs-lookup"><span data-stu-id="29fdb-129">The alignment of the image payload, in number of bytes.</span></span> <span data-ttu-id="29fdb-130">Il valore massimo è la dimensione della pagina \_ .</span><span class="sxs-lookup"><span data-stu-id="29fdb-130">The maximum is PAGE\_SIZE.</span></span> <span data-ttu-id="29fdb-131">La dimensione di trasferimento è un mutliple di queste dimensioni.</span><span class="sxs-lookup"><span data-stu-id="29fdb-131">The transfer size is a mutliple of this size.</span></span> <span data-ttu-id="29fdb-132">Alcuni protocolli richiedono almeno dimensioni del settore.</span><span class="sxs-lookup"><span data-stu-id="29fdb-132">Some protocols require at least sector size.</span></span> <span data-ttu-id="29fdb-133">Quando questo valore è impostato su 0, significa che questo valore non è valido.</span><span class="sxs-lookup"><span data-stu-id="29fdb-133">When this value is set to 0, this means that this value is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="29fdb-134">**ImagePayloadMaxSize**</span><span class="sxs-lookup"><span data-stu-id="29fdb-134">**ImagePayloadMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="29fdb-135">Dimensioni massime del payload dell'immagine, utilizzate per un singolo comando.</span><span class="sxs-lookup"><span data-stu-id="29fdb-135">The image payload maximum size, this is used for a single command.</span></span>

</dd> <dt>

<span data-ttu-id="29fdb-136">**Slot**</span><span class="sxs-lookup"><span data-stu-id="29fdb-136">**Slot**</span></span>
</dt> <dd>

<span data-ttu-id="29fdb-137">Contiene le informazioni sugli slot per ogni slot del dispositivo, di tipo [**informazioni slot del \_ \_ firmware \_ \_ HW di archiviazione**](storage-hw-firmware-slot-info.md).</span><span class="sxs-lookup"><span data-stu-id="29fdb-137">Contains the slot information for each slot on the device, of type [**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**](storage-hw-firmware-slot-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="29fdb-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29fdb-138">Requirements</span></span>



| <span data-ttu-id="29fdb-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="29fdb-139">Requirement</span></span> | <span data-ttu-id="29fdb-140">Valore</span><span class="sxs-lookup"><span data-stu-id="29fdb-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29fdb-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29fdb-141">Minimum supported client</span></span><br/> | <span data-ttu-id="29fdb-142">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="29fdb-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="29fdb-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29fdb-143">Minimum supported server</span></span><br/> | <span data-ttu-id="29fdb-144">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="29fdb-144">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="29fdb-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29fdb-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="29fdb-146"><dt>Winioctl. h. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29fdb-146"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29fdb-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29fdb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29fdb-148">**\_attivazione del \_ firmware di archiviazione IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="29fdb-148">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="29fdb-149">**\_attivazione del \_ firmware \_ HW di archiviazione**</span><span class="sxs-lookup"><span data-stu-id="29fdb-149">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="29fdb-150">**\_download del \_ firmware di archiviazione IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="29fdb-150">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="29fdb-151">**\_download del \_ firmware \_ HW di archiviazione**</span><span class="sxs-lookup"><span data-stu-id="29fdb-151">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="29fdb-152">**\_informazioni sul \_ firmware di archiviazione \_ IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="29fdb-152">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="29fdb-153">**\_query sulle \_ informazioni del firmware HW \_ di archiviazione \_**</span><span class="sxs-lookup"><span data-stu-id="29fdb-153">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> <dt>

[<span data-ttu-id="29fdb-154">**\_informazioni sugli \_ slot del firmware HW \_ di archiviazione \_**</span><span class="sxs-lookup"><span data-stu-id="29fdb-154">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




