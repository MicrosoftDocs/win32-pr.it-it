---
title: Enumerazione MPNOTIFY (MpClient. h)
description: Possibili notifiche di callback.
ms.assetid: CCD0CD89-2C6E-453F-9437-E6ED87AD9F29
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPNOTIFY
- Funzionalità dell'ambiente Windows legacy del puntatore di enumerazione PMPNOTIFY
topic_type:
- apiref
api_name:
- MPNOTIFY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afa0eeb6cb1d610f28cc82f578617f7bd71cf886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301946"
---
# <a name="mpnotify-enumeration"></a><span data-ttu-id="848f5-105">Enumerazione MPNOTIFY</span><span class="sxs-lookup"><span data-stu-id="848f5-105">MPNOTIFY enumeration</span></span>

<span data-ttu-id="848f5-106">Possibili notifiche di callback.</span><span class="sxs-lookup"><span data-stu-id="848f5-106">Possible callback notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="848f5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="848f5-107">Syntax</span></span>


```C++
typedef enum tagMPNOTIFY { 
  MPNOTIFY_NONE,
  MPNOTIFY_CALL_START,
  MPNOTIFY_CALL_COMPLETE,
  MPNOTIFY_INTERNAL_FAILURE,
  MPNOTIFY_STATUS_SERVICE_START,
  MPNOTIFY_STATUS_SERVICE_RUNNING,
  MPNOTIFY_STATUS_SERVICE_STOP,
  MPNOTIFY_STATUS_COMPONENT,
  MPNOTIFY_STATUS_CHANGE,
  MPNOTIFY_STATUS_COMPONENT_CONFIGURATION,
  MPNOTIFY_STATUS_EXPIRATION_CHANGE,
  MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE,
  MPNOTIFY_SCAN_START,
  MPNOTIFY_SCAN_PAUSED,
  MPNOTIFY_SCAN_RESUMED,
  MPNOTIFY_SCAN_CANCEL,
  MPNOTIFY_SCAN_COMPLETE,
  MPNOTIFY_SCAN_PROGRESS,
  MPNOTIFY_SCAN_ERROR,
  MPNOTIFY_SCAN_INFECTED,
  MPNOTIFY_SCAN_MEMORYSTART,
  MPNOTIFY_SCAN_MEMORYCOMPLETE,
  MPNOTIFY_SCAN_SFC_BUILD_START,
  MPNOTIFY_SCAN_SFC_BUILD_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_START,
  MPNOTIFY_SCAN_FASTPATH_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_PROGRESS,
  MPNOTIFY_CLEAN_START,
  MPNOTIFY_CLEAN_COMPLETE,
  MPNOTIFY_CLEAN_RESTOREPOINT_START,
  MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED,
  MPNOTIFY_CLEAN_RESTOREPOINT_FAILED,
  MPNOTIFY_CLEAN_THREAT_START,
  MPNOTIFY_CLEAN_THREAT_SUCCEEDED,
  MPNOTIFY_CLEAN_THREAT_FAILED,
  MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED,
  MPNOTIFY_CLEAN_RESOURCE_FAILED,
  MPNOTIFY_CLEAN_THREAT_COMPLETE,
  MPNOTIFY_PRECHECK_START,
  MPNOTIFY_PRECHECK_COMPLETE,
  MPNOTIFY_PRECHECK_RESOURCE_BLOCKED,
  MPNOTIFY_THREAT_DETECTED,
  MPNOTIFY_THREAT_MODIFIED,
  MPNOTIFY_THREAT_CLEAN_SUCCEEDED,
  MPNOTIFY_THREAT_CLEAN_FAILED,
  MPNOTIFY_THREAT_ABANDONED,
  MPNOTIFY_THREAT_CLEAN_EVENT_START,
  MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE,
  MPNOTIFY_SIGUPDATE_START,
  MPNOTIFY_SIGUPDATE_SEARCH_START,
  MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE,
  MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_START,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE,
  MPNOTIFY_SIGUPDATE_INSTALL_START,
  MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS,
  MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE,
  MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED,
  MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED,
  MPNOTIFY_SIGUPDATE_COMPLETE,
  MPNOTIFY_SAMPLE_START,
  MPNOTIFY_SAMPLE_COMPLETE,
  MPNOTIFY_SAMPLE_ITEM_START,
  MPNOTIFY_SAMPLE_ITEM_SUCCEEDED,
  MPNOTIFY_SAMPLE_ITEM_FAILED,
  MPNOTIFY_RESERVED_DATA,
  MPNOTIFY_FASTPATH_SIG_ADDED,
  MPNOTIFY_FASTPATH_SIG_REMOVED,
  MPNOTIFY_NIS_PRIVATE,
  MPNOTIFY_HEALTH_CHANGE,
  MPNOTIFY_HEALTH_RECOVERY,
  MPNOTIFY_HEALTH_START,
  MPNOTIFY_ENDOFLIFE_CHANGE,
  MPNOTIFY_MALWARETOAST_DATA
} MPNOTIFY, *PMPNOTIFY;
```



## <a name="constants"></a><span data-ttu-id="848f5-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="848f5-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="848f5-109"><span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY \_ None**</span><span class="sxs-lookup"><span data-stu-id="848f5-109"><span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY\_NONE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="848f5-110"><span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**\_inizio chiamata \_ MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="848f5-110"><span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**MPNOTIFY\_CALL\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-111">Avvio della chiamata di notifica.</span><span class="sxs-lookup"><span data-stu-id="848f5-111">Notification call start.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-112"><span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**\_chiamata MPNOTIFY \_ completata**</span><span class="sxs-lookup"><span data-stu-id="848f5-112"><span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**MPNOTIFY\_CALL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-113">Chiamata di notifica completata.</span><span class="sxs-lookup"><span data-stu-id="848f5-113">Notification call completed.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-114"><span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**\_errore interno \_ MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="848f5-114"><span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**MPNOTIFY\_INTERNAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-115">Errore interno generico.</span><span class="sxs-lookup"><span data-stu-id="848f5-115">Generic internal failure.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-116"><span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**\_ \_ avvio servizio stato \_ MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="848f5-116"><span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**MPNOTIFY\_STATUS\_SERVICE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-117">Il servizio malware Protection è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="848f5-117">Malware protection service has started.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-118"><span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**\_servizio stato \_ MPNOTIFY \_ in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="848f5-118"><span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**MPNOTIFY\_STATUS\_SERVICE\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-119">Il servizio malware Protection è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="848f5-119">Malware protection service is running.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-120"><span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**\_ \_ arresto servizio stato \_ MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="848f5-120"><span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**MPNOTIFY\_STATUS\_SERVICE\_STOP**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-121">Il servizio malware Protection è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="848f5-121">Malware protection service has stopped.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-122"><span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**\_componente stato \_ MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="848f5-122"><span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**MPNOTIFY\_STATUS\_COMPONENT**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-123">Stato di abilitazione/disabilitazione del componente specifico.</span><span class="sxs-lookup"><span data-stu-id="848f5-123">Particular component enable/disable status.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-124"><span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**\_modifica stato \_ MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="848f5-124"><span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**MPNOTIFY\_STATUS\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-125">Lo stato generale del prodotto è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="848f5-125">Overall product status has changed.</span></span> <span data-ttu-id="848f5-126">Chiamare [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) per ottenere lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="848f5-126">Call [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) to obtain the current status.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-127"><span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**\_configurazione del \_ componente \_ stato MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="848f5-127"><span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**MPNOTIFY\_STATUS\_COMPONENT\_CONFIGURATION**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-128">Un particolare componente ha modificato la configurazione.</span><span class="sxs-lookup"><span data-stu-id="848f5-128">A particular component has changed configuration.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-129"><span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**\_ \_ modifica scadenza stato \_ MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="848f5-129"><span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**MPNOTIFY\_STATUS\_EXPIRATION\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-130">Lo stato di scadenza del prodotto è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="848f5-130">Product expiration status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-131"><span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**\_ \_ \_ modifica analisi offline stato \_ MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="848f5-131"><span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**MPNOTIFY\_STATUS\_OFFLINE\_SCAN\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-132">Stato di analisi non in linea obbligatorio modificato.</span><span class="sxs-lookup"><span data-stu-id="848f5-132">Offline scan required state changed.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-133"><span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**\_avvio dell'analisi MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="848f5-133"><span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**MPNOTIFY\_SCAN\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-134">Analisi avviata.</span><span class="sxs-lookup"><span data-stu-id="848f5-134">Scan started.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-135"><span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**\_analisi MPNOTIFY \_ sospesa**</span><span class="sxs-lookup"><span data-stu-id="848f5-135"><span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**MPNOTIFY\_SCAN\_PAUSED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-136">Analisi sospesa.</span><span class="sxs-lookup"><span data-stu-id="848f5-136">Scan paused.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-137"><span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**\_analisi MPNOTIFY \_ ripresa**</span><span class="sxs-lookup"><span data-stu-id="848f5-137"><span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**MPNOTIFY\_SCAN\_RESUMED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-138">analisi ripresa.</span><span class="sxs-lookup"><span data-stu-id="848f5-138">scan resumed.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-139"><span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**\_annullamento dell'analisi MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="848f5-139"><span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**MPNOTIFY\_SCAN\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-140">Analisi annullata.</span><span class="sxs-lookup"><span data-stu-id="848f5-140">Scan cancelled.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-141"><span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**\_analisi MPNOTIFY \_ completata**</span><span class="sxs-lookup"><span data-stu-id="848f5-141"><span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**MPNOTIFY\_SCAN\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-142">Analisi completata.</span><span class="sxs-lookup"><span data-stu-id="848f5-142">Scan completed.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-143"><span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**\_stato analisi \_ MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="848f5-143"><span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**MPNOTIFY\_SCAN\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-144">Notifica di stato per la risorsa specifica sottoposta a scansione.</span><span class="sxs-lookup"><span data-stu-id="848f5-144">Progress notification for the specific resource being scanned.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-145"><span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**\_errore di analisi MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="848f5-145"><span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**MPNOTIFY\_SCAN\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-146">Errore durante l'analisi di una determinata risorsa.</span><span class="sxs-lookup"><span data-stu-id="848f5-146">Failure to scan a particular resource.</span></span> <span data-ttu-id="848f5-147">L'analisi continuerà comunque.</span><span class="sxs-lookup"><span data-stu-id="848f5-147">Scan will still continue.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-148"><span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**\_analisi MPNOTIFY \_ infettata**</span><span class="sxs-lookup"><span data-stu-id="848f5-148"><span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**MPNOTIFY\_SCAN\_INFECTED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-149">L'analisi ha rilevato una risorsa infetta.</span><span class="sxs-lookup"><span data-stu-id="848f5-149">Scan found an infected resource.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-150"><span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY \_ Scan \_ MEMORYSTART**</span><span class="sxs-lookup"><span data-stu-id="848f5-150"><span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY\_SCAN\_MEMORYSTART**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-151">L'analisi dello stato di avanzamento per notificare la parte dell'analisi di sistema è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="848f5-151">Scan progress to notify memory scan portion of the system scan has started.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-152"><span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY \_ Scan \_ MEMORYCOMPLETE**</span><span class="sxs-lookup"><span data-stu-id="848f5-152"><span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY\_SCAN\_MEMORYCOMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-153">Analisi dello stato di avanzamento per notificare la porzione di analisi della memoria del sistema completata.</span><span class="sxs-lookup"><span data-stu-id="848f5-153">Scan progress to notify memory scan portion of the system scan has completed.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-154"><span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**\_ \_ \_ avvio compilazione SFC MPNOTIFY \_ Scan**</span><span class="sxs-lookup"><span data-stu-id="848f5-154"><span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**MPNOTIFY\_SCAN\_SFC\_BUILD\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-155">Lo stato di avanzamento dell'analisi per notificare la compilazione SFC è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="848f5-155">Scan progress to notify sfc build portion has started.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-156"><span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**\_compilazione SFC di MPNOTIFY Scan \_ \_ \_ completata**</span><span class="sxs-lookup"><span data-stu-id="848f5-156"><span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**MPNOTIFY\_SCAN\_SFC\_BUILD\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-157">Analisi dello stato di avanzamento per notificare la parte di compilazione SFC completata.</span><span class="sxs-lookup"><span data-stu-id="848f5-157">Scan progress to notify sfc build portion has completed.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-158"><span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**avvio di MPNOTIFY \_ Scan \_ FastPath \_**</span><span class="sxs-lookup"><span data-stu-id="848f5-158"><span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**MPNOTIFY\_SCAN\_FASTPATH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-159">L'analisi FastPath SpyNet è iniziata.</span><span class="sxs-lookup"><span data-stu-id="848f5-159">Scan fastpath spynet has begun.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-160"><span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**\_FastPath MPNOTIFY \_ Scan \_ completato**</span><span class="sxs-lookup"><span data-stu-id="848f5-160"><span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**MPNOTIFY\_SCAN\_FASTPATH\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-161">Analisi FastPath SpyNet terminata.</span><span class="sxs-lookup"><span data-stu-id="848f5-161">Scan fastpath spynet has ended.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-162"><span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**MPNOTIFY \_ Scan \_ FastPath- \_ stato**</span><span class="sxs-lookup"><span data-stu-id="848f5-162"><span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**MPNOTIFY\_SCAN\_FASTPATH\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-163">Notifica sullo stato di avanzamento per le ripetizioni FastPath, utilizzate internamente e convertite nello **\_ \_ stato di analisi MPNOTIFY** per l'esterno.</span><span class="sxs-lookup"><span data-stu-id="848f5-163">Progress notification for fastpath rescans, used internally and converted to **MPNOTIFY\_SCAN\_PROGRESS** for external.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-164"><span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**\_Inizio pulizia \_ MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="848f5-164"><span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**MPNOTIFY\_CLEAN\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-165">Pulizia avviata.</span><span class="sxs-lookup"><span data-stu-id="848f5-165">Cleaning started.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-166"><span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**\_pulizia MPNOTIFY \_ completata**</span><span class="sxs-lookup"><span data-stu-id="848f5-166"><span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**MPNOTIFY\_CLEAN\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-167">Pulizia completata.</span><span class="sxs-lookup"><span data-stu-id="848f5-167">Cleaning completed.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-168"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY \_ Clean \_ RESTOREPOINT \_ Start**</span><span class="sxs-lookup"><span data-stu-id="848f5-168"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-169">Avvio della creazione di un punto di ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="848f5-169">Started to create a system restore point.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-170"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY \_ Clean \_ RESTOREPOINT \_ riuscita**</span><span class="sxs-lookup"><span data-stu-id="848f5-170"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-171">Creazione del punto di ripristino del sistema completata.</span><span class="sxs-lookup"><span data-stu-id="848f5-171">System restore point successfully created.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-172"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**\_RESTOREPOINT Clean \_ MPNOTIFY \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="848f5-172"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-173">Impossibile creare il punto di ripristino del sistema.</span><span class="sxs-lookup"><span data-stu-id="848f5-173">System restore point creation failed.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-174"><span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**\_avvio della \_ minaccia MPNOTIFY Clean \_**</span><span class="sxs-lookup"><span data-stu-id="848f5-174"><span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**MPNOTIFY\_CLEAN\_THREAT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-175">Viene avviata la pulizia per una minaccia specifica.</span><span class="sxs-lookup"><span data-stu-id="848f5-175">Cleaning is started for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-176"><span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**\_minaccia MPNOTIFY \_ pulita \_ riuscita**</span><span class="sxs-lookup"><span data-stu-id="848f5-176"><span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-177">La pulizia è riuscita per una minaccia specifica.</span><span class="sxs-lookup"><span data-stu-id="848f5-177">Cleaning is succeeded for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-178"><span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**\_minaccia MPNOTIFY \_ Clean \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="848f5-178"><span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**MPNOTIFY\_CLEAN\_THREAT\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-179">La pulizia non è riuscita per una minaccia specifica.</span><span class="sxs-lookup"><span data-stu-id="848f5-179">Cleaning has failed for a particular threat.</span></span> <span data-ttu-id="848f5-180">**Errore \_ Il codice di errore della \_ minaccia MP \_ non \_ trovato** indica che la minaccia non è stata trovata (e non è un errore di pulizia).</span><span class="sxs-lookup"><span data-stu-id="848f5-180">**ERROR\_MP\_THREAT\_NOT\_FOUND** error code indicates that the threat was not found (and was not a failure to clean).</span></span>

</dd> <dt>

<span data-ttu-id="848f5-181"><span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**\_risorsa pulita \_ MPNOTIFY \_ riuscita**</span><span class="sxs-lookup"><span data-stu-id="848f5-181"><span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**MPNOTIFY\_CLEAN\_RESOURCE\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-182">La pulizia è riuscita per una determinata risorsa.</span><span class="sxs-lookup"><span data-stu-id="848f5-182">Cleaning is succeeded for a particular resource.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-183"><span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**\_risorsa pulita \_ MPNOTIFY \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="848f5-183"><span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**MPNOTIFY\_CLEAN\_RESOURCE\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-184">La pulizia non è riuscita per una determinata risorsa.</span><span class="sxs-lookup"><span data-stu-id="848f5-184">Cleaning has failed for a particular resource.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-185"><span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**MPNOTIFY \_ una \_ minaccia pulita \_ completa**</span><span class="sxs-lookup"><span data-stu-id="848f5-185"><span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**MPNOTIFY\_CLEAN\_THREAT\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-186">La pulizia è stata completata per una minaccia specifica.</span><span class="sxs-lookup"><span data-stu-id="848f5-186">Cleaning has completed for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-187"><span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**\_avvio della PREVERIFICA MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="848f5-187"><span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**MPNOTIFY\_PRECHECK\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-188">Verifica preliminare pulita avviata.</span><span class="sxs-lookup"><span data-stu-id="848f5-188">Clean precheck started.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-189"><span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**\_PRECONTROLLO MPNOTIFY \_ completato**</span><span class="sxs-lookup"><span data-stu-id="848f5-189"><span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**MPNOTIFY\_PRECHECK\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-190">Pulizia Preverifica completata.</span><span class="sxs-lookup"><span data-stu-id="848f5-190">Clean precheck completed.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-191"><span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**\_risorsa PREVERIFICA \_ MPNOTIFY \_ bloccata**</span><span class="sxs-lookup"><span data-stu-id="848f5-191"><span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-192">Pulire la Preverifica della risorsa bloccata rilevata.</span><span class="sxs-lookup"><span data-stu-id="848f5-192">Clean precheck detected blocked resource.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-193"><span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**è \_ stata \_ rilevata una minaccia MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="848f5-193"><span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**MPNOTIFY\_THREAT\_DETECTED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-194">Nuova minaccia rilevata nel sistema.</span><span class="sxs-lookup"><span data-stu-id="848f5-194">New threat detected in system.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-195"><span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**\_minaccia MPNOTIFY \_ modificata**</span><span class="sxs-lookup"><span data-stu-id="848f5-195"><span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**MPNOTIFY\_THREAT\_MODIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-196">Informazioni sulle minacce modificate.</span><span class="sxs-lookup"><span data-stu-id="848f5-196">Threat information modified.</span></span> <span data-ttu-id="848f5-197">Ad esempio, è stata aggiunta una nuova risorsa.</span><span class="sxs-lookup"><span data-stu-id="848f5-197">For example, a new resource was added.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-198"><span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**la \_ pulizia della minaccia MPNOTIFY è \_ \_ riuscita**</span><span class="sxs-lookup"><span data-stu-id="848f5-198"><span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**MPNOTIFY\_THREAT\_CLEAN\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-199">L'azione di pulizia è riuscita per una minaccia.</span><span class="sxs-lookup"><span data-stu-id="848f5-199">Cleaning action succeeded for a threat.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-200"><span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**la \_ pulizia della minaccia MPNOTIFY \_ \_ non è riuscita**</span><span class="sxs-lookup"><span data-stu-id="848f5-200"><span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**MPNOTIFY\_THREAT\_CLEAN\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-201">Azione di pulizia non riuscita per una minaccia.</span><span class="sxs-lookup"><span data-stu-id="848f5-201">Cleaning action failed for a threat.</span></span> <span data-ttu-id="848f5-202">**Errore \_ Il codice di errore della \_ minaccia MP \_ non \_ trovato** indica che la minaccia non è stata trovata (e non è un errore di pulizia).</span><span class="sxs-lookup"><span data-stu-id="848f5-202">**ERROR\_MP\_THREAT\_NOT\_FOUND** error code indicates that the threat was not found (and was not a failure to clean).</span></span>

</dd> <dt>

<span data-ttu-id="848f5-203"><span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**\_minaccia MPNOTIFY \_ abbandonata**</span><span class="sxs-lookup"><span data-stu-id="848f5-203"><span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**MPNOTIFY\_THREAT\_ABANDONED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-204">Non è stata eseguita alcuna correzione prima dell'arresto del servizio.</span><span class="sxs-lookup"><span data-stu-id="848f5-204">No remediation occurred before the service was stopped.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-205"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**\_ \_ \_ inizio evento MPNOTIFY Threat \_ clean**</span><span class="sxs-lookup"><span data-stu-id="848f5-205"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**MPNOTIFY\_THREAT\_CLEAN\_EVENT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-206">È stata avviata un'azione di pulizia.</span><span class="sxs-lookup"><span data-stu-id="848f5-206">A cleaning action has been started.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-207"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**\_evento MPNOTIFY \_ Threat \_ Clean \_ completato**</span><span class="sxs-lookup"><span data-stu-id="848f5-207"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**MPNOTIFY\_THREAT\_CLEAN\_EVENT\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-208">È stata terminata un'azione di pulizia.</span><span class="sxs-lookup"><span data-stu-id="848f5-208">A cleaning action has ended.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-209"><span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**\_inizio MPNOTIFY SIGUPDATE \_**</span><span class="sxs-lookup"><span data-stu-id="848f5-209"><span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**MPNOTIFY\_SIGUPDATE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-210">Aggiornamento della firma avviato.</span><span class="sxs-lookup"><span data-stu-id="848f5-210">Signature update started.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-211"><span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**\_avvio della \_ ricerca \_ SIGUPDATE di MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="848f5-211"><span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**MPNOTIFY\_SIGUPDATE\_SEARCH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-212">Ricerca degli aggiornamenti avviata.</span><span class="sxs-lookup"><span data-stu-id="848f5-212">Search for updates started.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-213"><span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**\_ricerca MPNOTIFY \_ SIGUPDATE \_ completata**</span><span class="sxs-lookup"><span data-stu-id="848f5-213"><span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**MPNOTIFY\_SIGUPDATE\_SEARCH\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-214">Ricerca degli aggiornamenti completata.</span><span class="sxs-lookup"><span data-stu-id="848f5-214">Search for updates completed.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-215"><span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**\_ \_ aggiornamento software MPNOTIFY \_ SIGUPDATE \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="848f5-215"><span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**MPNOTIFY\_SIGUPDATE\_SOFTWARE\_UPDATE\_AVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-216">Aggiornamento software disponibile.</span><span class="sxs-lookup"><span data-stu-id="848f5-216">Software update available.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-217"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**avvio del download di MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="848f5-217"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-218">Download avviato.</span><span class="sxs-lookup"><span data-stu-id="848f5-218">Download started.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-219"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**stato del download di MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="848f5-219"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-220">Il download è in corso.</span><span class="sxs-lookup"><span data-stu-id="848f5-220">Download in progress.</span></span> <span data-ttu-id="848f5-221">I dati di callback contengono lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="848f5-221">Callback data contains progress.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-222"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**Download di MPNOTIFY \_ SIGUPDATE \_ \_ completato**</span><span class="sxs-lookup"><span data-stu-id="848f5-222"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-223">Download completato.</span><span class="sxs-lookup"><span data-stu-id="848f5-223">Download completed.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-224"><span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**\_ \_ avvio installazione di MPNOTIFY SIGUPDATE \_**</span><span class="sxs-lookup"><span data-stu-id="848f5-224"><span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-225">Installazione avviata.</span><span class="sxs-lookup"><span data-stu-id="848f5-225">Installation started.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-226"><span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**stato di installazione di MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="848f5-226"><span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-227">Installazione in corso.</span><span class="sxs-lookup"><span data-stu-id="848f5-227">Installation in progress.</span></span> <span data-ttu-id="848f5-228">I dati di callback contengono lo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="848f5-228">Callback data contains progress.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-229"><span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**installazione di MPNOTIFY \_ SIGUPDATE \_ \_ completata**</span><span class="sxs-lookup"><span data-stu-id="848f5-229"><span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-230">Installazione completata.</span><span class="sxs-lookup"><span data-stu-id="848f5-230">Installation complete.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-231"><span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**riavvio di MPNOTIFY \_ SIGUPDATE \_ \_ obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="848f5-231"><span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**MPNOTIFY\_SIGUPDATE\_REBOOT\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-232">Aggiornamento richiede il riavvio.</span><span class="sxs-lookup"><span data-stu-id="848f5-232">Update requires reboot.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-233"><span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**\_richiesta SIGUPDATE \_ MPNOTIFY \_ elaborata**</span><span class="sxs-lookup"><span data-stu-id="848f5-233"><span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**MPNOTIFY\_SIGUPDATE\_REQUEST\_PROCESSED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-234">Il servizio ha elaborato una richiesta di aggiornamento della firma.</span><span class="sxs-lookup"><span data-stu-id="848f5-234">Service processed a signature update request.</span></span> <span data-ttu-id="848f5-235">Esito negativo o esito positivo è indicato da **HRESULT** nei dati di callback.</span><span class="sxs-lookup"><span data-stu-id="848f5-235">Failure or success is indicated by **hResult** in the callback data.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-236"><span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ completata**</span><span class="sxs-lookup"><span data-stu-id="848f5-236"><span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY\_SIGUPDATE\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-237">Aggiornamento completato.</span><span class="sxs-lookup"><span data-stu-id="848f5-237">Update complete.</span></span> <span data-ttu-id="848f5-238">**S \_ FALSE** Status indica che non è necessario alcun aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="848f5-238">**S\_FALSE** status indicates that no updates were needed.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-239"><span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**\_inizio dell'esempio MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="848f5-239"><span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**MPNOTIFY\_SAMPLE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-240">Invio di esempio avviato.</span><span class="sxs-lookup"><span data-stu-id="848f5-240">Sample submission started.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-241"><span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**\_esempio MPNOTIFY \_ completato**</span><span class="sxs-lookup"><span data-stu-id="848f5-241"><span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**MPNOTIFY\_SAMPLE\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-242">Invio di esempio completato.</span><span class="sxs-lookup"><span data-stu-id="848f5-242">Sample submission completed.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-243"><span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**\_inizio dell' \_ elemento di esempio MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="848f5-243"><span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**MPNOTIFY\_SAMPLE\_ITEM\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-244">Invio di elementi di esempio specifico avviato.</span><span class="sxs-lookup"><span data-stu-id="848f5-244">Specific sample item submission started.</span></span> <span data-ttu-id="848f5-245">L'indice degli elementi di esempio è disponibile nei [**\_ dati MPSAMPLE**](mpsample-data.md).</span><span class="sxs-lookup"><span data-stu-id="848f5-245">Sample item index is available in [**MPSAMPLE\_DATA**](mpsample-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="848f5-246"><span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**\_elemento di esempio MPNOTIFY \_ \_ riuscito**</span><span class="sxs-lookup"><span data-stu-id="848f5-246"><span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**MPNOTIFY\_SAMPLE\_ITEM\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-247">Invio specifico di un elemento di esempio completato.</span><span class="sxs-lookup"><span data-stu-id="848f5-247">Specific sample item submission succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-248"><span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**\_elemento di esempio MPNOTIFY \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="848f5-248"><span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**MPNOTIFY\_SAMPLE\_ITEM\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-249">Invio specifico di un elemento di esempio non riuscito.</span><span class="sxs-lookup"><span data-stu-id="848f5-249">Specific sample item submission failed.</span></span> <span data-ttu-id="848f5-250">Il codice di errore è disponibile nei [**\_ dati di MPCALLBACK**](mpcallback-data.md).</span><span class="sxs-lookup"><span data-stu-id="848f5-250">Error code is available in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="848f5-251"><span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**MPNOTIFY \_ \_ dati riservati**</span><span class="sxs-lookup"><span data-stu-id="848f5-251"><span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**MPNOTIFY\_RESERVED\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-252">Dati riservati interni.</span><span class="sxs-lookup"><span data-stu-id="848f5-252">Internal reserved data.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-253"><span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**MPNOTIFY \_ FastPath \_ sig \_ aggiunto**</span><span class="sxs-lookup"><span data-stu-id="848f5-253"><span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**MPNOTIFY\_FASTPATH\_SIG\_ADDED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-254">Una firma FastPath ha aggiunto o disabilitato una firma.</span><span class="sxs-lookup"><span data-stu-id="848f5-254">A Fastpath signature has either added or disabled a signature.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-255"><span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY \_ FastPath \_ sig \_ rimosso**</span><span class="sxs-lookup"><span data-stu-id="848f5-255"><span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY\_FASTPATH\_SIG\_REMOVED**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-256">È stata rimossa una firma FastPath.</span><span class="sxs-lookup"><span data-stu-id="848f5-256">A FastPath signature has been removed.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-257"><span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY \_ NIS \_ privato**</span><span class="sxs-lookup"><span data-stu-id="848f5-257"><span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY\_NIS\_PRIVATE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-258">Notifiche privato NIS.</span><span class="sxs-lookup"><span data-stu-id="848f5-258">NIS private notifcations.</span></span> <span data-ttu-id="848f5-259">Non è necessario che i partner si registrino a questo.</span><span class="sxs-lookup"><span data-stu-id="848f5-259">No partners should register for this.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-260"><span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**\_Modifica integrità \_ MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="848f5-260"><span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**MPNOTIFY\_HEALTH\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-261">Il servizio AM è entrato in uno stato nuovo.</span><span class="sxs-lookup"><span data-stu-id="848f5-261">The AM service has entered a new state.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-262"><span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**\_ripristino integrità \_ MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="848f5-262"><span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**MPNOTIFY\_HEALTH\_RECOVERY**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-263">Il servizio AM è stato recuperato da uno stato.</span><span class="sxs-lookup"><span data-stu-id="848f5-263">The AM service has recovered from a state.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-264"><span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**\_inizio integrità \_ MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="848f5-264"><span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**MPNOTIFY\_HEALTH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-265">Il servizio AM ha inizializzato l'integrità del sistema.</span><span class="sxs-lookup"><span data-stu-id="848f5-265">The AM service has initialized the health of the system.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-266"><span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**\_modifica MPNOTIFY ENDOFLIFE \_**</span><span class="sxs-lookup"><span data-stu-id="848f5-266"><span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**MPNOTIFY\_ENDOFLIFE\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-267">Le date di scadenza per il servizio AM sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="848f5-267">The "End Of Life" expiry dates for the AM service have changed.</span></span>

</dd> <dt>

<span data-ttu-id="848f5-268"><span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**\_dati MALWARETOAST di MPNOTIFY \_**</span><span class="sxs-lookup"><span data-stu-id="848f5-268"><span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**MPNOTIFY\_MALWARETOAST\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="848f5-269">Il servizio AM ha rilevato malware che potrebbe aver causato la modifica delle impostazioni critiche nel computer.</span><span class="sxs-lookup"><span data-stu-id="848f5-269">The AM service has encountered malware that might have caused critical settings change in the machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="848f5-270">Requisiti</span><span class="sxs-lookup"><span data-stu-id="848f5-270">Requirements</span></span>



| <span data-ttu-id="848f5-271">Requisito</span><span class="sxs-lookup"><span data-stu-id="848f5-271">Requirement</span></span> | <span data-ttu-id="848f5-272">Valore</span><span class="sxs-lookup"><span data-stu-id="848f5-272">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="848f5-273">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="848f5-273">Minimum supported client</span></span><br/> | <span data-ttu-id="848f5-274">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="848f5-274">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="848f5-275">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="848f5-275">Minimum supported server</span></span><br/> | <span data-ttu-id="848f5-276">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="848f5-276">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="848f5-277">Intestazione</span><span class="sxs-lookup"><span data-stu-id="848f5-277">Header</span></span><br/>                   | <dl> <span data-ttu-id="848f5-278"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="848f5-278"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="848f5-279">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="848f5-279">See also</span></span>

<dl> <dt>

[<span data-ttu-id="848f5-280">**MpManagerStatusQueryEx**</span><span class="sxs-lookup"><span data-stu-id="848f5-280">**MpManagerStatusQueryEx**</span></span>](mpmanagerstatusqueryex.md)
</dt> <dt>

[<span data-ttu-id="848f5-281">**\_dati MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="848f5-281">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="848f5-282">**\_dati MPSAMPLE**</span><span class="sxs-lookup"><span data-stu-id="848f5-282">**MPSAMPLE\_DATA**</span></span>](mpsample-data.md)
</dt> </dl>

 

 





