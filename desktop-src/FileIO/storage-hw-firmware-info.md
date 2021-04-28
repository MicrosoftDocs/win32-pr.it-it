---
description: 'STORAGE_HW_FIRMWARE_INFO: questa struttura contiene informazioni sul firmware del dispositivo.'
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: STORAGE_HW_FIRMWARE_INFO struttura (Winioctl.h)
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
ms.openlocfilehash: e7aa3d33f744b00fc742a2862add83149cb265b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090959"
---
# <a name="storage_hw_firmware_info-structure"></a><span data-ttu-id="a2c82-103">Struttura DELLE \_ INFORMAZIONI \_ DEL FIRMWARE HW DI \_ ARCHIVIAZIONE</span><span class="sxs-lookup"><span data-stu-id="a2c82-103">STORAGE\_HW\_FIRMWARE\_INFO structure</span></span>

<span data-ttu-id="a2c82-104">Questa struttura contiene informazioni sul firmware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a2c82-104">This structure contains information about the device firmware.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2c82-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a2c82-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="a2c82-106">Members</span><span class="sxs-lookup"><span data-stu-id="a2c82-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a2c82-107">**Versione**</span><span class="sxs-lookup"><span data-stu-id="a2c82-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="a2c82-108">Versione di questa struttura .</span><span class="sxs-lookup"><span data-stu-id="a2c82-108">The version of this structure.</span></span> <span data-ttu-id="a2c82-109">Deve essere impostato su sizeof(STORAGE \_ HW \_ FIRMWARE \_ INFO)</span><span class="sxs-lookup"><span data-stu-id="a2c82-109">This should be set to sizeof(STORAGE\_HW\_FIRMWARE\_INFO)</span></span>

</dd> <dt>

<span data-ttu-id="a2c82-110">**Size**</span><span class="sxs-lookup"><span data-stu-id="a2c82-110">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="a2c82-111">Dimensione di questa struttura come buffer che include lo slot.</span><span class="sxs-lookup"><span data-stu-id="a2c82-111">The size of this structure as a buffer including slot.</span></span>

</dd> <dt>

<span data-ttu-id="a2c82-112">**SupportUpgrade**</span><span class="sxs-lookup"><span data-stu-id="a2c82-112">**SupportUpgrade**</span></span>
</dt> <dd>

<span data-ttu-id="a2c82-113">Indica che questo firmware supporta un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="a2c82-113">Indicates that this firmware supports an upgrade.</span></span>

</dd> <dt>

<span data-ttu-id="a2c82-114">**Riservato0**</span><span class="sxs-lookup"><span data-stu-id="a2c82-114">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="a2c82-115">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="a2c82-115">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="a2c82-116">**SlotCount**</span><span class="sxs-lookup"><span data-stu-id="a2c82-116">**SlotCount**</span></span>
</dt> <dd>

<span data-ttu-id="a2c82-117">Numero di slot del firmware nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a2c82-117">The number of firmware slots on the device.</span></span> <span data-ttu-id="a2c82-118">Si tratta della dimensione della matrice Slot.</span><span class="sxs-lookup"><span data-stu-id="a2c82-118">This is the dimension of the Slot array.</span></span>

> [!Note]  
> <span data-ttu-id="a2c82-119">Alcuni dispositivi possono archiviare più di un'immagine del firmware, se hanno più di uno slot del firmware.</span><span class="sxs-lookup"><span data-stu-id="a2c82-119">Some devices can store more than 1 firmware image, if they have more than 1 firmware slot.</span></span>

 

</dd> <dt>

<span data-ttu-id="a2c82-120">**ActiveSlot**</span><span class="sxs-lookup"><span data-stu-id="a2c82-120">**ActiveSlot**</span></span>
</dt> <dd>

<span data-ttu-id="a2c82-121">Slot del firmware contenente l'immagine del firmware attualmente attiva/in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a2c82-121">The firmware slot containing the currently active/running firmware image.</span></span>

</dd> <dt>

<span data-ttu-id="a2c82-122">**PendingActivateSlot**</span><span class="sxs-lookup"><span data-stu-id="a2c82-122">**PendingActivateSlot**</span></span>
</dt> <dd>

<span data-ttu-id="a2c82-123">Slot del firmware in attesa di attivazione.</span><span class="sxs-lookup"><span data-stu-id="a2c82-123">The firmware slot that is pending activation.</span></span>

</dd> <dt>

<span data-ttu-id="a2c82-124">**Firmware Condiviso**</span><span class="sxs-lookup"><span data-stu-id="a2c82-124">**FirmwareShared**</span></span>
</dt> <dd>

<span data-ttu-id="a2c82-125">Indica che il firmware si applica sia al dispositivo che al controller/adattatore, ad esempio alle unità SSD NVMe.</span><span class="sxs-lookup"><span data-stu-id="a2c82-125">Indicates that the firmware applies to both the device and controller/adapter, e.g. NVMe SSD.</span></span>

</dd> <dt>

<span data-ttu-id="a2c82-126">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="a2c82-126">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="a2c82-127">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="a2c82-127">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="a2c82-128">**ImagePayloadAlignment**</span><span class="sxs-lookup"><span data-stu-id="a2c82-128">**ImagePayloadAlignment**</span></span>
</dt> <dd>

<span data-ttu-id="a2c82-129">Allineamento del payload dell'immagine, in numero di byte.</span><span class="sxs-lookup"><span data-stu-id="a2c82-129">The alignment of the image payload, in number of bytes.</span></span> <span data-ttu-id="a2c82-130">Il valore massimo è PAGE \_ SIZE.</span><span class="sxs-lookup"><span data-stu-id="a2c82-130">The maximum is PAGE\_SIZE.</span></span> <span data-ttu-id="a2c82-131">Le dimensioni di trasferimento sono un'mutlipla di queste dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a2c82-131">The transfer size is a mutliple of this size.</span></span> <span data-ttu-id="a2c82-132">Alcuni protocolli richiedono almeno le dimensioni del settore.</span><span class="sxs-lookup"><span data-stu-id="a2c82-132">Some protocols require at least sector size.</span></span> <span data-ttu-id="a2c82-133">Quando questo valore è impostato su 0, questo valore non è valido.</span><span class="sxs-lookup"><span data-stu-id="a2c82-133">When this value is set to 0, this means that this value is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="a2c82-134">**ImagePayloadMaxSize**</span><span class="sxs-lookup"><span data-stu-id="a2c82-134">**ImagePayloadMaxSize**</span></span>
</dt> <dd>

<span data-ttu-id="a2c82-135">Dimensione massima del payload dell'immagine, usata per un singolo comando.</span><span class="sxs-lookup"><span data-stu-id="a2c82-135">The image payload maximum size, this is used for a single command.</span></span>

</dd> <dt>

<span data-ttu-id="a2c82-136">**Slot**</span><span class="sxs-lookup"><span data-stu-id="a2c82-136">**Slot**</span></span>
</dt> <dd>

<span data-ttu-id="a2c82-137">Contiene le informazioni sullo slot per ogni slot nel dispositivo, di tipo [**STORAGE \_ HW \_ FIRMWARE SLOT \_ \_ INFO**](storage-hw-firmware-slot-info.md).</span><span class="sxs-lookup"><span data-stu-id="a2c82-137">Contains the slot information for each slot on the device, of type [**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**](storage-hw-firmware-slot-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a2c82-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2c82-138">Requirements</span></span>



| <span data-ttu-id="a2c82-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2c82-139">Requirement</span></span> | <span data-ttu-id="a2c82-140">Valore</span><span class="sxs-lookup"><span data-stu-id="a2c82-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2c82-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2c82-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a2c82-142">Windows 10 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a2c82-142">Windows 10 \[desktop apps only\]</span></span><br/>                                                                 |
| <span data-ttu-id="a2c82-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2c82-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a2c82-144">Solo app desktop di Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2c82-144">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="a2c82-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2c82-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2c82-146"><dt>Winioctl.h.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2c82-146"><dt>Winioctl.h.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2c82-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2c82-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2c82-148">**ATTIVAZIONE DEL FIRMWARE DI ARCHIVIAZIONE IOCTL \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a2c82-148">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[<span data-ttu-id="a2c82-149">**ATTIVAZIONE \_ FIRMWARE HW \_ DI \_ ARCHIVIAZIONE**</span><span class="sxs-lookup"><span data-stu-id="a2c82-149">**STORAGE\_HW\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[<span data-ttu-id="a2c82-150">**DOWNLOAD DEL FIRMWARE DI ARCHIVIAZIONE IOCTL \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a2c82-150">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[<span data-ttu-id="a2c82-151">**DOWNLOAD \_ DEL FIRMWARE HW DI \_ \_ ARCHIVIAZIONE**</span><span class="sxs-lookup"><span data-stu-id="a2c82-151">**STORAGE\_HW\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[<span data-ttu-id="a2c82-152">**INFORMAZIONI SUL \_ FIRMWARE DI \_ ARCHIVIAZIONE \_ IOCTL \_**</span><span class="sxs-lookup"><span data-stu-id="a2c82-152">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[<span data-ttu-id="a2c82-153">**\_QUERY DI INFORMAZIONI SUL FIRMWARE HW DI \_ \_ \_ ARCHIVIAZIONE**</span><span class="sxs-lookup"><span data-stu-id="a2c82-153">**STORAGE\_HW\_FIRMWARE\_INFO\_QUERY**</span></span>](storage-hw-firmware-info-query.md)
</dt> <dt>

[<span data-ttu-id="a2c82-154">**INFORMAZIONI \_ DELLO SLOT DEL FIRMWARE HW DI \_ \_ \_ ARCHIVIAZIONE**</span><span class="sxs-lookup"><span data-stu-id="a2c82-154">**STORAGE\_HW\_FIRMWARE\_SLOT\_INFO**</span></span>](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




