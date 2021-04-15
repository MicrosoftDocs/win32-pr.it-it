---
title: Enumerazione VMStartupOption (VPCCOMInterfaces. h)
description: Specifica l'opzione di avvio.
ms.assetid: ac4de9a7-7fc7-4361-89dd-e7da8f5dbb92
keywords:
- VMStartupOption enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMStartupOption
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc4a3bbcc1c82c57dfe144f818c29b403fd83a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476540"
---
# <a name="vmstartupoption-enumeration"></a><span data-ttu-id="9544c-104">Enumerazione VMStartupOption</span><span class="sxs-lookup"><span data-stu-id="9544c-104">VMStartupOption enumeration</span></span>

<span data-ttu-id="9544c-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9544c-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9544c-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9544c-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9544c-107">Specifica l'opzione di avvio.</span><span class="sxs-lookup"><span data-stu-id="9544c-107">Specifies the start-up option.</span></span>

## <a name="syntax"></a><span data-ttu-id="9544c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9544c-108">Syntax</span></span>


```C++
typedef enum  { 
  vmStartupOption_Normal                      = 0,
  vmStartupOption_FixParentTimestampMismatch  = 1
} VMStartupOption;
```



## <a name="constants"></a><span data-ttu-id="9544c-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="9544c-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9544c-110"><span id="vmStartupOption_Normal"></span><span id="vmstartupoption_normal"></span><span id="VMSTARTUPOPTION_NORMAL"></span>**vmStartupOption \_ normale**</span><span class="sxs-lookup"><span data-stu-id="9544c-110"><span id="vmStartupOption_Normal"></span><span id="vmstartupoption_normal"></span><span id="VMSTARTUPOPTION_NORMAL"></span>**vmStartupOption\_Normal**</span></span>
</dt> <dd>

<span data-ttu-id="9544c-111">Avviare normalmente.</span><span class="sxs-lookup"><span data-stu-id="9544c-111">Start normally.</span></span>

</dd> <dt>

<span data-ttu-id="9544c-112"><span id="vmStartupOption_FixParentTimestampMismatch"></span><span id="vmstartupoption_fixparenttimestampmismatch"></span><span id="VMSTARTUPOPTION_FIXPARENTTIMESTAMPMISMATCH"></span>**\_FixParentTimestampMismatch vmStartupOption**</span><span class="sxs-lookup"><span data-stu-id="9544c-112"><span id="vmStartupOption_FixParentTimestampMismatch"></span><span id="vmstartupoption_fixparenttimestampmismatch"></span><span id="VMSTARTUPOPTION_FIXPARENTTIMESTAMPMISMATCH"></span>**vmStartupOption\_FixParentTimestampMismatch**</span></span>
</dt> <dd>

<span data-ttu-id="9544c-113">Correggere la mancata corrispondenza del timestamp padre.</span><span class="sxs-lookup"><span data-stu-id="9544c-113">Fix the parent timestamp mismatch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9544c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9544c-114">Requirements</span></span>



| <span data-ttu-id="9544c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9544c-115">Requirement</span></span> | <span data-ttu-id="9544c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9544c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9544c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9544c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9544c-118">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9544c-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9544c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9544c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9544c-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9544c-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9544c-121">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="9544c-121">End of client support</span></span><br/>    | <span data-ttu-id="9544c-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9544c-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9544c-123">Prodotto</span><span class="sxs-lookup"><span data-stu-id="9544c-123">Product</span></span><br/>                  | <span data-ttu-id="9544c-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9544c-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9544c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9544c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9544c-126"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9544c-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9544c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9544c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9544c-128">**IVMVirtualMachine:: Startup2**</span><span class="sxs-lookup"><span data-stu-id="9544c-128">**IVMVirtualMachine::Startup2**</span></span>](ivmvirtualmachine-startup2.md)
</dt> </dl>

 

