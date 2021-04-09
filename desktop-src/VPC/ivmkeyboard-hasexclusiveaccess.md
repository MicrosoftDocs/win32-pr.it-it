---
title: Proprietà IVMKeyboard HasExclusiveAccess (VPCCOMInterfaces. h)
description: Indica se questo oggetto ha un controllo esclusivo sul dispositivo della tastiera della macchina virtuale.
ms.assetid: edba154e-e700-488c-9133-91649daecef1
keywords:
- Proprietà HasExclusiveAccess Virtual PC
- Proprietà HasExclusiveAccess Virtual PC, interfaccia IVMKeyboard
- Interfaccia IVMKeyboard Virtual PC, proprietà HasExclusiveAccess
topic_type:
- apiref
api_name:
- IVMKeyboard.HasExclusiveAccess
- IVMKeyboard.get_HasExclusiveAccess
- IVMKeyboard.put_HasExclusiveAccess
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62c235f3b4325a70a939239ac1e44360b3b5d9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121103"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a><span data-ttu-id="8726b-106">Proprietà IVMKeyboard:: HasExclusiveAccess</span><span class="sxs-lookup"><span data-stu-id="8726b-106">IVMKeyboard::HasExclusiveAccess property</span></span>

<span data-ttu-id="8726b-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8726b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8726b-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8726b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8726b-109">Indica se questo oggetto dispone del controllo esclusivo sul dispositivo della tastiera della macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="8726b-109">Indicates whether this object has exclusive control over the virtual machine's (VM) keyboard device.</span></span>

<span data-ttu-id="8726b-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="8726b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8726b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8726b-111">Syntax</span></span>


```C++
HRESULT put_HasExclusiveAccess(
  [in]          VARIANT_BOOL makeExclusive
);

HRESULT get_HasExclusiveAccess(
  [out, retval] VARIANT_BOOL *isExclusive
);
```



## <a name="property-value"></a><span data-ttu-id="8726b-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="8726b-112">Property value</span></span>

<span data-ttu-id="8726b-113">**True** se l'accesso esclusivo al dispositivo della tastiera della macchina virtuale è stato acquisito; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="8726b-113">**TRUE** if exclusive access to the VM's keyboard device has been acquired, **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8726b-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="8726b-114">Error codes</span></span>



| <span data-ttu-id="8726b-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="8726b-115">Name/value</span></span>                                                                                                                                                                   | <span data-ttu-id="8726b-116">Significato</span><span class="sxs-lookup"><span data-stu-id="8726b-116">Meaning</span></span>                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8726b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8726b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                      | <span data-ttu-id="8726b-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="8726b-118">The operation was successful.</span></span><br/>                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="8726b-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8726b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                        | <span data-ttu-id="8726b-120">Il parametro *Noexclusive* è **null**.</span><span class="sxs-lookup"><span data-stu-id="8726b-120">The *isExclusive* parameter is **NULL**.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="8726b-121"><dt>S \_ FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8726b-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                   | <span data-ttu-id="8726b-122">La modalità esclusiva richiesta è già impostata per questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8726b-122">The requested exclusive mode is already set for this device.</span></span> <span data-ttu-id="8726b-123">Questo problema può verificarsi quando si tenta di impostare la modalità esclusiva quando è già stata acquisita o quando si tenta di rilasciare la modalità esclusiva quando non è stata acquisita in precedenza.</span><span class="sxs-lookup"><span data-stu-id="8726b-123">This can happen when trying to set exclusive mode when it has already been acquired, or when trying to release exclusive mode when it had not been previously acquired.</span></span><br/> |
| <dl> <span data-ttu-id="8726b-124"><dt>Macchina virtuale \_ E \_ imposta \_ \_ modalità esclusiva \_ non riuscita</dt> <dt>0xA0040825</dt></span><span class="sxs-lookup"><span data-stu-id="8726b-124"><dt>VM\_E\_SET\_EXCLUSIVE\_MODE\_FAIL</dt> <dt>0xA0040825</dt></span></span> </dl> | <span data-ttu-id="8726b-125">Non è stato possibile impostare o rilasciare la modalità esclusiva come richiesto.</span><span class="sxs-lookup"><span data-stu-id="8726b-125">Failed to set or release exclusive mode as requested.</span></span> <span data-ttu-id="8726b-126">Questo potrebbe essere dovuto al fatto che la macchina virtuale non è più in esecuzione o perché un altro processo ha già acquisito la modalità esclusiva sul dispositivo della tastiera della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="8726b-126">This could be because the VM is no longer running, or because another process has already acquired exclusive mode on the VM's keyboard device.</span></span><br/>                                 |
| <dl> <span data-ttu-id="8726b-127"><dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8726b-127"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                     | <span data-ttu-id="8726b-128">La stringa specificata è vuota o contiene un codice chiave non valido.</span><span class="sxs-lookup"><span data-stu-id="8726b-128">The specified string is empty, or contains an invalid key code.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="8726b-129"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8726b-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                | <span data-ttu-id="8726b-130">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="8726b-130">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                    |



## <a name="requirements"></a><span data-ttu-id="8726b-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8726b-131">Requirements</span></span>



| <span data-ttu-id="8726b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8726b-132">Requirement</span></span> | <span data-ttu-id="8726b-133">Valore</span><span class="sxs-lookup"><span data-stu-id="8726b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8726b-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8726b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8726b-135">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8726b-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8726b-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8726b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8726b-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8726b-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8726b-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8726b-138">End of client support</span></span><br/>    | <span data-ttu-id="8726b-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8726b-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8726b-140">Prodotto</span><span class="sxs-lookup"><span data-stu-id="8726b-140">Product</span></span><br/>                  | <span data-ttu-id="8726b-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8726b-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8726b-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8726b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="8726b-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8726b-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8726b-144">IID</span><span class="sxs-lookup"><span data-stu-id="8726b-144">IID</span></span><br/>                      | <span data-ttu-id="8726b-145">IID \_ IVMKeyboard è definito come 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="8726b-145">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="8726b-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8726b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8726b-147">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="8726b-147">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

