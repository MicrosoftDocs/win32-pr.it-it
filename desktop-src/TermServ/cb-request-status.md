---
title: CB_REQUEST_STATUS enumerazione (Cbclient.h)
description: Specifica lo stato di una richiesta asincrona.
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- CB_REQUEST_STATUS enumerazione Servizi Desktop remoto
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
ms.openlocfilehash: d6647f10ab91fd5cb1919d49c4c00d22b8b1722de9b20d9b83fdee8fcceaef95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871971"
---
# <a name="cb_request_status-enumeration"></a>Enumerazione CB \_ REQUEST \_ STATUS

Specifica lo stato di una richiesta asincrona. Questa enumerazione viene usata con il [**metodo IConnectionBrokerRequest::CheckStatus.**](iconnectionbrokerrequest-checkstatus.md)

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

<span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**STATO CB \_ \_ NON VALIDO**
</dt> <dd>

L'oggetto richiesta non è inizializzato.

</dd> <dt>

<span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**STATO CB \_ \_ CHE AVVIA LA \_ RICHIESTA**
</dt> <dd>

Non usato.

</dd> <dt>

<span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**RICHIESTA DI \_ STATO CB \_ \_ COMPLETATA**
</dt> <dd>

La richiesta è stata completata.

</dd> <dt>

<span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**RICHIESTA DI STATO CB \_ \_ NON \_ RIUSCITA**
</dt> <dd>

Richiesta non riuscita.

</dd> <dt>

<span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**RICHIESTA DI \_ STATO CB \_ \_ INTERROTTA**
</dt> <dd>

La richiesta è stata interrotta.

</dd> <dt>

<span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**DESTINAZIONE DI RICERCA DELLO STATO CB \_ \_ \_**
</dt> <dd>

Non usato.

</dd> <dt>

<span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**DESTINAZIONE DI CARICAMENTO \_ DELLO \_ STATO \_ CB**
</dt> <dd>

Non usato.

</dd> <dt>

<span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**STATO CB \_ PORTARE \_ ONLINE LA \_ \_ SESSIONE**
</dt> <dd>

Non usato.

</dd> <dt>

<span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**STATO CB \_ \_ REINDIRIZZAMENTO \_ ALLA \_ DESTINAZIONE**
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Cbclient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 





