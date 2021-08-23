---
title: MPTHREAT_STATS struttura (MpClient.h)
description: Statistiche correlate alle minacce.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- MPTHREAT_STATS struttura Legacy Windows Environment Features
- PMPTHREAT_STATS puntatore alla struttura Legacy Windows Environment Features
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
ms.openlocfilehash: 7671b45dc09c8aca494ad270aa69fc386ef3d7c03d5144fdc3e89b4f657bb07b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975941"
---
# <a name="mpthreat_stats-structure"></a>Struttura MPTHREAT \_ STATS

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

Tipo: **UINT**

</dd> <dd>

Numero di minacce rilevate.

</dd> <dt>

**SuspiciousThreatCount**
</dt> <dd>

Tipo: **UINT**

</dd> <dd>

Numero di minacce rilevate con il monitoraggio del comportamento.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **UINT \[ 4 \]**

</dd> <dd>

Campi riservati per un uso futuro.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





