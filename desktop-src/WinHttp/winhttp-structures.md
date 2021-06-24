---
description: Questo argomento identifica le strutture utilizzate da WinHTTP.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: Strutture WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9d6f0cdbb467e916b1a6ac54b90491cbee9efdb
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587977"
---
# <a name="winhttp-structures"></a>Strutture WinHTTP

WinHTTP usa le strutture seguenti:

<dl> <dt>

[**HTTP_VERSION_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

Contiene la versione HTTP globale.

</dd> <dt>

[**URL_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

Contiene le parti costituenti di un URL. Questa struttura viene usata con le [**funzioni WinHttpUrl e**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) [**WinHttpCreateUrl.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)

</dd> <dt>

[**WINHTTP_ASYNC_RESULT**](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

Contiene il risultato di una chiamata a una funzione asincrona. Questa struttura viene usata con il [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) prototipo.

</dd> <dt>

[**WINHTTP_AUTOPROXY_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

Usato per indicare alla funzione [**WinHttpGetProxyForURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) se specificare l'URL del file di configurazione automatica del proxy o individuare automaticamente l'URL con query DHCP o DNS per la rete.

</dd> <dt>

[**WINHTTP_CERTIFICATE_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

Contiene le informazioni sul certificato restituite dal server. Questa struttura viene usata dalla [**funzione WinHttpQueryOption.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)

</dd> <dt>

[**WINHTTP_CONNECTION_GROUP**](/windows/win32/api/Winhttp/ns-winhttp-winhttp_connection_group)
</dt> <dd>

Rappresenta un gruppo di connessioni.

</dd> <dt>

[**WINHTTP_CONNECTION_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

Contiene l'indirizzo IP di origine e di destinazione della richiesta che ha generato la risposta.

</dd> <dt>

[**WINHTTP_CREDS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

Contiene le informazioni sulle credenziali utente utilizzate per l'autenticazione del server e del proxy.

> [!Note]
> Questa struttura è stata deprecata. È invece consigliabile usare [**la WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) struttura .

</dd> <dt>

[**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

Contiene le informazioni sulle credenziali utente utilizzate per l'autenticazione del server e del proxy.

</dd> <dt>

[**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

Contiene le informazioni Internet Explorer configurazione del proxy.

</dd> <dt>

[**WINHTTP_HOST_CONNECTION_GROUP**](/windows/win32/api/Winhttp/ns-winhttp-winhttp_host_connection_group)
</dt> <dd>

Rappresenta una raccolta di gruppi di connessioni.

</dd> <dt>

[**WINHTTP_MATCH_CONNECTION_GUID**](/windows/win32/api/Winhttp/ns-winhttp-winhttp_match_connection_group)
</dt> <dd>

Rappresenta il GUID di una connessione, ai fini della corrispondenza della connessione.

</dd> <dt>

[**WINHTTP_PROXY_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

Contiene la configurazione della sessione o del proxy predefinito.

</dd> <dt>

[**WINHTTP_PROXY_RESULT**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

Raccolta di voci dei risultati proxy fornite da [**WinHttpGetProxyResult.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)

</dd> <dt>

[**WINHTTP_PROXY_RESULT_ENTRY**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

Voce del risultato da una chiamata a [**WinHttpGetProxyResult.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)

</dd> <dt>

[**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**](/windows/win32/api/Winhttp/ns-winhttp-winhttp_query_connection_group_result)
</dt> <dd>

Rappresenta una descrizione dello stato corrente delle connessioni di WinHttp.

</dd> <dt>

[**WINHTTP_REQUEST_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

Contiene statistiche per una richiesta.

</dd> <dt>

[**WINHTTP_REQUEST_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

Contiene informazioni sull'intervallo per una richiesta.

</dd> <dt>

[**WINHTTP_SECURITY_INFO**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

Contiene informazioni di connessione e crittografia SChannel per una richiesta.

</dd> <dt>

[**WINHTTP_WEB_SOCKET_ASYNC_RESULT**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

Stato del risultato di un'operazione WebSocket.

</dd> <dt>

[**WINHTTP_WEB_SOCKET_STATUS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

Stato di un'operazione WebSocket.

</dd> </dl>
