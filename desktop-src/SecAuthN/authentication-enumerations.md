---
description: Elenca le enumerazioni usate nelle API di autenticazione.
ms.assetid: e27888e5-d01a-4fdd-8c7d-9849c0f90eb5
title: Enumerazioni di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc42553074b79726c9d1b70bfc6292f4acf44df225fa1f86c7f7a28289ec8ab7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101321"
---
# <a name="authentication-enumerations"></a>Enumerazioni di autenticazione

Le enumerazioni di autenticazione vengono classificate in base all'utilizzo, come indicato di seguito:

-   [Enumerazioni di gestione delle credenziali](#credentials-management-enumerations)
-   [Enumerazioni LSA](#lsa-enumerations)
-   [Enumerazioni del provider di rete](#network-provider-enumerations)
-   [Enumerazioni del provider di supporto per la sicurezza delle credenziali (CredSSP)](#credential-security-support-provider-credssp-enumerations)
-   [Altre enumerazioni](#other-enumerations)

## <a name="credentials-management-enumerations"></a>Enumerazioni di gestione delle credenziali

Gestione credenziali usa le enumerazioni seguenti.



| Enumerazione                                            | Descrizione                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO DI \_ MARSHALLING \_ CRED**](/windows/desktop/api/WinCred/ne-wincred-cred_marshal_type)       | Contiene i tipi di credenziali di cui è possibile effettuare il marshalling [**tramite CredMarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credmarshalcredentiala) o di cui è stato eseguito il unmarshaled [**da CredUnmarshalCredential.**](/windows/desktop/api/WinCred/nf-wincred-credunmarshalcredentiala)<br/> |
| [**TIPO DI \_ PROTEZIONE CRED \_**](/windows/desktop/api/WinCred/ne-wincred-cred_protection_type) | Specifica il contesto di sicurezza in cui vengono crittografate le credenziali quando si usa la [**funzione CredProtect.**](/windows/desktop/api/WinCred/nf-wincred-credprotecta)<br/>                                                                  |



 

## <a name="lsa-enumerations"></a>Enumerazioni LSA

LSA usa le enumerazioni seguenti.



| Enumerazione                                                                                   | Descrizione                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**KERB LOGON SUBMIT TYPE (TIPO DI \_ INVIO ACCESSO KERB) \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_logon_submit_type)                                   | Elenca il tipo di accesso richiesto.<br/>                                                                                                                                                                                                                  |
| [**TIPO DI \_ BUFFER DEL PROFILO \_ \_ KERB**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_profile_buffer_type)                               | Elenca il tipo di profilo di accesso restituito.<br/>                                                                                                                                                                                                                 |
| [**TIPO DI MESSAGGIO \_ DEL \_ PROTOCOLLO \_ KERB**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_protocol_message_type)                           | Elenca i tipi di messaggi che possono essere inviati al pacchetto di autenticazione [*Kerberos*](/windows/desktop/SecGloss/k-gly) chiamando [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).<br/> |
| [**TIPO DI \_ RECORD DI \_ COLLISIONE TRUST TRA \_ \_ FORESTE \_ LSA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_collision_record_type) | Definisce i tipi di collisione che possono verificarsi tra record di trust tra foreste LSA.<br/>                                                                                                                                                                           |
| [**TIPO DI \_ RECORD TRUST TRA \_ \_ FORESTE \_ LSA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_record_type)                      | Definisce il tipo di record di trust tra foreste LSA.<br/>                                                                                                                                                                                                           |
| [**TIPO DI INFORMAZIONI SUL TOKEN LSA \_ \_ \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-lsa_token_information_type)                           | Specifica i livelli di informazioni che possono essere inclusi in un token di accesso.<br/>                                                                                                                                                                                |
| [**MSV1 \_ 0 \_ LOGON \_ SUBMIT \_ TYPE**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_logon_submit_type)                              | Elenca il tipo di accesso richiesto.<br/>                                                                                                                                                                                                                  |
| [**TIPO DI BUFFER DEL PROFILO MSV1 \_ 0 \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_profile_buffer_type)                          | Elenca il tipo di profilo di accesso restituito.<br/>                                                                                                                                                                                                                 |
| [**TIPO DI MESSAGGIO DEL PROTOCOLLO MSV1 \_ 0 \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_protocol_message_type)                      | Elenca i tipi di messaggi che possono essere inviati al pacchetto di autenticazione [MSV1 \_ 0](msv1-0-authentication-package.md) chiamando [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).<br/>                                                 |
| [**CLASSE DI \_ INFORMAZIONI SUL DOMINIO DEI \_ \_ CRITERI**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_domain_information_class)                 | Definisce il tipo di informazioni sul dominio dei criteri.<br/>                                                                                                                                                                                                            |
| [**TIPO \_ DI ACCESSO DI \_ SICUREZZA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-security_logon_type)                                          | Indica il tipo di accesso richiesto da un processo di accesso.<br/>                                                                                                                                                                                                 |



 

## <a name="network-provider-enumerations"></a>Enumerazioni del provider di rete

Il provider di rete usa le enumerazioni seguenti.



| Enumerazione                                                                       | Descrizione                                                                                                                                                                                |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CLASSE DI INFORMAZIONI \_ ESTESE SECPKG \_ \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class) | Tipo di enumerazione che specifica il tipo di informazioni da impostare o ottenere per un [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly).<br/> |
| [**TIPO DI NOME \_ \_ SECPKG**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_name_type)                                    | Valore di enumerazione che specifica il tipo di nome specificato per un account.<br/>                                                                                                     |



 

## <a name="credential-security-support-provider-credssp-enumerations"></a>Enumerazioni credSSP (Credential Security Support Provider)

CredSSP usa le enumerazioni seguenti.



| Enumerazione                                          | Descrizione                                                                                                  |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**TIPO DI INVIO \_ \_ CREDSPP**](/windows/win32/api/credssp/ne-credssp-credspp_submit_type) | Specifica il tipo di credenziali specificato da una [**struttura \_ CRED CRED CREDSSP.**](/windows/desktop/api/Credssp/ns-credssp-credssp_cred)<br/> |



 

## <a name="other-enumerations"></a>Altre enumerazioni

Ecco le altre enumerazioni usate dall'autenticazione.



| Enumerazione                                                   | Descrizione                                                                                                                                                                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TIPO \_ DI IDENTITÀ**](/windows/win32/api/identitycommon/ne-identitycommon-identity_type)                       | Specifica il tipo di identità da enumerare.<br/>                                                                                                                                                                  |
| [**TIPO DI INVIO DI ACCESSO PKU2U \_ \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-pku2u_logon_submit_type) | Indica il tipo di messaggio di accesso passato in una [**struttura PKU2U \_ CERTIFICATE \_ S4U \_ LOGON.**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-pku2u_certificate_s4u_logon)<br/>                                                                                |
| [**SECPKG \_ ATTR \_ LCT \_ STATUS**](/windows/desktop/api/Sspi/ne-sspi-secpkg_attr_lct_status)   | Indica se il token dalla chiamata più recente alla funzione [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) è l'ultimo token del client.<br/>                               |
| [**CLASSE SECPKG \_ CRED \_**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class)              | Indica il tipo di credenziale usato in un contesto client. [**L'enumerazione \_ SECPKG CRED \_ CLASS**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class) viene usata nella [**struttura SecPkgContext \_ CredInfo.**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_credinfo)<br/> |



 

 

