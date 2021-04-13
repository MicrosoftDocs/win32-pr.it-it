---
title: Proprietà IVMVirtualMachine ShutdownActionOnQuit (VPCCOMInterfaces. h)
description: Azione da eseguire in questa macchina virtuale se è in esecuzione quando viene chiuso il PC virtuale di Windows.
ms.assetid: 3f6b256e-c48a-4a7c-acee-83d996e13ec7
keywords:
- Proprietà ShutdownActionOnQuit Virtual PC
- Proprietà ShutdownActionOnQuit Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà ShutdownActionOnQuit
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ShutdownActionOnQuit
- IVMVirtualMachine.get_ShutdownActionOnQuit
- IVMVirtualMachine.put_ShutdownActionOnQuit
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01469e48e767777c6ea3daa4d0f3a923dce67726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478329"
---
# <a name="ivmvirtualmachineshutdownactiononquit-property"></a><span data-ttu-id="3e88a-106">Proprietà IVMVirtualMachine:: ShutdownActionOnQuit</span><span class="sxs-lookup"><span data-stu-id="3e88a-106">IVMVirtualMachine::ShutdownActionOnQuit property</span></span>

<span data-ttu-id="3e88a-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3e88a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3e88a-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3e88a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3e88a-109">Recupera e imposta l'azione da eseguire su questa macchina virtuale (VM) se è in esecuzione quando Windows Virtual PC viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="3e88a-109">Retrieves and sets the action to be performed on this virtual machine (VM) if it is running when Windows Virtual PC is quit.</span></span>

<span data-ttu-id="3e88a-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3e88a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e88a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e88a-111">Syntax</span></span>


```C++
HRESULT put_ShutdownActionOnQuit(
  [in]          VMShutdownAction shutdownAction
);

HRESULT get_ShutdownActionOnQuit(
  [out, retval] VMShutdownAction *shutdownAction
);
```



## <a name="property-value"></a><span data-ttu-id="3e88a-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3e88a-112">Property value</span></span>

<span data-ttu-id="3e88a-113">Specifica come arrestare questa macchina virtuale se è in esecuzione quando viene chiuso il PC virtuale di Windows.</span><span class="sxs-lookup"><span data-stu-id="3e88a-113">Specifies how to shut down this VM if it is running when Windows Virtual PC is quit.</span></span> <span data-ttu-id="3e88a-114">Per un elenco di valori, vedere [**VMShutdownAction**](vmshutdownaction.md).</span><span class="sxs-lookup"><span data-stu-id="3e88a-114">For a list of values, see [**VMShutdownAction**](vmshutdownaction.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="3e88a-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="3e88a-115">Error codes</span></span>



| <span data-ttu-id="3e88a-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="3e88a-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3e88a-117">Significato</span><span class="sxs-lookup"><span data-stu-id="3e88a-117">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e88a-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3e88a-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3e88a-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="3e88a-119">The operation was successful.</span></span><br/>                                       |
| <dl> <span data-ttu-id="3e88a-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3e88a-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3e88a-121">Il parametro è **null** o non è un valore valido.</span><span class="sxs-lookup"><span data-stu-id="3e88a-121">The parameter is **NULL** or not a valid value.</span></span><br/>                     |
| <dl> <span data-ttu-id="3e88a-122"><dt>E \_ </dt> <dt>0x80070005</dt> AccessDenied</span><span class="sxs-lookup"><span data-stu-id="3e88a-122"><dt>E\_ACCESSDENIED</dt> <dt>0x80070005</dt></span></span> </dl>    | <span data-ttu-id="3e88a-123">L'utente corrente non dispone di accesso sufficiente al file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="3e88a-123">The current user has insufficient access to the configuration file.</span></span><br/> |
| <dl> <span data-ttu-id="3e88a-124"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3e88a-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="3e88a-125">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="3e88a-125">The configuration is unknown.</span></span><br/>                                       |
| <dl> <span data-ttu-id="3e88a-126"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3e88a-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3e88a-127">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="3e88a-127">An unexpected error has occurred.</span></span><br/>                                   |



## <a name="remarks"></a><span data-ttu-id="3e88a-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e88a-128">Remarks</span></span>

<span data-ttu-id="3e88a-129">Per impostazione predefinita, le macchine virtuali in esecuzione vengono salvate alla chiusura di Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="3e88a-129">By default, running VMs are saved when Windows Virtual PC is quit.</span></span> <span data-ttu-id="3e88a-130">L'azione di arresto **vmShutdownAction \_ Save** (0) salverà lo stato della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3e88a-130">The shutdown action **vmShutdownAction\_Save** (0) will save the VM's state.</span></span> <span data-ttu-id="3e88a-131">L'azione **vmShutdownAction \_ deviazione** (1) disattiva la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="3e88a-131">The **vmShutdownAction\_TurnOff** (1) action will turn off the VM.</span></span> <span data-ttu-id="3e88a-132">L'azione di **\_ arresto vmShutdownAction** (2) arresterà il sistema operativo guest se i componenti di integrazione sono disponibili e salverà la macchina virtuale in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3e88a-132">The **vmShutdownAction\_Shutdown** (2) action will shut down the guest operating system if the integration components are available and will save the VM otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e88a-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e88a-133">Requirements</span></span>



| <span data-ttu-id="3e88a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e88a-134">Requirement</span></span> | <span data-ttu-id="3e88a-135">Valore</span><span class="sxs-lookup"><span data-stu-id="3e88a-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e88a-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e88a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3e88a-137">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3e88a-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e88a-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e88a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3e88a-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3e88a-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3e88a-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="3e88a-140">End of client support</span></span><br/>    | <span data-ttu-id="3e88a-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3e88a-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3e88a-142">Prodotto</span><span class="sxs-lookup"><span data-stu-id="3e88a-142">Product</span></span><br/>                  | <span data-ttu-id="3e88a-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3e88a-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3e88a-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e88a-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e88a-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e88a-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3e88a-146">IID</span><span class="sxs-lookup"><span data-stu-id="3e88a-146">IID</span></span><br/>                      | <span data-ttu-id="3e88a-147">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="3e88a-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="3e88a-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e88a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e88a-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="3e88a-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="3e88a-150">**VMShutdownAction**</span><span class="sxs-lookup"><span data-stu-id="3e88a-150">**VMShutdownAction**</span></span>](vmshutdownaction.md)
</dt> </dl>

 

