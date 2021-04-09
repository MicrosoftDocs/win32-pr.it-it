---
title: Associazioni di sicurezza
description: Un'associazione di sicurezza è la specifica di un token di sicurezza e indica al runtime come ottenere e usare un token di sicurezza per la sicurezza del canale.
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- Associazioni di sicurezza servizi Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a263c1a79212f3438e77c3dca519f6493cf40e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104118670"
---
# <a name="security-bindings"></a>Associazioni di sicurezza

Un'associazione di sicurezza è la specifica di un token di sicurezza e indica al runtime come ottenere e usare un token di sicurezza per la sicurezza del canale. Il token di sicurezza contiene informazioni che giustificano il diritto di accesso alle risorse. Potrebbe inoltre disporre di una chiave crittografica associata per eseguire le firme e la crittografia.


Ogni associazione di sicurezza contiene una raccolta specifica di [impostazioni di associazione di sicurezza](security-binding-settings.md) facoltative che hanno come ambito il token di sicurezza definito. Contiene anche le [credenziali di sicurezza](security-credentials.md), che rappresentano l'evidenza di sicurezza, ad esempio nome utente e password o certificati, necessari per creare i token di sicurezza.

I callback seguenti fanno parte dell'associazione di sicurezza:

-   [**\_ \_ callback SAML WS \_ Validate**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

Le enumerazioni seguenti fanno parte dell'associazione di sicurezza:

-   [**\_utilizzo della \_ sicurezza del messaggio WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [**\_tipo di \_ autenticatore WS SAML \_**](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [**\_tipo di \_ associazione di sicurezza WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [**\_tipo di \_ handle della chiave di sicurezza WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

Le funzioni seguenti fanno parte dell'associazione di sicurezza:

-   [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [**WsFreeSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

Le strutture seguenti fanno parte dell'associazione di sicurezza:

-   [**\_handle della \_ \_ chiave di sicurezza asimmetrica \_ \_ di WS capi**](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [**\_ \_ \_ autenticatore SAML firmato da WS CERT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [**\_binding di \_ sicurezza di autenticazione dell'intestazione WS http \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [**\_binding di \_ \_ sicurezza del messaggio WS Kerberos APREQ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [**BINDING di sicurezza del trasporto di WS \_ NAMEDPIPE \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**\_handle della \_ \_ chiave di sicurezza asimmetrica WS NCRYPT \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [**\_handle di \_ \_ chiave di sicurezza simmetrica WS RAW \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [**\_ \_ autenticatore WS SAML**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [**\_binding di \_ sicurezza del messaggio WS SAML \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [**\_binding di sicurezza WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [**\_associazione di \_ sicurezza del messaggio del contesto di sicurezza WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [**\_handle della \_ chiave di sicurezza WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [**\_binding di \_ sicurezza del trasporto \_ \_ di WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [**\_binding di \_ \_ sicurezza del trasporto SSPI \_ \_ di WS TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [**\_binding di \_ \_ sicurezza messaggio WS nomeutente \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [**\_associazione di \_ sicurezza del messaggio del token WS XML \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




