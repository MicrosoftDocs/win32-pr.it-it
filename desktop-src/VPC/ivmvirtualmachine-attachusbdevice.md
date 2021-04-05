---
title: Metodo IVMVirtualMachine AttachUSBDevice (VPCCOMInterfaces. h)
description: Connette un dispositivo USB a una macchina virtuale.
ms.assetid: 505078ee-9159-407d-ab8c-a9aba86dec48
keywords:
- Metodo AttachUSBDevice Virtual PC
- Metodo AttachUSBDevice Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo AttachUSBDevice
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachUSBDevice
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3c36224823e4bd74b6a1c757816d55608e6d95a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048494"
---
# <a name="ivmvirtualmachineattachusbdevice-method"></a><span data-ttu-id="7f9c1-106">Metodo IVMVirtualMachine:: AttachUSBDevice</span><span class="sxs-lookup"><span data-stu-id="7f9c1-106">IVMVirtualMachine::AttachUSBDevice method</span></span>

<span data-ttu-id="7f9c1-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7f9c1-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7f9c1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7f9c1-109">Connette un dispositivo USB a una macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="7f9c1-109">Attaches a USB device to a virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="7f9c1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f9c1-110">Syntax</span></span>


```C++
HRESULT AttachUSBDevice(
  [in] IVMUSBDevice *inUSBDevice
);
```



## <a name="parameters"></a><span data-ttu-id="7f9c1-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f9c1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f9c1-112">*inUSBDevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f9c1-112">*inUSBDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f9c1-113">Puntatore [**IVMUSBDevice**](ivmusbdevice.md) che rappresenta il dispositivo USB connesso all'host.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-113">A [**IVMUSBDevice**](ivmusbdevice.md) pointer that represents the USB device connected to the host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f9c1-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f9c1-114">Return value</span></span>

<span data-ttu-id="7f9c1-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-115">This method can return one of these values.</span></span>



| <span data-ttu-id="7f9c1-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f9c1-116">Return code/value</span></span>                                                                                                                                                                             | <span data-ttu-id="7f9c1-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f9c1-117">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f9c1-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7f9c1-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                   | <span data-ttu-id="7f9c1-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-119">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="7f9c1-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7f9c1-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                     | <span data-ttu-id="7f9c1-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-121">The parameter is **NULL**.</span></span><br/>                                              |
| <dl> <span data-ttu-id="7f9c1-122"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="7f9c1-122"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                        | <span data-ttu-id="7f9c1-123">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-123">The VM is not running.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="7f9c1-124"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7f9c1-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                             | <span data-ttu-id="7f9c1-125">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-125">The configuration is unknown.</span></span><br/>                                           |
| <dl> <span data-ttu-id="7f9c1-126"><dt>**Macchina virtuale \_ \_Aggiunte di E \_ non \_ disponibili**</dt> <dt>0xA0040504</dt></span><span class="sxs-lookup"><span data-stu-id="7f9c1-126"><dt>**VM\_E\_ADDITIONS\_NOT\_AVAIL**</dt> <dt>0xA0040504</dt></span></span> </dl>                   | <span data-ttu-id="7f9c1-127">I componenti di integrazione non sono disponibili nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-127">Integration Components are not available in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="7f9c1-128"><dt>**Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="7f9c1-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>          | <span data-ttu-id="7f9c1-129">La funzionalità USB non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-129">The USB feature is not available.</span></span><br/>                                       |
| <dl> <span data-ttu-id="7f9c1-130"><dt>**Macchina virtuale \_ \_ \_ \_ \_ Errore driver connettore USB E**</dt> <dt>0xA00400925</dt></span><span class="sxs-lookup"><span data-stu-id="7f9c1-130"><dt>**VM\_E\_USB\_CONNECTOR\_DRIVER\_ERROR**</dt> <dt>0xA00400925</dt></span></span> </dl>          | <span data-ttu-id="7f9c1-131">Si è verificato un errore del driver del connettore USB.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-131">There was a USB Connector driver error.</span></span><br/>                                 |
| <dl> <span data-ttu-id="7f9c1-132"><dt>**Macchina virtuale \_ E \_ \_ collegamento USB \_ non riuscito \_ più \_ dispositivi**</dt> <dt>0xA00400931</dt></span><span class="sxs-lookup"><span data-stu-id="7f9c1-132"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_MORE\_DEVICES**</dt> <dt>0xA00400931</dt></span></span> </dl>     | <span data-ttu-id="7f9c1-133">Non è possibile aggiungere più dispositivi alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-133">Cannot attach more devices to the VM.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7f9c1-134"><dt>**Macchina virtuale \_ \_Errore del \_ GP di collegamento USB E \_ non riuscito \_ \_**</dt> <dt>0xA00400932</dt></span><span class="sxs-lookup"><span data-stu-id="7f9c1-134"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_GP\_ERROR**</dt> <dt>0xA00400932</dt></span></span> </dl>         | <span data-ttu-id="7f9c1-135">Un'impostazione di criteri di gruppo impedisce il reindirizzamento USB.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-135">A group policy setting is preventing the USB redirection.</span></span><br/>               |
| <dl> <span data-ttu-id="7f9c1-136"><dt>**Macchina virtuale \_ Il \_ \_ collegamento USB \_ non è stato \_ già \_ assegnato**</dt> <dt>0xA00400933</dt></span><span class="sxs-lookup"><span data-stu-id="7f9c1-136"><dt>**VM\_E\_USB\_ATTACH\_FAILED\_ALREADY\_ASSIGNED**</dt> <dt>0xA00400933</dt></span></span> </dl> | <span data-ttu-id="7f9c1-137">Un dispositivo USB è già stato collegato da un altro client.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-137">A USB device has already been attached by some other client.</span></span><br/>            |
| <dl> <span data-ttu-id="7f9c1-138"><dt>**Macchina virtuale \_ E \_ \_ collegamento USB \_ non riuscito**</dt> <dt>0xA00400926</dt></span><span class="sxs-lookup"><span data-stu-id="7f9c1-138"><dt>**VM\_E\_USB\_ATTACH\_FAILED**</dt> <dt>0xA00400926</dt></span></span> </dl>                    | <span data-ttu-id="7f9c1-139">Operazione di connessione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-139">The attach operation failed.</span></span><br/>                                            |
| <dl> <span data-ttu-id="7f9c1-140"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7f9c1-140"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                             | <span data-ttu-id="7f9c1-141">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="7f9c1-141">An unexpected error has occurred.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="7f9c1-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f9c1-142">Requirements</span></span>



| <span data-ttu-id="7f9c1-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f9c1-143">Requirement</span></span> | <span data-ttu-id="7f9c1-144">Valore</span><span class="sxs-lookup"><span data-stu-id="7f9c1-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f9c1-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f9c1-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7f9c1-146">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7f9c1-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7f9c1-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f9c1-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7f9c1-148">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7f9c1-148">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7f9c1-149">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="7f9c1-149">End of client support</span></span><br/>    | <span data-ttu-id="7f9c1-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7f9c1-150">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7f9c1-151">Prodotto</span><span class="sxs-lookup"><span data-stu-id="7f9c1-151">Product</span></span><br/>                  | <span data-ttu-id="7f9c1-152">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7f9c1-152">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7f9c1-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f9c1-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f9c1-154"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f9c1-154"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7f9c1-155">IID</span><span class="sxs-lookup"><span data-stu-id="7f9c1-155">IID</span></span><br/>                      | <span data-ttu-id="7f9c1-156">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="7f9c1-156">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="7f9c1-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f9c1-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f9c1-158">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="7f9c1-158">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

