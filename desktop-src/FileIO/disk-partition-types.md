---
description: Tipi di partizione validi usati dai driver del disco.
ms.assetid: b2e15b93-a02b-4d6f-b242-b5ec9a30c97b
title: Tipi di partizione del disco (WinIoCtl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4109d4386d4892ca695fe8876b61501110cef455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316771"
---
# <a name="disk-partition-types"></a><span data-ttu-id="e13f0-103">Tipi di partizione del disco</span><span class="sxs-lookup"><span data-stu-id="e13f0-103">Disk Partition Types</span></span>

<span data-ttu-id="e13f0-104">Nella tabella seguente vengono identificati i tipi di partizione validi utilizzati dai driver del disco.</span><span class="sxs-lookup"><span data-stu-id="e13f0-104">The following table identifies the valid partition types that are used by disk drivers.</span></span>



| <span data-ttu-id="e13f0-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="e13f0-105">Constant/value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="e13f0-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e13f0-106">Description</span></span>                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PARTITION_ENTRY_UNUSED"></span><span id="partition_entry_unused"></span><dl> <span data-ttu-id="e13f0-107"><dt>**Partizione \_ di VOCE \_**</dt> <dt>0x00</dt> non usata</span><span class="sxs-lookup"><span data-stu-id="e13f0-107"><dt>**PARTITION\_ENTRY\_UNUSED**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="e13f0-108">Partizione di immissione inutilizzata.</span><span class="sxs-lookup"><span data-stu-id="e13f0-108">An unused entry partition.</span></span><br/>                                                                                                                      |
| <span id="PARTITION_EXTENDED"></span><span id="partition_extended"></span><dl> <span data-ttu-id="e13f0-109"><dt>**Partizione \_ di**</dt> <dt>0x05</dt> esteso</span><span class="sxs-lookup"><span data-stu-id="e13f0-109"><dt>**PARTITION\_EXTENDED**</dt> <dt>0x05</dt></span></span> </dl>              | <span data-ttu-id="e13f0-110">Partizione estesa.</span><span class="sxs-lookup"><span data-stu-id="e13f0-110">An extended partition.</span></span><br/>                                                                                                                          |
| <span id="PARTITION_FAT_12"></span><span id="partition_fat_12"></span><dl> <span data-ttu-id="e13f0-111"><dt>**Partizione \_ di FAT \_ 12**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="e13f0-111"><dt>**PARTITION\_FAT\_12**</dt> <dt>0x01</dt></span></span> </dl>                   | <span data-ttu-id="e13f0-112">Partizione file system FAT12.</span><span class="sxs-lookup"><span data-stu-id="e13f0-112">A FAT12 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_FAT_16"></span><span id="partition_fat_16"></span><dl> <span data-ttu-id="e13f0-113"><dt>**Partizione \_ di FAT \_ 16**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="e13f0-113"><dt>**PARTITION\_FAT\_16**</dt> <dt>0x04</dt></span></span> </dl>                   | <span data-ttu-id="e13f0-114">Una partizione file system FAT16.</span><span class="sxs-lookup"><span data-stu-id="e13f0-114">A FAT16 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_FAT32"></span><span id="partition_fat32"></span><dl> <span data-ttu-id="e13f0-115"><dt>**Partizione \_ di**</dt> <dt>0x0B</dt> FAT32</span><span class="sxs-lookup"><span data-stu-id="e13f0-115"><dt>**PARTITION\_FAT32**</dt> <dt>0x0B</dt></span></span> </dl>                       | <span data-ttu-id="e13f0-116">Una partizione file system FAT32.</span><span class="sxs-lookup"><span data-stu-id="e13f0-116">A FAT32 file system partition.</span></span><br/>                                                                                                                  |
| <span id="PARTITION_IFS"></span><span id="partition_ifs"></span><dl> <span data-ttu-id="e13f0-117"><dt>**Partizione \_ di**</dt> <dt>0x07</dt> IFS</span><span class="sxs-lookup"><span data-stu-id="e13f0-117"><dt>**PARTITION\_IFS**</dt> <dt>0x07</dt></span></span> </dl>                             | <span data-ttu-id="e13f0-118">Una partizione IFS.</span><span class="sxs-lookup"><span data-stu-id="e13f0-118">An IFS partition.</span></span><br/>                                                                                                                               |
| <span id="PARTITION_LDM"></span><span id="partition_ldm"></span><dl> <span data-ttu-id="e13f0-119"><dt>**Partizione \_ di**</dt> <dt>0x42</dt> LDM</span><span class="sxs-lookup"><span data-stu-id="e13f0-119"><dt>**PARTITION\_LDM**</dt> <dt>0x42</dt></span></span> </dl>                             | <span data-ttu-id="e13f0-120">Una partizione di gestione dischi logici (LDM).</span><span class="sxs-lookup"><span data-stu-id="e13f0-120">A logical disk manager (LDM) partition.</span></span><br/>                                                                                                         |
| <span id="PARTITION_NTFT"></span><span id="partition_ntft"></span><dl> <span data-ttu-id="e13f0-121"><dt>**Partizione \_ di**</dt> <dt>0x80</dt> NTFT</span><span class="sxs-lookup"><span data-stu-id="e13f0-121"><dt>**PARTITION\_NTFT**</dt> <dt>0x80</dt></span></span> </dl>                          | <span data-ttu-id="e13f0-122">Una partizione NTFT.</span><span class="sxs-lookup"><span data-stu-id="e13f0-122">An NTFT partition.</span></span><br/>                                                                                                                              |
| <span id="VALID_NTFT"></span><span id="valid_ntft"></span><dl> <span data-ttu-id="e13f0-123">Valore <dt>**valido \_**</dt> <dt>0xC0</dt> NTFT</span><span class="sxs-lookup"><span data-stu-id="e13f0-123"><dt>**VALID\_NTFT**</dt> <dt>0xC0</dt></span></span> </dl>                                      | <span data-ttu-id="e13f0-124">Una partizione NTFT valida.</span><span class="sxs-lookup"><span data-stu-id="e13f0-124">A valid NTFT partition.</span></span><br/> <span data-ttu-id="e13f0-125">Il bit più elevato del codice di un tipo di partizione indica che una partizione fa parte di un mirror NTFT o di una matrice con striping.</span><span class="sxs-lookup"><span data-stu-id="e13f0-125">The high bit of a partition type code indicates that a partition is part of an NTFT mirror or striped array.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e13f0-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="e13f0-126">Remarks</span></span>

<span data-ttu-id="e13f0-127">Sono disponibili diverse macro che consentono di rilevare il tipo di partizione: **IsContainerPartition**, **IsFTPartition** e **IsRecognizedPartition**.</span><span class="sxs-lookup"><span data-stu-id="e13f0-127">There are several macros that can help you detect the partition type: **IsContainerPartition**, **IsFTPartition**, and **IsRecognizedPartition**.</span></span> <span data-ttu-id="e13f0-128">Per ulteriori informazioni, vedere WinIoCtl. h.</span><span class="sxs-lookup"><span data-stu-id="e13f0-128">For more information, see WinIoCtl.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="e13f0-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e13f0-129">Requirements</span></span>



| <span data-ttu-id="e13f0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e13f0-130">Requirement</span></span> | <span data-ttu-id="e13f0-131">Valore</span><span class="sxs-lookup"><span data-stu-id="e13f0-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e13f0-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e13f0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e13f0-133">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e13f0-133">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="e13f0-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e13f0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e13f0-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e13f0-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e13f0-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e13f0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e13f0-137"><dt>WinIoCtl. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e13f0-137"><dt>WinIoCtl.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e13f0-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e13f0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13f0-139">**informazioni sulle partizioni, ad \_ \_ esempio**</span><span class="sxs-lookup"><span data-stu-id="e13f0-139">**PARTITION\_INFORMATION\_EX**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_ex)
</dt> <dt>

[<span data-ttu-id="e13f0-140">**\_informazioni sulle partizioni \_ MBR**</span><span class="sxs-lookup"><span data-stu-id="e13f0-140">**PARTITION\_INFORMATION\_MBR**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_mbr)
</dt> <dt>

[<span data-ttu-id="e13f0-141">**IMPOSTA \_ \_ informazioni sulle partizioni**</span><span class="sxs-lookup"><span data-stu-id="e13f0-141">**SET\_PARTITION\_INFORMATION**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-set_partition_information)
</dt> </dl>

 

 




