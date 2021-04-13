---
title: Enumerazione CB_REQUEST_STATUS (Cbclient. h)
description: Specifica lo stato di una richiesta asincrona.
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- Enumerazione CB_REQUEST_STATUS Servizi Desktop remoto
topic_type:
- apiref
api_name:
- CB_REQUEST_STATUS
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd57efd12d3fb5c708d5c4861ee144543bb49f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340533"
---
# <a name="cb_request_status-enumeration"></a>\_ \_ Enumerazione dello stato della richiesta CB

Specifica lo stato di una richiesta asincrona. Questa enumerazione viene utilizzata con il metodo [**IConnectionBrokerRequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef enum _CB_REQUEST_STATUS { 
  CB_STATUS_INVALID                     = 1,
  CB_STATUS_INITIATING_REQUEST          = 0,
  CB_STATUS_REQUEST_COMPLETED,
  CB_STATUS_REQUEST_FAILED,
  CB_STATUS_REQUEST_ABORTED,
  CB_STATUS_FINDING_DESTINATION,
  CB_STATUS_LOADING_DESTINATION,
  CB_STATUS_BRINGING_SESSION_ONLINE,
  CB_STATUS_REDIRECTING_TO_DESTINATION
} CB_REQUEST_STATUS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**\_stato CB \_ non valido**
</dt> <dd>

L'oggetto Request non è inizializzato.

</dd> <dt>

<span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**\_richiesta di \_ avvio stato \_ CB**
</dt> <dd>

Non usato.

</dd> <dt>

<span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**\_richiesta di stato CB \_ \_ completata**
</dt> <dd>

La richiesta è stata completata.

</dd> <dt>

<span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**\_richiesta di stato CB \_ \_ non riuscita**
</dt> <dd>

Richiesta non riuscita.

</dd> <dt>

<span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**\_richiesta di stato CB \_ \_ interrotta**
</dt> <dd>

La richiesta è stata interrotta.

</dd> <dt>

<span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**\_ \_ destinazione ricerca stato \_ CB**
</dt> <dd>

Non usato.

</dd> <dt>

<span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**\_ \_ destinazione caricamento stato \_ CB**
</dt> <dd>

Non usato.

</dd> <dt>

<span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**stato CB che \_ \_ porta la \_ sessione \_ online**
</dt> <dd>

Non usato.

</dd> <dt>

<span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**\_Reindirizzamento stato CB \_ \_ a \_ destinazione**
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IConnectionBrokerRequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 





