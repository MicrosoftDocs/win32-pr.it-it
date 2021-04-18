---
title: Metodo IVMVirtualMachine DetachUSBDevice (VPCCOMInterfaces. h)
description: Rilascia un dispositivo USB da una macchina virtuale.
ms.assetid: ae2b70b1-7bf3-4a84-9f05-4e91de93fa73
keywords:
- Metodo DetachUSBDevice Virtual PC
- Metodo DetachUSBDevice Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo DetachUSBDevice
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DetachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f5a858c25822e9e9ba1a11686003b326133a59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302093"
---
# <a name="ivmvirtualmachinedetachusbdevice-method"></a><span data-ttu-id="01941-106">IVMVirtualMachine::D Metodo etachUSBDevice</span><span class="sxs-lookup"><span data-stu-id="01941-106">IVMVirtualMachine::DetachUSBDevice method</span></span>

<span data-ttu-id="01941-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="01941-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="01941-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="01941-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="01941-109">Rilascia un dispositivo USB da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="01941-109">Releases a USB device from a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="01941-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01941-110">Syntax</span></span>


```C++
HRESULT DetachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a><span data-ttu-id="01941-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="01941-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01941-112">*inUSBDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01941-112">*inUSBDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01941-113">Puntatore [**IVMUSBDevice**](ivmusbdevice.md) che rappresenta il dispositivo USB da scollegare dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="01941-113">A [**IVMUSBDevice**](ivmusbdevice.md) pointer that represents the USB device to be detached from the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01941-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01941-114">Return value</span></span>

<span data-ttu-id="01941-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="01941-115">This method can return one of these values.</span></span>



| <span data-ttu-id="01941-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="01941-116">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="01941-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01941-117">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="01941-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="01941-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="01941-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="01941-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="01941-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="01941-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                  | <span data-ttu-id="01941-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="01941-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="01941-122"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="01941-122"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>     | <span data-ttu-id="01941-123">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="01941-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="01941-124"><dt>**Macchina virtuale \_ \_Scollegamento USB E 0xA00400927 \_ \_ non riuscito**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="01941-124"><dt>**VM\_E\_USB\_DETACH\_FAILED**</dt> <dt>0xA00400927</dt></span></span> </dl> | <span data-ttu-id="01941-125">Operazione di scollegamento non riuscita.</span><span class="sxs-lookup"><span data-stu-id="01941-125">The detach operation failed.</span></span><br/>        |
| <dl> <span data-ttu-id="01941-126"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="01941-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="01941-127">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="01941-127">An unexpected error has occurred.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="01941-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01941-128">Requirements</span></span>



| <span data-ttu-id="01941-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="01941-129">Requirement</span></span> | <span data-ttu-id="01941-130">Valore</span><span class="sxs-lookup"><span data-stu-id="01941-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="01941-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01941-131">Minimum supported client</span></span><br/> | <span data-ttu-id="01941-132">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="01941-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="01941-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01941-133">Minimum supported server</span></span><br/> | <span data-ttu-id="01941-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="01941-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="01941-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="01941-135">End of client support</span></span><br/>    | <span data-ttu-id="01941-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="01941-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="01941-137">Prodotto</span><span class="sxs-lookup"><span data-stu-id="01941-137">Product</span></span><br/>                  | <span data-ttu-id="01941-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="01941-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="01941-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="01941-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="01941-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="01941-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="01941-141">IID</span><span class="sxs-lookup"><span data-stu-id="01941-141">IID</span></span><br/>                      | <span data-ttu-id="01941-142">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="01941-142">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="01941-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01941-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01941-144">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="01941-144">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

