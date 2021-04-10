---
title: Struttura MPSIGUPDATE_DATA (MpClient. h)
description: Dati di notifica passati alla funzione di callback dell'aggiornamento della firma.
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- Struttura MPSIGUPDATE_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPSIGUPDATE_DATA
topic_type:
- apiref
api_name:
- MPSIGUPDATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442b19da394043b6fc6b8693f51c5f150233f970
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120343"
---
# <a name="mpsigupdate_data-structure"></a>\_Struttura dei dati MPSIGUPDATE

Dati di notifica passati alla funzione di callback dell'aggiornamento della firma.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPSIGUPDATE_DATA {
  DWORD                 dwPercentComplete;
  DWORD                 dwTotalUpdates;
  DWORD                 dwCurrentUpdateIndex;
  MPSIGUPDATE_TYPE      eType;
  MP_UPDATE_STAGE       Stage;
  MP_MIDL_STRING LPWSTR Path;
} MPSIGUPDATE_DATA, *PMPSIGUPDATE_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**dwPercentComplete**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Stima della percentuale in tutti gli aggiornamenti scaricati e/o installati.

</dd> <dt>

**dwTotalUpdates**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Numero totale di aggiornamenti da scaricare e/o installare.

</dd> <dt>

**dwCurrentUpdateIndex**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Valore di indice in base zero che specifica quale aggiornamento tra quelli richiesti è attualmente in fase di download e/o di installazione.

</dd> <dt>

**eType**
</dt> <dd>

Tipo: **MPSIGUPDATE \_**

</dd> <dd>

Tipo di aggiornamento. Uno dei valori possibili seguenti:



| Valore                                                                                                                                                                                                                             | Significato                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <dt>**\_tipo MPSIGUPDATE \_ None**</dt> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <dt>**\_tipo MPSIGUPDATE \_ gestito**</dt> </dl>                                   | Aggiornamento WSUS. Annulla è necessario disporre dei diritti di amministratore.<br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <dt>**MPSIGUPDATE \_ tipo \_ http**</dt> </dl>                                            | Aggiornamento HTTP. Diritti di amministratore non necessari per l'annullamento.<br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <dt>**MPSIGUPDATE \_ digitare \_ http \_ SRV**</dt> </dl>                               | HTTP dal servizio. Annulla è necessario disporre dei diritti di amministratore.<br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <dt>**\_UNC di tipo MPSIGUPDATE \_**</dt> </dl>                                               | Condivisione UNC. Diritti di amministratore non necessari per l'annullamento.<br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <dt>**tipo di MPSIGUPDATE \_ \_ non gestito**</dt> </dl>                             | Aggiornamento di MU/WU. Annulla è necessario disporre dei diritti di amministratore.<br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <dt>**\_ \_ piattaforma gestita di tipo MPSIGUPDATE \_**</dt> </dl>       | Aggiornamento WSUS per la piattaforma. Annulla è necessario disporre dei diritti di amministratore.<br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <dt>**MPSIGUPDATE \_ tipo \_ piattaforma non gestita \_**</dt> </dl> | Aggiornamento di MU/WU per la piattaforma. Annulla è necessario disporre dei diritti di amministratore.<br/> |



 

</dd> <dt>

**Fase**
</dt> <dd>

Tipo: **\_ \_ fase di aggiornamento MP**

</dd> <dd>

Fase di aggiornamento. Uno dei valori possibili seguenti:



| Valore                                                                                                                                                                         | Significato                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <dt>**\_fase MP \_ sconosciuta**</dt> </dl>       | La fase di aggiornamento è sconosciuta.<br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <dt>**\_aggiornamento ricerca \_ MP**</dt> </dl>       | Fase di ricerca dell'aggiornamento.<br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <dt>**\_aggiornamento del download MP \_**</dt> </dl> | Fase di download dell'aggiornamento.<br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <dt>**\_aggiornamento installazione \_ MP**</dt> </dl>    | Aggiornare la fase di installazione.<br/>  |



 

</dd> <dt>

**Percorso**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Percorso di aggiornamento.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





