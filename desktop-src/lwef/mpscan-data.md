---
title: MPSCAN_DATA struttura (MpClient.h)
description: Analizzare i dati passati al callback.
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- MPSCAN_DATA struttura Legacy Windows Environment Features
- PMPSCAN_DATA puntatore alla struttura Legacy Windows Environment Features
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
ms.openlocfilehash: 5b7c00357b8f104fff42b94de552d52979c364dee64a82bb8e438946319c8c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975991"
---
# <a name="mpscan_data-structure"></a>Struttura MPSCAN \_ DATA

Analizzare i dati passati al callback.

Questa struttura contiene statistiche sulle minacce e sulle risorse cumulative. Questi campi stat sono sempre validi.

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

Tipo: **[ **TIPO \_ MPSCAN**](mpscan-type.md)**

</dd> <dd>

Tipo di analisi.

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Tipo: **PMPRESOURCE \_ INFO**

</dd> <dd>

Informazioni sulla risorsa. Vedere [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> <dt>

**ResourceStats**
</dt> <dd>

Tipo: **[ **MPRESOURCE \_ STATS**](mpresource-stats.md)**

</dd> <dd>

Statistiche cumulative correlate alle risorse.

</dd> <dt>

**ThreatStats**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ STATS**](mpthreat-stats.md)**

</dd> <dd>

Statistiche sulle minacce con completamenti dell'analisi riusciti.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INFORMAZIONI SU \_ MPRESOURCE**](mpresource-info.md)
</dt> <dt>

[**STATISTICHE \_ MPRESOURCE**](mpresource-stats.md)
</dt> <dt>

[**TIPO \_ MPSCAN**](mpscan-type.md)
</dt> <dt>

[**STATISTICHE DI \_ MPTHREAT**](mpthreat-stats.md)
</dt> </dl>

 

 





