---
title: Enumerazione MPTHREAT_SEVERITY (MpClient. h)
description: Possibili livelli di gravità della minaccia.
ms.assetid: 7C50AC74-16CB-4198-ABB2-D6999429F2EA
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPTHREAT_SEVERITY
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPTHREAT_SEVERITY
topic_type:
- apiref
api_name:
- MPTHREAT_SEVERITY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eec7bff3b23a89ce8187798d8a69a9968cbc2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301538"
---
# <a name="mpthreat_severity-enumeration"></a>\_Enumerazione gravità MPTHREAT

Possibili livelli di gravità della minaccia.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMPTHREAT_SEVERITY { 
  MP_THREAT_SEVERITY_UNKNOWN   = 0,
  MP_THREAT_SEVERITY_LOW       = 1,
  MP_THREAT_SEVERITY_MODERATE  = 2,
  MP_THREAT_SEVERITY_HIGH      = 4,
  MP_THREAT_SEVERITY_SEVERE    = 5,
  MP_THREAT_SEVERITY_MAXVALUE  = 5
} MPTHREAT_SEVERITY, *PMPTHREAT_SEVERITY;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MP_THREAT_SEVERITY_UNKNOWN"></span><span id="mp_threat_severity_unknown"></span>**\_gravità minaccia \_ MP \_ sconosciuta**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_LOW"></span><span id="mp_threat_severity_low"></span>**\_gravità minacce \_ MP \_ bassa**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_MODERATE"></span><span id="mp_threat_severity_moderate"></span>**\_gravità della minaccia MP \_ \_ moderata**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_HIGH"></span><span id="mp_threat_severity_high"></span>**\_gravità della minaccia MP \_ \_ elevata**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_SEVERE"></span><span id="mp_threat_severity_severe"></span>**\_gravità della minaccia MP \_ \_ grave**
</dt> <dd></dd> <dt>

<span id="MP_THREAT_SEVERITY_MAXVALUE"></span><span id="mp_threat_severity_maxvalue"></span>**\_gravità della minaccia MP \_ \_ MaxValue**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





