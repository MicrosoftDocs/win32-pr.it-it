---
title: Struttura MPSCAN_DATA (MpClient. h)
description: Analizza i dati passati al callback.
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- Struttura MPSCAN_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPSCAN_DATA
topic_type:
- apiref
api_name:
- MPSCAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e78508313f102e2baad19cf359a5c3a7c172db0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479168"
---
# <a name="mpscan_data-structure"></a>\_Struttura dei dati MPSCAN

Analizza i dati passati al callback.

Questa struttura contiene statistiche sulle risorse e sulle minacce cumulative. Questi campi stat sono sempre validi.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPSCAN_DATA {
  MPSCAN_TYPE      ScanType;
  PMPRESOURCE_INFO ResourceInfo;
  MPRESOURCE_STATS ResourceStats;
  MPTHREAT_STATS   ThreatStats;
} MPSCAN_DATA, *PMPSCAN_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**ScanType**
</dt> <dd>

Tipo: **[ **MPSCAN \_**](mpscan-type.md)**

</dd> <dd>

Tipo di analisi.

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Tipo: **PMPRESOURCE \_ info**

</dd> <dd>

Informazioni sulla risorsa. Vedere [**MPRESOURCE \_ info**](mpresource-info.md).

</dd> <dt>

**ResourceStats**
</dt> <dd>

Tipo: **[ **MPRESOURCE \_ stats**](mpresource-stats.md)**

</dd> <dd>

Statistiche cumulative correlate alle risorse.

</dd> <dt>

**ThreatStats**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ stats**](mpthreat-stats.md)**

</dd> <dd>

Statistiche sulle minacce con completamenti riusciti di analisi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_informazioni MPRESOURCE**](mpresource-info.md)
</dt> <dt>

[**\_statistiche MPRESOURCE**](mpresource-stats.md)
</dt> <dt>

[**\_tipo MPSCAN**](mpscan-type.md)
</dt> <dt>

[**\_statistiche MPTHREAT**](mpthreat-stats.md)
</dt> </dl>

 

 





