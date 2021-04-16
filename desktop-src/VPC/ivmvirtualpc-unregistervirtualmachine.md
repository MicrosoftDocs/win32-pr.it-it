---
title: Metodo IVMVirtualPC UnregisterVirtualMachine (VPCCOMInterfaces. h)
description: Annulla la registrazione di una configurazione di macchina virtuale senza eliminare il file di configurazione.
ms.assetid: 82ca6ef3-e9e5-471e-b2dc-0ff689a618d9
keywords:
- Metodo UnregisterVirtualMachine Virtual PC
- Metodo UnregisterVirtualMachine Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo UnregisterVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.UnregisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d74380a822253918791b78bc34ac1c796f595ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478994"
---
# <a name="ivmvirtualpcunregistervirtualmachine-method"></a><span data-ttu-id="5f5c5-106">Metodo IVMVirtualPC:: UnregisterVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5f5c5-106">IVMVirtualPC::UnregisterVirtualMachine method</span></span>

<span data-ttu-id="5f5c5-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5f5c5-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5f5c5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5f5c5-109">Annulla la registrazione di una configurazione di macchina virtuale (VM) senza eliminare il file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-109">Unregisters a virtual machine (VM) configuration without deleting the configuration file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f5c5-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f5c5-110">Syntax</span></span>


```C++
HRESULT UnregisterVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="5f5c5-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f5c5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f5c5-112">*virtualmachine* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f5c5-112">*virtualMachine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f5c5-113">Puntatore a un oggetto [**IVMVirtualMachine**](ivmvirtualmachine.md) che rappresenta la configurazione della macchina virtuale di cui annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-113">A pointer to an [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents the VM configuration to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f5c5-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f5c5-114">Return value</span></span>

<span data-ttu-id="5f5c5-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-115">This method can return one of these values.</span></span>



| <span data-ttu-id="5f5c5-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f5c5-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="5f5c5-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f5c5-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5f5c5-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5f5c5-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="5f5c5-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="5f5c5-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="5f5c5-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="5f5c5-121">Il parametro *virtualmachine* è **null**.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-121">The *virtualMachine* parameter was **NULL**.</span></span><br/>                                         |
| <dl> <span data-ttu-id="5f5c5-122"><dt>**Macchina virtuale \_ E \_ macchina virtuale \_ che esegue**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="5f5c5-122"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                        | <span data-ttu-id="5f5c5-123">La macchina virtuale è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-123">The VM is running.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="5f5c5-124"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="5f5c5-124"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="5f5c5-125">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="5f5c5-125">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="5f5c5-126"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5f5c5-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="5f5c5-127">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-127">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="5f5c5-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f5c5-128">Remarks</span></span>

<span data-ttu-id="5f5c5-129">È possibile annullare la registrazione solo delle macchine virtuali arrestate.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-129">Only stopped VMs can be unregistered.</span></span> <span data-ttu-id="5f5c5-130">I dati relativi allo stato salvato o all'unità di annullamento esistenti per questa configurazione verranno conservati quando viene annullata la registrazione di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5f5c5-130">Existing saved state or undo drive data for this configuration will be retained when a VM is unregistered.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f5c5-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f5c5-131">Requirements</span></span>



| <span data-ttu-id="5f5c5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f5c5-132">Requirement</span></span> | <span data-ttu-id="5f5c5-133">Valore</span><span class="sxs-lookup"><span data-stu-id="5f5c5-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f5c5-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f5c5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5f5c5-135">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5f5c5-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5f5c5-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f5c5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5f5c5-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5f5c5-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5f5c5-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5f5c5-138">End of client support</span></span><br/>    | <span data-ttu-id="5f5c5-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5f5c5-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5f5c5-140">Prodotto</span><span class="sxs-lookup"><span data-stu-id="5f5c5-140">Product</span></span><br/>                  | <span data-ttu-id="5f5c5-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5f5c5-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5f5c5-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f5c5-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f5c5-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f5c5-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5f5c5-144">IID</span><span class="sxs-lookup"><span data-stu-id="5f5c5-144">IID</span></span><br/>                      | <span data-ttu-id="5f5c5-145">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="5f5c5-145">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="5f5c5-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f5c5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f5c5-147">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="5f5c5-147">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

