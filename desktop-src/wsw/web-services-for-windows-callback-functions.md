---
title: Windows Funzioni di callback dei servizi Web
description: I callback consentono a un'applicazione di chiamare una funzione definita a un altro livello o livello.
ms.assetid: 7398ec42-388a-494c-9fe4-5bd62aa009cb
keywords:
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a78bce5c4023d889748af103148088462cb4b267192b1c0b3845fc735fd1bb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926871"
---
# <a name="windows-web-services-callback-functions"></a>Windows Funzioni di callback dei servizi Web

I callback consentono a un'applicazione di chiamare una funzione definita a un altro livello o livello. L'applicazione registra l'argomento della funzione come gestore che deve essere chiamato in modo asincrono in un secondo momento in base alle esigenze. Il callback viene richiamato se la funzione viene completata in modo asincrono indicando l'esito positivo o l'errore della funzione. Il callback non viene chiamato se l'operazione viene completata in modo sincrono.

L Windows aPI dei servizi Web include le funzioni di callback seguenti:

-   [**CALLBACK DEL \_ MESSAGGIO DI \_ ABBANDONO WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)
-   [**CALLBACK DEL \_ CANALE DI \_ INTERRUZIONE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)
-   [**CALLBACK DEL \_ LISTENER DI \_ \_ INTERRUZIONE WS**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**WS \_ ACCEPT \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**CALLBACK \_ ASINCRONO WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
-   [**WS \_ ASYNC \_ FUNCTION**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function)
-   [**CALLBACK DI \_ NOTIFICA \_ DELL'ELENCO DI AUTORITÀ DI \_ \_ CERTIFICAZIONE \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_cert_issuer_list_notification_callback)
-   [**CALLBACK DI \_ CONVALIDA \_ DEL CERTIFICATO \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_certificate_validation_callback)
-   [**WS \_ CLOSE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)
-   [**CALLBACK \_ DEL LISTENER DI \_ CHIUSURA WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**WS \_ CREATE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)
-   [**WS \_ CREATE \_ CHANNEL \_ FOR \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**WS \_ CREATE \_ DECODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)
-   [**WS \_ CREATE \_ ENCODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)
-   [**CALLBACK \_ DI WS CREATE \_ LISTENER \_**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**CALLBACK \_ \_ DECODE DEL DECODIFICATORE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)
-   [**CALLBACK DI FINE DECODIFICATORE WS \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)
-   [**CALLBACK DEL \_ TIPO DI CONTENUTO GET \_ \_ DEL \_ DECODIFICATORE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback)
-   [**CALLBACK DI \_ AVVIO DEL \_ DECODIFICATORE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)
-   [**CALLBACK DI \_ CONFRONTO DELLA \_ DURATA DI WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**CALLBACK DINAMICO \_ \_ DELLE STRINGHE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**CALLBACK DI CODIFICA \_ \_ DEL CODIFICATORE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)
-   [**CALLBACK DI FINE \_ \_ CODIFICATORE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)
-   [**CALLBACK DEL TIPO \_ DI CONTENUTO GET DEL \_ \_ \_ CODIFICATORE \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback)
-   [**CALLBACK DI \_ AVVIO DEL \_ CODIFICATORE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)
-   [**CALLBACK DEL \_ CANALE \_ GRATUITO DI \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)
-   [**CALLBACK DEL \_ \_ DECODIFICATORE LIBERO WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)
-   [**CALLBACK DEL \_ \_ CODIFICATORE GRATUITO WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)
-   [**CALLBACK \_ DEL \_ LISTENER LIBERO DI WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**WS \_ GET \_ CERT \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)
-   [**CALLBACK DELLE \_ PROPRIETÀ DEL CANALE WS \_ GET \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)
-   [**CALLBACK DELLA \_ PROPRIETÀ DEL LISTENER WS GET \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**CALLBACK DI \_ REINDIRIZZAMENTO HTTP WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)
-   [**WS \_ È IL CALLBACK DEL VALORE \_ \_ \_ PREDEFINITO**](/windows/desktop/api/WebServices/nc-webservices-ws_is_default_value_callback)
-   [**CALLBACK DEL \_ MESSAGGIO WS \_ \_ COMPLETATO**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback)
-   [**CALLBACK DI WS \_ OPEN \_ CHANNEL \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)
-   [**CALLBACK DEL LISTENER APERTO WS \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**CALLBACK DI \_ ANNULLAMENTO \_ DELL'OPERAZIONE WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)
-   [**CALLBACK DELLO \_ STATO \_ LIBERO \_ DELL'OPERAZIONE \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback)
-   [**CALLBACK DEL \_ MESSAGGIO \_ PROXY WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback)
-   [**CALLBACK DI WS \_ PULL \_ BYTES \_**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**CALLBACK DI WS \_ PUSH \_ BYTES \_**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**WS \_ READ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)
-   [**WS \_ READ \_ MESSAGE \_ END \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)
-   [**CALLBACK DI \_ AVVIO \_ DEL MESSAGGIO \_ DI \_ WS READ**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)
-   [**CALLBACK DEL \_ TIPO DI \_ LETTURA WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**CALLBACK DEL \_ CANALE WS RESET \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)
-   [**CALLBACK DEL \_ LISTENER WS RESET \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**CALLBACK DEL \_ CANALE \_ DI \_ ACCETTAZIONE DEL SERVIZIO \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback)
-   [**CALLBACK DEL \_ CANALE DI CHIUSURA DEL \_ \_ SERVIZIO \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)
-   [**CALLBACK DI \_ RICEZIONE DEI MESSAGGI DEL \_ \_ SERVIZIO \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**CALLBACK DI \_ SICUREZZA \_ DEL SERVIZIO \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)
-   [**CALLBACK \_ \_ STUB DEL SERVIZIO WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)
-   [**CALLBACK DELLE \_ PROPRIETÀ DEL CANALE WS SET \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)
-   [**CALLBACK DELLA \_ PROPRIETÀ DEL LISTENER WS SET \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)
-   [**CALLBACK DEL CANALE \_ DELLA SESSIONE DI ARRESTO \_ \_ DI \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)
-   [**WS \_ VALIDATE \_ PASSWORD \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback)
-   [**WS \_ VALIDATE \_ SAML \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)
-   [**CALLBACK DI SCRITTURA WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)
-   [**WS \_ WRITE \_ MESSAGE \_ END \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)
-   [**CALLBACK DI \_ AVVIO \_ DEL MESSAGGIO \_ WS WRITE \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)
-   [**CALLBACK DEL \_ TIPO \_ DI SCRITTURA \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

 

 




