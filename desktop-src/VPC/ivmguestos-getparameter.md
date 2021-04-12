---
title: Metodo GetParameter IVMGuestOS (VPCCOMInterfaces. h)
description: Recupera un parametro denominato all'interno del sistema operativo guest.
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- Metodo GetParameter Virtual PC
- Metodo GetParameter Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, Metodo GetParameter
topic_type:
- apiref
api_name:
- IVMGuestOS.GetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0acbdd5a1d633a8c032651d2df16f4d0e26dec70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518796"
---
# <a name="ivmguestosgetparameter-method"></a><span data-ttu-id="07fb0-106">Metodo IVMGuestOS:: GetParameter</span><span class="sxs-lookup"><span data-stu-id="07fb0-106">IVMGuestOS::GetParameter method</span></span>

<span data-ttu-id="07fb0-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="07fb0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="07fb0-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="07fb0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="07fb0-109">Recupera un parametro denominato all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="07fb0-109">Retrieves a named parameter within the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="07fb0-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07fb0-110">Syntax</span></span>


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a><span data-ttu-id="07fb0-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="07fb0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07fb0-112">*Inparametername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07fb0-112">*inParameterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07fb0-113">Nome del parametro.</span><span class="sxs-lookup"><span data-stu-id="07fb0-113">The parameter name.</span></span> <span data-ttu-id="07fb0-114">Deve avere una lunghezza compresa tra 1 e 255 caratteri e non può contenere una barra rovesciata ( \) carattere.</span><span class="sxs-lookup"><span data-stu-id="07fb0-114">It must be between 1 and 255 characters in length and cannot contain a backslash (\) character.</span></span>

</dd> <dt>

<span data-ttu-id="07fb0-115">*outParameterValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="07fb0-115">*outParameterValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="07fb0-116">Valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="07fb0-116">The parameter value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07fb0-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07fb0-117">Return value</span></span>

<span data-ttu-id="07fb0-118">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="07fb0-118">This method can return one of these values.</span></span>



| <span data-ttu-id="07fb0-119">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="07fb0-119">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="07fb0-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07fb0-120">Description</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="07fb0-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="07fb0-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="07fb0-122">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="07fb0-122">The operation was successful.</span></span><br/>                                     |
| <dl> <span data-ttu-id="07fb0-123"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="07fb0-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="07fb0-124">Un parametro non è valido o non è specificato.</span><span class="sxs-lookup"><span data-stu-id="07fb0-124">A parameter is not valid or not specified.</span></span><br/>                        |
| <dl> <span data-ttu-id="07fb0-125"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="07fb0-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="07fb0-126">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="07fb0-126">The parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="07fb0-127"><dt>**Macchina virtuale \_ E \_ timeout \_**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="07fb0-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="07fb0-128">L'operazione non è stata completata in modo tempestivo.</span><span class="sxs-lookup"><span data-stu-id="07fb0-128">The operation did not complete in a timely manner.</span></span><br/>                |
| <dl> <span data-ttu-id="07fb0-129"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="07fb0-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="07fb0-130">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="07fb0-130">The virtual machine is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="07fb0-131"><dt>**Macchina virtuale \_ 0xA00400507 \_ macchina virtuale E \_ sospesa**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="07fb0-131"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                    | <span data-ttu-id="07fb0-132">La macchina virtuale è sospesa.</span><span class="sxs-lookup"><span data-stu-id="07fb0-132">The virtual machine is paused.</span></span><br/>                                    |
| <dl> <span data-ttu-id="07fb0-133"><dt>**Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="07fb0-133"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="07fb0-134">I componenti di integrazione non sono installati in questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="07fb0-134">Integration components are not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="07fb0-135"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="07fb0-135"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="07fb0-136">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="07fb0-136">An unexpected error has occurred.</span></span><br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="07fb0-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="07fb0-137">Remarks</span></span>

<span data-ttu-id="07fb0-138">Quando viene richiamato questo metodo, è necessario che la macchina virtuale sia in esecuzione e che i componenti di integrazione siano installati.</span><span class="sxs-lookup"><span data-stu-id="07fb0-138">The virtual machine must be running and integration components must be installed when this method is invoked.</span></span> <span data-ttu-id="07fb0-139">Questo metodo è supportato solo per i sistemi operativi guest basati su Windows.</span><span class="sxs-lookup"><span data-stu-id="07fb0-139">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="07fb0-140">Con i componenti di integrazione installati, la chiave seguente viene aggiunta automaticamente al registro di sistema del sistema operativo guest:</span><span class="sxs-lookup"><span data-stu-id="07fb0-140">With integration components installed, the following key is automatically added to the guest operating system's registry:</span></span>

<span data-ttu-id="07fb0-141">**HKEY \_ \_ computer locale \\ software \\ Microsoft \\ Virtual Machine \\ \\ parametri Guest**</span><span class="sxs-lookup"><span data-stu-id="07fb0-141">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Guest\\Parameters**</span></span>

<span data-ttu-id="07fb0-142">Quando viene avviato il sistema operativo guest, i valori stringa del registro di sistema seguenti vengono popolati nella chiave **Parameters** :</span><span class="sxs-lookup"><span data-stu-id="07fb0-142">When the guest operating system starts, the following registry string values are populated in the **Parameters** key:</span></span>

-   <span data-ttu-id="07fb0-143">**HostName**</span><span class="sxs-lookup"><span data-stu-id="07fb0-143">**HostName**</span></span>
-   <span data-ttu-id="07fb0-144">**PhysicalHostName**</span><span class="sxs-lookup"><span data-stu-id="07fb0-144">**PhysicalHostName**</span></span>
-   <span data-ttu-id="07fb0-145">**PhysicalHostNameFullyQualified**</span><span class="sxs-lookup"><span data-stu-id="07fb0-145">**PhysicalHostNameFullyQualified**</span></span>
-   <span data-ttu-id="07fb0-146">**VirtualMachineName**</span><span class="sxs-lookup"><span data-stu-id="07fb0-146">**VirtualMachineName**</span></span>

## <a name="requirements"></a><span data-ttu-id="07fb0-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07fb0-147">Requirements</span></span>



| <span data-ttu-id="07fb0-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="07fb0-148">Requirement</span></span> | <span data-ttu-id="07fb0-149">Valore</span><span class="sxs-lookup"><span data-stu-id="07fb0-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="07fb0-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07fb0-150">Minimum supported client</span></span><br/> | <span data-ttu-id="07fb0-151">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="07fb0-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="07fb0-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07fb0-152">Minimum supported server</span></span><br/> | <span data-ttu-id="07fb0-153">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="07fb0-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="07fb0-154">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="07fb0-154">End of client support</span></span><br/>    | <span data-ttu-id="07fb0-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="07fb0-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="07fb0-156">Prodotto</span><span class="sxs-lookup"><span data-stu-id="07fb0-156">Product</span></span><br/>                  | <span data-ttu-id="07fb0-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="07fb0-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="07fb0-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07fb0-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="07fb0-159"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="07fb0-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="07fb0-160">IID</span><span class="sxs-lookup"><span data-stu-id="07fb0-160">IID</span></span><br/>                      | <span data-ttu-id="07fb0-161">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="07fb0-161">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="07fb0-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07fb0-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07fb0-163">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="07fb0-163">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

