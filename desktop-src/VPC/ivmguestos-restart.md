---
title: Metodo di riavvio IVMGuestOS (VPCCOMInterfaces. h)
description: Riavvia il sistema operativo guest.
ms.assetid: 328c7aa1-d9bd-452d-95dd-9f6a03fa8c9e
keywords:
- Riavviare il metodo Virtual PC
- Metodo di riavvio Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo Restart
topic_type:
- apiref
api_name:
- IVMGuestOS.Restart
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 110718e45d04445dd895a2bdb27419fbd24731c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400671"
---
# <a name="ivmguestosrestart-method"></a><span data-ttu-id="52c9c-106">Metodo IVMGuestOS:: Restart</span><span class="sxs-lookup"><span data-stu-id="52c9c-106">IVMGuestOS::Restart method</span></span>

<span data-ttu-id="52c9c-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="52c9c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="52c9c-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="52c9c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="52c9c-109">Riavvia il sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="52c9c-109">Restarts the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c9c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52c9c-110">Syntax</span></span>


```C++
HRESULT Restart(
  [in]          VARIANT_BOOL inForced,
  [out, retval] IVMTask      **outRestartTask
);
```



## <a name="parameters"></a><span data-ttu-id="52c9c-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="52c9c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52c9c-112">*applicato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52c9c-112">*inForced* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52c9c-113">**Variante \_ TRUE** se è necessario un riavvio forzato e **Variant \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="52c9c-113">**VARIANT\_TRUE** if a forced restart is required and **VARIANT\_FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="52c9c-114">*outRestartTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="52c9c-114">*outRestartTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="52c9c-115">Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia dello stato di completamento della sequenza di riavvio.</span><span class="sxs-lookup"><span data-stu-id="52c9c-115">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the restart sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52c9c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="52c9c-116">Return value</span></span>

<span data-ttu-id="52c9c-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="52c9c-117">This method can return one of these values.</span></span>



| <span data-ttu-id="52c9c-118">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="52c9c-118">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="52c9c-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52c9c-119">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="52c9c-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="52c9c-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="52c9c-121">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="52c9c-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="52c9c-122"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="52c9c-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="52c9c-123">Il parametro *outRestartTask* è **null**.</span><span class="sxs-lookup"><span data-stu-id="52c9c-123">The *outRestartTask* parameter is **NULL**.</span></span><br/>                     |
| <dl> <span data-ttu-id="52c9c-124"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="52c9c-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="52c9c-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="52c9c-125">An unexpected error has occurred.</span></span><br/>                               |
| <dl> <span data-ttu-id="52c9c-126"><dt>**Macchina virtuale \_ E \_ timeout \_**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="52c9c-126"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="52c9c-127">L'operazione non è stata completata in modo tempestivo.</span><span class="sxs-lookup"><span data-stu-id="52c9c-127">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="52c9c-128"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="52c9c-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="52c9c-129">Per questa operazione è necessario che la macchina virtuale (VM) sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="52c9c-129">The virtual machine (VM) must be running for this operation.</span></span><br/>    |
| <dl> <span data-ttu-id="52c9c-130"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="52c9c-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="52c9c-131">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="52c9c-131">The configuration is unknown.</span></span><br/>                                   |
| <dl> <span data-ttu-id="52c9c-132"><dt>**Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="52c9c-132"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="52c9c-133">La funzionalità componenti di integrazione non è installata in questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="52c9c-133">The integration components feature is not installed in this VM.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="52c9c-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="52c9c-134">Remarks</span></span>

<span data-ttu-id="52c9c-135">I valori seguenti possono essere restituiti tramite la proprietà [**Error**](ivmtask-error.md) dell'oggetto [**IVMTask**](ivmtask.md) restituito.</span><span class="sxs-lookup"><span data-stu-id="52c9c-135">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="52c9c-136">Codice [**errore**](ivmtask-error.md) /valore</span><span class="sxs-lookup"><span data-stu-id="52c9c-136">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="52c9c-137">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52c9c-137">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="52c9c-138"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` 0x80070005</span><span class="sxs-lookup"><span data-stu-id="52c9c-138"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)</span></span><br/>                             | <span data-ttu-id="52c9c-139">Il chiamante deve avere le autorizzazioni di accesso Execute per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="52c9c-139">The caller must have execute access permissions for this VM.</span></span><br/>             |
| <span data-ttu-id="52c9c-140"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span><span class="sxs-lookup"><span data-stu-id="52c9c-140"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span></span><br/>                         | <span data-ttu-id="52c9c-141">Il computer è bloccato e non può essere arrestato senza l'opzione Force.</span><span class="sxs-lookup"><span data-stu-id="52c9c-141">The computer is locked and cannot be shut down without the force option.</span></span><br/> |
| <span data-ttu-id="52c9c-142"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span><span class="sxs-lookup"><span data-stu-id="52c9c-142"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span></span><br/>                                             | <span data-ttu-id="52c9c-143">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="52c9c-143">The device is not ready.</span></span><br/>                                                 |
| <span data-ttu-id="52c9c-144"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span><span class="sxs-lookup"><span data-stu-id="52c9c-144"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span></span><br/> | <span data-ttu-id="52c9c-145">È in corso l'arresto del sistema.</span><span class="sxs-lookup"><span data-stu-id="52c9c-145">A system shutdown is in progress.</span></span><br/>                                        |



 

## <a name="requirements"></a><span data-ttu-id="52c9c-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52c9c-146">Requirements</span></span>



| <span data-ttu-id="52c9c-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="52c9c-147">Requirement</span></span> | <span data-ttu-id="52c9c-148">Valore</span><span class="sxs-lookup"><span data-stu-id="52c9c-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="52c9c-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52c9c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="52c9c-150">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="52c9c-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52c9c-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52c9c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="52c9c-152">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="52c9c-152">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="52c9c-153">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="52c9c-153">End of client support</span></span><br/>    | <span data-ttu-id="52c9c-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52c9c-154">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="52c9c-155">Prodotto</span><span class="sxs-lookup"><span data-stu-id="52c9c-155">Product</span></span><br/>                  | <span data-ttu-id="52c9c-156">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="52c9c-156">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="52c9c-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="52c9c-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="52c9c-158"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="52c9c-158"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="52c9c-159">IID</span><span class="sxs-lookup"><span data-stu-id="52c9c-159">IID</span></span><br/>                      | <span data-ttu-id="52c9c-160">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="52c9c-160">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="52c9c-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52c9c-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52c9c-162">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="52c9c-162">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

