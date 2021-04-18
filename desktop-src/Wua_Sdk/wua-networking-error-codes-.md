---
description: 'Altre informazioni su: codici di errore di rete WUA'
ms.assetid: 07ff2ed7-09bc-4af7-84f9-66a921c0f53f
title: Codici di errore di rete WUA (Wuerror. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4fb2c027939afda3fe5817a8a860469fc90b766
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330445"
---
# <a name="wua-networking-error-codes"></a>Codici di errore di rete WUA

L'API dell'agente di Windows Update (WUA) può restituire i codici di errore seguenti durante l'esecuzione di operazioni di rete, ad esempio la ricerca di aggiornamenti:



| Costante/valore                                                                                                                                                                                                                                                                                        | Descrizione                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WU_E_WINHTTP_INVALID_FILE"></span><span id="wu_e_winhttp_invalid_file"></span><dl> <dt>**Wu \_ Il \_ \_ \_ file 0x80240038 E WinHTTP non è valido**</dt> <dt></dt> </dl>                                  | Il file scaricato ha un tipo di contenuto imprevisto.<br/>                                                                                                                               |
| <span id="WU_E_PT_HTTP_STATUS_BAD_REQUEST"></span><span id="wu_e_pt_http_status_bad_request"></span><dl> <dt>**Wu \_ E 0x80244016 di \_ \_ stato http PT \_ \_ \_ richiesta non valida**</dt> <dt></dt> </dl>              | Uguale allo stato HTTP 400: il server non è stato in grado di elaborare la richiesta a causa della sintassi non valida.<br/>                                                                                         |
| <span id="WU_E_PT_HTTP_STATUS_DENIED"></span><span id="wu_e_pt_http_status_denied"></span><dl> <dt>**Wu \_ \_Stato http di E PT \_ \_ \_ negato**</dt> <dt>0x80244017</dt> </dl>                              | Uguale allo stato HTTP 401: la risorsa richiesta richiede l'autenticazione dell'utente.<br/>                                                                                                    |
| <span id="WU_E_PT_HTTP_STATUS_FORBIDDEN"></span><span id="wu_e_pt_http_status_forbidden"></span><dl> <dt>**Wu \_ E \_ \_ \_ lo stato http \_ PT**</dt> non è consentito <dt>0x80244018</dt> </dl>                     | Uguale allo stato HTTP 403: il server ha compreso la richiesta, ma non lo soddisfa.<br/>                                                                                              |
| <span id="WU_E_PT_HTTP_STATUS_NOT_FOUND"></span><span id="wu_e_pt_http_status_not_found"></span><dl> <dt>**Wu \_ \_ \_ Stato http E \_ PT \_ non \_ trovato**</dt> <dt>0x80244019</dt> </dl>                    | Uguale allo stato HTTP 404: il server non è in grado di trovare l'URI richiesto (Uniform Resource Identifier).<br/>                                                                                 |
| <span id="WU_E_PT_HTTP_STATUS_BAD_METHOD"></span><span id="wu_e_pt_http_status_bad_method"></span><dl> <dt>**Wu \_ E il metodo 0x8024401A di \_ \_ stato http PT non \_ \_ valido \_**</dt> <dt></dt> </dl>                 | Uguale allo stato HTTP 405: il metodo HTTP non è consentito.<br/>                                                                                                                         |
| <span id="WU_E_PT_HTTP_STATUS_PROXY_AUTH_REQ"></span><span id="wu_e_pt_http_status_proxy_auth_req"></span><dl> <dt>**Wu \_ E \_ PT \_ http \_ status \_ proxy \_ di \_ autenticazione**</dt> <dt>0x8024401B</dt> </dl>    | Uguale allo stato HTTP 407: è richiesta l'autenticazione proxy.<br/>                                                                                                                       |
| <span id="WU_E_PT_HTTP_STATUS_REQUEST_TIMEOUT"></span><span id="wu_e_pt_http_status_request_timeout"></span><dl> <dt>**Wu \_ E \_ \_ \_ \_ \_ timeout richiesta stato http pt**</dt> <dt>0x8024401C</dt> </dl>  | Uguale allo stato HTTP 408: timeout del server durante l'attesa della richiesta.<br/>                                                                                                           |
| <span id="WU_E_PT_HTTP_STATUS_CONFLICT"></span><span id="wu_e_pt_http_status_conflict"></span><dl> <dt>**Wu \_ 0x8024401D \_ \_ conflitto di \_ stato \_ http E PT**</dt> <dt></dt> </dl>                        | Uguale allo stato HTTP 409: la richiesta non è stata completata a causa di un conflitto con lo stato corrente della risorsa.<br/>                                                                 |
| <span id="WU_E_PT_HTTP_STATUS_GONE"></span><span id="wu_e_pt_http_status_gone"></span><dl> <dt>**Wu \_ \_ \_ \_ Lo stato \_ http di E PT è andato**</dt> <dt>0x8024401E</dt> </dl>                                    | Uguale allo stato HTTP 410: la risorsa richiesta non è più disponibile nel server.<br/>                                                                                                |
| <span id="WU_E_PT_HTTP_STATUS_SERVER_ERROR"></span><span id="wu_e_pt_http_status_server_error"></span><dl> <dt>**Wu \_ 0x8024401F \_ \_ errore del \_ \_ server di \_ stato http E pt**</dt> <dt></dt> </dl>           | Uguale allo stato HTTP 500: un errore interno del server ha impedito di soddisfare la richiesta.<br/>                                                                                       |
| <span id="WU_E_PT_HTTP_STATUS_NOT_SUPPORTED"></span><span id="wu_e_pt_http_status_not_supported"></span><dl> <dt>**Wu \_ \_ \_ Lo stato http di E PT \_ non è \_ \_ supportato**</dt> <dt>0x80244020</dt> </dl>        | Uguale allo stato HTTP 501: il server non supporta la funzionalità necessaria per soddisfare la richiesta. <br/>                                                                             |
| <span id="WU_E_PT_HTTP_STATUS_BAD_GATEWAY"></span><span id="wu_e_pt_http_status_bad_gateway"></span><dl> <dt>**Wu \_ \_Stato http E PT 0x80244021 \_ \_ \_ \_ gateway non valido**</dt> <dt></dt> </dl>              | Uguale allo stato HTTP 502: il server, che funge da gateway o proxy, ha ricevuto una risposta non valida dal server padre a cui ha effettuato l'accesso nel tentativo di completare la richiesta.<br/> |
| <span id="WU_E_PT_HTTP_STATUS_SERVICE_UNAVAIL"></span><span id="wu_e_pt_http_status_service_unavail"></span><dl> <dt>**Wu \_ E \_ \_ servizio di \_ stato \_ \_ http**</dt> <dt>0x80244022</dt> non disponibile </dl>  | Uguale allo stato HTTP 503: il servizio è temporaneamente sovraccarico.<br/>                                                                                                                  |
| <span id="WU_E_PT_HTTP_STATUS_GATEWAY_TIMEOUT"></span><span id="wu_e_pt_http_status_gateway_timeout"></span><dl> <dt>**Wu \_ 0x80244023 \_ \_ \_ \_ \_ timeout gateway di stato http E pt**</dt> <dt></dt> </dl>  | Uguale allo stato HTTP 504: timeout della richiesta durante l'attesa di un gateway.<br/>                                                                                                        |
| <span id="WU_E_PT_HTTP_STATUS_VERSION_NOT_SUP"></span><span id="wu_e_pt_http_status_version_not_sup"></span><dl> <dt>**Wu \_ \_Versione di \_ stato http E PT \_ \_ \_ non \_ sup**</dt> <dt>0x80244024</dt> </dl> | Uguale allo stato HTTP 505: il server non supporta la versione del protocollo HTTP utilizzata per la richiesta.<br/>                                                                             |
| <span id="WU_E_PT_HTTP_STATUS_NOT_MAPPED"></span><span id="wu_e_pt_http_status_not_mapped"></span><dl> <dt>**Wu \_ \_ \_ Stato http E \_ PT \_ non \_ mappato**</dt> <dt>0x8024402B</dt> </dl>                 | Non è stato possibile completare la richiesta e il motivo non corrisponde a nessuno dei codici di \_ errore HTTP di Wu e \_ PT \_ \_ \* .<br/>                                                               |
| <span id="WU_E_PT_WINHTTP_NAME_NOT_RESOLVED"></span><span id="wu_e_pt_winhttp_name_not_resolved"></span><dl> <dt>**Wu \_ E \_ il \_ nome WinHTTP PT \_ \_ non \_**</dt> è stato risolto <dt>0x8024402C</dt> </dl>        | Uguale \_ al nome di errore WinHTTP \_ \_ non \_ risolto. Impossibile risolvere il nome del server proxy o del server di destinazione.<br/>                                                                          |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Wuerror. h</dt> </dl> |



 

 




