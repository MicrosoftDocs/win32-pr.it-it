---
title: Struttura MPTHREAT_STATS (MpClient. h)
description: Statistiche correlate alle minacce.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- Struttura MPTHREAT_STATS le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPTHREAT_STATS
topic_type:
- apiref
api_name:
- MPTHREAT_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2eef7acde5fbeac2cf9951dfad3e6923ccea2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873729"
---
# <a name="mpthreat_stats-structure"></a>\_Struttura statistiche MPTHREAT

Statistiche correlate alle minacce.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPTHREAT_STATS {
  UINT ThreatCount;
  UINT SuspiciousThreatCount;
  UINT Reserved[4];
} MPTHREAT_STATS, *PMPTHREAT_STATS;
```



## <a name="members"></a>Members

<dl> <dt>

**ThreatCount**
</dt> <dd>

Tipo: **uint**

</dd> <dd>

Numero di minacce rilevate.

</dd> <dt>

**SuspiciousThreatCount**
</dt> <dd>

Tipo: **uint**

</dd> <dd>

Numero di minacce rilevate con monitoraggio del comportamento.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **uint \[ 4 \]**

</dd> <dd>

Campi riservati per utilizzi futuri.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





