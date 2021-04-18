---
title: Metodo IVMVirtualPC DeleteVirtualMachine (VPCCOMInterfaces. h)
description: Elimina la configurazione di una macchina virtuale.
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- Metodo DeleteVirtualMachine Virtual PC
- Metodo DeleteVirtualMachine Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo DeleteVirtualMachine
topic_type:
- apiref
api_name:
- IVMVirtualPC.DeleteVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee9c1591ccd736099fab04cce31c8a8b77b5fb06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302162"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a><span data-ttu-id="b2cf2-106">IVMVirtualPC::D Metodo eleteVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="b2cf2-106">IVMVirtualPC::DeleteVirtualMachine method</span></span>

<span data-ttu-id="b2cf2-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b2cf2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b2cf2-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b2cf2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b2cf2-109">Elimina la configurazione di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b2cf2-109">Deletes a virtual machine configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2cf2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2cf2-110">Syntax</span></span>


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="b2cf2-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2cf2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2cf2-112">*virtualmachine* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2cf2-112">*virtualMachine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2cf2-113">Puntatore a un oggetto [**IVMVirtualMachine**](ivmvirtualmachine.md) che rappresenta la configurazione della macchina virtuale da eliminare.</span><span class="sxs-lookup"><span data-stu-id="b2cf2-113">A pointer to an [**IVMVirtualMachine**](ivmvirtualmachine.md) object representing the virtual machine configuration to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2cf2-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2cf2-114">Return value</span></span>

<span data-ttu-id="b2cf2-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="b2cf2-115">This method can return one of these values.</span></span>



| <span data-ttu-id="b2cf2-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2cf2-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="b2cf2-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b2cf2-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b2cf2-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b2cf2-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="b2cf2-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b2cf2-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b2cf2-120"><dt>**S \_ FALSE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b2cf2-120"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                           | <span data-ttu-id="b2cf2-121">Impossibile trovare la configurazione specificata.</span><span class="sxs-lookup"><span data-stu-id="b2cf2-121">The specified configuration could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="b2cf2-122"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b2cf2-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="b2cf2-123">Il parametro *virtualmachine* è **null**.</span><span class="sxs-lookup"><span data-stu-id="b2cf2-123">The *virtualMachine* parameter was **NULL**.</span></span><br/>                                         |
| <dl> <span data-ttu-id="b2cf2-124"><dt>**Macchina virtuale \_ E \_ macchina virtuale \_ che esegue**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="b2cf2-124"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                        | <span data-ttu-id="b2cf2-125">La macchina virtuale è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b2cf2-125">The virtual machine is running.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="b2cf2-126"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="b2cf2-126"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="b2cf2-127">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="b2cf2-127">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="b2cf2-128"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b2cf2-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="b2cf2-129">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="b2cf2-129">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="b2cf2-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2cf2-130">Remarks</span></span>

<span data-ttu-id="b2cf2-131">È possibile eliminare solo le macchine virtuali arrestate.</span><span class="sxs-lookup"><span data-stu-id="b2cf2-131">Only stopped virtual machines can be deleted.</span></span> <span data-ttu-id="b2cf2-132">Si noti che tutti i dati dello stato salvato o dell'unità di annullamento esistenti per questa configurazione verranno eliminati oltre al file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b2cf2-132">Note that any existing saved state or undo drive data for this configuration will be deleted in addition to the configuration file.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2cf2-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2cf2-133">Requirements</span></span>



| <span data-ttu-id="b2cf2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2cf2-134">Requirement</span></span> | <span data-ttu-id="b2cf2-135">Valore</span><span class="sxs-lookup"><span data-stu-id="b2cf2-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2cf2-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2cf2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b2cf2-137">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b2cf2-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b2cf2-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2cf2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b2cf2-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b2cf2-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b2cf2-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b2cf2-140">End of client support</span></span><br/>    | <span data-ttu-id="b2cf2-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b2cf2-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b2cf2-142">Prodotto</span><span class="sxs-lookup"><span data-stu-id="b2cf2-142">Product</span></span><br/>                  | <span data-ttu-id="b2cf2-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b2cf2-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b2cf2-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2cf2-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2cf2-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2cf2-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b2cf2-146">IID</span><span class="sxs-lookup"><span data-stu-id="b2cf2-146">IID</span></span><br/>                      | <span data-ttu-id="b2cf2-147">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="b2cf2-147">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b2cf2-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2cf2-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2cf2-149">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="b2cf2-149">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

