---
title: Proprietà IVMGuestOS HeartbeatPercentage (VPCCOMInterfaces. h)
description: Percentuale di heartbeat previsti ricevuti nel minuto precedente.
ms.assetid: 456dd8ae-e946-429d-98aa-5773362fdd4e
keywords:
- Proprietà HeartbeatPercentage Virtual PC
- Proprietà HeartbeatPercentage Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà HeartbeatPercentage
topic_type:
- apiref
api_name:
- IVMGuestOS.HeartbeatPercentage
- IVMGuestOS.get_HeartbeatPercentage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22d568ed85281e8940b69afd1c72e76e2f208a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518801"
---
# <a name="ivmguestosheartbeatpercentage-property"></a><span data-ttu-id="68a3d-106">Proprietà IVMGuestOS:: HeartbeatPercentage</span><span class="sxs-lookup"><span data-stu-id="68a3d-106">IVMGuestOS::HeartbeatPercentage property</span></span>

<span data-ttu-id="68a3d-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="68a3d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="68a3d-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="68a3d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="68a3d-109">Recupera la percentuale di heartbeat previsti ricevuti nel minuto precedente.</span><span class="sxs-lookup"><span data-stu-id="68a3d-109">Retrieves the percentage of expected heartbeats received over the past minute.</span></span>

<span data-ttu-id="68a3d-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="68a3d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="68a3d-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68a3d-111">Syntax</span></span>


```C++
HRESULT get_HeartbeatPercentage(
  [out, retval] long *heartbeatPercentage
);
```



## <a name="property-value"></a><span data-ttu-id="68a3d-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="68a3d-112">Property value</span></span>

<span data-ttu-id="68a3d-113">Percentuale di heartbeat previsti ricevuti nel minuto precedente.</span><span class="sxs-lookup"><span data-stu-id="68a3d-113">The percentage of expected heartbeats received over the past minute.</span></span>

## <a name="error-codes"></a><span data-ttu-id="68a3d-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="68a3d-114">Error codes</span></span>



| <span data-ttu-id="68a3d-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="68a3d-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="68a3d-116">Significato</span><span class="sxs-lookup"><span data-stu-id="68a3d-116">Meaning</span></span>                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68a3d-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="68a3d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="68a3d-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="68a3d-118">The operation was successful.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="68a3d-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="68a3d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="68a3d-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="68a3d-120">The parameter is **NULL**.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="68a3d-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="68a3d-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="68a3d-122">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="68a3d-122">The configuration is unknown.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="68a3d-123"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="68a3d-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>      | <span data-ttu-id="68a3d-124">Per questa operazione è necessario che la macchina virtuale (VM) sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="68a3d-124">The virtual machine (VM) must be running for this operation.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="68a3d-125"><dt>Macchina virtuale \_ \_Aggiunte di E \_ non \_ disponibili</dt> <dt>0xA0040504</dt></span><span class="sxs-lookup"><span data-stu-id="68a3d-125"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="68a3d-126">La macchina virtuale non è stata avviata completamente, la funzionalità componenti di integrazione non è installata oppure la versione installata non supporta questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="68a3d-126">The VM is not fully booted, the integration components feature is not installed, or the installed version does not support this feature.</span></span><br/> |
| <dl> <span data-ttu-id="68a3d-127"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="68a3d-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="68a3d-128">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="68a3d-128">An unexpected error has occurred.</span></span><br/>                                                                                                        |



## <a name="remarks"></a><span data-ttu-id="68a3d-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="68a3d-129">Remarks</span></span>

<span data-ttu-id="68a3d-130">I componenti di integrazione invieranno un heartbeat periodico a Windows Virtual PC mentre è in esecuzione il sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="68a3d-130">Integration components will send a periodic heartbeat to Windows Virtual PC while the guest operating system is running.</span></span> <span data-ttu-id="68a3d-131">Se il sistema operativo guest è caricato in modo elevato, è possibile che Windows Virtual PC riceva un minor numero di heartbeat del previsto.</span><span class="sxs-lookup"><span data-stu-id="68a3d-131">If the guest operating system is heavily loaded, it's possible that Windows Virtual PC will receive fewer heartbeats than expected.</span></span> <span data-ttu-id="68a3d-132">Se la percentuale di heartbeat scende a zero, è possibile che il sistema operativo guest non risponda o venga arrestato in modo anomalo.</span><span class="sxs-lookup"><span data-stu-id="68a3d-132">If the heartbeat percentage drops to zero, it is possible that the guest operating system is not responding or is crashed.</span></span> <span data-ttu-id="68a3d-133">La macchina virtuale deve essere in esecuzione (ovvero completamente avviata e non arrestata) e i componenti di integrazione devono essere installati quando questa proprietà viene richiamata.</span><span class="sxs-lookup"><span data-stu-id="68a3d-133">The virtual machine must be running (that is, fully booted and not shutting down) and integration components must be installed when this property is invoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="68a3d-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68a3d-134">Requirements</span></span>



| <span data-ttu-id="68a3d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="68a3d-135">Requirement</span></span> | <span data-ttu-id="68a3d-136">Valore</span><span class="sxs-lookup"><span data-stu-id="68a3d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="68a3d-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68a3d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="68a3d-138">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="68a3d-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="68a3d-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68a3d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="68a3d-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="68a3d-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="68a3d-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="68a3d-141">End of client support</span></span><br/>    | <span data-ttu-id="68a3d-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="68a3d-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="68a3d-143">Prodotto</span><span class="sxs-lookup"><span data-stu-id="68a3d-143">Product</span></span><br/>                  | <span data-ttu-id="68a3d-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="68a3d-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="68a3d-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68a3d-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="68a3d-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="68a3d-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="68a3d-147">IID</span><span class="sxs-lookup"><span data-stu-id="68a3d-147">IID</span></span><br/>                      | <span data-ttu-id="68a3d-148">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="68a3d-148">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="68a3d-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68a3d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68a3d-150">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="68a3d-150">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

