---
title: Enumerazione VMDriveBusType (VPCCOMInterfaces. h)
description: Specifica il tipo di bus.
ms.assetid: 7e0926f3-8218-49c9-8d3a-27214c111a77
keywords:
- VMDriveBusType enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMDriveBusType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c53b8da4b9c7a6943f083eec62a144dcfb5bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120162"
---
# <a name="vmdrivebustype-enumeration"></a><span data-ttu-id="0aa1a-104">Enumerazione VMDriveBusType</span><span class="sxs-lookup"><span data-stu-id="0aa1a-104">VMDriveBusType enumeration</span></span>

<span data-ttu-id="0aa1a-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0aa1a-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0aa1a-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0aa1a-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0aa1a-107">Specifica il tipo di bus.</span><span class="sxs-lookup"><span data-stu-id="0aa1a-107">Specifies the type of bus.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aa1a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0aa1a-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDriveBusType_Invalid  = -1,
  vmDriveBusType_IDE      = 0,
  vmDriveBusType_SCSI     = 1
} VMDriveBusType;
```



## <a name="constants"></a><span data-ttu-id="0aa1a-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="0aa1a-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0aa1a-110"><span id="vmDriveBusType_Invalid"></span><span id="vmdrivebustype_invalid"></span><span id="VMDRIVEBUSTYPE_INVALID"></span>**vmDriveBusType \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="0aa1a-110"><span id="vmDriveBusType_Invalid"></span><span id="vmdrivebustype_invalid"></span><span id="VMDRIVEBUSTYPE_INVALID"></span>**vmDriveBusType\_Invalid**</span></span>
</dt> <dd>

<span data-ttu-id="0aa1a-111">Nessun tipo di bus.</span><span class="sxs-lookup"><span data-stu-id="0aa1a-111">No bus type.</span></span>

</dd> <dt>

<span data-ttu-id="0aa1a-112"><span id="vmDriveBusType_IDE"></span><span id="vmdrivebustype_ide"></span><span id="VMDRIVEBUSTYPE_IDE"></span>**\_IDE vmDriveBusType**</span><span class="sxs-lookup"><span data-stu-id="0aa1a-112"><span id="vmDriveBusType_IDE"></span><span id="vmdrivebustype_ide"></span><span id="VMDRIVEBUSTYPE_IDE"></span>**vmDriveBusType\_IDE**</span></span>
</dt> <dd>

<span data-ttu-id="0aa1a-113">Tipo di bus IDE.</span><span class="sxs-lookup"><span data-stu-id="0aa1a-113">IDE bus type.</span></span>

</dd> <dt>

<span data-ttu-id="0aa1a-114"><span id="vmDriveBusType_SCSI"></span><span id="vmdrivebustype_scsi"></span><span id="VMDRIVEBUSTYPE_SCSI"></span>**\_SCSI vmDriveBusType**</span><span class="sxs-lookup"><span data-stu-id="0aa1a-114"><span id="vmDriveBusType_SCSI"></span><span id="vmdrivebustype_scsi"></span><span id="VMDRIVEBUSTYPE_SCSI"></span>**vmDriveBusType\_SCSI**</span></span>
</dt> <dd>

<span data-ttu-id="0aa1a-115">Tipo di bus SCSI.</span><span class="sxs-lookup"><span data-stu-id="0aa1a-115">SCSI bus type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0aa1a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0aa1a-116">Requirements</span></span>



| <span data-ttu-id="0aa1a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0aa1a-117">Requirement</span></span> | <span data-ttu-id="0aa1a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0aa1a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0aa1a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0aa1a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0aa1a-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0aa1a-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0aa1a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0aa1a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0aa1a-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0aa1a-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0aa1a-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="0aa1a-123">End of client support</span></span><br/>    | <span data-ttu-id="0aa1a-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0aa1a-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0aa1a-125">Prodotto</span><span class="sxs-lookup"><span data-stu-id="0aa1a-125">Product</span></span><br/>                  | <span data-ttu-id="0aa1a-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0aa1a-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0aa1a-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0aa1a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aa1a-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0aa1a-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



 

