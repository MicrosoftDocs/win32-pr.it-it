---
title: Enumerazione VMDVDDriveAttachmentType (VPCCOMInterfaces. h)
description: Specifica ciò che viene collegato a un'unità DVD.
ms.assetid: 66f33974-8622-4fa3-b5ac-3fae5a637434
keywords:
- VMDVDDriveAttachmentType enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMDVDDriveAttachmentType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c5918fd414a5a83a114ebddf5752647e8db83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477393"
---
# <a name="vmdvddriveattachmenttype-enumeration"></a><span data-ttu-id="bb3cb-104">Enumerazione VMDVDDriveAttachmentType</span><span class="sxs-lookup"><span data-stu-id="bb3cb-104">VMDVDDriveAttachmentType enumeration</span></span>

<span data-ttu-id="bb3cb-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bb3cb-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bb3cb-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bb3cb-107">Specifica ciò che viene collegato a un'unità DVD.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-107">Specifies what is attached to a DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb3cb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb3cb-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDVDDrive_None       = 0,
  vmDVDDrive_Image      = 1,
  vmDVDDrive_HostDrive  = 2
} VMDVDDriveAttachmentType;
```



## <a name="constants"></a><span data-ttu-id="bb3cb-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="bb3cb-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bb3cb-110"><span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**vmDVDDrive \_ None**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-110"><span id="vmDVDDrive_None"></span><span id="vmdvddrive_none"></span><span id="VMDVDDRIVE_NONE"></span>**vmDVDDrive\_None**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-111">Nessun elemento collegato.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-111">There is nothing attached.</span></span>

</dd> <dt>

<span data-ttu-id="bb3cb-112"><span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**immagine di vmDVDDrive \_**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-112"><span id="vmDVDDrive_Image"></span><span id="vmdvddrive_image"></span><span id="VMDVDDRIVE_IMAGE"></span>**vmDVDDrive\_Image**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-113">È presente un file di immagine ISO collegato.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-113">There is an ISO image file attached.</span></span>

</dd> <dt>

<span data-ttu-id="bb3cb-114"><span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**\_HostDrive vmDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-114"><span id="vmDVDDrive_HostDrive"></span><span id="vmdvddrive_hostdrive"></span><span id="VMDVDDRIVE_HOSTDRIVE"></span>**vmDVDDrive\_HostDrive**</span></span>
</dt> <dd>

<span data-ttu-id="bb3cb-115">È collegata un'unità CD o DVD host.</span><span class="sxs-lookup"><span data-stu-id="bb3cb-115">There is a host CD or DVD drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb3cb-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb3cb-116">Requirements</span></span>



| <span data-ttu-id="bb3cb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb3cb-117">Requirement</span></span> | <span data-ttu-id="bb3cb-118">Valore</span><span class="sxs-lookup"><span data-stu-id="bb3cb-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb3cb-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb3cb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bb3cb-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bb3cb-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb3cb-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb3cb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bb3cb-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bb3cb-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bb3cb-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bb3cb-123">End of client support</span></span><br/>    | <span data-ttu-id="bb3cb-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bb3cb-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bb3cb-125">Prodotto</span><span class="sxs-lookup"><span data-stu-id="bb3cb-125">Product</span></span><br/>                  | <span data-ttu-id="bb3cb-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bb3cb-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bb3cb-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb3cb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb3cb-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb3cb-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb3cb-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb3cb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb3cb-130">**IVMDVDDrive:: Attachment**</span><span class="sxs-lookup"><span data-stu-id="bb3cb-130">**IVMDVDDrive::Attachment**</span></span>](ivmdvddrive-attachment.md)
</dt> </dl>

 

