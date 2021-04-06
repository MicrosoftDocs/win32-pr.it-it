---
title: Metodo Shutdown IVMGuestOS (VPCCOMInterfaces. h)
description: Arresta il sistema operativo guest nella macchina virtuale.
ms.assetid: a1453ad1-c4c2-47bb-a612-d203a6ee8c18
keywords:
- Metodo Shutdown Virtual PC
- Metodo Shutdown Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo Shutdown
topic_type:
- apiref
api_name:
- IVMGuestOS.Shutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63025270752af044a572cf9b6299e54b31b89ffe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742063"
---
# <a name="ivmguestosshutdown-method"></a><span data-ttu-id="86717-106">Metodo IVMGuestOS:: Shutdown</span><span class="sxs-lookup"><span data-stu-id="86717-106">IVMGuestOS::Shutdown method</span></span>

<span data-ttu-id="86717-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="86717-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="86717-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="86717-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="86717-109">Arresta il sistema operativo guest nella macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="86717-109">Shuts down the guest operating system in the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="86717-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86717-110">Syntax</span></span>


```C++
HRESULT Shutdown(
  [in]          VARIANT_BOOL isForced,
  [out, retval] IVMTask      **outShutdownTask
);
```



## <a name="parameters"></a><span data-ttu-id="86717-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="86717-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86717-112">*applicazione forzata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86717-112">*isForced* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86717-113">**Variante \_ TRUE** se l'arresto deve essere forzato, **Variant \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="86717-113">**VARIANT\_TRUE** if the shutdown is to be forced, **VARIANT\_FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="86717-114">*outShutdownTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="86717-114">*outShutdownTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="86717-115">Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia del completamento del processo di arresto.</span><span class="sxs-lookup"><span data-stu-id="86717-115">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the shutdown process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86717-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86717-116">Return value</span></span>

<span data-ttu-id="86717-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="86717-117">This method can return one of these values.</span></span>



| <span data-ttu-id="86717-118">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="86717-118">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="86717-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86717-119">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="86717-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="86717-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="86717-121">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="86717-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="86717-122"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="86717-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="86717-123">Il parametro *outShutdownTask* è **null**.</span><span class="sxs-lookup"><span data-stu-id="86717-123">The *outShutdownTask* parameter is **NULL**.</span></span><br/>                    |
| <dl> <span data-ttu-id="86717-124"><dt>**Macchina virtuale \_ E \_ timeout \_**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="86717-124"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="86717-125">L'operazione non è stata completata in modo tempestivo.</span><span class="sxs-lookup"><span data-stu-id="86717-125">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="86717-126"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="86717-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="86717-127">Non è stato possibile trovare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="86717-127">The VM could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="86717-128"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="86717-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="86717-129">Per questa operazione è necessario che la macchina virtuale sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="86717-129">The VM must be running for this operation.</span></span><br/>                      |
| <dl> <span data-ttu-id="86717-130"><dt>**HRESULT \_ DA \_ Win32 ( \_ accesso errore \_ negato)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="86717-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="86717-131">Il chiamante deve avere le autorizzazioni di accesso Execute per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="86717-131">The caller must have execute access permissions for this VM.</span></span><br/>    |
| <dl> <span data-ttu-id="86717-132"><dt>**Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="86717-132"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>       | <span data-ttu-id="86717-133">La funzionalità componenti di integrazione non è installata in questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="86717-133">The integration components feature is not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="86717-134"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="86717-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="86717-135">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="86717-135">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="86717-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="86717-136">Remarks</span></span>

<span data-ttu-id="86717-137">Quando viene richiamato questo metodo, è necessario che la macchina virtuale sia in esecuzione e che sia installata la funzionalità componenti di integrazione.</span><span class="sxs-lookup"><span data-stu-id="86717-137">The VM must be running and integration components feature must be installed when this method is invoked.</span></span> <span data-ttu-id="86717-138">Questo metodo è supportato solo per i sistemi operativi guest basati su Windows.</span><span class="sxs-lookup"><span data-stu-id="86717-138">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="86717-139">I valori seguenti possono essere restituiti tramite la proprietà [**Error**](ivmtask-error.md) dell'oggetto [**IVMTask**](ivmtask.md) restituito.</span><span class="sxs-lookup"><span data-stu-id="86717-139">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="86717-140">Codice [**errore**](ivmtask-error.md) /valore</span><span class="sxs-lookup"><span data-stu-id="86717-140">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="86717-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86717-141">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="86717-142"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` 0x80070005</span><span class="sxs-lookup"><span data-stu-id="86717-142"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)</span></span><br/>                             | <span data-ttu-id="86717-143">Il chiamante deve avere le autorizzazioni di accesso Execute per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="86717-143">The caller must have execute access permissions for this VM.</span></span><br/>             |
| <span data-ttu-id="86717-144"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span><span class="sxs-lookup"><span data-stu-id="86717-144"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span></span><br/>                         | <span data-ttu-id="86717-145">Il computer è bloccato e non può essere arrestato senza l'opzione Force.</span><span class="sxs-lookup"><span data-stu-id="86717-145">The computer is locked and cannot be shut down without the force option.</span></span><br/> |
| <span data-ttu-id="86717-146"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span><span class="sxs-lookup"><span data-stu-id="86717-146"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span></span><br/>                                             | <span data-ttu-id="86717-147">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="86717-147">The device is not ready.</span></span><br/>                                                 |
| <span data-ttu-id="86717-148"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span><span class="sxs-lookup"><span data-stu-id="86717-148"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span></span><br/> | <span data-ttu-id="86717-149">È in corso l'arresto del sistema.</span><span class="sxs-lookup"><span data-stu-id="86717-149">A system shutdown is in progress.</span></span><br/>                                        |



 

## <a name="requirements"></a><span data-ttu-id="86717-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86717-150">Requirements</span></span>



| <span data-ttu-id="86717-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="86717-151">Requirement</span></span> | <span data-ttu-id="86717-152">Valore</span><span class="sxs-lookup"><span data-stu-id="86717-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="86717-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86717-153">Minimum supported client</span></span><br/> | <span data-ttu-id="86717-154">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="86717-154">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="86717-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86717-155">Minimum supported server</span></span><br/> | <span data-ttu-id="86717-156">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="86717-156">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="86717-157">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="86717-157">End of client support</span></span><br/>    | <span data-ttu-id="86717-158">Windows 7</span><span class="sxs-lookup"><span data-stu-id="86717-158">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="86717-159">Prodotto</span><span class="sxs-lookup"><span data-stu-id="86717-159">Product</span></span><br/>                  | <span data-ttu-id="86717-160">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="86717-160">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="86717-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86717-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="86717-162"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="86717-162"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="86717-163">IID</span><span class="sxs-lookup"><span data-stu-id="86717-163">IID</span></span><br/>                      | <span data-ttu-id="86717-164">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="86717-164">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="86717-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86717-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86717-166">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="86717-166">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

