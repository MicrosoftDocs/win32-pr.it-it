---
title: MPTHREAT_DETECTION enumerazione (MpClient.h)
description: Possibili tipi noti di rilevamento delle minacce non validi.
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- MPTHREAT_DETECTION funzionalità dell'ambiente Windows legacy
- PMPTHREAT_DETECTION puntatore di enumerazione Legacy Windows Environment Features
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
ms.openlocfilehash: 6d362edbb7257f8be5577880a4390c5a2f5f5703504a5f7447154bebe5ada500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601181"
---
# <a name="mpthreat_detection-enumeration"></a>Enumerazione MPTHREAT \_ DETECTION

Possibili tipi noti di rilevamento delle minacce non validi.

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

<span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**MP \_ THREAT \_ DETECTION \_ CONCRETE**
</dt> <dd>

La minaccia è stata rilevata tramite firme concrete.

</dd> <dt>

<span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**\_EURISTICA DI RILEVAMENTO DELLE MINACCE \_ \_ DEL MP**
</dt> <dd>

La minaccia è stata rilevata tramite euristica.

</dd> <dt>

<span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**MP \_ THREAT \_ DETECTION \_ GENERIC**
</dt> <dd>

La minaccia è stata rilevata tramite firme generiche.

</dd> <dt>

<span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**MP \_ THREAT \_ DETECTION \_ SUSPICIOUS**
</dt> <dd>

È stata rilevata una minaccia tramite il monitoraggio del comportamento.

</dd> <dt>

<span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**MP \_ THREAT \_ DETECTION \_ FASTPATH**
</dt> <dd>

La minaccia è stata rilevata tramite fastpath.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





