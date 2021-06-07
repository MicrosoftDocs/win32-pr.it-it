---
title: Metodo SetParameter IVMGuestOS (VPCCOMInterfaces.h)
description: Imposta un parametro denominato all'interno del sistema operativo guest.
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- Metodo SetParameter Virtual PC
- Metodo SetParameter Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo SetParameter
topic_type:
- apiref
api_name:
- IVMGuestOS.SetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cc99d9b38ab43327b4a435c4128378d49682935
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386710"
---
# <a name="ivmguestossetparameter-method"></a><span data-ttu-id="65bbd-106">Metodo IVMGuestOS::SetParameter</span><span class="sxs-lookup"><span data-stu-id="65bbd-106">IVMGuestOS::SetParameter method</span></span>

<span data-ttu-id="65bbd-107">\[Windows Virtual PC non è più disponibile per l'uso a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="65bbd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="65bbd-108">Usare invece il [provider WMI Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]</span><span class="sxs-lookup"><span data-stu-id="65bbd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="65bbd-109">Imposta un parametro denominato all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="65bbd-109">Sets a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="65bbd-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65bbd-110">Syntax</span></span>


```C++
HRESULT SetParameter(
  [in] BSTR inParameterName,
  [in] BSTR inParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="65bbd-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="65bbd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65bbd-112">*inParameterName* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="65bbd-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65bbd-113">Nome del parametro.</span><span class="sxs-lookup"><span data-stu-id="65bbd-113">The parameter name.</span></span> <span data-ttu-id="65bbd-114">Deve avere una lunghezza compresa tra 1 e 255 caratteri e non può contenere una barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="65bbd-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\\) character.</span></span>

</dd> <dt>

<span data-ttu-id="65bbd-115">*inParameterValue* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="65bbd-115">*inParameterValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65bbd-116">Valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="65bbd-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65bbd-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65bbd-117">Return value</span></span>

<span data-ttu-id="65bbd-118">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="65bbd-118">This method can return one of these values.</span></span>



| <span data-ttu-id="65bbd-119">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="65bbd-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="65bbd-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65bbd-120">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="65bbd-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="65bbd-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="65bbd-122">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="65bbd-122">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="65bbd-123"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="65bbd-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="65bbd-124">Parametro non valido o non specificato.</span><span class="sxs-lookup"><span data-stu-id="65bbd-124">A parameter is not valid or not specified.</span></span><br/>           |
| <dl> <span data-ttu-id="65bbd-125"><dt>**Macchina virtuale \_ E \_ TIMEOUT \_ 0xA0040202**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="65bbd-125"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="65bbd-126">L'operazione non è stata completata in modo corretto.</span><span class="sxs-lookup"><span data-stu-id="65bbd-126">The operation did not complete in a timely manner.</span></span><br/>   |
| <dl> <span data-ttu-id="65bbd-127"><dt>**Macchina virtuale \_ E \_ MACCHINA VIRTUALE NON IN \_ \_ ESECUZIONE**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="65bbd-127"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="65bbd-128">La macchina virtuale (VM) non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="65bbd-128">The virtual machine (VM) is not running.</span></span><br/>             |
| <dl> <span data-ttu-id="65bbd-129"><dt>**Macchina virtuale \_ E \_ MACCHINA \_ VIRTUALE SOSPESA**</dt> <dt>0xA00400507</dt></span><span class="sxs-lookup"><span data-stu-id="65bbd-129"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="65bbd-130">La macchina virtuale è sospesa.</span><span class="sxs-lookup"><span data-stu-id="65bbd-130">The VM is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="65bbd-131"><dt>**Macchina virtuale \_ FUNZIONALITÀ \_ DELLE AGGIUNTE E NON \_ \_ \_ 0XA0040505**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="65bbd-131"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="65bbd-132">I componenti di integrazione non sono installati in questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="65bbd-132">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="65bbd-133"><dt>**DISP \_ E \_ ECCEZIONE**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="65bbd-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="65bbd-134">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="65bbd-134">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="65bbd-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="65bbd-135">Remarks</span></span>

<span data-ttu-id="65bbd-136">La macchina virtuale deve essere in esecuzione e i componenti di integrazione devono essere installati quando viene richiamato questo metodo.</span><span class="sxs-lookup"><span data-stu-id="65bbd-136">The VM must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="65bbd-137">Questo metodo è supportato solo per i sistemi operativi guest basati su Windows.</span><span class="sxs-lookup"><span data-stu-id="65bbd-137">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="65bbd-138">Con i componenti di integrazione installati, la chiave seguente viene aggiunta automaticamente al Registro di sistema del sistema operativo guest:</span><span class="sxs-lookup"><span data-stu-id="65bbd-138">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="65bbd-139">**HKEY \_ LOCAL MACHINE SOFTWARE Parametri guest macchina virtuale \_ \\ \\ \\ \\ \\ Microsoft**</span><span class="sxs-lookup"><span data-stu-id="65bbd-139">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="65bbd-140">All'avvio del sistema operativo guest, i valori della stringa del Registro di sistema seguenti vengono popolati nella **chiave Parameters:**</span><span class="sxs-lookup"><span data-stu-id="65bbd-140">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="65bbd-141">**HostName**</span><span class="sxs-lookup"><span data-stu-id="65bbd-141">**HostName**</span></span>
-   <span data-ttu-id="65bbd-142">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="65bbd-142">**PhysicalHostName**</span></span>
-   <span data-ttu-id="65bbd-143">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="65bbd-143">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="65bbd-144">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="65bbd-144">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="65bbd-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65bbd-145">Requirements</span></span>



| <span data-ttu-id="65bbd-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="65bbd-146">Requirement</span></span> | <span data-ttu-id="65bbd-147">Valore</span><span class="sxs-lookup"><span data-stu-id="65bbd-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="65bbd-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65bbd-148">Minimum supported client</span></span><br/> | <span data-ttu-id="65bbd-149">Solo app desktop di Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="65bbd-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="65bbd-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65bbd-150">Minimum supported server</span></span><br/> | <span data-ttu-id="65bbd-151">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="65bbd-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="65bbd-152">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="65bbd-152">End of client support</span></span><br/>    | <span data-ttu-id="65bbd-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="65bbd-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="65bbd-154">Prodotto</span><span class="sxs-lookup"><span data-stu-id="65bbd-154">Product</span></span><br/>                  | <span data-ttu-id="65bbd-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="65bbd-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="65bbd-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65bbd-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="65bbd-157"><dt>VPCCOMInterfaces.h</dt></span><span class="sxs-lookup"><span data-stu-id="65bbd-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="65bbd-158">IID</span><span class="sxs-lookup"><span data-stu-id="65bbd-158">IID</span></span><br/>                      | <span data-ttu-id="65bbd-159">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="65bbd-159">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="65bbd-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65bbd-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65bbd-161">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="65bbd-161">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

