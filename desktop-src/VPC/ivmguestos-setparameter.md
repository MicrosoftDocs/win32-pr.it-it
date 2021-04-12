---
title: Metodo separameter IVMGuestOS (VPCCOMInterfaces. h)
description: Imposta un parametro denominato all'interno del sistema operativo guest.
ms.assetid: ed6ade61-19dc-44ac-9e86-29fffe80e874
keywords:
- Metodo separameter Virtual PC
- Metodo separameter Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo separameter
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
ms.openlocfilehash: 80dd2290578ef55d56e4c194e27102a1075d7a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517896"
---
# <a name="ivmguestossetparameter-method"></a><span data-ttu-id="f72da-106">Metodo IVMGuestOS:: separameter</span><span class="sxs-lookup"><span data-stu-id="f72da-106">IVMGuestOS::SetParameter method</span></span>

<span data-ttu-id="f72da-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f72da-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f72da-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f72da-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f72da-109">Imposta un parametro denominato all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="f72da-109">Sets a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f72da-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f72da-110">Syntax</span></span>


```C++
HRESULT SetParameter(
  [in] BSTR inParameterName,
  [in] BSTR inParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="f72da-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="f72da-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f72da-112">*Inparametername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f72da-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f72da-113">Nome del parametro.</span><span class="sxs-lookup"><span data-stu-id="f72da-113">The parameter name.</span></span> <span data-ttu-id="f72da-114">Deve avere una lunghezza compresa tra 1 e 255 caratteri e non può contenere una barra rovesciata ( \) carattere.</span><span class="sxs-lookup"><span data-stu-id="f72da-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\) character.</span></span>

</dd> <dt>

<span data-ttu-id="f72da-115">*inParameterValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f72da-115">*inParameterValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f72da-116">Valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="f72da-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f72da-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f72da-117">Return value</span></span>

<span data-ttu-id="f72da-118">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="f72da-118">This method can return one of these values.</span></span>



| <span data-ttu-id="f72da-119">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="f72da-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="f72da-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f72da-120">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f72da-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f72da-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="f72da-122">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f72da-122">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="f72da-123"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f72da-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="f72da-124">Un parametro non è valido o non è specificato.</span><span class="sxs-lookup"><span data-stu-id="f72da-124">A parameter is not valid or not specified.</span></span><br/>           |
| <dl> <span data-ttu-id="f72da-125"><dt>**Macchina virtuale \_ E \_ timeout \_**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="f72da-125"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="f72da-126">L'operazione non è stata completata in modo tempestivo.</span><span class="sxs-lookup"><span data-stu-id="f72da-126">The operation did not complete in a timely manner.</span></span><br/>   |
| <dl> <span data-ttu-id="f72da-127"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="f72da-127"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="f72da-128">La macchina virtuale (VM) non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f72da-128">The virtual machine (VM) is not running.</span></span><br/>             |
| <dl> <span data-ttu-id="f72da-129"><dt>**Macchina virtuale \_ 0xA00400507 \_ macchina virtuale E \_ sospesa**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f72da-129"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="f72da-130">La macchina virtuale è sospesa.</span><span class="sxs-lookup"><span data-stu-id="f72da-130">The VM is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f72da-131"><dt>**Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="f72da-131"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="f72da-132">I componenti di integrazione non sono installati in questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f72da-132">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="f72da-133"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f72da-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="f72da-134">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f72da-134">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="f72da-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="f72da-135">Remarks</span></span>

<span data-ttu-id="f72da-136">Quando viene richiamato questo metodo, è necessario che la macchina virtuale sia in esecuzione e che i componenti di integrazione siano installati.</span><span class="sxs-lookup"><span data-stu-id="f72da-136">The VM must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="f72da-137">Questo metodo è supportato solo per i sistemi operativi guest basati su Windows.</span><span class="sxs-lookup"><span data-stu-id="f72da-137">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="f72da-138">Con i componenti di integrazione installati, la chiave seguente viene aggiunta automaticamente al registro di sistema del sistema operativo guest:</span><span class="sxs-lookup"><span data-stu-id="f72da-138">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="f72da-139">**HKEY \_ \_ computer locale \\ software \\ Microsoft \\ Virtual Machine \\ \\ parametri Guest**</span><span class="sxs-lookup"><span data-stu-id="f72da-139">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="f72da-140">Quando viene avviato il sistema operativo guest, i valori stringa del registro di sistema seguenti vengono popolati nella chiave **Parameters** :</span><span class="sxs-lookup"><span data-stu-id="f72da-140">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="f72da-141">**HostName**</span><span class="sxs-lookup"><span data-stu-id="f72da-141">**HostName**</span></span>
-   <span data-ttu-id="f72da-142">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="f72da-142">**PhysicalHostName**</span></span>
-   <span data-ttu-id="f72da-143">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="f72da-143">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="f72da-144">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="f72da-144">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="f72da-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f72da-145">Requirements</span></span>



| <span data-ttu-id="f72da-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="f72da-146">Requirement</span></span> | <span data-ttu-id="f72da-147">Valore</span><span class="sxs-lookup"><span data-stu-id="f72da-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f72da-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f72da-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f72da-149">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f72da-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f72da-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f72da-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f72da-151">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f72da-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f72da-152">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f72da-152">End of client support</span></span><br/>    | <span data-ttu-id="f72da-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f72da-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f72da-154">Prodotto</span><span class="sxs-lookup"><span data-stu-id="f72da-154">Product</span></span><br/>                  | <span data-ttu-id="f72da-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f72da-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f72da-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f72da-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="f72da-157"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f72da-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f72da-158">IID</span><span class="sxs-lookup"><span data-stu-id="f72da-158">IID</span></span><br/>                      | <span data-ttu-id="f72da-159">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="f72da-159">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f72da-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f72da-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f72da-161">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="f72da-161">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

