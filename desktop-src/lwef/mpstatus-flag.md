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
# <a name="mpstatus_flag-enumeration"></a>\_Enumerazione flag MPSTATUS

Possibili flag di bit di stato generale del prodotto.

## <a name="syntax"></a>Sintassi


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



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**\_flag di stato MP \_ \_ None**
</dt> <dd>

Nessun flag di stato impostato (stato non inizializzato).

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**\_servizio flag di stato MP non \_ \_ \_ disponibile**
</dt> <dd>

Il servizio non è in esecuzione.

</dd> <dt>

<span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**\_flag di stato MP MPENGINE non \_ \_ \_ disponibile**
</dt> <dd>

Il servizio è stato avviato senza alcun motore di protezione da malware.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**il \_ flag di stato MP \_ \_ Threat \_ FullScan è \_ obbligatorio**
</dt> <dd>

Analisi completa in sospeso a causa di un'azione di minaccia.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**è \_ \_ \_ \_ necessario riavviare il flag di stato MP \_**
</dt> <dd>

Riavvio in sospeso a causa di un'azione di minaccia.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**sono \_ \_ \_ \_ \_ necessari passaggi manuali \_ per la minaccia del flag di stato MP**
</dt> <dd>

Passaggi manuali in sospeso a causa di un'azione di minaccia.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**\_flag di stato MP \_ \_ a causa della \_ \_ firma AV**
</dt> <dd>

Le firme antivirus non sono aggiornate.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**\_ \_ flag di stato MP \_ a causa della \_ \_ firma**
</dt> <dd>

Firme antispyware obsolete.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**\_flag di stato MP \_ \_ scadenza \_ \_ analisi veloce**
</dt> <dd>

Non è stata eseguita alcuna analisi veloce per un periodo specificato.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**\_flag di stato MP \_ \_ a causa dell' \_ \_ analisi completa**
</dt> <dd>

non è stata eseguita un'analisi completa per un periodo specificato

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**analisi di sistema del flag di stato MP in \_ \_ \_ corso \_ \_**
</dt> <dd>

Analisi avviata dal sistema in corso.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**\_ \_ \_ pulizia routine in corso del flag di \_ stato MP \_**
</dt> <dd>

Pulizia avviata dal sistema in corso.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**\_esempi di flag di stato MP \_ \_ dovuti \_**
</dt> <dd>

Sono presenti campioni in attesa di invio.

</dd> <dt>

<span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**\_modalità di \_ valutazione del flag di stato MP \_ \_**
</dt> <dd>

Il prodotto è in esecuzione in modalità di valutazione.

</dd> <dt>

<span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**FLAG di stato MP non \_ \_ \_ autentico**
</dt> <dd>

Il prodotto è in esecuzione in modalità Windows non originale.

</dd> <dt>

<span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**il \_ prodotto del flag di stato MP è \_ \_ \_ scaduto**
</dt> <dd>

Prodotto scaduto.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**il \_ flag di stato del MP \_ \_ minaccia \_ Callisto \_**
</dt> <dd>

È richiesta l'analisi non in linea di Callisto.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**\_ \_ servizio flag di stato MP \_ \_ all' \_ arresto del sistema \_**
</dt> <dd>

Il servizio verrà arrestato nell'ambito dell'arresto del sistema.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**\_ \_ \_ \_ errore critico servizio flag di stato MP \_**
</dt> <dd>

La correzione delle minacce non è riuscita.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**\_ \_ \_ \_ \_ errore non critico del servizio flag di stato \_ MP**
</dt> <dd>

La correzione delle minacce non è riuscita in modo non critico.

</dd> <dt>

<span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**\_stato del flag di stato MP \_ \_ \_ inizializzato**
</dt> <dd>

Nessun flag di stato impostato (stato ben inizializzato).

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**\_flag di stato MP \_ \_ a causa dell' \_ aggiornamento della piattaforma \_**
</dt> <dd>

La piattaforma non è aggiornata.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**\_aggiornamento della \_ \_ piattaforma di inesecuzione del flag di \_ stato MP \_**
</dt> <dd>

Aggiornamento della piattaforma in corso.

</dd> <dt>

<span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**\_ \_ \_ piattaforma del flag di stato MP \_ \_ che sta per \_ essere \_ obsoleta**
</dt> <dd>

La piattaforma sta per essere obsoleta

</dd> <dt>

<span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**\_ \_ \_ fine \_ della durata del flag di stato MP \_**
</dt> <dd>

La fine del ciclo di vita della firma o della piattaforma è passata o è in sospeso.

</dd> <dt>

<span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**\_flag di \_ stato \_ massimo MP**
</dt> <dd>

Flag massimo valido.

</dd> <dt>

<span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**\_flag di stato MP \_ \_ All**
</dt> <dd>

Valore massimo possibile.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





