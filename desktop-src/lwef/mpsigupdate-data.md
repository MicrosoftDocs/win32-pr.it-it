---
title: MPSIGUPDATE_DATA (MpClient.h)
description: Dati di notifica passati alla funzione di callback di aggiornamento della firma.
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- MPSIGUPDATE_DATA funzionalità dell'ambiente Windows legacy
- PMPSIGUPDATE_DATA puntatore alla struttura Legacy Windows Environment Features
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
ms.openlocfilehash: d3c117b92882a24a825aee5c5b008e10721c40b8a93d26a9a677bb79858635c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476253"
---
# <a name="mpsigupdate_data-structure"></a>Struttura MPSIGUPDATE \_ DATA

Dati di notifica passati alla funzione di callback di aggiornamento della firma.

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

Stima della percentuale tra tutti gli aggiornamenti scaricati e/o installati.

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

Valore di indice in base zero che specifica quale aggiornamento tra quelli necessari è attualmente in fase di download e/o installazione.

</dd> <dt>

**eType**
</dt> <dd>

Tipo: **MPSIGUPDATE \_ TYPE**

</dd> <dd>

Tipo di aggiornamento. Uno dei valori possibili seguenti:



| Valore                                                                                                                                                                                                                             | Significato                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <dt>**MPSIGUPDATE \_ TYPE \_ NONE**</dt> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <dt>**TIPO MPSIGUPDATE \_ \_ GESTITO**</dt> </dl>                                   | Aggiornamento WSUS. L'annullamento richiede diritti di amministratore.<br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <dt>**MPSIGUPDATE \_ TYPE \_ HTTP**</dt> </dl>                                            | Aggiornamento HTTP. Diritti di amministratore non necessari per l'annullamento.<br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <dt>**MPSIGUPDATE \_ TYPE \_ HTTP \_ SRV**</dt> </dl>                               | HTTP dal servizio. L'annullamento richiede diritti di amministratore.<br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <dt>**TIPO MPSIGUPDATE \_ \_ UNC**</dt> </dl>                                               | Condivisione UNC. Diritti di amministratore non necessari per l'annullamento.<br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <dt>**TIPO MPSIGUPDATE \_ \_ NON GESTITO**</dt> </dl>                             | Aggiornamento MU/WU. L'annullamento richiede diritti di amministratore.<br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <dt>**PIATTAFORMA GESTITA DI TIPO MPSIGUPDATE \_ \_ \_**</dt> </dl>       | Aggiornamento WSUS per PLATFORM. L'annullamento richiede diritti di amministratore.<br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <dt>**PIATTAFORMA NON \_ GESTITA DI TIPO MPSIGUPDATE \_ \_**</dt> </dl> | Aggiornamento mu/WU per PLATFORM. L'annullamento richiede diritti di amministratore.<br/> |



 

</dd> <dt>

**Fase**
</dt> <dd>

Tipo: **MP \_ UPDATE \_ STAGE**

</dd> <dd>

Fase di aggiornamento. Uno dei valori possibili seguenti:



| Valore                                                                                                                                                                         | Significato                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <dt>**MP \_ STAGE \_ UNKNOWN**</dt> </dl>       | Fase di aggiornamento sconosciuta.<br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <dt>**AGGIORNAMENTO \_ DI MP SEARCH \_**</dt> </dl>       | Aggiornare la fase di ricerca.<br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <dt>**AGGIORNAMENTO \_ DEL DOWNLOAD \_ MP**</dt> </dl> | Fase di download dell'aggiornamento.<br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <dt>**MP \_ INSTALL \_ UPDATE**</dt> </dl>    | Fase di installazione dell'aggiornamento.<br/>  |



 

</dd> <dt>

**Percorso**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Percorso di aggiornamento.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





