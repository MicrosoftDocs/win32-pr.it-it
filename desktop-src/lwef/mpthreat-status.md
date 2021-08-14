---
title: MPTHREAT_STATUS enumerazione (MpClient.h)
description: Possibile stato di minaccia.
ms.assetid: 64B57C8B-231B-4A2C-BF2E-45DB62B8350E
keywords:
- MPTHREAT_STATUS funzionalità dell'ambiente Windows legacy
- PMPTHREAT_STATUS puntatore di enumerazione Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPTHREAT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d800cbfb0adbeb994586a69e38ac4a1ad2a8957091508b147bd582fef5233e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476263"
---
# <a name="mpthreat_status-enumeration"></a>Enumerazione MPTHREAT \_ STATUS

Possibile stato di minaccia.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMPTHREAT_STATUS { 
  MP_THREAT_STATUS_UNKNOWN            = 0,
  MP_THREAT_STATUS_DETECTED           = 1,
  MP_THREAT_STATUS_CLEANED            = 2,
  MP_THREAT_STATUS_QUARANTINED        = 3,
  MP_THREAT_STATUS_REMOVED            = 4,
  MP_THREAT_STATUS_ALLOWED            = 5,
  MP_THREAT_STATUS_BLOCKED            = 6,
  MP_THREAT_STATUS_CLEAN_FAILED       = 102,
  MP_THREAT_STATUS_QUARANTINE_FAILED  = 103,
  MP_THREAT_STATUS_REMOVE_FAILED      = 104,
  MP_THREAT_STATUS_ALLOW_FAILED       = 105,
  MP_THREAT_STATUS_ABANDONED          = 106,
  MP_THREAT_STATUS_BLOCK_FAILED       = 107
} MPTHREAT_STATUS, *PMPTHREAT_STATUS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MP_THREAT_STATUS_UNKNOWN"></span><span id="mp_threat_status_unknown"></span>**MP \_ THREAT STATUS UNKNOWN (STATO MINACCIA MP \_ \_ SCONOSCIUTO)**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_DETECTED"></span><span id="mp_threat_status_detected"></span>**RILEVATO \_ STATO DI MINACCIA DEL \_ MP \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_CLEANED"></span><span id="mp_threat_status_cleaned"></span>**MP \_ THREAT \_ STATUS \_ CLEANED**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_QUARANTINED"></span><span id="mp_threat_status_quarantined"></span>**MP \_ THREAT \_ STATUS \_ QUARANTINED**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_REMOVED"></span><span id="mp_threat_status_removed"></span>**MP \_ THREAT \_ STATUS \_ REMOVED**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_ALLOWED"></span><span id="mp_threat_status_allowed"></span>**MP \_ THREAT \_ STATUS \_ ALLOWED**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_BLOCKED"></span><span id="mp_threat_status_blocked"></span>**MP \_ THREAT \_ STATUS \_ BLOCKED**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_CLEAN_FAILED"></span><span id="mp_threat_status_clean_failed"></span>**\_PULITURA DELLO STATO DELLE MINACCE DEL MP NON \_ \_ \_ RIUSCITA**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_QUARANTINE_FAILED"></span><span id="mp_threat_status_quarantine_failed"></span>**QUARANTENA \_ STATO MINACCIA MP NON \_ \_ \_ RIUSCITA**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_REMOVE_FAILED"></span><span id="mp_threat_status_remove_failed"></span>**RIMOZIONE \_ DELLO STATO DI MINACCIA DEL MP NON \_ \_ \_ RIUSCITA**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_ALLOW_FAILED"></span><span id="mp_threat_status_allow_failed"></span>**MP \_ THREAT \_ STATUS \_ ALLOW \_ FAILED**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_ABANDONED"></span><span id="mp_threat_status_abandoned"></span>**MP \_ THREAT \_ STATUS \_ ABANDONED**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_STATUS_BLOCK_FAILED"></span><span id="mp_threat_status_block_failed"></span>**BLOCCO STATO \_ MINACCIA \_ MP NON \_ \_ RIUSCITO**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





