---
title: MPSTATUS_INFO struttura (MpClient.h)
description: Informazioni sullo stato per Malware Protection Manager.
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- MPSTATUS_INFO struttura Legacy Windows Environment Features
- PMPSTATUS_INFO puntatore alla struttura Legacy Windows Environment Features
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
ms.openlocfilehash: 8cb93bd15fe05955c9e8d87828d4b94b08e3d577659c629b52b3f908cb045ba3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883302"
---
# <a name="mpstatus_info-structure"></a>Struttura MPSTATUS \_ INFO

Informazioni sullo stato per Malware Protection Manager.

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

Stato complessivo del prodotto. Si tratta di una combinazione di flag di bit [**da MPSTATUS \_ FLAG**](mpstatus-flag.md).

</dd> <dt>

**LastQuickScan**
</dt> <dd>

Tipo: **[ **MPSCAN \_ RESULT**](mpscan-result.md)**

</dd> <dd>

Risultati dell'ultima analisi da parte di Malware Protection Manager. Vedere [**MPSCAN \_ RESULT**](mpscan-result.md).

</dd> <dt>

**LastFullScan**
</dt> <dd>

Tipo: **[ **MPSCAN \_ RESULT**](mpscan-result.md)**

</dd> <dd>

Risultati dell'ultima analisi completa da parte di Malware Protection Manager. Vedere [**MPSCAN \_ RESULT**](mpscan-result.md).

</dd> <dt>

**ThreatStats**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ STATS**](mpthreat-stats.md)**

</dd> <dd>

Statistiche sulle minacce attive. Vedere [**MPTHREAT \_ STATS**](mpthreat-stats.md).

</dd> <dt>

**ThreatState**
</dt> <dd>

Tipo: **[**MPTHREAT \_ STATS \_ DATA**](mpthreat-stats-data.md) \[ MP THREAT \_ \_ STAT MAX \_ \_ VALUE+1\]**

</dd> <dd>

Dati aggiuntivi sulle statistiche delle minacce, ad esempio il numero di minacce. Vedere [**MPTHREAT \_ STATS \_ DATA**](mpthreat-stats-data.md).

</dd> <dt>

**Componente**
</dt> <dd>

Tipo: **[**MPCOMPONENT \_ STATUS**](mpcomponent-status.md) \[ MPCOMPONENT \_ MAXVALUE+1\]**

</dd> <dd>

Matrice di stati per più componenti. Usare un valore [**dell'enumerazione MPCOMPONENT \_ ID**](mpcomponent-id.md) come indice nella matrice.

</dd> <dt>

**ProductExpirationTime**
</dt> <dd>

Tipo: **ULARGE \_ INTEGER**

</dd> <dd>

Timestamp di scadenza del prodotto in UNC. Questa opzione è valida solo se lo stato di scadenza è impostato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MPCOMPONENT \_ ID**](mpcomponent-id.md)
</dt> <dt>

[**STATO \_ MPCOMPONENT**](mpcomponent-status.md)
</dt> <dt>

[**RISULTATO \_ MPSCAN**](mpscan-result.md)
</dt> <dt>

[**MPSTATUS \_ FLAG**](mpstatus-flag.md)
</dt> <dt>

[**STATISTICHE DI \_ MPTHREAT**](mpthreat-stats.md)
</dt> <dt>

[**DATI DELLE STATISTICHE DI MPTHREAT \_ \_**](mpthreat-stats-data.md)
</dt> </dl>

 

 





