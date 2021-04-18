---
title: Enumerazione VMHardDiskType (VPCCOMInterfaces. h)
description: Specifica il tipo di immagine del disco rigido.
ms.assetid: 14480bad-523a-40d8-a6ba-9ec31fe4b217
keywords:
- VMHardDiskType enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMHardDiskType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b59fed6577aa957bae960f7af65be766a03c727e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302092"
---
# <a name="vmharddisktype-enumeration"></a><span data-ttu-id="300d7-104">Enumerazione VMHardDiskType</span><span class="sxs-lookup"><span data-stu-id="300d7-104">VMHardDiskType enumeration</span></span>

<span data-ttu-id="300d7-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="300d7-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="300d7-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="300d7-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="300d7-107">Specifica il tipo di immagine del disco rigido.</span><span class="sxs-lookup"><span data-stu-id="300d7-107">Specifies the hard disk image type.</span></span>

## <a name="syntax"></a><span data-ttu-id="300d7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="300d7-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDiskType_Dynamic       = 0,
  vmDiskType_FixedSize     = 1,
  vmDiskType_Differencing  = 2
} VMHardDiskType;
```



## <a name="constants"></a><span data-ttu-id="300d7-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="300d7-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="300d7-110"><span id="vmDiskType_Dynamic"></span><span id="vmdisktype_dynamic"></span><span id="VMDISKTYPE_DYNAMIC"></span>**vmDiskType \_ dinamico**</span><span class="sxs-lookup"><span data-stu-id="300d7-110"><span id="vmDiskType_Dynamic"></span><span id="vmdisktype_dynamic"></span><span id="VMDISKTYPE_DYNAMIC"></span>**vmDiskType\_Dynamic**</span></span>
</dt> <dd>

<span data-ttu-id="300d7-111">Un'immagine del disco rigido ad espansione dinamica.</span><span class="sxs-lookup"><span data-stu-id="300d7-111">A dynamically expanding hard disk image.</span></span>

</dd> <dt>

<span data-ttu-id="300d7-112"><span id="vmDiskType_FixedSize"></span><span id="vmdisktype_fixedsize"></span><span id="VMDISKTYPE_FIXEDSIZE"></span>**\_FixedSize vmDiskType**</span><span class="sxs-lookup"><span data-stu-id="300d7-112"><span id="vmDiskType_FixedSize"></span><span id="vmdisktype_fixedsize"></span><span id="VMDISKTYPE_FIXEDSIZE"></span>**vmDiskType\_FixedSize**</span></span>
</dt> <dd>

<span data-ttu-id="300d7-113">Immagine del disco rigido a dimensione fissa.</span><span class="sxs-lookup"><span data-stu-id="300d7-113">A fixed-size hard disk image.</span></span>

</dd> <dt>

<span data-ttu-id="300d7-114"><span id="vmDiskType_Differencing"></span><span id="vmdisktype_differencing"></span><span id="VMDISKTYPE_DIFFERENCING"></span>**\_differenze vmDiskType**</span><span class="sxs-lookup"><span data-stu-id="300d7-114"><span id="vmDiskType_Differencing"></span><span id="vmdisktype_differencing"></span><span id="VMDISKTYPE_DIFFERENCING"></span>**vmDiskType\_Differencing**</span></span>
</dt> <dd>

<span data-ttu-id="300d7-115">Immagine del disco rigido differenze.</span><span class="sxs-lookup"><span data-stu-id="300d7-115">A differencing hard disk image.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="300d7-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="300d7-116">Requirements</span></span>



| <span data-ttu-id="300d7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="300d7-117">Requirement</span></span> | <span data-ttu-id="300d7-118">Valore</span><span class="sxs-lookup"><span data-stu-id="300d7-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="300d7-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="300d7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="300d7-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="300d7-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="300d7-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="300d7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="300d7-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="300d7-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="300d7-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="300d7-123">End of client support</span></span><br/>    | <span data-ttu-id="300d7-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="300d7-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="300d7-125">Prodotto</span><span class="sxs-lookup"><span data-stu-id="300d7-125">Product</span></span><br/>                  | <span data-ttu-id="300d7-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="300d7-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="300d7-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="300d7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="300d7-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="300d7-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="300d7-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="300d7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="300d7-130">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="300d7-130">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

