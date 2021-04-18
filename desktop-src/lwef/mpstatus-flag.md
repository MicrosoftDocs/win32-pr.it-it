---
title: Enumerazione MPSTATUS_FLAG (MpClient. h)
description: Possibili flag di bit di stato generale del prodotto.
ms.assetid: BF2E6506-E76A-4785-8E91-99937B413548
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPSTATUS_FLAG
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPSTATUS_FLAG
topic_type:
- apiref
api_name:
- MPSTATUS_FLAG
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c7175980c09c63938be04626091c31b53335756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301539"
---
# <a name="mpstatus_flag-enumeration"></a><span data-ttu-id="6e7ae-105">\_Enumerazione flag MPSTATUS</span><span class="sxs-lookup"><span data-stu-id="6e7ae-105">MPSTATUS\_FLAG enumeration</span></span>

<span data-ttu-id="6e7ae-106">Possibili flag di bit di stato generale del prodotto.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-106">Possible overall product status bit flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e7ae-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e7ae-107">Syntax</span></span>


```C++
typedef enum tagMPSTATUS_FLAG { 
  MP_STATUS_FLAG_NONE                           = 0,
  MP_STATUS_FLAG_SERVICE_UNAVAILABLE            = 1 << 0,
  MP_STATUS_FLAG_MPENGINE_UNAVAILABLE           = 1 << 1,
  MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED       = 1 << 2,
  MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED         = 1 << 3,
  MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED   = 1 << 4,
  MP_STATUS_FLAG_DUE_AV_SIGNATURE               = 1 << 5,
  MP_STATUS_FLAG_DUE_AS_SIGNATURE               = 1 << 6,
  MP_STATUS_FLAG_DUE_QUICK_SCAN                 = 1 << 7,
  MP_STATUS_FLAG_DUE_FULL_SCAN                  = 1 << 8,
  MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN         = 1 << 9,
  MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING    = 1 << 10,
  MP_STATUS_FLAG_DUE_SAMPLES                    = 1 << 11,
  MP_STATUS_FLAG_EVALUATION_MODE                = 1 << 12,
  MP_STATUS_FLAG_NONGENUINE                     = 1 << 13,
  MP_STATUS_FLAG_PRODUCT_EXPIRED                = 1 << 14,
  MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED       = 1 << 15,
  MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN     = 1 << 16,
  MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE       = 1 << 17,
  MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE   = 1 << 18,
  MP_STATUS_FLAG_HEALTH_INITIALIZED             = 1 << 19,
  MP_STATUS_FLAG_DUE_PLATFORM_UPDATE            = 1 << 20,
  MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE     = 1 << 21,
  MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED  = 1 << 22,
  MP_STATUS_FLAG_END_OF_LIFE                    = 1 << 23,
  MP_STATUS_FLAG_MAX                            = 1 << 23,
  MP_STATUS_FLAG_ALL                            = (1 << 24)-1
} MPSTATUS_FLAG, *PMPSTATUS_FLAG;
```



## <a name="constants"></a><span data-ttu-id="6e7ae-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="6e7ae-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6e7ae-109"><span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**\_flag di stato MP \_ \_ None**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-109"><span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**MP\_STATUS\_FLAG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-110">Nessun flag di stato impostato (stato non inizializzato).</span><span class="sxs-lookup"><span data-stu-id="6e7ae-110">No status flags set (non-initialized state).</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-111"><span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**\_servizio flag di stato MP non \_ \_ \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-111"><span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**MP\_STATUS\_FLAG\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-112">Il servizio non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-112">Service not running.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-113"><span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**\_flag di stato MP MPENGINE non \_ \_ \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-113"><span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**MP\_STATUS\_FLAG\_MPENGINE\_UNAVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-114">Il servizio è stato avviato senza alcun motore di protezione da malware.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-114">Service started without any malware protection engine.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-115"><span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**il \_ flag di stato MP \_ \_ Threat \_ FullScan è \_ obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-115"><span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**MP\_STATUS\_FLAG\_THREAT\_FULLSCAN\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-116">Analisi completa in sospeso a causa di un'azione di minaccia.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-116">Pending full scan due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-117"><span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**è \_ \_ \_ \_ necessario riavviare il flag di stato MP \_**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-117"><span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**MP\_STATUS\_FLAG\_THREAT\_REBOOT\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-118">Riavvio in sospeso a causa di un'azione di minaccia.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-118">Pending reboot due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-119"><span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**sono \_ \_ \_ \_ \_ necessari passaggi manuali \_ per la minaccia del flag di stato MP**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-119"><span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**MP\_STATUS\_FLAG\_THREAT\_MANUAL\_STEPS\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-120">Passaggi manuali in sospeso a causa di un'azione di minaccia.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-120">Pending manual steps due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-121"><span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**\_flag di stato MP \_ \_ a causa della \_ \_ firma AV**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-121"><span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**MP\_STATUS\_FLAG\_DUE\_AV\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-122">Le firme antivirus non sono aggiornate.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-122">Antivirus signatures out of date.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-123"><span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**\_ \_ flag di stato MP \_ a causa della \_ \_ firma**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-123"><span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**MP\_STATUS\_FLAG\_DUE\_AS\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-124">Firme antispyware obsolete.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-124">Antispyware signatures out of date.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-125"><span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**\_flag di stato MP \_ \_ scadenza \_ \_ analisi veloce**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-125"><span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**MP\_STATUS\_FLAG\_DUE\_QUICK\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-126">Non è stata eseguita alcuna analisi veloce per un periodo specificato.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-126">No quick scan has happened for a specified period.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-127"><span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**\_flag di stato MP \_ \_ a causa dell' \_ \_ analisi completa**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-127"><span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**MP\_STATUS\_FLAG\_DUE\_FULL\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-128">non è stata eseguita un'analisi completa per un periodo specificato</span><span class="sxs-lookup"><span data-stu-id="6e7ae-128">no full scan has happened for a specified period</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-129"><span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**analisi di sistema del flag di stato MP in \_ \_ \_ corso \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-129"><span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_SYSTEM\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-130">Analisi avviata dal sistema in corso.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-130">System-initiated scan in progress.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-131"><span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**\_ \_ \_ pulizia routine in corso del flag di \_ stato MP \_**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-131"><span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_ROUTINE\_CLEANING**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-132">Pulizia avviata dal sistema in corso.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-132">System-initiated clean in progress.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-133"><span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**\_esempi di flag di stato MP \_ \_ dovuti \_**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-133"><span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**MP\_STATUS\_FLAG\_DUE\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-134">Sono presenti campioni in attesa di invio.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-134">There are samples pending submission.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-135"><span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**\_modalità di \_ valutazione del flag di stato MP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-135"><span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**MP\_STATUS\_FLAG\_EVALUATION\_MODE**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-136">Il prodotto è in esecuzione in modalità di valutazione.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-136">Product is running in evaluation mode.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-137"><span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**FLAG di stato MP non \_ \_ \_ autentico**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-137"><span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**MP\_STATUS\_FLAG\_NONGENUINE**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-138">Il prodotto è in esecuzione in modalità Windows non originale.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-138">Product is running in non-genuine Windows mode.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-139"><span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**il \_ prodotto del flag di stato MP è \_ \_ \_ scaduto**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-139"><span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**MP\_STATUS\_FLAG\_PRODUCT\_EXPIRED**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-140">Prodotto scaduto.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-140">Product expired.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-141"><span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**il \_ flag di stato del MP \_ \_ minaccia \_ Callisto \_**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-141"><span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**MP\_STATUS\_FLAG\_THREAT\_CALLISTO\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-142">È richiesta l'analisi non in linea di Callisto.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-142">Callisto off-line scan required.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-143"><span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**\_ \_ servizio flag di stato MP \_ \_ all' \_ arresto del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-143"><span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**MP\_STATUS\_FLAG\_SERVICE\_ON\_SYSTEM\_SHUTDOWN**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-144">Il servizio verrà arrestato nell'ambito dell'arresto del sistema.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-144">Service is shutting down as part of system shutdown.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-145"><span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**\_ \_ \_ \_ errore critico servizio flag di stato MP \_**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-145"><span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**MP\_STATUS\_FLAG\_SERVICE\_CRITICAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-146">La correzione delle minacce non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-146">Threat remediation failed critically.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-147"><span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**\_ \_ \_ \_ \_ errore non critico del servizio flag di stato \_ MP**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-147"><span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**MP\_STATUS\_FLAG\_SERVICE\_NON\_CRITICAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-148">La correzione delle minacce non è riuscita in modo non critico.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-148">Threat remediation failed non-critically.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-149"><span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**\_stato del flag di stato MP \_ \_ \_ inizializzato**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-149"><span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**MP\_STATUS\_FLAG\_HEALTH\_INITIALIZED**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-150">Nessun flag di stato impostato (stato ben inizializzato).</span><span class="sxs-lookup"><span data-stu-id="6e7ae-150">No status flags set (well-initialized state).</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-151"><span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**\_flag di stato MP \_ \_ a causa dell' \_ aggiornamento della piattaforma \_**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-151"><span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**MP\_STATUS\_FLAG\_DUE\_PLATFORM\_UPDATE**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-152">La piattaforma non è aggiornata.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-152">The platform is out of date.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-153"><span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**\_aggiornamento della \_ \_ piattaforma di inesecuzione del flag di \_ stato MP \_**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-153"><span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_PLATFORM\_UPDATE**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-154">Aggiornamento della piattaforma in corso.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-154">Platform update is in progress.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-155"><span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**\_ \_ \_ piattaforma del flag di stato MP \_ \_ che sta per \_ essere \_ obsoleta**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-155"><span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**MP\_STATUS\_FLAG\_PLATFORM\_ABOUT\_TO\_BE\_OUTDATED**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-156">La piattaforma sta per essere obsoleta</span><span class="sxs-lookup"><span data-stu-id="6e7ae-156">The platform is about to be outdated</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-157"><span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**\_ \_ \_ fine \_ della durata del flag di stato MP \_**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-157"><span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**MP\_STATUS\_FLAG\_END\_OF\_LIFE**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-158">La fine del ciclo di vita della firma o della piattaforma è passata o è in sospeso.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-158">The signature or platform end of life is past or is pending.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-159"><span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**\_flag di \_ stato \_ massimo MP**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-159"><span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**MP\_STATUS\_FLAG\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-160">Flag massimo valido.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-160">Maximum valid flag.</span></span>

</dd> <dt>

<span data-ttu-id="6e7ae-161"><span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**\_flag di stato MP \_ \_ All**</span><span class="sxs-lookup"><span data-stu-id="6e7ae-161"><span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**MP\_STATUS\_FLAG\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="6e7ae-162">Valore massimo possibile.</span><span class="sxs-lookup"><span data-stu-id="6e7ae-162">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6e7ae-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e7ae-163">Requirements</span></span>



| <span data-ttu-id="6e7ae-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e7ae-164">Requirement</span></span> | <span data-ttu-id="6e7ae-165">Valore</span><span class="sxs-lookup"><span data-stu-id="6e7ae-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e7ae-166">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e7ae-166">Minimum supported client</span></span><br/> | <span data-ttu-id="6e7ae-167">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6e7ae-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6e7ae-168">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e7ae-168">Minimum supported server</span></span><br/> | <span data-ttu-id="6e7ae-169">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6e7ae-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6e7ae-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e7ae-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e7ae-171"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e7ae-171"><dt>MpClient.h</dt></span></span> </dl> |



 

 





