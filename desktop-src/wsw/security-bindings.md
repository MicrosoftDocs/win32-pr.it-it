---
title: Associazioni di sicurezza
description: Un'associazione di sicurezza è la specifica di un token di sicurezza e indica al runtime come ottenere e usare un token di sicurezza per la sicurezza del canale.
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- Servizi Web di associazioni di sicurezza per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4afc668e6dc6ab42e2d57066ecfb47ce337603bcadeccfb6b12a14a0e0550381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054541"
---
# <a name="security-bindings"></a>Associazioni di sicurezza

Un'associazione di sicurezza è la specifica di un token di sicurezza e indica al runtime come ottenere e usare un token di sicurezza per la sicurezza del canale. Il token di sicurezza contiene informazioni che garantisce il diritto di accedere alle risorse. Può anche avere una chiave crittografica associata per l'esecuzione di firme e crittografia.


Ogni associazione di sicurezza contiene la propria raccolta di impostazioni di [associazione di](security-binding-settings.md) sicurezza facoltative che hanno come ambito il token di sicurezza definito. Contiene anche le [credenziali di sicurezza](security-credentials.md), che rappresentano l'evidenza di sicurezza (ad esempio nome utente e password o certificati) necessaria per creare i token di sicurezza.

I callback seguenti fanno parte dell'associazione di sicurezza:

-   [**WS \_ VALIDATE \_ SAML \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

Le enumerazioni seguenti fanno parte dell'associazione di sicurezza:

-   [**UTILIZZO DELLA SICUREZZA \_ DEI \_ MESSAGGI WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [**TIPO DI \_ \_ AUTENTICATORE SAML WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [**TIPO DI \_ ASSOCIAZIONE DI \_ SICUREZZA WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [**TIPO DI \_ HANDLE DELLA CHIAVE DI SICUREZZA \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

Le funzioni seguenti fanno parte dell'associazione di sicurezza:

-   [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [**WsFreeSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

Le strutture seguenti fanno parte dell'associazione di sicurezza:

-   [**HANDLE DELLA CHIAVE DI \_ SICUREZZA \_ \_ \_ ASIMMETRICA WS CAPI \_**](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [**AUTENTICATORE SAML FIRMATO DA WS \_ CERT \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [**WS \_ HTTP \_ HEADER \_ AUTH \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [**WS \_ KERBEROS \_ APREQ \_ MESSAGE \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [**WS \_ NAMEDPIPE \_ SSPI \_ TRANSPORT \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**HANDLE DELLA CHIAVE \_ DI SICUREZZA \_ \_ ASIMMETRICA \_ WS NCRYPT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [**HANDLE DI \_ CHIAVE DI \_ SICUREZZA \_ SIMMETRICA WS RAW \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [**AUTENTICATORE \_ SAML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [**WS \_ SAML \_ MESSAGE \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [**ASSOCIAZIONE DI \_ SICUREZZA WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [**WS \_ SECURITY \_ CONTEXT \_ MESSAGE \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [**HANDLE DELLA \_ CHIAVE DI SICUREZZA \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [**WS \_ SSL \_ TRANSPORT \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [**ASSOCIAZIONE DI \_ SICUREZZA \_ DEL TRASPORTO SSPI TCP WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [**WS \_ USERNAME \_ MESSAGE \_ SECURITY \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [**ASSOCIAZIONE DI \_ SICUREZZA WS XML \_ TOKEN \_ \_ MESSAGE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




