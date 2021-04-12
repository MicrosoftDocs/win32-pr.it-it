---
title: Enumerazione MPTHREAT_ACTION (MpClient. h)
description: Possibili azioni di minaccia.
ms.assetid: 142249A5-4C9D-4E3A-A06E-70C040F9C14F
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPTHREAT_ACTION
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPTHREAT_ACTION
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
ms.openlocfilehash: 2ae0377517af590072b797a57c051ad062842ea9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119667"
---
# <a name="mpthreat_action-enumeration"></a>\_Enumerazione azione MPTHREAT

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

<span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**\_azione di minaccia MP \_ \_ sconosciuta**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**\_azione di minaccia MP \_ \_ pulita**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**\_ \_ quarantena azione minaccia MP \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**\_azione di minaccia MP \_ \_ Rimuovi**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**\_azione di minaccia MP \_ \_ Consenti**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**\_azione di minaccia MP \_ \_ USERDEFINED**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**NoAction MP \_ Threat \_ Action \_**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**\_ \_ blocco azione minaccia \_ MP**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**\_ \_ \_ valore massimo azione minaccia \_ MP**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





