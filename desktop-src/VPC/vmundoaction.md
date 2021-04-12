---
title: Enumerazione VMUndoAction (VPCCOMInterfaces. h)
description: Specifica che cosa accade per annullare le unità quando una macchina virtuale viene arrestata o disattivata.
ms.assetid: f8f96fd3-0b2a-40ae-8b2e-b6bcc995dedd
keywords:
- VMUndoAction enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMUndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10917a5fb8d00e16a28f4b175237484b977cf914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518904"
---
# <a name="vmundoaction-enumeration"></a><span data-ttu-id="f7b49-104">Enumerazione VMUndoAction</span><span class="sxs-lookup"><span data-stu-id="f7b49-104">VMUndoAction enumeration</span></span>

<span data-ttu-id="f7b49-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f7b49-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f7b49-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f7b49-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f7b49-107">Specifica che cosa accade per annullare le unità quando una macchina virtuale viene arrestata o disattivata.</span><span class="sxs-lookup"><span data-stu-id="f7b49-107">Specifies what happens to undo drives when a virtual machine is shut down or turned off.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b49-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7b49-108">Syntax</span></span>


```C++
typedef enum  { 
  vmUndoAction_Discard  = 0,
  vmUndoAction_Keep     = 1,
  vmUndoAction_Commit   = 2
} VMUndoAction;
```



## <a name="constants"></a><span data-ttu-id="f7b49-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="f7b49-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f7b49-110"><span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**eliminazione di vmUndoAction \_**</span><span class="sxs-lookup"><span data-stu-id="f7b49-110"><span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**vmUndoAction\_Discard**</span></span>
</dt> <dd>

<span data-ttu-id="f7b49-111">Rimuovere le unità di annullamento; le unità padre rimangono invariate.</span><span class="sxs-lookup"><span data-stu-id="f7b49-111">Discard the undo drives; the parent drives remain unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="f7b49-112"><span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmUndoAction \_ Keep**</span><span class="sxs-lookup"><span data-stu-id="f7b49-112"><span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmUndoAction\_Keep**</span></span>
</dt> <dd>

<span data-ttu-id="f7b49-113">Mantieni le unità di annullamento; le unità padre rimangono invariate, ma le modifiche verranno mantenute al successivo avvio della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f7b49-113">Keep the undo drives; the parent drives remain unchanged, but changes will be maintained the next time the virtual machine starts.</span></span>

</dd> <dt>

<span data-ttu-id="f7b49-114"><span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**\_commit vmUndoAction**</span><span class="sxs-lookup"><span data-stu-id="f7b49-114"><span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**vmUndoAction\_Commit**</span></span>
</dt> <dd>

<span data-ttu-id="f7b49-115">Eseguire il commit delle modifiche apportate alle unità padre.</span><span class="sxs-lookup"><span data-stu-id="f7b49-115">Commit changes to the parent drives.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f7b49-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f7b49-116">Requirements</span></span>



| <span data-ttu-id="f7b49-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7b49-117">Requirement</span></span> | <span data-ttu-id="f7b49-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f7b49-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b49-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7b49-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b49-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f7b49-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f7b49-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f7b49-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b49-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f7b49-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f7b49-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f7b49-123">End of client support</span></span><br/>    | <span data-ttu-id="f7b49-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f7b49-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f7b49-125">Prodotto</span><span class="sxs-lookup"><span data-stu-id="f7b49-125">Product</span></span><br/>                  | <span data-ttu-id="f7b49-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f7b49-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f7b49-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f7b49-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7b49-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7b49-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7b49-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7b49-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b49-130">**IVMVirtualMachine:: UndoAction**</span><span class="sxs-lookup"><span data-stu-id="f7b49-130">**IVMVirtualMachine::UndoAction**</span></span>](ivmvirtualmachine-undoaction.md)
</dt> </dl>

 

