---
title: Credenziali di protezione
description: Le credenziali di sicurezza sono un elemento di prova che una parte comunicante possiede che può essere usata per creare o ottenere un token di sicurezza.
ms.assetid: 70e260ce-9e45-436f-b6d1-b650a5c9c0e9
keywords:
- Servizi Web credenziali di sicurezza per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f5703d9f58e7fee57f1ce8465e0413a7ca3c246590b816e84f7419e80f6efb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192762"
---
# <a name="security-credentials"></a>Credenziali di protezione

Le credenziali di sicurezza sono un elemento di prova che una parte comunicante possiede che può essere usata per creare o ottenere un token di sicurezza. Di conseguenza, le credenziali hanno in genere una durata più lunga rispetto ai token di sicurezza e un token di sicurezza può essere visualizzato come espressione di runtime delle credenziali di sicurezza. Ad esempio, le credenziali includono un certificato del computer (che può essere convertito in un token di sicurezza X.509 in fase di esecuzione) o una coppia nome utente/password per un dominio (che può essere usata per ottenere un token di sicurezza Kerberos).


Le credenziali vengono specificate come parte delle [associazioni di sicurezza](security-bindings.md).

Gli elementi API seguenti vengono usati con le credenziali di sicurezza.

| Callback                                                                  | Descrizione                                              |
|---------------------------------------------------------------------------|----------------------------------------------------------|
| [**CALLBACK DI WS \_ GET \_ CERT \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)                   | Fornisce un certificato al runtime di sicurezza.          |
| [**CALLBACK DI \_ CONVALIDA \_ DELLA \_ PASSWORD WS**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback) | Convalida una coppia nome utente/password sul lato ricevitore. |



 



| Enumerazione                                                                                           | Descrizione                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**TIPO DI \_ CREDENZIALE DEL \_ CERTIFICATO \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_cert_credential_type)                                         | Tipo di credenziale del certificato.                       |
| [**TIPO DI \_ CREDENZIALE DEL NOME UTENTE \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_username_credential_type)                                 | Tipo di credenziale nome utente/password.                 |
| [**TIPO DI CREDENZIALE DI AUTENTICAZIONE \_ INTEGRATA DI WINDOWS \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_credential_type) | Tipo di credenziale Windows'autenticazione integrata. |



 



| Struttura                                                                                                   | Descrizione                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**CREDENZIALI DEL CERTIFICATO WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)                                                          | Tipo di base astratto per tutti i tipi di credenziali del certificato.                                                          |
| [**CREDENZIALI DEL CERTIFICATO PERSONALIZZATO DI WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_cert_credential)                                           | Tipo per specificare una credenziale del certificato che deve essere fornita da un callback all'applicazione.             |
| [**CREDENZIALI DI AUTENTICAZIONE \_ \_ INTEGRATA DI WINDOWS \_ \_ \_ PREDEFINITE DI WS**](/windows/desktop/api/WebServices/ns-webservices-ws_default_windows_integrated_auth_credential) | Digitare per fornire una credenziale Windows'autenticazione integrata basata sul token del thread corrente.                  |
| [**WS \_ OPAQUE \_ WINDOWS \_ INTEGRATED \_ AUTH \_ CREDENTIAL**](/windows/desktop/api/WebServices/ns-webservices-ws_opaque_windows_integrated_auth_credential)   | Digitare per fornire una credenziale Windows'autenticazione integrata.                                                    |
| [**CREDENZIALI DEL NOME \_ \_ UTENTE DELLA STRINGA WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_string_username_credential)                                   | Tipo per fornire una coppia nome utente/password come stringhe.                                                           |
| [**WS \_ STRING \_ WINDOWS \_ INTEGRATED \_ AUTH \_ CREDENTIAL**](/windows/desktop/api/WebServices/ns-webservices-ws_string_windows_integrated_auth_credential)   | Digitare per fornire una credenziale Windows come nome utente, password e stringhe di dominio.                                        |
| [**CREDENZIALI DEL \_ CERTIFICATO \_ DEL NOME \_ SOGGETTO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_subject_name_cert_credential)                              | Tipo per specificare le credenziali del certificato usando il nome del soggetto, il percorso dell'archivio e il nome dell'archivio del certificato. |
| [**CREDENZIALI CERTIFICATO DI IDENTIFICAZIONE PERSONALE WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_thumbprint_cert_credential)                                   | Tipo per specificare le credenziali del certificato usando l'identificazione personale, il percorso e il nome dell'archivio del certificato.   |
| [**CREDENZIALI DEL NOME UTENTE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)                                                  | Tipo di base astratto per tutte le credenziali di nome utente/password.                                                         |
| [**CREDENZIALI DI \_ AUTENTICAZIONE \_ INTEGRATA \_ DI WINDOWS WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)                  | Tipo di base astratto per tutti i tipi di credenziali usati Windows'autenticazione integrata.                          |



 

 

 




