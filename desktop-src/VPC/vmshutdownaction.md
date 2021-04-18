---
title: Enumerazione VMShutdownAction (VPCCOMInterfaces. h)
description: Specifica come arrestare una macchina virtuale all'arresto dell'host o alla chiusura del vpc.exe processo.
ms.assetid: 271a685a-cac9-4a15-b363-bf8873fd5324
keywords:
- VMShutdownAction enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMShutdownAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b939954042a446f7ad9f128580e804d73e9d29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301558"
---
# <a name="vmshutdownaction-enumeration"></a><span data-ttu-id="6526b-104">Enumerazione VMShutdownAction</span><span class="sxs-lookup"><span data-stu-id="6526b-104">VMShutdownAction enumeration</span></span>

<span data-ttu-id="6526b-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6526b-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6526b-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6526b-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6526b-107">Specifica come arrestare una macchina virtuale (VM) quando l'host viene arrestato o il processo vpc.exe viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="6526b-107">Specifies how to shut down a virtual machine (VM) when the host shuts down or the vpc.exe process exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="6526b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6526b-108">Syntax</span></span>


```C++
typedef enum  { 
  vmShutdownAction_Save      = 0,
  vmShutdownAction_TurnOff   = 1,
  vmShutdownAction_Shutdown  = 2
} VMShutdownAction;
```



## <a name="constants"></a><span data-ttu-id="6526b-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="6526b-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6526b-110"><span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**\_Salva vmShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="6526b-110"><span id="vmShutdownAction_Save"></span><span id="vmshutdownaction_save"></span><span id="VMSHUTDOWNACTION_SAVE"></span>**vmShutdownAction\_Save**</span></span>
</dt> <dd>

<span data-ttu-id="6526b-111">Salvare lo stato della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6526b-111">Save the VM state.</span></span>

</dd> <dt>

<span data-ttu-id="6526b-112"><span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**vmShutdownAction \_ deviazione**</span><span class="sxs-lookup"><span data-stu-id="6526b-112"><span id="vmShutdownAction_TurnOff"></span><span id="vmshutdownaction_turnoff"></span><span id="VMSHUTDOWNACTION_TURNOFF"></span>**vmShutdownAction\_TurnOff**</span></span>
</dt> <dd>

<span data-ttu-id="6526b-113">Spegnere la macchina virtuale senza eseguire la disattivazione delle unità.</span><span class="sxs-lookup"><span data-stu-id="6526b-113">Turn off the VM without undoing the drives.</span></span>

</dd> <dt>

<span data-ttu-id="6526b-114"><span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**\_arresto vmShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="6526b-114"><span id="vmShutdownAction_Shutdown"></span><span id="vmshutdownaction_shutdown"></span><span id="VMSHUTDOWNACTION_SHUTDOWN"></span>**vmShutdownAction\_Shutdown**</span></span>
</dt> <dd>

<span data-ttu-id="6526b-115">Arrestare il sistema operativo guest nella macchina virtuale senza annotare le unità se i componenti di integrazione sono disponibili e la VM verrà salvata in altro modo.</span><span class="sxs-lookup"><span data-stu-id="6526b-115">Shut down the guest operating system on the VM without undoing the drives if the integration components are available and will save the VM otherwise.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6526b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6526b-116">Requirements</span></span>



| <span data-ttu-id="6526b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6526b-117">Requirement</span></span> | <span data-ttu-id="6526b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6526b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6526b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6526b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6526b-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6526b-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6526b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6526b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6526b-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6526b-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6526b-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6526b-123">End of client support</span></span><br/>    | <span data-ttu-id="6526b-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6526b-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6526b-125">Prodotto</span><span class="sxs-lookup"><span data-stu-id="6526b-125">Product</span></span><br/>                  | <span data-ttu-id="6526b-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6526b-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6526b-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6526b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6526b-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6526b-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6526b-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6526b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6526b-130">Enumerazioni Virtual PC Windows</span><span class="sxs-lookup"><span data-stu-id="6526b-130">Windows Virtual PC Enumerations</span></span>](virtual-pc-enumerations.md)
</dt> <dt>

[<span data-ttu-id="6526b-131">**IVMVirtualMachine::ShutdownActionOnQuit**</span><span class="sxs-lookup"><span data-stu-id="6526b-131">**IVMVirtualMachine::ShutdownActionOnQuit**</span></span>](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

