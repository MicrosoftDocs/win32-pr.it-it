---
title: Funzioni di callback dei servizi Web Windows
description: I callback consentono a un'applicazione di chiamare una funzione definita a un livello o a un livello diverso.
ms.assetid: 7398ec42-388a-494c-9fe4-5bd62aa009cb
keywords:
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a385ca21d00e8845f89bda0d9b04221a922ba421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116737"
---
# <a name="windows-web-services-callback-functions"></a>Funzioni di callback dei servizi Web Windows

I callback consentono a un'applicazione di chiamare una funzione definita a un livello o a un livello diverso. L'applicazione registra l'argomento della funzione come un gestore che deve essere chiamato in modo asincrono in un secondo momento, se necessario. Il callback viene richiamato se la funzione viene completata in modo asincrono indicando l'esito positivo o negativo della funzione. Il callback non viene chiamato se l'operazione viene completata in modo sincrono.

L'API per servizi Web Windows include le funzioni di callback seguenti:

-   [**\_callback del \_ messaggio WS Abandon \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)
-   [**\_callback del \_ canale WS Abort \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)
-   [**\_callback del \_ listener WS Abort \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**\_ \_ callback canale WS \_ Accept**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**\_callback asincrono \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
-   [**\_funzione ws Async \_**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function)
-   [**\_callback di \_ notifica dell' \_ elenco delle autorità emittenti \_ WS CERT \_**](/windows/desktop/api/WebServices/nc-webservices-ws_cert_issuer_list_notification_callback)
-   [**\_callback di \_ convalida del certificato WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_certificate_validation_callback)
-   [**\_callback del \_ canale WS Close \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)
-   [**\_callback del \_ listener WS Close \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**\_callback del \_ canale WS create \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)
-   [**WS \_ Crea \_ canale \_ per \_ \_ callback listener**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**CALLBACK di WS \_ Create \_ decoder \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)
-   [**\_callback WS crea \_ codificatore \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)
-   [**\_callback WS crea \_ listener \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**\_callback decodifica \_ decodificatore WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)
-   [**\_callback finale del decodificatore WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)
-   [**\_callback del \_ \_ tipo di contenuto Get del \_ decodificatore WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback)
-   [**\_callback di avvio del decodificatore WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)
-   [**\_callback di \_ confronto \_ durata WS**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**\_ \_ callback stringa dinamica \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**\_ \_ callback codifica WS codificatore \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)
-   [**\_ \_ callback finale WS \_ Encoder**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)
-   [**\_callback del \_ \_ tipo di contenuto Get \_ \_ di WS Encoder**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback)
-   [**\_ \_ callback iniziale WS \_ Encoder**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)
-   [**\_ \_ callback canale libero \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)
-   [**\_callback del \_ decodificatore WS Free \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)
-   [**\_callback del \_ codificatore WS Free \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)
-   [**CALLBACK di WS \_ Free \_ listener \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**CALLBACK di WS \_ get \_ CERT \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)
-   [**\_callback della \_ proprietà del canale WS Get \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)
-   [**\_callback della \_ proprietà del listener WS Get \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**\_callback di \_ Reindirizzamento \_ http ws**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)
-   [**il \_ \_ callback del \_ valore \_ predefinito è WS**](/windows/desktop/api/WebServices/nc-webservices-ws_is_default_value_callback)
-   [**CALLBACK di WS \_ message \_ Done \_**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback)
-   [**CALLBACK di WS \_ Open \_ Channel \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)
-   [**CALLBACK di WS \_ Open \_ listener \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**\_ \_ annullamento callback operazione \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)
-   [**\_ \_ \_ callback dello stato libero dell'operazione WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback)
-   [**\_callback del \_ messaggio WS proxy \_**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback)
-   [**CALLBACK di WS \_ pull \_ byte \_**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**CALLBACK di WS \_ push \_ bytes \_**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**\_callback di lettura WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)
-   [**\_ \_ callback finale del messaggio WS Read \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)
-   [**\_callback di \_ avvio del messaggio WS Read \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)
-   [**\_callback del \_ tipo di lettura WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**\_callback del \_ canale WS Reset \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)
-   [**CALLBACK di WS \_ Reset \_ listener \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**\_ \_ \_ callback canale accettazione servizio \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback)
-   [**\_ \_ \_ callback canale chiusura servizio \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)
-   [**\_ \_ \_ callback ricezione messaggio servizio \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**\_callback di \_ sicurezza del servizio WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)
-   [**\_ \_ callback Stub servizio \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)
-   [**\_callback della \_ proprietà del canale WS set \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)
-   [**\_callback della \_ proprietà del listener set \_ WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)
-   [**\_ \_ \_ callback canale sessione WS \_ Shutdown**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)
-   [**\_callback WS Validate \_ password \_**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback)
-   [**\_ \_ callback SAML WS \_ Validate**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)
-   [**\_callback WS Write \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)
-   [**\_ \_ callback finale del messaggio WS Write \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)
-   [**\_callback di \_ avvio del messaggio WS Write \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)
-   [**\_callback di \_ tipo WS Write \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

 

 




