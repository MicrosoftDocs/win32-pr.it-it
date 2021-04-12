---
title: Struttura MPSCAN_RESULT (MpClient. h)
description: Risultati di un'analisi.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- Struttura MPSCAN_RESULT le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPSCAN_RESULT
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
ms.openlocfilehash: e7be60df7993732bafcd7c44ac2fb581c111aed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225240"
---
# <a name="mpscan_result-structure"></a>\_Struttura di risultati MPSCAN

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

**ScanType**
</dt> <dd>

Tipo: **[ **MPSCAN \_**](mpscan-type.md)**

</dd> <dd>

Tipo di analisi. Vedere [**MPSCAN \_ Type**](mpscan-type.md).

</dd> <dt>

**Origine**
</dt> <dd>

Tipo: **[ **MPSOURCE**](mpsource.md)**

</dd> <dd>

Origine dell'analisi, ad esempio avviata dall'utente o dal sistema. Vedere [**MPSOURCE**](mpsource.md).

</dd> <dt>

**ScanGuid**
</dt> <dd>

Tipo: **GUID**

</dd> <dd>

Identificatore di analisi.

</dd> <dt>

**StartTime**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

Ora di inizio dell'analisi.

</dd> <dt>

**EndTime**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

Ora di fine dell'analisi.

</dd> <dt>

**ThreatStats**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ stats**](mpthreat-stats.md)**

</dd> <dd>

Statistiche correlate alle minacce. Vedere [**MPTHREAT \_ Statistics**](mpthreat-stats.md).

</dd> <dt>

**ResourceStats**
</dt> <dd>

Tipo: **[ **MPRESOURCE \_ stats**](mpresource-stats.md)**

</dd> <dd>

Statistiche correlate alle risorse. Vedere [**MPRESOURCE \_ Statistics**](mpresource-stats.md).

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_statistiche MPRESOURCE**](mpresource-stats.md)
</dt> <dt>

[**\_tipo MPSCAN**](mpscan-type.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**\_statistiche MPTHREAT**](mpthreat-stats.md)
</dt> </dl>

 

 





