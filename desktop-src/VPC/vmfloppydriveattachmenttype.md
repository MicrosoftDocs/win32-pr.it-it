---
title: Enumerazione VMFloppyDriveAttachmentType (VPCCOMInterfaces. h)
description: Specifica ciò che viene collegato a un'unità floppy.
ms.assetid: aba1be92-bd07-4edb-ad62-f8d76dbd19b9
keywords:
- VMFloppyDriveAttachmentType enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMFloppyDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4a291778b2fea8039bf41fc04799a03421342f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964410"
---
# <a name="vmfloppydriveattachmenttype-enumeration"></a><span data-ttu-id="6461c-104">Enumerazione VMFloppyDriveAttachmentType</span><span class="sxs-lookup"><span data-stu-id="6461c-104">VMFloppyDriveAttachmentType enumeration</span></span>

<span data-ttu-id="6461c-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6461c-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6461c-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6461c-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6461c-107">Specifica ciò che viene collegato a un'unità floppy.</span><span class="sxs-lookup"><span data-stu-id="6461c-107">Specifies what is attached to a floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="6461c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6461c-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDrive_None       = 0,
  vmFloppyDrive_Image      = 1,
  vmFloppyDrive_HostDrive  = 2
} VMFloppyDriveAttachmentType;
```



## <a name="constants"></a><span data-ttu-id="6461c-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="6461c-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6461c-110"><span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**vmFloppyDrive \_ None**</span><span class="sxs-lookup"><span data-stu-id="6461c-110"><span id="vmFloppyDrive_None"></span><span id="vmfloppydrive_none"></span><span id="VMFLOPPYDRIVE_NONE"></span>**vmFloppyDrive\_None**</span></span>
</dt> <dd>

<span data-ttu-id="6461c-111">Nessun elemento collegato.</span><span class="sxs-lookup"><span data-stu-id="6461c-111">There is nothing attached.</span></span>

</dd> <dt>

<span data-ttu-id="6461c-112"><span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**immagine di vmFloppyDrive \_**</span><span class="sxs-lookup"><span data-stu-id="6461c-112"><span id="vmFloppyDrive_Image"></span><span id="vmfloppydrive_image"></span><span id="VMFLOPPYDRIVE_IMAGE"></span>**vmFloppyDrive\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="6461c-113">È presente un file di immagine disco floppy collegato.</span><span class="sxs-lookup"><span data-stu-id="6461c-113">There is a floppy disk image file attached.</span></span>

</dd> <dt>

<span data-ttu-id="6461c-114"><span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**\_HostDrive vmFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="6461c-114"><span id="vmFloppyDrive_HostDrive"></span><span id="vmfloppydrive_hostdrive"></span><span id="VMFLOPPYDRIVE_HOSTDRIVE"></span>**vmFloppyDrive\_HostDrive**</span></span>
</dt> <dd>

<span data-ttu-id="6461c-115">È presente un'unità floppy host collegata.</span><span class="sxs-lookup"><span data-stu-id="6461c-115">There is a host floppy drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6461c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6461c-116">Requirements</span></span>



| <span data-ttu-id="6461c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6461c-117">Requirement</span></span> | <span data-ttu-id="6461c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6461c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6461c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6461c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6461c-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6461c-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6461c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6461c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6461c-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6461c-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6461c-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6461c-123">End of client support</span></span><br/>    | <span data-ttu-id="6461c-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6461c-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6461c-125">Prodotto</span><span class="sxs-lookup"><span data-stu-id="6461c-125">Product</span></span><br/>                  | <span data-ttu-id="6461c-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6461c-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6461c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6461c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6461c-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6461c-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6461c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6461c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6461c-130">**IVMFloppyDrive:: Attachment**</span><span class="sxs-lookup"><span data-stu-id="6461c-130">**IVMFloppyDrive::Attachment**</span></span>](ivmfloppydrive-attachment.md)
</dt> </dl>

 

