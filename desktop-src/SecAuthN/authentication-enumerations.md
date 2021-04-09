---
description: Elenca le enumerazioni usate nelle API di autenticazione.
ms.assetid: e27888e5-d01a-4fdd-8c7d-9849c0f90eb5
title: Enumerazioni di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5640151967867f610aa8b18c81940c684d23c18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750935"
---
# <a name="authentication-enumerations"></a>Enumerazioni di autenticazione

Le enumerazioni di autenticazione vengono categorizzate in base all'utilizzo come indicato di seguito:

-   [Enumerazioni di gestione delle credenziali](#credentials-management-enumerations)
-   [Enumerazioni LSA](#lsa-enumerations)
-   [Enumerazioni del provider di rete](#network-provider-enumerations)
-   [Enumerazioni CredSSP (Credential Security Support Provider)](#credential-security-support-provider-credssp-enumerations)
-   [Altre enumerazioni](#other-enumerations)

## <a name="credentials-management-enumerations"></a>Enumerazioni di gestione delle credenziali

Gestione credenziali utilizza le enumerazioni seguenti.



| Enumerazione                                            | Descrizione                                                                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tipo di marshalling cred \_**](/windows/desktop/api/WinCred/ne-wincred-cred_marshal_type)       | Contiene i tipi di credenziali che possono essere sottoposti a marshalling da [**CredMarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credmarshalcredentiala) o di cui è stato effettuato l'unmarshalling da [**CredUnmarshalCredential**](/windows/desktop/api/WinCred/nf-wincred-credunmarshalcredentiala).<br/> |
| [**\_tipo di protezione cred \_**](/windows/desktop/api/WinCred/ne-wincred-cred_protection_type) | Specifica il contesto di sicurezza in cui le credenziali vengono crittografate quando si utilizza la funzione [**CredProtect**](/windows/desktop/api/WinCred/nf-wincred-credprotecta) .<br/>                                                                  |



 

## <a name="lsa-enumerations"></a>Enumerazioni LSA

LSA utilizza le enumerazioni seguenti.



| Enumerazione                                                                                   | Descrizione                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_tipo di \_ invio di accesso a cordolo \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_logon_submit_type)                                   | Elenca il tipo di accesso richiesto.<br/>                                                                                                                                                                                                                  |
| [**\_tipo di \_ buffer del profilo marciapiede \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_profile_buffer_type)                               | Elenca il tipo di profilo di accesso restituito.<br/>                                                                                                                                                                                                                 |
| [**\_tipo di \_ messaggio del protocollo marciapiede \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-kerb_protocol_message_type)                           | Elenca i tipi di messaggi che possono essere inviati al pacchetto di autenticazione [*Kerberos*](/windows/desktop/SecGloss/k-gly) chiamando [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).<br/> |
| [**\_tipo di \_ \_ record collisione ATTENDIBILità foresta \_ \_ LSA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_collision_record_type) | Definisce i tipi di collisione che possono verificarsi tra i record di trust tra insiemi di strutture LSA.<br/>                                                                                                                                                                           |
| [**\_tipo di \_ \_ record trust della foresta \_ LSA**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-lsa_forest_trust_record_type)                      | Definisce il tipo di un record di attendibilità della foresta LSA.<br/>                                                                                                                                                                                                           |
| [**\_tipo di \_ informazioni \_ token LSA**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-lsa_token_information_type)                           | Specifica i livelli di informazioni che possono essere inclusi in un token di accesso.<br/>                                                                                                                                                                                |
| [**\_Tipo di \_ \_ invio accesso MSV1 0 \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_logon_submit_type)                              | Elenca il tipo di accesso richiesto.<br/>                                                                                                                                                                                                                  |
| [**\_Tipo di \_ buffer del profilo MSV1 0 \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_profile_buffer_type)                          | Elenca il tipo di profilo di accesso restituito.<br/>                                                                                                                                                                                                                 |
| [**\_Tipo di \_ messaggio del protocollo MSV1 0 \_ \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-msv1_0_protocol_message_type)                      | Elenca i tipi di messaggi che possono essere inviati al [pacchetto di \_ autenticazione MSV1 0](msv1-0-authentication-package.md) chiamando [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage).<br/>                                                 |
| [**\_classe di \_ informazioni sul dominio dei criteri \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-policy_domain_information_class)                 | Definisce il tipo di informazioni sul dominio dei criteri.<br/>                                                                                                                                                                                                            |
| [**\_tipo di accesso di sicurezza \_**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-security_logon_type)                                          | Indica il tipo di accesso richiesto da un processo di accesso.<br/>                                                                                                                                                                                                 |



 

## <a name="network-provider-enumerations"></a>Enumerazioni del provider di rete

Il provider di rete utilizza le enumerazioni seguenti.



| Enumerazione                                                                       | Descrizione                                                                                                                                                                                |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_classe di \_ informazioni ESTESe SECPKG \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_extended_information_class) | Tipo di enumerazione che specifica il tipo di informazioni da impostare o ottenere per un [*pacchetto di sicurezza*](/windows/desktop/SecGloss/s-gly).<br/> |
| [**\_tipo di nome SECPKG \_**](/windows/desktop/api/Ntsecpkg/ne-ntsecpkg-secpkg_name_type)                                    | Valore di enumerazione che specifica il tipo di nome specificato per un account.<br/>                                                                                                     |



 

## <a name="credential-security-support-provider-credssp-enumerations"></a>Enumerazioni CredSSP (Credential Security Support Provider)

CredSSP utilizza le enumerazioni seguenti.



| Enumerazione                                          | Descrizione                                                                                                  |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**\_tipo di invio CREDSPP \_**](/windows/win32/api/credssp/ne-credssp-credspp_submit_type) | Specifica il tipo di credenziali specificato da una struttura [**CredSSP \_ cred**](/windows/desktop/api/Credssp/ns-credssp-credssp_cred) .<br/> |



 

## <a name="other-enumerations"></a>Altre enumerazioni

Di seguito sono riportate le altre enumerazioni utilizzate dall'autenticazione di.



| Enumerazione                                                   | Descrizione                                                                                                                                                                                                                |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**tipo di identità \_**](/windows/win32/api/identitycommon/ne-identitycommon-identity_type)                       | Specifica il tipo di identità da enumerare.<br/>                                                                                                                                                                  |
| [**\_Tipo di \_ INVIO \_ accesso PKU2U**](/windows/desktop/api/Ntsecapi/ne-ntsecapi-pku2u_logon_submit_type) | Indica il tipo di messaggio di accesso passato in una struttura di [**\_ \_ \_ accesso S4U certificate PKU2U**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-pku2u_certificate_s4u_logon) .<br/>                                                                                |
| [**\_stato SECPKG attr \_ LCT \_**](/windows/desktop/api/Sspi/ne-sspi-secpkg_attr_lct_status)   | Indica se il token della chiamata più recente alla funzione [**InitializeSecurityContext**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) è l'ultimo token del client.<br/>                               |
| [**\_classe cred \_ SECPKG**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class)              | Indica il tipo di credenziale usato in un contesto client. L'enumerazione della [**\_ \_ classe cred SECPKG**](/windows/desktop/api/Sspi/ne-sspi-secpkg_cred_class) viene utilizzata nella [**struttura \_ CredInfo di SecPkgContext**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_credinfo) .<br/> |



 

 

