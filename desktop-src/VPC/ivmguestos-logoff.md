---
title: Metodo di disconnessione IVMGuestOS (VPCCOMInterfaces. h)
description: Disconnette tutti gli utenti dal sistema operativo guest.
ms.assetid: 224aa7cb-0892-4e8a-84bd-78dd5cb724df
keywords:
- Metodo di disconnessione Virtual PC
- Metodo di disconnessione Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, metodo di disconnessione
topic_type:
- apiref
api_name:
- IVMGuestOS.Logoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c67e917cc9ff93d162bc340185f426fe9eee3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048723"
---
# <a name="ivmguestoslogoff-method"></a><span data-ttu-id="14b61-106">Metodo IVMGuestOS:: disconnessione</span><span class="sxs-lookup"><span data-stu-id="14b61-106">IVMGuestOS::Logoff method</span></span>

<span data-ttu-id="14b61-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="14b61-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="14b61-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="14b61-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="14b61-109">Disconnette tutti gli utenti dal sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="14b61-109">Logs off all users from the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="14b61-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14b61-110">Syntax</span></span>


```C++
HRESULT Logoff(
  [out, retval] IVMTask **outLogoffTask
);
```



## <a name="parameters"></a><span data-ttu-id="14b61-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="14b61-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14b61-112">*outLogoffTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="14b61-112">*outLogoffTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="14b61-113">Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia dello stato di completamento della sequenza di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="14b61-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the logoff sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14b61-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14b61-114">Return value</span></span>

<span data-ttu-id="14b61-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="14b61-115">This method can return one of these values.</span></span>



| <span data-ttu-id="14b61-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="14b61-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="14b61-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14b61-117">Description</span></span>                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14b61-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="14b61-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="14b61-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="14b61-119">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="14b61-120"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="14b61-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="14b61-121">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="14b61-121">An unexpected error has occurred.</span></span><br/>                                            |
| <dl> <span data-ttu-id="14b61-122"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="14b61-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="14b61-123">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="14b61-123">The parameter is **NULL**.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="14b61-124"><dt>**HRESULT \_ DA \_ Win32 ( \_ accesso errore \_ negato)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="14b61-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="14b61-125">Il chiamante deve avere le autorizzazioni di accesso Execute per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="14b61-125">The caller must have execute access permissions for this VM.</span></span><br/>                 |
| <dl> <span data-ttu-id="14b61-126"><dt>**Macchina virtuale \_ E \_ timeout \_**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="14b61-126"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="14b61-127">L'operazione non è stata completata in modo tempestivo.</span><span class="sxs-lookup"><span data-stu-id="14b61-127">The operation did not complete in a timely manner.</span></span><br/>                           |
| <dl> <span data-ttu-id="14b61-128"><dt>**Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="14b61-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>       | <span data-ttu-id="14b61-129">La funzionalità componenti di integrazione non è installata in questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="14b61-129">The integration components feature is not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="14b61-130"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="14b61-130"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="14b61-131">Per questa operazione è necessario che la macchina virtuale (VM) sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="14b61-131">The virtual machine (VM) must be running for this operation.</span></span><br/>                 |
| <dl> <span data-ttu-id="14b61-132"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="14b61-132"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="14b61-133">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="14b61-133">The configuration is unknown.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="14b61-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="14b61-134">Remarks</span></span>

<span data-ttu-id="14b61-135">`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) viene restituito tramite la proprietà [**Error**](ivmtask-error.md) dell'oggetto [**IVMTask**](ivmtask.md) restituito non sono presenti sessioni di accesso nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="14b61-135">`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) is returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object there are no logon sessions in the guest operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="14b61-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14b61-136">Requirements</span></span>



| <span data-ttu-id="14b61-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="14b61-137">Requirement</span></span> | <span data-ttu-id="14b61-138">Valore</span><span class="sxs-lookup"><span data-stu-id="14b61-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="14b61-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14b61-139">Minimum supported client</span></span><br/> | <span data-ttu-id="14b61-140">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="14b61-140">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="14b61-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14b61-141">Minimum supported server</span></span><br/> | <span data-ttu-id="14b61-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="14b61-142">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="14b61-143">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="14b61-143">End of client support</span></span><br/>    | <span data-ttu-id="14b61-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="14b61-144">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="14b61-145">Prodotto</span><span class="sxs-lookup"><span data-stu-id="14b61-145">Product</span></span><br/>                  | <span data-ttu-id="14b61-146">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="14b61-146">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="14b61-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14b61-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="14b61-148"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="14b61-148"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="14b61-149">IID</span><span class="sxs-lookup"><span data-stu-id="14b61-149">IID</span></span><br/>                      | <span data-ttu-id="14b61-150">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="14b61-150">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="14b61-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14b61-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14b61-152">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="14b61-152">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

