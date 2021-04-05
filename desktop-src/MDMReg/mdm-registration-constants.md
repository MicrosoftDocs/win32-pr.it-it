---
title: Valori degli errori di registrazione MDM (MDMRegistration. h)
description: I seguenti valori di errore sono con la registrazione MDM.
ms.assetid: 1f42ed5e-e221-47ec-a019-ed06c05d55d0
topic_type:
- apiref
api_name:
- E_DATATYPE_MISMATCH
- MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR
- MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR
- MREGISTER_E_DEVICE_AUTHENTICATION_ERROR
- MENROLL_E_DEVICE_AUTHENTICATION_ERROR
- MREGISTER_E_DEVICE_AUTHORIZATION_ERROR
- MENROLL_E_DEVICE_AUTHORIZATION_ERROR
- MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR
- MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR
- MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR
- MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR
- MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR
- MENROLL_E_DEVICE_INTERNALSERVICE_ERROR
- MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR
- MENROLL_E_DEVICE_INVALIDSECURITY_ERROR
- MREGISTER_E_DEVICE_UNKNOWN_ERROR
- MENROLL_E_DEVICE_UNKNOWN_ERROR
- MREGISTER_E_REGISTRATION_IN_PROGRESS
- MENROLL_E_ENROLLMENT_IN_PROGRESS
- MREGISTER_E_DEVICE_ALREADY_REGISTERED
- MENROLL_E_DEVICE_ALREADY_ENROLLED
- MREGISTER_E_DEVICE_NOT_REGISTERED
- MENROLL_E_DEVICE_NOT_ENROLLED
- MREGISTER_E_DISCOVERY_REDIRECTED
- MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR
- MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID
- MREGISTER_E_DISCOVERY_FAILED
- MENROLL_E_PASSWORD_NEEDED
- MENROLL_E_WAB_ERROR
- MENROLL_E_CONNECTIVITY
- MENROLL_S_ENROLLMENT_SUSPENDED
- MENROLL_E_INVALIDSSLCERT
- MENROLL_E_DEVICECAPREACHED
- MENROLL_E_DEVICENOTSUPPORTED
- MENROLL_E_NOTSUPPORTED
- MREGISTER_E_NOTELIGIBLETORENEW
- MENROLL_E_INMAINTENANCE
- MENROLL_E_USERLICENSE
- MENROLL_E_ENROLLMENTDATAINVALID
- MENROLL_E_INSECUREREDIRECT
- MENROLL_E_PLATFORM_WRONG_STATE
- MENROLL_E_PLATFORM_LICENSE_ERROR
- MENROLL_E_PLATFORM_UNKNOWN_ERROR
- MENROLL_E_PROV_CSP_CERTSTORE
- MENROLL_E_PROV_CSP_W7
- MENROLL_E_PROV_CSP_DMCLIENT
- MENROLL_E_PROV_CSP_PFW
- MENROLL_E_PROV_CSP_MISC
- MENROLL_E_PROV_UNKNOWN
- MENROLL_E_PROV_SSLCERTNOTFOUND
- MENROLL_E_PROV_CSP_APPMGMT
- MENROLL_E_DEVICE_MANAGEMENT_BLOCKED
- MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED
- MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT
- MENROLL_E_EMPTY_MESSAGE
- MENROLL_E_USER_CANCELED
- MENROLL_E_MDM_NOT_CONFIGURED
api_location:
- MDMRegistration.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28c21732a102b052d4be51cbbbf5627e42cc487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048442"
---
# <a name="mdm-registration-error-values"></a>Valori degli errori di registrazione MDM

I seguenti valori di errore sono con la registrazione MDM.

<dl> <dt>

<span id="E_DATATYPE_MISMATCH"></span><span id="e_datatype_mismatch"></span>**tipo di dati E non \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

0x8007065d
</dt> <dt>



Il tipo di dati non corrisponde al tipo di dati previsto.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="mregister_e_device_message_format_error"></span>**\_errore di \_ formato del messaggio del dispositivo MREGISTER E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80190001
</dt> <dt>



Schema non valido. errore di formato del messaggio dal server.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="menroll_e_device_message_format_error"></span>**\_errore di \_ formato del messaggio del dispositivo MENROLL E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80180001
</dt> <dt>



Schema non valido. errore di formato del messaggio dal server.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="mregister_e_device_authentication_error"></span>**\_errore di \_ autenticazione del dispositivo E \_ MREGISTER \_**
</dt> <dd> <dl> <dt>

0x80190002
</dt> <dt>



Il server non è riuscito ad autenticare l'utente.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="menroll_e_device_authentication_error"></span>**\_errore di \_ autenticazione del dispositivo E \_ MENROLL \_**
</dt> <dd> <dl> <dt>

0x80180002
</dt> <dt>



Il server non è riuscito ad autenticare l'utente.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="mregister_e_device_authorization_error"></span>**\_errore di \_ \_ autorizzazione dispositivo E MREGISTER \_**
</dt> <dd> <dl> <dt>

0x80190003
</dt> <dt>



L'utente non è autorizzato a eseguire la registrazione.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="menroll_e_device_authorization_error"></span>**\_errore di \_ \_ autorizzazione dispositivo E MENROLL \_**
</dt> <dd> <dl> <dt>

0x80180003
</dt> <dt>



L'utente non è autorizzato a eseguire la registrazione.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="mregister_e_device_certifcaterequest_error"></span>**\_ \_ errore CERTIFCATEREQUEST del dispositivo MREGISTER E \_ \_**
</dt> <dd> <dl> <dt>

0x80190004
</dt> <dt>



L'utente non dispone delle autorizzazioni per il modello di certificato o l'autorità di certificazione non è raggiungibile.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="menroll_e_device_certifcaterequest_error"></span>**\_ \_ errore CERTIFCATEREQUEST del dispositivo MENROLL E \_ \_**
</dt> <dd> <dl> <dt>

0x80180004
</dt> <dt>



L'utente non dispone delle autorizzazioni per il modello di certificato o l'autorità di certificazione non è raggiungibile.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="mregister_e_device_configmgrserver_error"></span>**\_ \_ errore CONFIGMGRSERVER del dispositivo MREGISTER E \_ \_**
</dt> <dd> <dl> <dt>

0x80190005
</dt> <dt>



Si è verificato un errore nel server di gestione, ad esempio un errore di accesso al database.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="menroll_e_device_configmgrserver_error"></span>**\_ \_ errore CONFIGMGRSERVER del dispositivo MENROLL E \_ \_**
</dt> <dd> <dl> <dt>

0x80180005
</dt> <dt>



Si è verificato un errore nel server di gestione, ad esempio un errore di accesso al database.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="mregister_e_device_internalservice_error"></span>**\_ \_ errore INTERNALSERVICE del dispositivo MREGISTER E \_ \_**
</dt> <dd> <dl> <dt>

0x80190006
</dt> <dt>



Si è verificata un'eccezione non gestita nel server.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="menroll_e_device_internalservice_error"></span>**\_ \_ errore INTERNALSERVICE del dispositivo MENROLL E \_ \_**
</dt> <dd> <dl> <dt>

0x80180006
</dt> <dt>



Si è verificata un'eccezione non gestita nel server.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="mregister_e_device_invalidsecurity_error"></span>**\_ \_ errore INVALIDSECURITY del dispositivo MREGISTER E \_ \_**
</dt> <dd> <dl> <dt>

0x80190007
</dt> <dt>



Si è verificata un'eccezione non gestita nel server.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="menroll_e_device_invalidsecurity_error"></span>**\_ \_ errore INVALIDSECURITY del dispositivo MENROLL E \_ \_**
</dt> <dd> <dl> <dt>

0x80180007
</dt> <dt>



Si è verificata un'eccezione non gestita nel server.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_UNKNOWN_ERROR"></span><span id="mregister_e_device_unknown_error"></span>**\_ \_ errore sconosciuto del dispositivo MREGISTER E \_ \_**
</dt> <dd> <dl> <dt>

0x80190008
</dt> <dt>



Errore del server sconosciuto.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_UNKNOWN_ERROR"></span><span id="menroll_e_device_unknown_error"></span>**\_ \_ errore sconosciuto del dispositivo MENROLL E \_ \_**
</dt> <dd> <dl> <dt>

0x80180008
</dt> <dt>



Errore del server sconosciuto.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_REGISTRATION_IN_PROGRESS"></span><span id="mregister_e_registration_in_progress"></span>**\_ \_ registrazione di MREGISTER E \_ in \_ corso**
</dt> <dd> <dl> <dt>

0x80190009
</dt> <dt>



È attualmente in corso un'altra operazione di registrazione.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENT_IN_PROGRESS"></span><span id="menroll_e_enrollment_in_progress"></span>**\_ \_ registrazione di MENROLL E \_ in \_ corso**
</dt> <dd> <dl> <dt>

0x80180009
</dt> <dt>



È attualmente in corso un'altra operazione di registrazione.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_ALREADY_REGISTERED"></span><span id="mregister_e_device_already_registered"></span>**il \_ dispositivo MREGISTER E è \_ \_ già \_ registrato**
</dt> <dd> <dl> <dt>

0x8019000A
</dt> <dt>



Non più utilizzata.

**Windows 8.1:** Il dispositivo è già registrato.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_ALREADY_ENROLLED"></span><span id="menroll_e_device_already_enrolled"></span>**il \_ dispositivo MENROLL E è \_ \_ già \_ registrato**
</dt> <dd> <dl> <dt>

0x8018000A
</dt> <dt>



Il dispositivo è già registrato.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_REGISTERED"></span><span id="mregister_e_device_not_registered"></span>**\_dispositivo MREGISTER \_ E \_ non \_ registrato**
</dt> <dd> <dl> <dt>

0x8019000B
</dt> <dt>



Non più utilizzata.

**Windows 8.1:** Il dispositivo non è registrato.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_NOT_ENROLLED"></span><span id="menroll_e_device_not_enrolled"></span>**\_dispositivo MENROLL \_ E \_ non \_ registrato**
</dt> <dd> <dl> <dt>

0x8018000B
</dt> <dt>



Il dispositivo non è registrato.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_REDIRECTED"></span><span id="mregister_e_discovery_redirected"></span>**MREGISTER \_ E \_ Discovery \_ reindirizzato**
</dt> <dd> <dl> <dt>

0x8019000C
</dt> <dt>



Non più utilizzata.

**Windows 8.1:** È necessario il reindirizzamento.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR"></span><span id="mregister_e_device_not_ad_registered_error"></span>**\_errore registrato del dispositivo MREGISTER E \_ \_ non \_ ad \_ \_**
</dt> <dd> <dl> <dt>

0x8019000D
</dt> <dt>



Non più utilizzata.

**Windows 8.1:** Il dispositivo non è registrato con Active Directory.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID"></span><span id="menroll_e_discovery_sec_cert_date_invalid"></span>**Data del certificato di MENROLL \_ E \_ individuazione \_ sec \_ \_ \_ non valida**
</dt> <dd> <dl> <dt>

0x8018000D
</dt> <dt>



Durante l'individuazione, la data del certificato sec non è valida.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_FAILED"></span><span id="mregister_e_discovery_failed"></span>**\_individuazione MREGISTER \_ E \_ non riuscita**
</dt> <dd> <dl> <dt>

0x8019000E
</dt> <dt>



Non più utilizzata.

**Windows 8.1:** Individuazione non riuscita. è necessario il reindirizzamento.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PASSWORD_NEEDED"></span><span id="menroll_e_password_needed"></span>**MENROLL \_ E \_ password \_ necessari**
</dt> <dd> <dl> <dt>

0x8018000E
</dt> <dt>



È necessaria una password, ma non è stata specificata.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_WAB_ERROR"></span><span id="menroll_e_wab_error"></span>**\_errore MENROLL E \_ WAB \_**
</dt> <dd> <dl> <dt>

0x8018000F
</dt> <dt>



Si è verificato un errore durante la registrazione di WAB.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CONNECTIVITY"></span><span id="menroll_e_connectivity"></span>**connettività di MENROLL \_ E \_**
</dt> <dd> <dl> <dt>

0x80180010
</dt> <dt>



Si è verificato un errore di rete, ad esempio DNS o timeout di rete.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_S_ENROLLMENT_SUSPENDED"></span><span id="menroll_s_enrollment_suspended"></span>**MENROLL \_ S \_ registrazione \_ sospesa**
</dt> <dd> <dl> <dt>

0x00180011
</dt> <dt>



La registrazione è stata sospesa. Non più supportata.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INVALIDSSLCERT"></span><span id="menroll_e_invalidsslcert"></span>**MENROLL \_ E \_ INVALIDSSLCERT**
</dt> <dd> <dl> <dt>

0x80180012
</dt> <dt>



Il certificato SSL non è valido.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICECAPREACHED"></span><span id="menroll_e_devicecapreached"></span>**MENROLL \_ E \_ viene visualizzato**
</dt> <dd> <dl> <dt>

0x80180013
</dt> <dt>



L'utente ha già registrato troppi dispositivi. Eliminare o annullare la registrazione di quelli precedenti per correggere l'errore. Si noti che l'utente può risolvere l'errore senza l'assistenza dell'amministratore.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICENOTSUPPORTED"></span><span id="menroll_e_devicenotsupported"></span>**MENROLL \_ E \_ DEVICENOTSUPPORTED**
</dt> <dd> <dl> <dt>

0x80180014
</dt> <dt>



Una piattaforma specifica (ad esempio Windows) o la versione non è supportata. La correzione generale per questo errore consiste nell'aggiornare il dispositivo.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_NOTSUPPORTED"></span><span id="menroll_e_notsupported"></span>**MENROLL \_ E \_ NotSupported**
</dt> <dd> <dl> <dt>

0x80180015
</dt> <dt>



La gestione dei dispositivi mobili in genere non è supportata per questo dispositivo. l'utente può chiamare l'amministratore, ma è improbabile che il problema venga risolto.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_NOTELIGIBLETORENEW"></span><span id="mregister_e_noteligibletorenew"></span>**MREGISTER \_ E \_ NOTELIGIBLETORENEW**
</dt> <dd> <dl> <dt>

0x80180016
</dt> <dt>



Il dispositivo sta provando a rinnovare, ma il server ha rifiutato la richiesta. Controllare l'ora del dispositivo. L'utente potrebbe essere in grado di risolvere l'errore eseguendo nuovamente la registrazione.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INMAINTENANCE"></span><span id="menroll_e_inmaintenance"></span>**MENROLL \_ E \_ inManutenzione**
</dt> <dd> <dl> <dt>

0x80180017
</dt> <dt>



L'account è in manutenzione; riprovare più tardi. L'utente può riprovare più tardi. Tuttavia, l'utente può scegliere di chiamare l'amministratore per determinare la pianificazione della manutenzione.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USERLICENSE"></span><span id="menroll_e_userlicense"></span>**MENROLL \_ E \_ USERLICENSE**
</dt> <dd> <dl> <dt>

0x80180018
</dt> <dt>



La licenza dell'utente è in uno stato non valido che blocca la registrazione; l'utente dovrà chiamare l'amministratore.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENTDATAINVALID"></span><span id="menroll_e_enrollmentdatainvalid"></span>**MENROLL \_ E \_ ENROLLMENTDATAINVALID**
</dt> <dd> <dl> <dt>

0x80180019
</dt> <dt>



Il server ha rifiutato i dati di registrazione; è possibile che il server non sia configurato correttamente.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INSECUREREDIRECT"></span><span id="menroll_e_insecureredirect"></span>**MENROLL \_ E \_ INSECUREREDIRECT**
</dt> <dd> <dl> <dt>

0x8018001A
</dt> <dt>



Il server ha richiesto HTTP anziché HTTPS, ma non è stato accettato.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_WRONG_STATE"></span><span id="menroll_e_platform_wrong_state"></span>**stato di MENROLL \_ E \_ piattaforma \_ non corretta \_**
</dt> <dd> <dl> <dt>

0x8018001B
</dt> <dt>



Si è tentato di eseguire un'operazione non valida, ad esempio il tentativo di registrare lo stesso dispositivo due volte o annullare la registrazione di un dispositivo sconosciuto.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_LICENSE_ERROR"></span><span id="menroll_e_platform_license_error"></span>**\_errore di \_ licenza della piattaforma MENROLL E \_ \_**
</dt> <dd> <dl> <dt>

0x8018001C
</dt> <dt>



La versione di Windows installata nel client non supporta questo tipo di registrazione.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_UNKNOWN_ERROR"></span><span id="menroll_e_platform_unknown_error"></span>**\_ \_ errore sconosciuto della piattaforma MENROLL E \_ \_**
</dt> <dd> <dl> <dt>

0x8018001D
</dt> <dt>



Si è verificato un errore sconosciuto nel client.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_CERTSTORE"></span><span id="menroll_e_prov_csp_certstore"></span>**MENROLL \_ E \_ prov \_ CSP \_ CERTSTORE**
</dt> <dd> <dl> <dt>

0x8018001E
</dt> <dt>



Il provisioning non è riuscito nell'archivio certificati CSP.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_W7"></span><span id="menroll_e_prov_csp_w7"></span>**MENROLL \_ E \_ prov \_ CSP ( \_ W7)**
</dt> <dd> <dl> <dt>

0x8018001F
</dt> <dt>



Il provisioning non è riuscito in un CPP W7/DMAcc.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_DMCLIENT"></span><span id="menroll_e_prov_csp_dmclient"></span>**MENROLL \_ E \_ prov \_ CSP \_ DMCLIENT**
</dt> <dd> <dl> <dt>

0x80180020
</dt> <dt>



Il provisioning non è riuscito in un CSP client DM.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_PFW"></span><span id="menroll_e_prov_csp_pfw"></span>**MENROLL \_ E \_ prov \_ CSP \_ PFW**
</dt> <dd> <dl> <dt>

0x80180021
</dt> <dt>



Il provisioning non è riuscito in un CSP Passport for work.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_MISC"></span><span id="menroll_e_prov_csp_misc"></span>**MENROLL \_ E \_ prov \_ CSP \_ varie**
</dt> <dd> <dl> <dt>

0x80180022
</dt> <dt>



Il provisioning non è riuscito in un CSP non elencato sopra.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_UNKNOWN"></span><span id="menroll_e_prov_unknown"></span>**MENROLL \_ E \_ prova \_ sconosciuta**
</dt> <dd> <dl> <dt>

0x80180023
</dt> <dt>



Il provisioning non è riuscito, ma non è indicato un CSP specifico.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_SSLCERTNOTFOUND"></span><span id="menroll_e_prov_sslcertnotfound"></span>**MENROLL \_ E \_ prov \_ SSLCERTNOTFOUND**
</dt> <dd> <dl> <dt>

0x80180024
</dt> <dt>



Quando si tenta di associare il certificato pubblico/chiave privata, il certificato pubblico non è stato trovato: quando si tenta di associare il certificato pubblico/chiave privata o quando si cerca il payload del provisioning (probabilmente destinato all'archivio errato).

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_APPMGMT"></span><span id="menroll_e_prov_csp_appmgmt"></span>**MENROLL \_ E \_ prov \_ CSP \_ APPMGMT**
</dt> <dd> <dl> <dt>

0x80180025
</dt> <dt>



Il provisioning non è riuscito in EnterpriseAppManagement CSP.

> [!Note]  
> Questa costante non è disponibile prima di Windows 10, versione 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MANAGEMENT_BLOCKED"></span><span id="menroll_e_device_management_blocked"></span>**\_ \_ gestione dei dispositivi MENROLL E \_ \_ bloccata**
</dt> <dd> <dl> <dt>

0x80180026
</dt> <dt>



La gestione dei dispositivi mobili (MDM) è stata bloccata, probabilmente da Criteri di gruppo o dalla funzione [**SetManagedExternally**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) .

> [!Note]  
> Questa costante non è disponibile prima di Windows 10, versione 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED"></span><span id="menroll_e_certpolicy_privatekeycreation_failed"></span>**MENROLL \_ E \_ CERTPOLICY \_ PRIVATEKEYCREATION \_ non riusciti**
</dt> <dd> <dl> <dt>

0x80180027
</dt> <dt>



Non è stato possibile creare la chiave privata.

> [!Note]  
> Questa costante non è disponibile prima di Windows 10, versione 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT"></span><span id="menroll_e_certauth_failed_to_find_cert"></span>**MENROLL \_ E \_ CERTAUTH \_ non sono riusciti \_ a \_ trovare il \_ certificato**
</dt> <dd> <dl> <dt>

0x80180028
</dt> <dt>



È stata richiesta l'autenticazione del certificato, ma non è stato possibile trovare un certificato da usare.

> [!Note]  
> Questa costante non è disponibile prima di Windows 10, versione 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_EMPTY_MESSAGE"></span><span id="menroll_e_empty_message"></span>**MENROLL \_ E \_ \_ messaggio vuoto**
</dt> <dd> <dl> <dt>

0x80180029
</dt> <dt>



Il server ha risposto con HTTP 200, ma il messaggio è vuoto.

> [!Note]  
> Questa costante non è disponibile prima di Windows 10, versione 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USER_CANCELED_"></span><span id="menroll_e_user_canceled_"></span>**MENROLL \_ E \_ utente \_ annullato** 
</dt> <dd> <dl> <dt>

0x80180030
</dt> <dt>



L'utente ha annullato l'operazione.

> [!Note]  
> Questa costante non è disponibile prima di Windows 10, versione 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_MDM_NOT_CONFIGURED"></span><span id="menroll_e_mdm_not_configured"></span>**MENROLL \_ E \_ MDM \_ non \_ configurati**
</dt> <dd> <dl> <dt>

0x80180031
</dt> <dt>



La gestione di dispositivi mobili (MDM) non è configurata.

> [!Note]  
> Questa costante non è disponibile prima di Windows 10, versione 1709.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                    |
| Intestazione<br/>                   | <dl> <dt>MDMRegistration. h</dt> </dl> |



 

 





