---
title: MPTHREAT_ACTION enumerazione (MpClient.h)
description: Possibili azioni di minaccia.
ms.assetid: 142249A5-4C9D-4E3A-A06E-70C040F9C14F
keywords:
- MPTHREAT_ACTION funzionalità dell'Windows legacy
- PMPTHREAT_ACTION puntatore di enumerazione Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPTHREAT_ACTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a3cd46583b9736ad8304c16e3b12d4f0157edcdb319fd0923a0fe737d504415
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247265"
---
# <a name="mpthreat_action-enumeration"></a>Enumerazione MPTHREAT \_ ACTION

Possibili azioni di minaccia.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMPTHREAT_ACTION { 
  MP_THREAT_ACTION_UNKNOWN      = 0,
  MP_THREAT_ACTION_CLEAN        = 1,
  MP_THREAT_ACTION_QUARANTINE   = 2,
  MP_THREAT_ACTION_REMOVE       = 3,
  MP_THREAT_ACTION_ALLOW        = 6,
  MP_THREAT_ACTION_USERDEFINED  = 8,
  MP_THREAT_ACTION_NOACTION     = 9,
  MP_THREAT_ACTION_BLOCK        = 10,
  MP_THREAT_ACTION_MAX_VALUE    = 10
} MPTHREAT_ACTION, *PMPTHREAT_ACTION;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**AZIONE \_ DI MINACCIA MP \_ \_ SCONOSCIUTA**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**MP \_ THREAT \_ ACTION \_ CLEAN**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**QUARANTENA \_ \_ DELL'AZIONE DI MINACCIA \_ MP**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**MP \_ THREAT \_ ACTION \_ REMOVE**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**AZIONE \_ DI MINACCIA MP \_ \_ CONSENTITA**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**AZIONE \_ DI MINACCIA MP DEFINITA \_ \_ DALL'UTENTE**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**MP \_ THREAT \_ ACTION \_ NOACTION**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**MP \_ THREAT \_ ACTION \_ BLOCK**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**VALORE MASSIMO \_ \_ DELL'AZIONE \_ DI MINACCIA \_ MP**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





