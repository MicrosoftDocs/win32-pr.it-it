---
title: Enumerazione MPTHREAT_DETECTION (MpClient. h)
description: Possibili tipi noti di rilevamento delle minacce non valide.
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPTHREAT_DETECTION
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPTHREAT_DETECTION
topic_type:
- apiref
api_name:
- MPTHREAT_DETECTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86edc0e1ca4ee130f2a2a4a678447771f1ae40ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741007"
---
# <a name="mpthreat_detection-enumeration"></a>\_Enumerazione rilevamento MPTHREAT

Possibili tipi noti di rilevamento delle minacce non valide.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMPTHREAT_DETECTION { 
  MP_THREAT_DETECTION_CONCRETE    = 0,
  MP_THREAT_DETECTION_HEURISTIC   = 1,
  MP_THREAT_DETECTION_GENERIC     = 2,
  MP_THREAT_DETECTION_SUSPICIOUS  = 4,
  MP_THREAT_DETECTION_FASTPATH    = 8
} MPTHREAT_DETECTION, *PMPTHREAT_DETECTION;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**\_concreta \_ rilevamento minacce MP \_**
</dt> <dd>

È stata rilevata una minaccia tramite firme concrete.

</dd> <dt>

<span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**\_ \_ euristica rilevamento minacce MP \_**
</dt> <dd>

Minaccia rilevata tramite euristica.

</dd> <dt>

<span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**\_rilevamento minacce \_ MP \_ generico**
</dt> <dd>

È stata rilevata una minaccia tramite firme generiche.

</dd> <dt>

<span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**\_rilevamento minacce \_ MP \_ sospetto**
</dt> <dd>

Minaccia rilevata tramite il monitoraggio del comportamento.

</dd> <dt>

<span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**\_ \_ FastPath rilevamento minacce \_ MP**
</dt> <dd>

È stata rilevata una minaccia tramite FastPath.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





