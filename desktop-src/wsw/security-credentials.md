---
title: Credenziali di protezione
description: Le credenziali di sicurezza sono una parte di evidenza che un'entità di comunicazione possiede, che può essere usata per creare o ottenere un token di sicurezza.
ms.assetid: 70e260ce-9e45-436f-b6d1-b650a5c9c0e9
keywords:
- Servizi Web per le credenziali di sicurezza per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0611e6e54fd83e09f811ffddcda4785cef162685
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "106300703"
---
# <a name="security-credentials"></a>Credenziali di protezione

Le credenziali di sicurezza sono una parte di evidenza che un'entità di comunicazione possiede, che può essere usata per creare o ottenere un token di sicurezza. Pertanto, le credenziali sono in genere più longeve dei token di sicurezza e un token di sicurezza può essere visualizzato come la manifestazione di runtime delle credenziali di sicurezza. Esempi di credenziali includono un certificato del computer (che può essere convertito in un token di sicurezza X. 509 in fase di esecuzione) o una coppia nome utente/password per un dominio (che può essere usato per ottenere un token di sicurezza Kerberos).


Le credenziali vengono specificate come parte delle [associazioni di sicurezza](security-bindings.md).

Con le credenziali di sicurezza vengono usati gli elementi API seguenti.

| Callback                                                                  | Descrizione                                              |
|---------------------------------------------------------------------------|----------------------------------------------------------|
| [**CALLBACK di WS \_ get \_ CERT \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)                   | Fornisce un certificato al runtime di sicurezza.          |
| [**\_callback WS Validate \_ password \_**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback) | Convalida una coppia nome utente/password sul lato ricevente. |



 



| Enumerazione                                                                                           | Descrizione                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**\_tipo di \_ credenziale WS CERT \_**](/windows/desktop/api/WebServices/ne-webservices-ws_cert_credential_type)                                         | Tipo di credenziale del certificato.                       |
| [**\_tipo di \_ credenziale WS nomeutente \_**](/windows/desktop/api/WebServices/ne-webservices-ws_username_credential_type)                                 | Tipo di credenziali nome utente/password.                 |
| [**\_tipo di \_ \_ credenziali di autenticazione integrata \_ \_ di WS Windows**](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_credential_type) | Tipo di credenziale di autenticazione integrata di Windows. |



 



| Struttura                                                                                                   | Descrizione                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**\_credenziali WS CERT \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)                                                          | Il tipo di base astratto per tutti i tipi di credenziali del certificato.                                                          |
| [**\_ \_ credenziale certificato personalizzata WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_cert_credential)                                           | Tipo per specificare le credenziali di un certificato che devono essere fornite da un callback all'applicazione.             |
| [**\_credenziali di \_ \_ autenticazione integrata \_ di Windows WS predefinite \_**](/windows/desktop/api/WebServices/ns-webservices-ws_default_windows_integrated_auth_credential) | Digitare per fornire le credenziali di autenticazione integrata di Windows in base al token del thread corrente.                  |
| [**\_credenziali di \_ \_ autenticazione integrata \_ di Windows WS opaco \_**](/windows/desktop/api/WebServices/ns-webservices-ws_opaque_windows_integrated_auth_credential)   | Digitare per fornire le credenziali di autenticazione integrata di Windows.                                                    |
| [**\_ \_ credenziali nome utente WS stringa \_**](/windows/desktop/api/WebServices/ns-webservices-ws_string_username_credential)                                   | Tipo per la fornitura di una coppia nome utente/password come stringhe.                                                           |
| [**\_credenziali di \_ \_ autenticazione integrata \_ di Windows WS String \_**](/windows/desktop/api/WebServices/ns-webservices-ws_string_windows_integrated_auth_credential)   | Digitare per specificare le credenziali di Windows come nome utente, password, stringhe di dominio.                                        |
| [**\_ \_ credenziali certificato del nome del soggetto ws \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_subject_name_cert_credential)                              | Tipo per specificare una credenziale del certificato usando il nome del soggetto, il percorso e il nome dell'archivio del certificato. |
| [**\_credenziali del certificato di identificazione personale ws \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_thumbprint_cert_credential)                                   | Tipo per specificare una credenziale del certificato utilizzando l'identificazione personale del certificato, il percorso dell'archivio e il nome dell'archivio.   |
| [**\_credenziali nome utente WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)                                                  | Il tipo di base astratto per tutte le credenziali nome utente/password.                                                         |
| [**\_credenziali di \_ \_ autenticazione integrata \_ di WS Windows**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)                  | Il tipo di base astratto per tutti i tipi di credenziali utilizzati con l'autenticazione integrata di Windows.                          |



 

 

 




