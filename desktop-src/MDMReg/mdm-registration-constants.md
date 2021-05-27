---
title: Valori degli errori di registrazione MDM (MDMRegistration.h)
description: I valori di errore seguenti si verificano con la registrazione MDM.
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
ms.openlocfilehash: cb62977a48400866e9fa8829696c884e58e54325
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548986"
---
# <a name="mdm-registration-error-values"></a>Valori di errore di registrazione MDM

I valori di errore seguenti si verificano con la registrazione MDM.

<dl> <dt>

<span id="E_DATATYPE_MISMATCH"></span><span id="e_datatype_mismatch"></span>**E \_ DATATYPE \_ MISMATCH**
</dt> <dd> <dl> <dt>

0x8007065d
</dt> <dt>



Il tipo di dati non corrisponde al tipo di dati previsto.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="mregister_e_device_message_format_error"></span>**MREGISTER \_ E \_ DEVICE \_ MESSAGE \_ FORMAT \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190001
</dt> <dt>



Schema non valido, errore di formato del messaggio dal server.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MESSAGE_FORMAT_ERROR"></span><span id="menroll_e_device_message_format_error"></span>**MENROLL \_ E \_ DEVICE \_ MESSAGE \_ FORMAT \_ ERROR**
</dt> <dd> <dl> <dt>

0x80180001
</dt> <dt>



Schema non valido, errore di formato del messaggio dal server.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="mregister_e_device_authentication_error"></span>**ERRORE DI \_ AUTENTICAZIONE DEL DISPOSITIVO MREGISTER \_ \_ \_ E**
</dt> <dd> <dl> <dt>

0x80190002
</dt> <dt>



Il server non è riuscito ad autenticare l'utente.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHENTICATION_ERROR"></span><span id="menroll_e_device_authentication_error"></span>**ERRORE DI AUTENTICAZIONE DI MENROLL \_ E \_ \_ \_ DEVICE**
</dt> <dd> <dl> <dt>

0x80180002
</dt> <dt>



Il server non è riuscito ad autenticare l'utente.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="mregister_e_device_authorization_error"></span>**MREGISTER \_ E \_ DEVICE \_ AUTHORIZATION \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190003
</dt> <dt>



L'utente non è autorizzato a eseguire la registrazione.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_AUTHORIZATION_ERROR"></span><span id="menroll_e_device_authorization_error"></span>**ERRORE DI \_ AUTORIZZAZIONE \_ DEL \_ DISPOSITIVO MENROLL E \_**
</dt> <dd> <dl> <dt>

0x80180003
</dt> <dt>



L'utente non è autorizzato a eseguire la registrazione.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="mregister_e_device_certifcaterequest_error"></span>**ERRORE MREGISTER \_ E \_ DEVICE \_ CERTIFCATEREQUEST \_**
</dt> <dd> <dl> <dt>

0x80190004
</dt> <dt>



L'utente non dispone di alcuna autorizzazione per il modello di certificato o l'autorità di certificazione non è raggiungibile.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CERTIFCATEREQUEST_ERROR"></span><span id="menroll_e_device_certifcaterequest_error"></span>**ERRORE MENROLL \_ E \_ DEVICE \_ CERTIFCATEREQUEST \_**
</dt> <dd> <dl> <dt>

0x80180004
</dt> <dt>



L'utente non dispone di alcuna autorizzazione per il modello di certificato o l'autorità di certificazione non è raggiungibile.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="mregister_e_device_configmgrserver_error"></span>**MREGISTER \_ E \_ DEVICE \_ CONFIGMGRSERVER \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190005
</dt> <dt>



Si è verificato un errore nel server di gestione, ad esempio un errore di accesso al database.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_CONFIGMGRSERVER_ERROR"></span><span id="menroll_e_device_configmgrserver_error"></span>**ERRORE MENROLL \_ E \_ DEVICE \_ CONFIGMGRSERVER \_**
</dt> <dd> <dl> <dt>

0x80180005
</dt> <dt>



Si è verificato un errore nel server di gestione, ad esempio un errore di accesso al database.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="mregister_e_device_internalservice_error"></span>**ERRORE INTERNO DEL DISPOSITIVO MREGISTER \_ \_ \_ \_ E**
</dt> <dd> <dl> <dt>

0x80190006
</dt> <dt>



Si è verificata un'eccezione non gestita nel server.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INTERNALSERVICE_ERROR"></span><span id="menroll_e_device_internalservice_error"></span>**ERRORE INTERNO DEL DISPOSITIVO MENROLL \_ \_ \_ \_ E**
</dt> <dd> <dl> <dt>

0x80180006
</dt> <dt>



Si è verificata un'eccezione non gestita nel server.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="mregister_e_device_invalidsecurity_error"></span>**MREGISTER \_ E \_ DEVICE \_ INVALIDSECURITY \_ ERROR**
</dt> <dd> <dl> <dt>

0x80190007
</dt> <dt>



Si è verificata un'eccezione non gestita nel server.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_INVALIDSECURITY_ERROR"></span><span id="menroll_e_device_invalidsecurity_error"></span>**MENROLL \_ E \_ DEVICE \_ INVALIDSECURITY \_ ERROR**
</dt> <dd> <dl> <dt>

0x80180007
</dt> <dt>



Si è verificata un'eccezione non gestita nel server.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_UNKNOWN_ERROR"></span><span id="mregister_e_device_unknown_error"></span>**ERRORE MREGISTER \_ E \_ DISPOSITIVO \_ \_ SCONOSCIUTO**
</dt> <dd> <dl> <dt>

0x80190008
</dt> <dt>



Errore del server sconosciuto.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_UNKNOWN_ERROR"></span><span id="menroll_e_device_unknown_error"></span>**ERRORE SCONOSCIUTO DEL DISPOSITIVO MENROLL \_ \_ \_ \_ E**
</dt> <dd> <dl> <dt>

0x80180008
</dt> <dt>



Errore del server sconosciuto.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_REGISTRATION_IN_PROGRESS"></span><span id="mregister_e_registration_in_progress"></span>**REGISTRAZIONE \_ DI MREGISTER E \_ \_ IN \_ CORSO**
</dt> <dd> <dl> <dt>

0x80190009
</dt> <dt>



È in corso un'altra operazione di registrazione.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENT_IN_PROGRESS"></span><span id="menroll_e_enrollment_in_progress"></span>**REGISTRAZIONE DI MENROLL \_ E \_ IN \_ \_ CORSO**
</dt> <dd> <dl> <dt>

0x80180009
</dt> <dt>



È in corso un'altra operazione di registrazione.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_ALREADY_REGISTERED"></span><span id="mregister_e_device_already_registered"></span>**MREGISTER \_ E DISPOSITIVO GIÀ \_ \_ \_ REGISTRATO**
</dt> <dd> <dl> <dt>

0x8019000A
</dt> <dt>



Non più utilizzata.

**Windows 8.1:** Il dispositivo è già registrato.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_ALREADY_ENROLLED"></span><span id="menroll_e_device_already_enrolled"></span>**DISPOSITIVO \_ MENROLL E \_ \_ GIÀ \_ REGISTRATO**
</dt> <dd> <dl> <dt>

0x8018000A
</dt> <dt>



Il dispositivo è già registrato.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_REGISTERED"></span><span id="mregister_e_device_not_registered"></span>**MREGISTER \_ E DISPOSITIVO NON \_ \_ \_ REGISTRATO**
</dt> <dd> <dl> <dt>

0x8019000B
</dt> <dt>



Non più utilizzata.

**Windows 8.1:** Il dispositivo non è registrato.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_NOT_ENROLLED"></span><span id="menroll_e_device_not_enrolled"></span>**DISPOSITIVO \_ MENROLL E \_ \_ NON \_ REGISTRATO**
</dt> <dd> <dl> <dt>

0x8018000B
</dt> <dt>



Il dispositivo non è registrato.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_REDIRECTED"></span><span id="mregister_e_discovery_redirected"></span>**MREGISTER \_ E \_ DISCOVERY \_ REDIRECTED**
</dt> <dd> <dl> <dt>

0x8019000C
</dt> <dt>



Non più utilizzata.

**Windows 8.1:** È necessario il reindirizzamento.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DEVICE_NOT_AD_REGISTERED_ERROR"></span><span id="mregister_e_device_not_ad_registered_error"></span>**MREGISTER \_ E \_ DEVICE \_ NOT \_ AD \_ REGISTERED \_ ERROR**
</dt> <dd> <dl> <dt>

0x8019000D
</dt> <dt>



Non più utilizzata.

**Windows 8.1:** Il dispositivo non è registrato con Active Directory.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DISCOVERY_SEC_CERT_DATE_INVALID"></span><span id="menroll_e_discovery_sec_cert_date_invalid"></span>**DATA CERTIFICATO \_ MENROLL E \_ DISCOVERY SEC \_ NON \_ \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

0x8018000D
</dt> <dt>



Durante l'individuazione la data del certificato al secondo non è valida.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_DISCOVERY_FAILED"></span><span id="mregister_e_discovery_failed"></span>**MREGISTER \_ E \_ DISCOVERY \_ FAILED**
</dt> <dd> <dl> <dt>

0x8019000E
</dt> <dt>



Non più utilizzata.

**Windows 8.1:** Individuazione non riuscita. è necessario il reindirizzamento.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PASSWORD_NEEDED"></span><span id="menroll_e_password_needed"></span>**MENROLL \_ E \_ PASSWORD \_ NECESSARIA**
</dt> <dd> <dl> <dt>

0x8018000E
</dt> <dt>



È necessaria una password, ma non è stata specificata.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_WAB_ERROR"></span><span id="menroll_e_wab_error"></span>**ERRORE MENROLL \_ E \_ WAB \_**
</dt> <dd> <dl> <dt>

0x8018000F
</dt> <dt>



Si è verificato un errore durante la registrazione WAB.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CONNECTIVITY"></span><span id="menroll_e_connectivity"></span>**MENROLL \_ E \_ CONNECTIVITY**
</dt> <dd> <dl> <dt>

0x80180010
</dt> <dt>



Si è verificato un errore di rete, ad esempio DNS o un timeout di rete.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_S_ENROLLMENT_SUSPENDED"></span><span id="menroll_s_enrollment_suspended"></span>**REGISTRAZIONE DI MENROLL \_ S \_ \_ SOSPESA**
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

<span id="MENROLL_E_DEVICECAPREACHED"></span><span id="menroll_e_devicecapreached"></span>**MENROLL \_ E \_ DEVICECAPREACHED**
</dt> <dd> <dl> <dt>

0x80180013
</dt> <dt>



L'utente ha già registrato troppi dispositivi. Eliminare o annullare la registrazione di quelli precedenti per correggere l'errore. Si noti che l'utente può risolvere l'errore senza assistenza dell'amministratore.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICENOTSUPPORTED"></span><span id="menroll_e_devicenotsupported"></span>**MENROLL \_ E \_ DEVICENOTSUPPORTED**
</dt> <dd> <dl> <dt>

0x80180014
</dt> <dt>



Una piattaforma o una versione specifica (ad esempio Windows) non è supportata. La correzione generale per questo errore è l'aggiornamento del dispositivo.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_NOTSUPPORTED"></span><span id="menroll_e_notsupported"></span>**MENROLL \_ E \_ NOTSUPPORTED**
</dt> <dd> <dl> <dt>

0x80180015
</dt> <dt>



La gestione dei dispositivi mobili in genere non è supportata per questo dispositivo. L'utente può chiamare l'amministratore, ma è improbabile che risolva il problema.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MREGISTER_E_NOTELIGIBLETORENEW"></span><span id="mregister_e_noteligibletorenew"></span>**MREGISTER \_ E \_ NOTELIGIBLETORENEW**
</dt> <dd> <dl> <dt>

0x80180016
</dt> <dt>



Il dispositivo sta tentando di rinnovare, ma il server ha rifiutato la richiesta. Controllare l'ora nel dispositivo. L'utente potrebbe essere in grado di risolvere l'errore registrando nuovamente.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INMAINTENANCE"></span><span id="menroll_e_inmaintenance"></span>**MENROLL \_ E \_ INMAINTENANCE**
</dt> <dd> <dl> <dt>

0x80180017
</dt> <dt>



L'account è in manutenzione. Riprovare più tardi. L'utente può riprovare in un secondo momento. Tuttavia, l'utente può scegliere di chiamare l'amministratore per determinare la pianificazione della manutenzione.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USERLICENSE"></span><span id="menroll_e_userlicense"></span>**MENROLL \_ E \_ USERLICENSE**
</dt> <dd> <dl> <dt>

0x80180018
</dt> <dt>



La licenza dell'utente è in uno stato non valido che blocca la registrazione. l'utente dovrà chiamare l'amministratore.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_ENROLLMENTDATAINVALID"></span><span id="menroll_e_enrollmentdatainvalid"></span>**MENROLL \_ E \_ ENROLLMENTDATAINVALID**
</dt> <dd> <dl> <dt>

0x80180019
</dt> <dt>



Il server ha rifiutato i dati di registrazione. il server potrebbe non essere configurato correttamente.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_INSECUREREDIRECT"></span><span id="menroll_e_insecureredirect"></span>**MENROLL \_ E \_ INSECUREREDIRECT**
</dt> <dd> <dl> <dt>

0x8018001A
</dt> <dt>



Il server ha richiesto HTTP anziché HTTPS, ma non è stato accettato.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_WRONG_STATE"></span><span id="menroll_e_platform_wrong_state"></span>**STATO \_ ERRATO DELLA PIATTAFORMA MENROLL \_ \_ \_ E**
</dt> <dd> <dl> <dt>

0x8018001B
</dt> <dt>



È stata tentata un'operazione non valida, ad esempio il tentativo di registrare due volte lo stesso dispositivo o annullare la registrazione di un dispositivo sconosciuto.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_LICENSE_ERROR"></span><span id="menroll_e_platform_license_error"></span>**ERRORE DI \_ LICENZA \_ DELLA \_ PIATTAFORMA MENROLL E \_**
</dt> <dd> <dl> <dt>

0x8018001C
</dt> <dt>



La versione di Windows installata nel client non supporta questo tipo di registrazione.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PLATFORM_UNKNOWN_ERROR"></span><span id="menroll_e_platform_unknown_error"></span>**ERRORE SCONOSCIUTO DELLA PIATTAFORMA MENROLL \_ E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x8018001D
</dt> <dt>



Si è verificato un errore sconosciuto nel client.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_CERTSTORE"></span><span id="menroll_e_prov_csp_certstore"></span>**MENROLL \_ E \_ PROV \_ CSP \_ CERTSTORE**
</dt> <dd> <dl> <dt>

0x8018001E
</dt> <dt>



Provisioning non riuscito nel provider di servizi di configurazione dell'archivio certificati.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_W7"></span><span id="menroll_e_prov_csp_w7"></span>**MENROLL \_ E \_ PROV \_ CSP \_ W7**
</dt> <dd> <dl> <dt>

0x8018001F
</dt> <dt>



Provisioning non riuscito in un CPP W7/DMAcc.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_DMCLIENT"></span><span id="menroll_e_prov_csp_dmclient"></span>**MENROLL \_ E \_ PROV \_ CSP \_ DMCLIENT**
</dt> <dd> <dl> <dt>

0x80180020
</dt> <dt>



Provisioning non riuscito in un provider di servizi di configurazione del client di Gestione dei dispositivi.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_PFW"></span><span id="menroll_e_prov_csp_pfw"></span>**MENROLL \_ E \_ PROV \_ CSP \_ PFW**
</dt> <dd> <dl> <dt>

0x80180021
</dt> <dt>



Provisioning non riuscito in un CSP Passport for Work.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_MISC"></span><span id="menroll_e_prov_csp_misc"></span>**MENROLL \_ E \_ PROV \_ CSP \_ MISC**
</dt> <dd> <dl> <dt>

0x80180022
</dt> <dt>



Provisioning non riuscito in un provider di servizi di configurazione non elencato in precedenza.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_UNKNOWN"></span><span id="menroll_e_prov_unknown"></span>**MENROLL \_ E \_ PROV \_ UNKNOWN**
</dt> <dd> <dl> <dt>

0x80180023
</dt> <dt>



Il provisioning non è riuscito, ma non viene indicato un provider di servizi di configurazione specifico.

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_SSLCERTNOTFOUND"></span><span id="menroll_e_prov_sslcertnotfound"></span>**MENROLL \_ E \_ PROV \_ SSLCERTNOTFOUND**
</dt> <dd> <dl> <dt>

0x80180024
</dt> <dt>



Quando si tenta di associare il certificato pubblico o la chiave privata, il certificato pubblico non è stato trovato: durante il tentativo di associare il certificato pubblico o la chiave privata o durante la ricerca del payload di provisioning (ad esempio l'archivio errato).

**Windows 8.1:** Questa costante non è disponibile prima di Windows 10.


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_PROV_CSP_APPMGMT"></span><span id="menroll_e_prov_csp_appmgmt"></span>**MENROLL \_ E \_ PROV \_ CSP \_ APPMGMT**
</dt> <dd> <dl> <dt>

0x80180025
</dt> <dt>



Provisioning non riuscito nel provider di servizi di configurazione EnterpriseAppManagement.

> [!Note]  
> Questa costante non è disponibile prima Windows 10 versione 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_DEVICE_MANAGEMENT_BLOCKED"></span><span id="menroll_e_device_management_blocked"></span>**GESTIONE \_ DEI DISPOSITIVI MENROLL E \_ \_ \_ BLOCCATA**
</dt> <dd> <dl> <dt>

0x80180026
</dt> <dt>



La gestione dei dispositivi mobili (MDM) è stata bloccata, probabilmente Criteri di gruppo o [**dalla funzione SetManagedExternally.**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally)

> [!Note]  
> Questa costante non è disponibile prima Windows 10 versione 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTPOLICY_PRIVATEKEYCREATION_FAILED"></span><span id="menroll_e_certpolicy_privatekeycreation_failed"></span>**MENROLL \_ E \_ CERTPOLICY \_ PRIVATEKEYCREATION \_ FAILED**
</dt> <dd> <dl> <dt>

0x80180027
</dt> <dt>



Impossibile creare la chiave privata.

> [!Note]  
> Questa costante non è disponibile prima Windows 10 versione 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_CERTAUTH_FAILED_TO_FIND_CERT"></span><span id="menroll_e_certauth_failed_to_find_cert"></span>**MENROLL \_ E \_ CERTAUTH \_ NON È RIUSCITO A TROVARE IL \_ \_ \_ CERTIFICATO**
</dt> <dd> <dl> <dt>

0x80180028
</dt> <dt>



È stata richiesta l'autenticazione del certificato, ma non è stato possibile trovare un certificato da usare.

> [!Note]  
> Questa costante non è disponibile prima Windows 10 versione 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_EMPTY_MESSAGE"></span><span id="menroll_e_empty_message"></span>**MENROLL \_ E \_ EMPTY \_ MESSAGE**
</dt> <dd> <dl> <dt>

0x80180029
</dt> <dt>



Il server ha risposto con HTTP 200, ma il messaggio era vuoto.

> [!Note]  
> Questa costante non è disponibile prima Windows 10 versione 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_USER_CANCELED_"></span><span id="menroll_e_user_canceled_"></span>**MENROLL \_ E \_ USER \_ CANCELED** 
</dt> <dd> <dl> <dt>

0x80180030
</dt> <dt>



L'utente ha annullato l'operazione.

> [!Note]  
> Questa costante non è disponibile prima Windows 10 versione 1709.

 


</dt> </dl> </dd> <dt>

<span id="MENROLL_E_MDM_NOT_CONFIGURED"></span><span id="menroll_e_mdm_not_configured"></span>**MENROLL \_ E MDM NON \_ \_ \_ CONFIGURATO**
</dt> <dd> <dl> <dt>

0x80180031
</dt> <dt>



Gestione dei dispositivi mobili (MDM) non è configurata.

> [!Note]  
> Questa costante non è disponibile prima Windows 10 versione 1709.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                    |
| Intestazione<br/>                   | <dl> <dt>MDMRegistration.h</dt> </dl> |



 

 





