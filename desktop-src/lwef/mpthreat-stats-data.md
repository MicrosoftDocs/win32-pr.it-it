---
title: Struttura MPTHREAT_STATS_DATA (MpClient. h)
description: Dati aggiuntivi sulle statistiche sulle minacce.
ms.assetid: 8C01C746-8FD8-4311-908D-D1F4E3488480
keywords:
- Struttura MPTHREAT_STATS_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPTHREAT_STATS_DATA
topic_type:
- apiref
api_name:
- MPTHREAT_STATS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9525ddcfc580e9a82ffdb191d20e3748f7a1e16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119666"
---
# <a name="mpthreat_stats_data-structure"></a>\_ \_ Struttura dei dati delle statistiche MPTHREAT

Dati aggiuntivi sulle statistiche sulle minacce.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPTHREAT_STATS_DATA {
  DWORD dwThreatCount;
} MPTHREAT_STATS_DATA, *PMPTHREAT_STATS_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**dwThreatCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Numero di minacce.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





