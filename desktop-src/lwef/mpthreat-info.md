---
title: Struttura MPTHREAT_INFO (MpClient. h)
description: Contiene informazioni su una minaccia.
ms.assetid: ED2A0BDB-0E7C-479D-ADA1-95B9A259F57E
keywords:
- Struttura MPTHREAT_INFO le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPTHREAT_INFO
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
ms.openlocfilehash: dfa850a4293006a2f4b107a3f2579fdc14c1ea6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478737"
---
# <a name="mpthreat_info-structure"></a>Struttura delle informazioni di MPTHREAT \_

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

Identificatore della minaccia. Il bit superiore è impostato in modo da identificare le minacce correlate all'antivirus.

</dd> <dt>

**DetectionID**
</dt> <dd>

Tipo: **GUID**

</dd> <dd>

ID rilevamento.

</dd> <dt>

**Nome**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Nome della minaccia.

</dd> <dt>

**ThreatType**
</dt> <dd>

Tipo: **[ **MPTHREAT \_**](mpthreat-type.md)**

</dd> <dd>

Tipo di minaccia. Usato per distinguere tra tipi di minacce diversi, ad esempio noti non validi, sconosciuti o noti. Vedere [**MPTHREAT \_ Type**](mpthreat-type.md).

</dd> <dt>

**ThreatCriticality**
</dt> <dd>

Tipo: **[ **\_ gravità MPTHREAT**](mpthreat-severity.md)**

</dd> <dd>

Criticità della minaccia. Vedere [**\_ gravità MPTHREAT**](mpthreat-severity.md).

</dd> <dt>

**ThreatCategory**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ categoria**](mpthreat-category.md)**

</dd> <dd>

Categoria di minacce, ad esempio un Trojan o un keylogger. Vedere [**la \_ categoria MPTHREAT**](mpthreat-category.md).

</dd> <dt>

**ThreatShortDescriptionID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

ID breve della descrizione della minaccia.

</dd> <dt>

**ThreatAdviseDescriptionID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

ID descrizione della notifica di minaccia.

</dd> <dt>

**ThreatStatus**
</dt> <dd>

Tipo: **[ **\_ stato MPTHREAT**](mpthreat-status.md)**

</dd> <dd>

Stato della minaccia, ad esempio rilevato, pulito o in quarantena. Vedere [**\_ lo stato di MPTHREAT**](mpthreat-status.md).

</dd> <dt>

**SuggestedActionCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Conteggio delle azioni suggerite in **SuggestedActionArray**.

</dd> <dt>

**SuggestedActionArray**
</dt> <dd>

Tipo: **[**MPTHREAT \_ Action**](mpthreat-action.md) \[ MP \_ Max \_ suggestions\]**

</dd> <dd>

Matrice di azioni suggerite. Vedere [**\_ azione MPTHREAT**](mpthreat-action.md).

</dd> <dt>

**ResourceCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Numero di risorse in **Resources**.

</dd> <dt>

**ResourceList**
</dt> <dd>

Tipo: **PMPRESOURCE \_ info \** _

</dd> <dd>

Elenco di risorse identificato con la minaccia. Vedere [_ *MPRESOURCE \_ info* *](mpresource-info.md).

</dd> <dt>

**ThreatStatusTime**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

Ora dell'Ultima modifica dello stato della minaccia.

</dd> <dt>

**ThreatStatusCode**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

Codice di stato associato allo stato della minaccia.

</dd> <dt>

**ThreatDetection**
</dt> <dd>

Tipo: **[ **\_ rilevamento MPTHREAT**](mpthreat-detection.md)**

</dd> <dd>

Tipo di rilevamento delle minacce, ad esempio concreto, sospetto o generico. Vedere [**\_ rilevamento MPTHREAT**](mpthreat-detection.md).

</dd> <dt>

**QuarantineGuid**
</dt> <dd>

Tipo: **GUID**

</dd> <dd>

GUID di quarantena.

</dd> <dt>

**ExecutionStatus**
</dt> <dd>

Tipo: **[ **\_ stato MPEXECUTION**](mpexecution-status.md)**

</dd> <dd>

Stato di esecuzione della minaccia, ad esempio non noto, bloccato o attivo. Vedere [**\_ lo stato di MPEXECUTION**](mpexecution-status.md).

</dd> <dt>

**Dati**
</dt> <dd>

Informazioni aggiuntive. Il puntatore alla struttura appropriata dipende dal valore di **ThreatType**.

<dl> <dt>

**pKnownBad**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX non \_ usato**

</dd> <dd>

Quando **ThreatType**  ==  **MPTHREAT \_ digitare \_ KNOWNBAD**. Vedere [**MPTHREAT \_ INFOEX \_ inutilizzato**](mpthreat-infoex-unused.md).

</dd> <dt>

**pBehavior**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ Behavior**

</dd> <dd>

Quando **ThreatType**  ==  **MPTHREAT \_ il \_ comportamento del tipo**. Vedere [**MPTHREAT \_ INFOEX \_ Behavior**](mpthreat-infoex-behavior.md).

</dd> <dt>

**pUnknown**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX non \_ usato**

</dd> <dd>

Quando **ThreatType**  ==  **MPTHREAT \_ tipo \_ sconosciuto**. Vedere [**MPTHREAT \_ INFOEX \_ inutilizzato**](mpthreat-infoex-unused.md).

</dd> <dt>

**pKnownGood**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX non \_ usato**

</dd> <dd>

Quando **ThreatType** = = MPTHREAT \_ \_ , digitare KNOWNGOOD. Vedere [**MPTHREAT \_ INFOEX \_ inutilizzato**](mpthreat-infoex-unused.md).

</dd> <dt>

**pNis**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ NIS**

</dd> <dd>

Quando **ThreatType**  ==  **MPTHREAT \_ digitare \_ NIS**. Vedere [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md).

</dd> </dl> </dd> <dt>

**State**
</dt> <dd>

Tipo: **[ **\_ stato MPDETECTION**](mpdetection-state.md)**

</dd> <dd>

Stato corrente del rilevamento. Vedere [**MPDETECTION \_ state**](mpdetection-state.md).

</dd> <dt>

**DetectionUser**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

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

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Nome del processo associato al rilevamento.

</dd> <dt>

**DetectionOrigin**
</dt> <dd>

Tipo: **[ **MPDETECTION \_ Origin**](mpdetection-origin.md)**

</dd> <dd>

Origine del rilevamento, ad esempio locale o rete. Vedere [**MPDETECTION \_ Origin**](mpdetection-origin.md).

</dd> <dt>

**Reserved1**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Metadati riservati sul rilevamento.

</dd> <dt>

**DetectionTime**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

Ora del rilevamento iniziale.

</dd> <dt>

**PreExecutionStatus**
</dt> <dd>

Tipo: **[ **\_ stato MPEXECUTION**](mpexecution-status.md)**

</dd> <dd>

Stato di esecuzione immediatamente prima della correzione. Vedere [**\_ lo stato di MPEXECUTION**](mpexecution-status.md).

</dd> <dt>

**RemediationTime**
</dt> <dd>

Tipo: **ULARGE \_ Integer**

</dd> <dd>

È stata eseguita la correzione dell'ora.

</dd> <dt>

**PostExecutionStatus**
</dt> <dd>

Tipo: **[ **\_ stato MPEXECUTION**](mpexecution-status.md)**

</dd> <dd>

Stato di esecuzione dopo la correzione. Vedere [**\_ lo stato di MPEXECUTION**](mpexecution-status.md).

</dd> <dt>

**CriticalFailure**
</dt> <dd>

Tipo: **bool**

</dd> <dd>

True se l'errore di correzione è stato critico.

</dd> <dt>

**NonCriticalReason**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Il motivo per cui l'errore di correzione non è critico. Questa operazione non è garantita per essere supportata in futuro.

</dd> <dt>

**RemediationUser**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Utente che ha richiesto la correzione, nel formato "dominio/utente".

</dd> <dt>

**RemediationResourceCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Numero di risorse in **RemediationResourceList**.

</dd> <dt>

**RemediationResourceList**
</dt> <dd>

Tipo: **PMPRESOURCE \_ info \[ RemediationResourceCount \]**

</dd> <dd>

Elenco di risorse non riuscite durante la correzione. Vedere [**MPRESOURCE \_ info**](mpresource-info.md).

</dd> <dt>

**FailureResolved**
</dt> <dd>

Tipo: **bool**

</dd> <dd>

True se l'errore di monitoraggio e aggiornamento è stato risolto. Il bucket verrà spostato in modo da essere completato o da un'altra azione.

</dd> <dt>

**ResolvedReason**
</dt> <dd>

Tipo: **[ **MPRESOLVED \_ reason**](mpresolved-reason.md)**

</dd> <dd>

Motivo per cui è stato risolto un errore di correzione. Questo è il motivo per cui il rilevamento è stato spostato da un'azione non riuscita o completata. Vedere [**MPRESOLVED \_ reason**](mpresolved-reason.md).

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

Aggiuntivi Informazioni sul rilevamento delle minacce.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MpFreeMemory**](mpfreememory.md)
</dt> <dt>

[**MpThreatEnumerate**](mpthreatenumerate.md)
</dt> <dt>

[**MpThreatQuery**](mpthreatquery.md)
</dt> <dt>

[**\_origine MPDETECTION**](mpdetection-origin.md)
</dt> <dt>

[**\_stato MPDETECTION**](mpdetection-state.md)
</dt> <dt>

[**\_stato MPEXECUTION**](mpexecution-status.md)
</dt> <dt>

[**\_motivo MPRESOLVED**](mpresolved-reason.md)
</dt> <dt>

[**\_informazioni MPRESOURCE**](mpresource-info.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**\_azione MPTHREAT**](mpthreat-action.md)
</dt> <dt>

[**\_categoria MPTHREAT**](mpthreat-category.md)
</dt> <dt>

[**\_rilevamento MPTHREAT**](mpthreat-detection.md)
</dt> <dt>

[**\_comportamento INFOEX \_ MPTHREAT**](mpthreat-infoex-behavior.md)
</dt> <dt>

[**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)
</dt> <dt>

[**MPTHREAT \_ INFOEX non \_ usato**](mpthreat-infoex-unused.md)
</dt> <dt>

[**\_gravità MPTHREAT**](mpthreat-severity.md)
</dt> <dt>

[**\_stato MPTHREAT**](mpthreat-status.md)
</dt> <dt>

[**\_tipo MPTHREAT**](mpthreat-type.md)
</dt> </dl>

 

 





