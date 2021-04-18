---
title: Proprietà di heartbeat IVMGuestOS (VPCCOMInterfaces. h)
description: Determina se la macchina virtuale ha un heartbeat.
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- Proprietà di heartbeat-PC virtuale
- Proprietà di heartbeat, Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà di heartbeat
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHeartbeating
- IVMGuestOS.get_IsHeartbeating
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faad446749cbf3cdb75d6e8fa7469022cc004ea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302562"
---
# <a name="ivmguestosisheartbeating-property"></a><span data-ttu-id="e61db-106">Proprietà IVMGuestOS:: heartbeat</span><span class="sxs-lookup"><span data-stu-id="e61db-106">IVMGuestOS::IsHeartbeating property</span></span>

<span data-ttu-id="e61db-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e61db-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e61db-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e61db-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e61db-109">Determina se la macchina virtuale ha un heartbeat.</span><span class="sxs-lookup"><span data-stu-id="e61db-109">Determines whether the virtual machine has a heartbeat.</span></span>

<span data-ttu-id="e61db-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e61db-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e61db-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e61db-111">Syntax</span></span>


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a><span data-ttu-id="e61db-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e61db-112">Property value</span></span>

<span data-ttu-id="e61db-113">**Variante \_ TRUE** se viene rilevato un heartbeat, **Variant \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e61db-113">**VARIANT\_TRUE** if a heartbeat is detected, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e61db-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e61db-114">Error codes</span></span>



| <span data-ttu-id="e61db-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="e61db-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="e61db-116">Significato</span><span class="sxs-lookup"><span data-stu-id="e61db-116">Meaning</span></span>                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e61db-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e61db-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="e61db-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="e61db-118">The operation was successful.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="e61db-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e61db-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="e61db-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="e61db-120">The parameter is **NULL**.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="e61db-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e61db-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="e61db-122">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="e61db-122">The configuration is unknown.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="e61db-123"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="e61db-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>      | <span data-ttu-id="e61db-124">Per questa operazione è necessario che la macchina virtuale sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e61db-124">The virtual machine must be running for this operation.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="e61db-125"><dt>Macchina virtuale \_ \_Aggiunte di E \_ non \_ disponibili</dt> <dt>0xA0040504</dt></span><span class="sxs-lookup"><span data-stu-id="e61db-125"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="e61db-126">La macchina virtuale non è stata avviata completamente, la funzionalità componenti di integrazione non è installata oppure la versione installata non supporta questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e61db-126">The virtual machine is not fully booted, the integration components feature is not installed, or the installed version does not support this feature.</span></span><br/> |
| <dl> <span data-ttu-id="e61db-127"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e61db-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="e61db-128">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="e61db-128">An unexpected error has occurred.</span></span><br/>                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="e61db-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="e61db-129">Remarks</span></span>

<span data-ttu-id="e61db-130">Quando si installano componenti di integrazione nel sistema operativo guest, viene inviato un normale "battito" o un heartbeat dalla sessione della macchina virtuale a Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="e61db-130">When integration components is installed in the guest operating system, a regular 'tick' or heartbeat is sent from the virtual machine session to Windows Virtual PC.</span></span> <span data-ttu-id="e61db-131">Se il sistema operativo guest è caricato in modo elevato, è possibile che Virtual PC riceva un minor numero di heartbeat del previsto.</span><span class="sxs-lookup"><span data-stu-id="e61db-131">If the guest operating system is heavily loaded, it's possible that Virtual PC will receive fewer heartbeats than expected.</span></span> <span data-ttu-id="e61db-132">Se non viene rilevato alcun heartbeat, è possibile che il sistema operativo guest non risponda o venga arrestato in modo anomalo.</span><span class="sxs-lookup"><span data-stu-id="e61db-132">If no heartbeat is detected, it is possible that the guest operating system is not responding or is crashed.</span></span>

<span data-ttu-id="e61db-133">Per impostazione predefinita, una macchina virtuale produce dieci cicli di heartbeat al minuto.</span><span class="sxs-lookup"><span data-stu-id="e61db-133">By default, a virtual machine produces ten heartbeat ticks per minute.</span></span> <span data-ttu-id="e61db-134">Se non viene rilevato alcun battito di heartbeat per un minuto intero, Windows Virtual PC tenterà di riavviare la sessione della macchina virtuale una volta ogni dieci secondi per un massimo di due minuti.</span><span class="sxs-lookup"><span data-stu-id="e61db-134">If no heartbeat ticks are detected for an entire minute, Windows Virtual PC will attempt to restart the virtual machine session once every ten seconds for up to two minutes.</span></span> <span data-ttu-id="e61db-135">Questo comportamento è controllato dai valori chiave seguenti nel file di configurazione della sessione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e61db-135">This behavior is controlled by the following key values in the virtual machine session's configuration file.</span></span>



| <span data-ttu-id="e61db-136">Chiave di configurazione</span><span class="sxs-lookup"><span data-stu-id="e61db-136">Configuration key</span></span>                                            | <span data-ttu-id="e61db-137">Predefinito</span><span class="sxs-lookup"><span data-stu-id="e61db-137">Default</span></span>       | <span data-ttu-id="e61db-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e61db-138">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e61db-139">integrazione/Microsoft/heartbeat/ora</span><span class="sxs-lookup"><span data-stu-id="e61db-139">integration/microsoft/heartbeat/time</span></span><br/>              | <span data-ttu-id="e61db-140">60</span><span class="sxs-lookup"><span data-stu-id="e61db-140">60</span></span><br/> | <span data-ttu-id="e61db-141">Lunghezza del blocco di tempo utilizzato per generare i cicli di heartbeat, in secondi.</span><span class="sxs-lookup"><span data-stu-id="e61db-141">The length of the block of time used to generate heartbeat ticks, in in seconds.</span></span><br/>                                             |
| <span data-ttu-id="e61db-142">integrazione/Microsoft/heartbeat/frequenza</span><span class="sxs-lookup"><span data-stu-id="e61db-142">integration/microsoft/heartbeat/rate</span></span><br/>              | <span data-ttu-id="e61db-143">10</span><span class="sxs-lookup"><span data-stu-id="e61db-143">10</span></span><br/> | <span data-ttu-id="e61db-144">Numero di cicli generati in ogni blocco di tempo heartbeat.</span><span class="sxs-lookup"><span data-stu-id="e61db-144">The number of ticks generated in each heartbeat time block.</span></span><br/>                                                                  |
| <span data-ttu-id="e61db-145">integrazione/Microsoft/heartbeat/intervallo di errori \_</span><span class="sxs-lookup"><span data-stu-id="e61db-145">integration/microsoft/heartbeat/failure\_interval</span></span><br/> | <span data-ttu-id="e61db-146">10</span><span class="sxs-lookup"><span data-stu-id="e61db-146">10</span></span><br/> | <span data-ttu-id="e61db-147">Il numero di secondi tra i tentativi di riavvio, quando non viene ricevuto alcun battito di heartbeat entro un blocco di tempo heartbeat specifico.</span><span class="sxs-lookup"><span data-stu-id="e61db-147">The number of seconds between restart attempts, once no heartbeat ticks are received within a specific heartbeat time block.</span></span><br/> |
| <span data-ttu-id="e61db-148">tentativi di integrazione/Microsoft/heartbeat/errore \_</span><span class="sxs-lookup"><span data-stu-id="e61db-148">integration/microsoft/heartbeat/failure\_attempts</span></span><br/> | <span data-ttu-id="e61db-149">12</span><span class="sxs-lookup"><span data-stu-id="e61db-149">12</span></span><br/> | <span data-ttu-id="e61db-150">Numero di tentativi di riavvio effettuati.</span><span class="sxs-lookup"><span data-stu-id="e61db-150">The number of restart attempts made.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="e61db-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e61db-151">Requirements</span></span>



| <span data-ttu-id="e61db-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="e61db-152">Requirement</span></span> | <span data-ttu-id="e61db-153">Valore</span><span class="sxs-lookup"><span data-stu-id="e61db-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e61db-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e61db-154">Minimum supported client</span></span><br/> | <span data-ttu-id="e61db-155">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e61db-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e61db-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e61db-156">Minimum supported server</span></span><br/> | <span data-ttu-id="e61db-157">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e61db-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e61db-158">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e61db-158">End of client support</span></span><br/>    | <span data-ttu-id="e61db-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e61db-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e61db-160">Prodotto</span><span class="sxs-lookup"><span data-stu-id="e61db-160">Product</span></span><br/>                  | <span data-ttu-id="e61db-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e61db-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e61db-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e61db-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="e61db-163"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e61db-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e61db-164">IID</span><span class="sxs-lookup"><span data-stu-id="e61db-164">IID</span></span><br/>                      | <span data-ttu-id="e61db-165">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="e61db-165">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="e61db-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e61db-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e61db-167">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="e61db-167">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

