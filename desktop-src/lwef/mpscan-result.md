---
title: MPSCAN_RESULT (MpClient.h)
description: Risultati di un'analisi.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- MPSCAN_RESULT funzionalità dell'ambiente Windows legacy
- PMPSCAN_RESULT puntatore alla struttura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPSCAN_RESULT
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a41efd40529976d4b7fe639c4907729ed39ae261f5ac644faf1a36e1a213a97e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747152"
---
# <a name="mpscan_result-structure"></a>Struttura RESULT di MPSCAN \_

Risultati di un'analisi.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPSCAN_RESULT {
  MPSCAN_TYPE      ScanType;
  MPSOURCE         Source;
  GUID             ScanGuid;
  ULARGE_INTEGER   StartTime;
  ULARGE_INTEGER   EndTime;
  MPTHREAT_STATS   ThreatStats;
  MPRESOURCE_STATS ResourceStats;
  ULONGLONG        SignatureVersion;
} MPSCAN_RESULT, *PMPSCAN_RESULT;
```



## <a name="members"></a>Members

<dl> <dt>

**Tipo di analisi**
</dt> <dd>

Tipo: **[ **TIPO \_ MPSCAN**](mpscan-type.md)**

</dd> <dd>

Tipo di analisi. Vedere [**MPSCAN \_ TYPE**](mpscan-type.md).

</dd> <dt>

**Origine**
</dt> <dd>

Tipo: **[ **MPSOURCE**](mpsource.md)**

</dd> <dd>

Analizzare l'origine, ad esempio avviata dall'utente o dal sistema. Vedere [**MPSOURCE.**](mpsource.md)

</dd> <dt>

**ScanGuid**
</dt> <dd>

Tipo: **GUID**

</dd> <dd>

Identificatore di analisi.

</dd> <dt>

**StartTime**
</dt> <dd>

Tipo: **ULARGE \_ INTEGER**

</dd> <dd>

Ora di inizio dell'analisi.

</dd> <dt>

**EndTime**
</dt> <dd>

Tipo: **ULARGE \_ INTEGER**

</dd> <dd>

Ora di fine dell'analisi.

</dd> <dt>

**ThreatStats**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ STATS**](mpthreat-stats.md)**

</dd> <dd>

Statistiche relative alle minacce. Vedere [**MPTHREAT \_ STATS (STATISTICHE MPTHREAT).**](mpthreat-stats.md)

</dd> <dt>

**ResourceStats**
</dt> <dd>

Tipo: **[ **MPRESOURCE \_ STATS**](mpresource-stats.md)**

</dd> <dd>

Statistiche relative alle risorse. Vedere [**MPRESOURCE \_ STATS**](mpresource-stats.md).

</dd> <dt>

**SignatureVersion**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Versione della firma utilizzata per l'analisi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**STATISTICHE \_ MPRESOURCE**](mpresource-stats.md)
</dt> <dt>

[**TIPO \_ MPSCAN**](mpscan-type.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**STATISTICHE \_ MPTHREAT**](mpthreat-stats.md)
</dt> </dl>

 

 





