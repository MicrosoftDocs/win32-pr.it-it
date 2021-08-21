---
title: MPSTATUS_FLAG enumerazione (MpClient.h)
description: Possibili flag di bit dello stato complessivo del prodotto.
ms.assetid: BF2E6506-E76A-4785-8E91-99937B413548
keywords:
- MPSTATUS_FLAG di enumerazione Legacy Windows Environment Features
- PMPSTATUS_FLAG puntatore di enumerazione Legacy Windows Environment Features
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
ms.openlocfilehash: 4d850f0e8de9a3b0ed18a1a1353dfdef40d41bcb1ce4d17265ec245e82ba73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747035"
---
# <a name="mpstatus_flag-enumeration"></a>Enumerazione MPSTATUS \_ FLAG

Possibili flag di bit dello stato complessivo del prodotto.

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

<span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**FLAG \_ DI STATO MP \_ \_ NONE**
</dt> <dd>

Nessun flag di stato impostato (stato non inizializzato).

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**SERVIZIO FLAG \_ DI STATO MP NON \_ \_ \_ DISPONIBILE**
</dt> <dd>

Servizio non in esecuzione.

</dd> <dt>

<span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**MP \_ STATUS \_ FLAG \_ MPENGINE NON \_ DISPONIBILE**
</dt> <dd>

Il servizio è stato avviato senza alcun motore di protezione da malware.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**MP \_ STATUS \_ FLAG \_ THREAT \_ FULLSCAN \_ REQUIRED**
</dt> <dd>

Analisi completa in sospeso a causa di un'azione di minaccia.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**RICHIESTO \_ RIAVVIO \_ DELLA MINACCIA DEL FLAG DI \_ \_ STATO \_ MP**
</dt> <dd>

Riavvio in sospeso a causa di un'azione di minaccia.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**PASSAGGI MANUALI DI MINACCIA DEL FLAG DI STATO MP \_ \_ \_ \_ \_ \_ NECESSARI**
</dt> <dd>

Passaggi manuali in sospeso a causa di un'azione di minaccia.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**MP \_ STATUS \_ FLAG \_ DUE \_ AV \_ SIGNATURE**
</dt> <dd>

Firme antivirus non aggiornate.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**FLAG \_ DI STATO MP DOVUTO COME \_ \_ \_ \_ FIRMA**
</dt> <dd>

Firme antispyware non aggiornate.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**MP \_ STATUS \_ FLAG \_ DUE \_ QUICK \_ SCAN**
</dt> <dd>

Non è stata eseguita alcuna analisi rapida per un periodo specificato.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**FLAG \_ DI STATO MP DOVUTO \_ \_ \_ \_ ALL'ANALISI COMPLETA**
</dt> <dd>

Non è stata eseguita alcuna analisi completa per un periodo specificato

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**MP \_ STATUS \_ FLAG \_ INPROGRESS \_ SYSTEM \_ SCAN**
</dt> <dd>

Analisi avviata dal sistema in corso.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**PULIZIA \_ DI ROUTINE DI ROUTINE IN INGRESSO DEL FLAG DI \_ \_ \_ STATO \_ MP**
</dt> <dd>

Pulizia avviata dal sistema in corso.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**ESEMPI \_ RELATIVI AL FLAG DI STATO \_ MP \_ \_**
</dt> <dd>

Sono presenti esempi in attesa di invio.

</dd> <dt>

<span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**MODALITÀ \_ DI VALUTAZIONE DEL FLAG DI STATO \_ \_ MP \_**
</dt> <dd>

Il prodotto è in esecuzione in modalità di valutazione.

</dd> <dt>

<span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**FLAG \_ DI STATO MP \_ \_ NONGENUINE**
</dt> <dd>

Il prodotto è in esecuzione in modalità Windows originale.

</dd> <dt>

<span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**IL PRODOTTO \_ CON FLAG DI STATO MP È \_ \_ \_ SCADUTO**
</dt> <dd>

Il prodotto è scaduto.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**MP \_ STATUS \_ FLAG \_ THREAT \_ CALLISTO \_ REQUIRED**
</dt> <dd>

È necessaria l'analisi off-line callisto.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**SERVIZIO MP \_ STATUS \_ FLAG \_ \_ \_ ALL'ARRESTO DEL \_ SISTEMA**
</dt> <dd>

Il servizio viene arrestato durante l'arresto del sistema.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**ERRORE \_ CRITICO DEL SERVIZIO DEL FLAG DI \_ \_ \_ STATO \_ MP**
</dt> <dd>

La correzione delle minacce non è riuscita in modo critico.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**ERRORE NON CRITICO DEL SERVIZIO DEL FLAG DI STATO \_ \_ \_ \_ \_ \_ MP**
</dt> <dd>

La correzione delle minacce non è riuscita in modo non critico.

</dd> <dt>

<span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**INTEGRITÀ \_ DEL FLAG DI STATO MP \_ \_ \_ INIZIALIZZATA**
</dt> <dd>

Nessun flag di stato impostato (stato ben inizializzato).

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**AGGIORNAMENTO \_ DELLA PIATTAFORMA DOVUTO AL FLAG DI \_ \_ \_ STATO \_ MP**
</dt> <dd>

La piattaforma non è aggiornata.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**MP \_ STATUS \_ FLAG \_ INPROGRESS \_ PLATFORM \_ UPDATE**
</dt> <dd>

Aggiornamento della piattaforma in corso.

</dd> <dt>

<span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**LA PIATTAFORMA DEL FLAG DI STATO MP \_ \_ STA PER ESSERE \_ \_ \_ \_ \_ OBSOLETA**
</dt> <dd>

La piattaforma sta per essere obsoleta

</dd> <dt>

<span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**FINE \_ DEL CICLO DI VITA DEL FLAG DI STATO \_ \_ \_ \_ MP**
</dt> <dd>

La firma o la fine del ciclo di vita della piattaforma è passata o è in sospeso.

</dd> <dt>

<span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**MP \_ STATUS \_ FLAG \_ MAX**
</dt> <dd>

Flag massimo valido.

</dd> <dt>

<span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**FLAG \_ DI STATO MP \_ \_ ALL**
</dt> <dd>

Valore massimo possibile.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





