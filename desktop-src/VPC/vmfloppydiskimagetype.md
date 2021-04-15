---
title: Enumerazione VMFloppyDiskImageType (VPCCOMInterfaces. h)
description: Specifica i formati dei dischi floppy.
ms.assetid: 7eb504c0-dfb7-45eb-a943-b453b5f8ca63
keywords:
- VMFloppyDiskImageType enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f20732e46617288602e841a1047db5db30eba5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400609"
---
# <a name="vmfloppydiskimagetype-enumeration"></a><span data-ttu-id="abd4a-104">Enumerazione VMFloppyDiskImageType</span><span class="sxs-lookup"><span data-stu-id="abd4a-104">VMFloppyDiskImageType enumeration</span></span>

<span data-ttu-id="abd4a-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="abd4a-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="abd4a-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="abd4a-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="abd4a-107">Specifica i formati dei dischi floppy.</span><span class="sxs-lookup"><span data-stu-id="abd4a-107">Specifies the floppy disk formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="abd4a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="abd4a-108">Syntax</span></span>


```C++
typedef enum  { 
  vmFloppyDiskImage_Unknown                = 0,
  vmFloppyDiskImage_LowDensity             = 1,
  vmFloppyDiskImage_HighDensity            = 2,
  vmFloppyDiskImage_DMF                    = 3,
  vmFloppyDiskImage_LowDensitySingleSided  = 4,
  vmFloppyDiskImage_MediumDensity          = 5,
  vmFloppyDiskImage_HighDensityMSS         = 6
} VMFloppyDiskImageType;
```



## <a name="constants"></a><span data-ttu-id="abd4a-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="abd4a-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="abd4a-110"><span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**vmFloppyDiskImage \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="abd4a-110"><span id="vmFloppyDiskImage_Unknown"></span><span id="vmfloppydiskimage_unknown"></span><span id="VMFLOPPYDISKIMAGE_UNKNOWN"></span>**vmFloppyDiskImage\_Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="abd4a-111">Formato sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="abd4a-111">Unknown format.</span></span>

</dd> <dt>

<span data-ttu-id="abd4a-112"><span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**\_LowDensity vmFloppyDiskImage**</span><span class="sxs-lookup"><span data-stu-id="abd4a-112"><span id="vmFloppyDiskImage_LowDensity"></span><span id="vmfloppydiskimage_lowdensity"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITY"></span>**vmFloppyDiskImage\_LowDensity**</span></span>
</dt> <dd>

<span data-ttu-id="abd4a-113">Formato A densità ridotta (720K).</span><span class="sxs-lookup"><span data-stu-id="abd4a-113">A low density format (720K).</span></span>

</dd> <dt>

<span data-ttu-id="abd4a-114"><span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**\_ad alta densità vmFloppyDiskImage**</span><span class="sxs-lookup"><span data-stu-id="abd4a-114"><span id="vmFloppyDiskImage_HighDensity"></span><span id="vmfloppydiskimage_highdensity"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITY"></span>**vmFloppyDiskImage\_HighDensity**</span></span>
</dt> <dd>

<span data-ttu-id="abd4a-115">Formato ad alta densità (1.44 MB).</span><span class="sxs-lookup"><span data-stu-id="abd4a-115">A high density format (1.44MB).</span></span>

</dd> <dt>

<span data-ttu-id="abd4a-116"><span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**\_DMF vmFloppyDiskImage**</span><span class="sxs-lookup"><span data-stu-id="abd4a-116"><span id="vmFloppyDiskImage_DMF"></span><span id="vmfloppydiskimage_dmf"></span><span id="VMFLOPPYDISKIMAGE_DMF"></span>**vmFloppyDiskImage\_DMF**</span></span>
</dt> <dd>

<span data-ttu-id="abd4a-117">Formato dei supporti di distribuzione (1.68 MB).</span><span class="sxs-lookup"><span data-stu-id="abd4a-117">A distribution media format (1.68Mb).</span></span>

</dd> <dt>

<span data-ttu-id="abd4a-118"><span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**\_LowDensitySingleSided vmFloppyDiskImage**</span><span class="sxs-lookup"><span data-stu-id="abd4a-118"><span id="vmFloppyDiskImage_LowDensitySingleSided"></span><span id="vmfloppydiskimage_lowdensitysinglesided"></span><span id="VMFLOPPYDISKIMAGE_LOWDENSITYSINGLESIDED"></span>**vmFloppyDiskImage\_LowDensitySingleSided**</span></span>
</dt> <dd>

<span data-ttu-id="abd4a-119">Formato A densità ridotta a singolo lato.</span><span class="sxs-lookup"><span data-stu-id="abd4a-119">A single-sided low density format.</span></span>

</dd> <dt>

<span data-ttu-id="abd4a-120"><span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**\_MediumDensity vmFloppyDiskImage**</span><span class="sxs-lookup"><span data-stu-id="abd4a-120"><span id="vmFloppyDiskImage_MediumDensity"></span><span id="vmfloppydiskimage_mediumdensity"></span><span id="VMFLOPPYDISKIMAGE_MEDIUMDENSITY"></span>**vmFloppyDiskImage\_MediumDensity**</span></span>
</dt> <dd>

<span data-ttu-id="abd4a-121">Formato A densità media (1,2 MB).</span><span class="sxs-lookup"><span data-stu-id="abd4a-121">A medium density format (1.2MB).</span></span>

</dd> <dt>

<span data-ttu-id="abd4a-122"><span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**\_HighDensityMSS vmFloppyDiskImage**</span><span class="sxs-lookup"><span data-stu-id="abd4a-122"><span id="vmFloppyDiskImage_HighDensityMSS"></span><span id="vmfloppydiskimage_highdensitymss"></span><span id="VMFLOPPYDISKIMAGE_HIGHDENSITYMSS"></span>**vmFloppyDiskImage\_HighDensityMSS**</span></span>
</dt> <dd>

<span data-ttu-id="abd4a-123">Una dimensione di settore multipla (MSS) a densità elevata utilizzata dal formato di distribuzione estesa (XDF).</span><span class="sxs-lookup"><span data-stu-id="abd4a-123">A high-density Multiple Sector Size (MSS), used by eXtended Distribution Format (XDF).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abd4a-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="abd4a-124">Requirements</span></span>



| <span data-ttu-id="abd4a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="abd4a-125">Requirement</span></span> | <span data-ttu-id="abd4a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="abd4a-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="abd4a-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abd4a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="abd4a-128">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="abd4a-128">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="abd4a-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="abd4a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="abd4a-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="abd4a-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="abd4a-131">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="abd4a-131">End of client support</span></span><br/>    | <span data-ttu-id="abd4a-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abd4a-132">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="abd4a-133">Prodotto</span><span class="sxs-lookup"><span data-stu-id="abd4a-133">Product</span></span><br/>                  | <span data-ttu-id="abd4a-134">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="abd4a-134">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="abd4a-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="abd4a-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="abd4a-136"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="abd4a-136"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abd4a-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="abd4a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abd4a-138">**IVMVirtualPC::CreateFloppyDiskImage**</span><span class="sxs-lookup"><span data-stu-id="abd4a-138">**IVMVirtualPC::CreateFloppyDiskImage**</span></span>](ivmvirtualpc-createfloppydiskimage.md)
</dt> <dt>

[<span data-ttu-id="abd4a-139">**IVMVirtualPC::GetFloppyDiskImageType**</span><span class="sxs-lookup"><span data-stu-id="abd4a-139">**IVMVirtualPC::GetFloppyDiskImageType**</span></span>](ivmvirtualpc-getfloppydiskimagetype.md)
</dt> </dl>

 

