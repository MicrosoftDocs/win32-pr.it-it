---
title: MPTHREAT_INFO struttura (MpClient.h)
description: Contiene informazioni su una minaccia.
ms.assetid: ED2A0BDB-0E7C-479D-ADA1-95B9A259F57E
keywords:
- MPTHREAT_INFO struttura Legacy Windows Environment Features
- PMPTHREAT_INFO puntatore alla struttura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPTHREAT_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7be9b1f38a2771d7c6e4831e7716552de34492b30429084f3e087e0a3b49602
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943921"
---
# <a name="mpthreat_info-structure"></a>Struttura MPTHREAT \_ INFO

Contiene informazioni su una minaccia.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPTHREAT_INFO {
  MPTHREAT_ID           ThreatID;
  GUID                  DetectionID;
  MP_MIDL_STRING LPWSTR Name;
  MPTHREAT_TYPE         ThreatType;
  MPTHREAT_SEVERITY     ThreatCriticality;
  MPTHREAT_CATEGORY     ThreatCategory;
  DWORD                 ThreatShortDescriptionID;
  DWORD                 ThreatAdviseDescriptionID;
  MPTHREAT_STATUS       ThreatStatus;
  DWORD                 SuggestedActionCount;
  MPTHREAT_ACTION       SuggestedActionArray[MP_MAX_SUGGESTIONS];
  DWORD                 ResourceCount;
  PMPRESOURCE_INFO      *ResourceList[ResourceCount];
  ULARGE_INTEGER        ThreatStatusTime;
  HRESULT               ThreatStatusCode;
  MPTHREAT_DETECTION    ThreatDetection;
  GUID                  QuarantineGuid;
  MPEXECUTION_STATUS    ExecutionStatus;
  union {
    PMPTHREAT_INFOEX_UNUSED   pKnownBad;
    PMPTHREAT_INFOEX_BEHAVIOR pBehavior;
    PMPTHREAT_INFOEX_UNUSED   pUnknown;
    PMPTHREAT_INFOEX_UNUSED   pKnownGood;
    PMPTHREAT_INFOEX_NIS      pNis;
  } Data;
  MPDETECTION_STATE     State;
  MP_MIDL_STRING LPWSTR DetectionUser;
  MPSOURCE              DetectionSource;
  MP_MIDL_STRING LPWSTR ProcessName;
  MPDETECTION_ORIGIN    DetectionOrigin;
  DWORD                 reserved1;
  ULARGE_INTEGER        DetectionTime;
  MPEXECUTION_STATUS    PreExecutionStatus;
  ULARGE_INTEGER        RemediationTime;
  MPEXECUTION_STATUS    PostExecutionStatus;
  BOOL                  CriticalFailure;
  DWORD                 NonCriticalReason;
  MP_MIDL_STRING LPWSTR RemediationUser;
  DWORD                 RemediationResourceCount;
  PMPRESOURCE_INFO      RemediationResourceList[RemediationResourceCount];
  BOOL                  FailureResolved;
  MPRESOLVED_REASON     ResolvedReason;
  DWORD                 AdditionalActions;
  DWORD                 ResolvedActions;
  DWORD                 dwThreatStatusFlag;
} MPTHREAT_INFO, *PMPTHREAT_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**ThreatID**
</dt> <dd>

Tipo: **MPTHREAT \_ ID**

</dd> <dd>

Identificatore della minaccia. Il bit superiore è impostato per identificare le minacce correlate all'antivirus.

</dd> <dt>

**DetectionID**
</dt> <dd>

Tipo: **GUID**

</dd> <dd>

ID rilevamento.

</dd> <dt>

**Nome**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Nome della minaccia.

</dd> <dt>

**ThreatType**
</dt> <dd>

Tipo: **[ **TIPO MPTHREAT \_**](mpthreat-type.md)**

</dd> <dd>

Tipo di minaccia. Usato per distinguere tra diversi tipi di minaccia, ad esempio quelli noti non validi, sconosciuti o noti. Vedere [**MPTHREAT \_ TYPE**](mpthreat-type.md).

</dd> <dt>

**ThreatCriticality**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ SEVERITY**](mpthreat-severity.md)**

</dd> <dd>

Criticità delle minacce. Vedere [**MPTHREAT \_ SEVERITY**](mpthreat-severity.md).

</dd> <dt>

**ThreatCategory**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ CATEGORY**](mpthreat-category.md)**

</dd> <dd>

Categoria di minacce, ad esempio un trojan o un keylogger. Vedere [**MPTHREAT \_ CATEGORY**](mpthreat-category.md).

</dd> <dt>

**ThreatShortDescriptionID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

ID descrizione breve della minaccia.

</dd> <dt>

**ThreatAdviseDescriptionID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

ID descrizione del consiglio di minaccia.

</dd> <dt>

**ThreatStatus**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ STATUS**](mpthreat-status.md)**

</dd> <dd>

Stato della minaccia, ad esempio rilevato, pulito o messo in quarantena. Vedere [**STATO MPTHREAT \_**](mpthreat-status.md).

</dd> <dt>

**SuggestedActionCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Conteggio delle azioni suggerite in **SuggestedActionArray**.

</dd> <dt>

**SuggestedActionArray**
</dt> <dd>

Tipo: **[**MPTHREAT \_ ACTION**](mpthreat-action.md) \[ MP MAX \_ \_ SUGGESTIONS\]**

</dd> <dd>

Matrice di azioni suggerite. Vedere [**MPTHREAT \_ ACTION**](mpthreat-action.md).

</dd> <dt>

**ResourceCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Conteggio delle risorse in **ResourceList**.

</dd> <dt>

**Elenco risorse**
</dt> <dd>

Tipo: **PMPRESOURCE \_ INFO \***

</dd> <dd>

Elenco di risorse identificate con la minaccia. Vedere [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> <dt>

**ThreatStatusTime**
</dt> <dd>

Tipo: **ULARGE \_ INTEGER**

</dd> <dd>

Ora dell'ultima modifica dello stato della minaccia.

</dd> <dt>

**ThreatStatusCode**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

Codice di stato associato allo stato della minaccia.

</dd> <dt>

**ThreatDetection**
</dt> <dd>

Tipo: **[ **RILEVAMENTO MPTHREAT \_**](mpthreat-detection.md)**

</dd> <dd>

Tipo di rilevamento delle minacce, ad esempio concreto, sospetto o generico. Vedere [**RILEVAMENTO MPTHREAT \_**](mpthreat-detection.md).

</dd> <dt>

**QuarantineGuid**
</dt> <dd>

Tipo: **GUID**

</dd> <dd>

GUID di quarantena.

</dd> <dt>

**ExecutionStatus**
</dt> <dd>

Tipo: **[ **\_ MPEXECUTION STATUS**](mpexecution-status.md)**

</dd> <dd>

Stato di esecuzione della minaccia, ad esempio non noto, bloccato o attivo. Vedere [**STATO \_ MPEXECUTION**](mpexecution-status.md).

</dd> <dt>

**Dati**
</dt> <dd>

Informazioni aggiuntive. Il puntatore alla struttura appropriata dipende dal valore **di ThreatType**.

<dl> <dt>

**pKnownBad**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ UNUSED**

</dd> <dd>

Quando **ThreatType**  ==  **MPTHREAT \_ TYPE \_ KNOWNBAD**. Vedere [**MPTHREAT \_ INFOEX \_ UNUSED**](mpthreat-infoex-unused.md).

</dd> <dt>

**pBehavior**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ BEHAVIOR**

</dd> <dd>

Quando **ThreatType**  ==  **MPTHREAT \_ TYPE \_ BEHAVIOR**. Vedere [**MPTHREAT INFOEX BEHAVIOR ( COMPORTAMENTO DI MPTHREAT \_ \_ INFOEX**](mpthreat-infoex-behavior.md)).

</dd> <dt>

**pUnknown**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ UNUSED**

</dd> <dd>

Quando **ThreatType**  ==  **MPTHREAT \_ TYPE \_ UNKNOWN**. Vedere [**MPTHREAT \_ INFOEX \_ UNUSED**](mpthreat-infoex-unused.md).

</dd> <dt>

**pKnownGood**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ UNUSED**

</dd> <dd>

Quando **ThreatType** == MPTHREAT \_ TYPE \_ KNOWNGOOD. Vedere [**MPTHREAT \_ INFOEX \_ UNUSED**](mpthreat-infoex-unused.md).

</dd> <dt>

**pNis**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ NIS**

</dd> <dd>

Quando **ThreatType**  ==  **MPTHREAT \_ TYPE \_ NIS**. Vedere [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md).

</dd> </dl> </dd> <dt>

**State**
</dt> <dd>

Tipo: **[ **MPDETECTION \_ STATE**](mpdetection-state.md)**

</dd> <dd>

Stato corrente del rilevamento. Vedere [**MPDETECTION \_ STATE**](mpdetection-state.md).

</dd> <dt>

**DetectionUser**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Utente associato al rilevamento, nel formato "dominio/utente".

</dd> <dt>

**DetectionSource**
</dt> <dd>

Tipo: **[ **MPSOURCE**](mpsource.md)**

</dd> <dd>

Origine del rilevamento. Vedere [**MPSOURCE**](mpsource.md).

</dd> <dt>

**ProcessName**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Nome del processo associato al rilevamento.

</dd> <dt>

**DetectionOrigin**
</dt> <dd>

Tipo: **[ **MPDETECTION \_ ORIGIN**](mpdetection-origin.md)**

</dd> <dd>

Origine del rilevamento, ad esempio locale o di rete. Vedere [**MPDETECTION \_ ORIGIN**](mpdetection-origin.md).

</dd> <dt>

**reserved1**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Metadati riservati sul rilevamento.

</dd> <dt>

**DetectionTime**
</dt> <dd>

Tipo: **ULARGE \_ INTEGER**

</dd> <dd>

Ora del rilevamento iniziale.

</dd> <dt>

**PreExecutionStatus**
</dt> <dd>

Tipo: **[ **\_ MPEXECUTION STATUS**](mpexecution-status.md)**

</dd> <dd>

Stato di esecuzione subito prima della correzione. Vedere [**STATO \_ MPEXECUTION**](mpexecution-status.md).

</dd> <dt>

**RemediationTime**
</dt> <dd>

Tipo: **ULARGE \_ INTEGER**

</dd> <dd>

Ora in cui si è verificata la correzione.

</dd> <dt>

**PostExecutionStatus**
</dt> <dd>

Tipo: **[ **\_ MPEXECUTION STATUS**](mpexecution-status.md)**

</dd> <dd>

Stato di esecuzione dopo la correzione. Vedere [**STATO \_ MPEXECUTION**](mpexecution-status.md).

</dd> <dt>

**CriticalFailure**
</dt> <dd>

Tipo: **BOOL**

</dd> <dd>

True se l'errore di correzione era critico.

</dd> <dt>

**NonCriticalReason**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Motivo per cui l'errore di correzione non è critico. Questo non è garantito per essere supportato in futuro.

</dd> <dt>

**RemediationUser**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Utente che ha richiesto la correzione, nel formato "dominio/utente".

</dd> <dt>

**RemediationResourceCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Conteggio delle risorse in **RemediationResourceList**.

</dd> <dt>

**RemediationResourceList**
</dt> <dd>

Tipo: **PMPRESOURCE \_ INFO \[ \] RemediationResourceCount**

</dd> <dd>

Elenco di risorse non riuscite durante la correzione. Vedere [**MPRESOURCE \_ INFO**](mpresource-info.md).

</dd> <dt>

**FailureResolved**
</dt> <dd>

Tipo: **BOOL**

</dd> <dd>

True se l'errore di correzione è stato risolto. In questo modo il bucket verrà spostato in modo da completare o eseguire un'azione aggiuntiva.

</dd> <dt>

**ResolvedReason**
</dt> <dd>

Tipo: **[ **MOTIVO \_ MPRESOLVED**](mpresolved-reason.md)**

</dd> <dd>

Motivo della risoluzione dell'errore di correzione. Questo è il motivo per cui il rilevamento è stato spostato da non riuscito a un'azione aggiuntiva o è stato completato. Vedere [**MPRESOLVED \_ REASON**](mpresolved-reason.md).

</dd> <dt>

**AdditionalActions**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Sono necessarie azioni aggiuntive.

</dd> <dt>

**ResolvedActions**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Eventuali azioni aggiuntive eseguite.

</dd> <dt>

**dwThreatStatusFlag**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Aggiungere informazioni sul rilevamento delle minacce.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MpFreeMemory**](mpfreememory.md)
</dt> <dt>

[**MpThreatEnumerate**](mpthreatenumerate.md)
</dt> <dt>

[**MpThreatQuery**](mpthreatquery.md)
</dt> <dt>

[**ORIGINE MPDETECTION \_**](mpdetection-origin.md)
</dt> <dt>

[**STATO MPDETECTION \_**](mpdetection-state.md)
</dt> <dt>

[**STATO \_ MPEXECUTION**](mpexecution-status.md)
</dt> <dt>

[**MOTIVO \_ MPRESOLVED**](mpresolved-reason.md)
</dt> <dt>

[**INFORMAZIONI SU \_ MPRESOURCE**](mpresource-info.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**AZIONE \_ MPTHREAT**](mpthreat-action.md)
</dt> <dt>

[**CATEGORIA \_ MPTHREAT**](mpthreat-category.md)
</dt> <dt>

[**RILEVAMENTO \_ MPTHREAT**](mpthreat-detection.md)
</dt> <dt>

[**COMPORTAMENTO DI MPTHREAT \_ \_ INFOEX**](mpthreat-infoex-behavior.md)
</dt> <dt>

[**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)
</dt> <dt>

[**MPTHREAT \_ INFOEX \_ NON USATO**](mpthreat-infoex-unused.md)
</dt> <dt>

[**GRAVITÀ \_ MPTHREAT**](mpthreat-severity.md)
</dt> <dt>

[**STATO \_ MPTHREAT**](mpthreat-status.md)
</dt> <dt>

[**TIPO \_ MPTHREAT**](mpthreat-type.md)
</dt> </dl>

 

 





