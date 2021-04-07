---
title: Enumerazione VMLogoffType (VPCCOMInterfaces. h)
description: Specifica come arrestare una macchina virtuale.
ms.assetid: 3a2965e3-2637-4677-b487-98d2b508672c
keywords:
- VMLogoffType enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMLogoffType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c2311736115390d807058bbfc54c24e7f9e9654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048320"
---
# <a name="vmlogofftype-enumeration"></a><span data-ttu-id="02c4c-104">Enumerazione VMLogoffType</span><span class="sxs-lookup"><span data-stu-id="02c4c-104">VMLogoffType enumeration</span></span>

<span data-ttu-id="02c4c-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02c4c-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="02c4c-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="02c4c-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="02c4c-107">Specifica come arrestare una macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="02c4c-107">Specifies how to shut down a virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="02c4c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02c4c-108">Syntax</span></span>


```C++
typedef enum  { 
  vmLogoff_Normal    = 0,
  vmLogoff_Forced    = 1,
  vmLogoff_External  = 2
} VMLogoffType;
```



## <a name="constants"></a><span data-ttu-id="02c4c-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="02c4c-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="02c4c-110"><span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmLogoff \_ normale**</span><span class="sxs-lookup"><span data-stu-id="02c4c-110"><span id="vmLogoff_Normal"></span><span id="vmlogoff_normal"></span><span id="VMLOGOFF_NORMAL"></span>**vmLogoff\_Normal**</span></span>
</dt> <dd>

<span data-ttu-id="02c4c-111">La disconnessione nella macchina virtuale Guest era normale.</span><span class="sxs-lookup"><span data-stu-id="02c4c-111">The logoff in the guest VM was normal.</span></span>

</dd> <dt>

<span data-ttu-id="02c4c-112"><span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmLogoff \_ forzato**</span><span class="sxs-lookup"><span data-stu-id="02c4c-112"><span id="vmLogoff_Forced"></span><span id="vmlogoff_forced"></span><span id="VMLOGOFF_FORCED"></span>**vmLogoff\_Forced**</span></span>
</dt> <dd>

<span data-ttu-id="02c4c-113">La disconnessione nella macchina virtuale Guest è stata forzata.</span><span class="sxs-lookup"><span data-stu-id="02c4c-113">The logoff in the guest VM was forced.</span></span>

</dd> <dt>

<span data-ttu-id="02c4c-114"><span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmLogoff \_ esterno**</span><span class="sxs-lookup"><span data-stu-id="02c4c-114"><span id="vmLogoff_External"></span><span id="vmlogoff_external"></span><span id="VMLOGOFF_EXTERNAL"></span>**vmLogoff\_External**</span></span>
</dt> <dd>

<span data-ttu-id="02c4c-115">La disconnessione nella VM Guest è stata eseguita usando il metodo [**IVMGuestOS:: disconnessione**](ivmguestos-logoff.md) .</span><span class="sxs-lookup"><span data-stu-id="02c4c-115">The logoff in the guest VM was done using the [**IVMGuestOS::Logoff**](ivmguestos-logoff.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02c4c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02c4c-116">Requirements</span></span>



| <span data-ttu-id="02c4c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="02c4c-117">Requirement</span></span> | <span data-ttu-id="02c4c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="02c4c-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="02c4c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02c4c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="02c4c-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="02c4c-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="02c4c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02c4c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="02c4c-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="02c4c-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="02c4c-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="02c4c-123">End of client support</span></span><br/>    | <span data-ttu-id="02c4c-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="02c4c-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="02c4c-125">Prodotto</span><span class="sxs-lookup"><span data-stu-id="02c4c-125">Product</span></span><br/>                  | <span data-ttu-id="02c4c-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="02c4c-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="02c4c-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02c4c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="02c4c-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="02c4c-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02c4c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02c4c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02c4c-130">**IVMVirtualMachine::ShutdownActionOnQuit**</span><span class="sxs-lookup"><span data-stu-id="02c4c-130">**IVMVirtualMachine::ShutdownActionOnQuit**</span></span>](ivmvirtualmachine-shutdownactiononquit.md)
</dt> </dl>

 

