---
title: Struttura MPSTATUS_INFO (MpClient. h)
description: Informazioni sullo stato di malware Protection Manager.
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- Struttura MPSTATUS_INFO le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPSTATUS_INFO
topic_type:
- apiref
api_name:
- MPSTATUS_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efe31981f819d85d13457553beb1ce3c869b98bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740130"
---
# <a name="mpstatus_info-structure"></a>Struttura delle informazioni di MPSTATUS \_

Informazioni sullo stato di malware Protection Manager.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPSTATUS_INFO {
  DWORD               ProductStatus;
  MPSCAN_RESULT       LastQuickScan;
  MPSCAN_RESULT       LastFullScan;
  MPTHREAT_STATS      ThreatStats;
  MPTHREAT_STATS_DATA ThreatState[MP_THREAT_STAT_MAX_VALUE+1];
  MPCOMPONENT_STATUS  Component[MPCOMPONENT_MAXVALUE+1];
  ULARGE_INTEGER      ProductExpirationTime;
} MPSTATUS_INFO, *PMPSTATUS_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**ProductStatus**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Stato generale del prodotto. Si tratta di una combinazione di flag di bit del [**\_ flag MPSTATUS**](mpstatus-flag.md).

</dd> <dt>

**LastQuickScan**
</dt> <dd>

Tipo: **[ **\_ risultato MPSCAN**](mpscan-result.md)**

</dd> <dd>

Risultati dell'ultima analisi da parte di malware Protection Manager. Vedere [**il \_ risultato di MPSCAN**](mpscan-result.md).

</dd> <dt>

**LastFullScan**
</dt> <dd>

Tipo: **[ **\_ risultato MPSCAN**](mpscan-result.md)**

</dd> <dd>

Risultati dell'ultima analisi completa da parte di malware Protection Manager. Vedere [**il \_ risultato di MPSCAN**](mpscan-result.md).

</dd> <dt>

**ThreatStats**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ stats**](mpthreat-stats.md)**

</dd> <dd>

Statistiche sulle minacce attive. Vedere [**MPTHREAT \_ Statistics**](mpthreat-stats.md).

</dd> <dt>

**ThreatState**
</dt> <dd>

Tipo: **[**MPTHREAT \_ stats \_ Data**](mpthreat-stats-data.md) \[ MP \_ Threat \_ Stat \_ Max \_ value + 1\]**

</dd> <dd>

Dati aggiuntivi sulle statistiche sulle minacce, ad esempio il numero di minacce. Vedere [**MPTHREAT \_ stats \_ Data**](mpthreat-stats-data.md).

</dd> <dt>

**Componente**
</dt> <dd>

Tipo: **[**MPCOMPONENT \_ stato**](mpcomponent-status.md) \[ MPCOMPONENT \_ MaxValue + 1\]**

</dd> <dd>

Matrice di stati per più componenti. Usare un valore dall'enumerazione [**\_ ID MPCOMPONENT**](mpcomponent-id.md) come indice nella matrice.

</dd> <dt>

**ProductExpirationTime**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

Timestamp scadenza prodotto in UNC. Questa operazione è valida solo se lo stato di scadenza è impostato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ID MPCOMPONENT**](mpcomponent-id.md)
</dt> <dt>

[**\_stato MPCOMPONENT**](mpcomponent-status.md)
</dt> <dt>

[**risultato di MPSCAN \_**](mpscan-result.md)
</dt> <dt>

[**\_flag MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**\_statistiche MPTHREAT**](mpthreat-stats.md)
</dt> <dt>

[**\_dati statistiche \_ MPTHREAT**](mpthreat-stats-data.md)
</dt> </dl>

 

 





