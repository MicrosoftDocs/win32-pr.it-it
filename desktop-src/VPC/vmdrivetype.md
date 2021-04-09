---
title: Enumerazione VMDriveType (VPCCOMInterfaces. h)
description: Specifica il tipo di unità collegata a una posizione del bus.
ms.assetid: 7d3acff2-e1e3-4622-a448-0996ee7436ae
keywords:
- VMDriveType enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMDriveType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6001a4a68db51b64eea9bb44d1d4c75863d315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741399"
---
# <a name="vmdrivetype-enumeration"></a><span data-ttu-id="299c4-104">Enumerazione VMDriveType</span><span class="sxs-lookup"><span data-stu-id="299c4-104">VMDriveType enumeration</span></span>

<span data-ttu-id="299c4-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="299c4-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="299c4-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="299c4-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="299c4-107">Specifica il tipo di unità collegata a una posizione del bus.</span><span class="sxs-lookup"><span data-stu-id="299c4-107">Specifies the type of drive attached to a bus location.</span></span>

## <a name="syntax"></a><span data-ttu-id="299c4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="299c4-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDriveType_Null      = 0,
  vmDriveType_HardDisk  = 1,
  vmDriveType_DVD       = 2
} VMDriveType;
```



## <a name="constants"></a><span data-ttu-id="299c4-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="299c4-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="299c4-110"><span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**vmDriveType \_ null**</span><span class="sxs-lookup"><span data-stu-id="299c4-110"><span id="vmDriveType_Null"></span><span id="vmdrivetype_null"></span><span id="VMDRIVETYPE_NULL"></span>**vmDriveType\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="299c4-111">Nessuna unità collegata.</span><span class="sxs-lookup"><span data-stu-id="299c4-111">There is no drive attached.</span></span>

</dd> <dt>

<span data-ttu-id="299c4-112"><span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**\_disco rigido vmDriveType**</span><span class="sxs-lookup"><span data-stu-id="299c4-112"><span id="vmDriveType_HardDisk"></span><span id="vmdrivetype_harddisk"></span><span id="VMDRIVETYPE_HARDDISK"></span>**vmDriveType\_HardDisk**</span></span>
</dt> <dd>

<span data-ttu-id="299c4-113">È presente un disco rigido collegato.</span><span class="sxs-lookup"><span data-stu-id="299c4-113">There is a hard disk attached.</span></span>

</dd> <dt>

<span data-ttu-id="299c4-114"><span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**vmDriveType \_ DVD**</span><span class="sxs-lookup"><span data-stu-id="299c4-114"><span id="vmDriveType_DVD"></span><span id="vmdrivetype_dvd"></span><span id="VMDRIVETYPE_DVD"></span>**vmDriveType\_DVD**</span></span>
</dt> <dd>

<span data-ttu-id="299c4-115">È presente un'unità CD o DVD collegata.</span><span class="sxs-lookup"><span data-stu-id="299c4-115">There is a CD or DVD drive attached.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="299c4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="299c4-116">Requirements</span></span>



| <span data-ttu-id="299c4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="299c4-117">Requirement</span></span> | <span data-ttu-id="299c4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="299c4-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="299c4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="299c4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="299c4-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="299c4-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="299c4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="299c4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="299c4-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="299c4-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="299c4-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="299c4-123">End of client support</span></span><br/>    | <span data-ttu-id="299c4-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="299c4-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="299c4-125">Prodotto</span><span class="sxs-lookup"><span data-stu-id="299c4-125">Product</span></span><br/>                  | <span data-ttu-id="299c4-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="299c4-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="299c4-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="299c4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="299c4-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="299c4-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="299c4-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="299c4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="299c4-130">**IVMVirtualMachine::AttachedDriveTypes**</span><span class="sxs-lookup"><span data-stu-id="299c4-130">**IVMVirtualMachine::AttachedDriveTypes**</span></span>](ivmvirtualmachine-attacheddrivetypes.md)
</dt> </dl>

 

