---
title: Costanti relative a errori e informazioni EAP (Eaphosterror.h)
description: Singoli gruppi di costanti di errore e informazioni correlate a EAP comuni a tutte le tecnologie API EAPHost.
ms.assetid: 081b7a72-abe3-4cbb-9b6c-07bb6717fbfe
topic_type:
- apiref
api_name:
- EAP_E_EAPHOST_FIRST
- EAP_E_EAPHOST_LAST
- EAP_I_EAPHOST_FIRST
- EAP_I_EAPHOST_LAST
- EAP_E_CERT_STORE_INACCESSIBLE
- EAP_E_EAPHOST_METHOD_NOT_INSTALLED
- EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET
- EAP_E_EAPHOST_EAPQEC_INACCESSIBLE
- EAP_E_EAPHOST_IDENTITY_UNKNOWN
- EAP_E_AUTHENTICATION_FAILED
- EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED
- EAP_E_EAPHOST_METHOD_INVALID_PACKET
- EAP_E_EAPHOST_REMOTE_INVALID_PACKET
- EAP_E_EAPHOST_XML_MALFORMED
- EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO
- EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED
- EAP_E_USER_FIRST
- EAP_E_USER_LAST
- EAP_I_USER_FIRST
- EAP_I_USER_LAST
- EAP_E_USER_CERT_NOT_FOUND
- EAP_E_USER_CERT_INVALID
- EAP_E_USER_CERT_EXPIRED
- EAP_E_USER_CERT_REVOKED
- EAP_E_USER_CERT_OTHER_ERROR
- EAP_E_USER_CERT_REJECTED
- EAP_I_USER_ACCOUNT_OTHER_ERROR
- EAP_E_USER_CREDENTIALS_REJECTED
- EAP_E_USER_NAME_PASSWORD_REJECTED
- EAP_E_NO_SMART_CARD_READER
- EAP_E_SERVER_FIRST
- EAP_E_SERVER_LAST
- EAP_E_SERVER_CERT_NOT_FOUND
- EAP_E_SERVER_CERT_INVALID
- EAP_E_SERVER_CERT_EXPIRED
- EAP_E_SERVER_CERT_REVOKED
- EAP_E_SERVER_CERT_OTHER_ERROR
- EAP_E_USER_ROOT_CERT_FIRST
- EAP_E_USER_ROOT_CERT_LAST
- EAP_E_USER_ROOT_CERT_NOT_FOUND
- EAP_E_USER_ROOT_CERT_INVALID
- EAP_E_USER_ROOT_CERT_EXPIRED
- EAP_E_SERVER_ROOT_CERT_FIRST
- EAP_E_SERVER_ROOT_CERT_LAST
- EAP_E_SERVER_ROOT_CERT_NOT_FOUND
- EAP_E_SERVER_ROOT_CERT_INVALID
- EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc4140444d1b5c3ae99c90c2447e165a4143b042dcc7567104e4b5f0063b645b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984241"
---
# <a name="eap-related-error-and-information-constants"></a>Costanti relative a errori e informazioni EAP

Singoli gruppi di costanti di errore e informazioni correlate a EAP comuni a tutte le tecnologie API EAPHost.

<dl> <dt>

<span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**EAP \_ E \_ EAPHOST \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



Definisce il limite delle segnalazioni errori. qualsiasi errore correlato a EAPHost si verificherà tra **EAP \_ \_ EAPHOST \_ FIRST** e **EAP \_ \_ EAP EAPHOST \_ LAST.**


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP \_ E \_ EAPHOST \_ LAST** 
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



Definisce il limite delle segnalazioni errori. qualsiasi errore correlato a EAPHost si verificherà tra **EAP \_ \_ EAPHOST \_ FIRST** e **EAP \_ \_ EAP EAPHOST \_ LAST.**


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP \_ I \_ EAPHOST \_ FIRST** 
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



Definisce il limite dei report di informazioni. qualsiasi registrazione degli eventi in informazioni correlata a EAPHost verrà eseguita tra **EAP \_ I \_ EAPHOST \_ FIRST** e **EAP \_ I \_ EAPHOST \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP \_ I \_ EAPHOST \_ LAST**
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



Definisce il limite dei report di informazioni. qualsiasi registrazione degli eventi in informazioni correlata a EAPHost verrà eseguita tra **EAP \_ I \_ EAPHOST \_ FIRST** e **EAP \_ I \_ EAPHOST \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**ARCHIVIO \_ CERTIFICATI EAP E \_ \_ \_ INACCESSIBILE**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



Né l'autenticatore né il peer possono accedere all'archivio certificati.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**METODO \_ \_ EAP EAPHOST \_ \_ NON \_ INSTALLATO**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



Il metodo EAP richiesto non è installato.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**REIMPOSTAZIONE \_ DELL'HOST DEL METODO \_ EAP EAPHOST \_ THIRDPARTY \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80420012
</dt> <dt>



L'host del metodo di terze parti non risponde ed è stato riavviato automaticamente.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**EAP \_ \_ EAPHOST \_ EAPQEC \_ INACCESSIBILE**
</dt> <dd> <dl> <dt>

0x80420013
</dt> <dt>



EAPHost non è in grado di comunicare con il [](/windows/desktop/NAP/network-access-protection-start-page) [client](/windows/desktop/NAP/nap-client-architecture) di imposizione quarantena EAP (QEC) in un client abilitato per Protezione accesso alla rete.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**IDENTITÀ \_ \_ EAPHOST \_ \_ SCONOSCIUTA**
</dt> <dd> <dl> <dt>

0x80420014
</dt> <dt>



EAPHost restituisce questo errore se l'autenticatore non riesce l'autenticazione dopo l'invio dell'identità peer.


</dt> </dl> </dd> <dt>

<span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**AUTENTICAZIONE \_ EAP E \_ NON \_ RIUSCITA**
</dt> <dd> <dl> <dt>

0x80420015 
</dt> <dt>



EAPHost restituisce questo errore in caso di errore di autenticazione.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**NEGOZIAZIONE \_ \_ EAPHOST \_ EAP IAP NON \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

0x40420016
</dt> <dt>



EAPHost registra questo evento di informazioni quando il client e il server non sono configurati con tipi EAP compatibili.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**PACCHETTO \_ NON \_ VALIDO PER IL METODO EAPHOST \_ EAPHOST \_ \_**
</dt> <dd> <dl> <dt>

0x80420017
</dt> <dt>



Un metodo EAP ha ricevuto un pacchetto EAP che non può essere elaborato. Un altro nome per IL METODO **\_ \_ EAP EAPHOST \_ NON VALIDO \_ \_ PACKET** è **EAP METHOD INVALID \_ \_ \_ PACKET**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**PACCHETTO \_ EAP \_ EAPHOST \_ REMOTO \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

0x80420018
</dt> <dt>



EAPHost ha ricevuto un pacchetto che non può essere elaborato. Un altro nome **per EAP \_ \_ EAP EAPHOST \_ REMOTE INVALID PACKET \_ \_ è** **EAP INVALID \_ \_ PACKET**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**XML \_ \_ EAPHOST \_ EAPHOST \_ IN FORMATO NON VALIDO** 
</dt> <dd> <dl> <dt>

0x80420019
</dt> <dt>



Convalida dello schema di configurazione EAPHost non riuscita.


</dt> </dl> </dd> <dt>

<span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**LA CONFIGURAZIONE \_ DEL METODO EAP \_ NON SUPPORTA \_ \_ \_ \_ \_ L'ACCESSO SSO**
</dt> <dd> <dl> <dt>

0x8042001A
</dt> <dt>



Windows 7 o versione successiva: il metodo EAP non supporta l'accesso Single Sign-On (SSO) per la configurazione fornita.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**OPERAZIONE \_ DEL METODO \_ EAPHOST EAPHOST \_ \_ NON \_ \_ SUPPORTATA**
</dt> <dd> <dl> <dt>

0x80420020
</dt> <dt>



EAPHost restituisce questo errore quando un metodo EAP configurato non supporta un'operazione richiesta (chiamata di procedura).


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**EAP \_ E \_ USER \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420100L
</dt> <dt>



Definisce il limite delle segnalazioni errori. qualsiasi errore correlato all'utente si verificherà tra **EAP \_ E USER \_ \_ FIRST** e **EAP E USER \_ \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**EAP \_ E \_ USER \_ LAST** 
</dt> <dd> <dl> <dt>

0x804201FFL
</dt> <dt>



Definisce il limite delle segnalazioni errori. qualsiasi errore correlato all'utente si verificherà tra **EAP \_ E USER \_ \_ FIRST** e **EAP E USER \_ \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**EAP \_ I \_ USER \_ FIRST**
</dt> <dd> <dl> <dt>

0x40420100L
</dt> <dt>



Definisce il limite dei report di informazioni; qualsiasi registrazione degli eventi in informazioni EAP correlata verrà eseguita tra **EAP \_ I USER \_ \_ FIRST** e **EAP I USER \_ \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**EAP \_ I \_ USER \_ LAST**
</dt> <dd> <dl> <dt>

0x404201FFL
</dt> <dt>



Definisce il limite dei report di informazioni; qualsiasi registrazione degli eventi in informazioni EAP correlata verrà eseguita tra **EAP \_ I USER \_ \_ FIRST** e **EAP I USER \_ \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**CERTIFICATO \_ UTENTE EAP E \_ \_ NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

0x80420100
</dt> <dt>



EAPHost non è stato in grado di trovare un certificato utente per l'autenticazione.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**CERTIFICATO \_ UTENTE EAP \_ \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

0x80420101
</dt> <dt>



Per il certificato utente utilizzato per l'autenticazione non è impostato un utilizzo delle chiavi esteso (EKU) appropriato.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**CERTIFICATO \_ UTENTE EAP E \_ \_ \_ SCADUTO**
</dt> <dd> <dl> <dt>

0x80420102
</dt> <dt>



EAPhost ha trovato un certificato utente scaduto.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**CERTIFICATO \_ UTENTE EAP E \_ \_ \_ REVOCATO**
</dt> <dd> <dl> <dt>

0x80420103
</dt> <dt>



Il certificato utente usato per l'autenticazione è stato revocato.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**EAP \_ E \_ USER \_ CERT \_ OTHER \_ ERROR**
</dt> <dd> <dl> <dt>

0x80420104
</dt> <dt>



Si è verificato un errore sconosciuto con la certificazione utente usata per l'autenticazione.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**CERTIFICATO \_ UTENTE EAP \_ \_ E \_ RIFIUTATO** 
</dt> <dd> <dl> <dt>

0x80420105
</dt> <dt>



L'autenticatore ha rifiutato la certificazione utente.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**EAP \_ I \_ USER \_ ACCOUNT \_ OTHER \_ ERROR**
</dt> <dd> <dl> <dt>

0x40420110
</dt> <dt>



È stato ricevuto un errore EAP dopo uno scambio di identità, che indica la probabilità di un problema con l'account dell'utente di autenticazione.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**CREDENZIALI \_ UTENTE EAP E \_ \_ \_ RIFIUTATE**
</dt> <dd> <dl> <dt>

0x80420111
</dt> <dt>



L'autenticatore ha rifiutato le credenziali utente per l'autenticazione.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**PASSWORD \_ DEL NOME UTENTE EAP \_ E \_ \_ \_ RIFIUTATA**
</dt> <dd> <dl> <dt>

0x80420112
</dt> <dt>



Windows 7 o versione successiva: autenticazione non riuscita. L'autenticatore ha rifiutato le credenziali utente.


</dt> </dl> </dd> <dt>

<span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ E \_ NO \_ SMART \_ CARD \_ READER**
</dt> <dd> <dl> <dt>

0x80420113
</dt> <dt>



Windows 7 o versione successiva: non è stato trovato smart card lettore.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**EAP \_ E \_ SERVER \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420200L
</dt> <dt>



Definisce il limite delle segnalazioni errori. qualsiasi errore correlato al server si verificherà tra **EAP \_ E SERVER \_ \_ FIRST** e **EAP E SERVER \_ \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**EAP \_ E \_ SERVER \_ LAST**
</dt> <dd> <dl> <dt>

0x804202FFL
</dt> <dt>



Definisce il limite delle segnalazioni errori. qualsiasi errore correlato al server si verificherà tra **EAP \_ E SERVER \_ \_ FIRST** e **EAP E SERVER \_ \_ \_ LAST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**CERTIFICATO SERVER EAP \_ \_ E NON \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

0x80420200
</dt> <dt>



EAPHost non è stato in grado di trovare il certificato del server per l'autenticazione.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**CERTIFICATO DEL SERVER EAP \_ \_ E NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

0x80420201
</dt> <dt>



Per il certificato del server utilizzato per l'autenticazione non è impostato un utilizzo chiavi esteso (EKU) appropriato.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**CERTIFICATO SERVER EAP \_ \_ \_ \_ SCADUTO**
</dt> <dd> <dl> <dt>

0x80420202
</dt> <dt>



EAPhost ha rilevato un certificato server scaduto.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**CERTIFICATO SERVER EAP \_ \_ E \_ \_ REVOCATO**
</dt> <dd> <dl> <dt>

0x80420203
</dt> <dt>



Il certificato del server usato per l'autenticazione è stato revocato.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**ALTRO \_ ERRORE DEL \_ CERTIFICATO DEL SERVER \_ \_ \_ EAP E**
</dt> <dd> <dl> <dt>

0x80420204
</dt> <dt>



Si è verificato un errore sconosciuto con il certificato del server.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**EAP \_ E \_ USER \_ ROOT \_ CERT \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420300L
</dt> <dt>



Definisce il limite delle segnalazioni errori. qualsiasi errore correlato al certificato radice dell'utente si verificherà tra **EAP \_ E USER ROOT \_ \_ \_ CERT \_ FIRST** e **EAP E USER ROOT \_ \_ \_ \_ CERT \_ FIRST.**


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**EAP \_ E \_ USER \_ ROOT \_ CERT \_ LAST**
</dt> <dd> <dl> <dt>

0x804203FFL
</dt> <dt>



Definisce il limite delle segnalazioni errori. qualsiasi errore correlato al certificato radice dell'utente si verificherà tra **EAP \_ E USER ROOT \_ \_ \_ CERT \_ FIRST** e **EAP E USER ROOT \_ \_ \_ \_ CERT \_ FIRST.**


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**CERTIFICATO RADICE UTENTE EAP \_ E \_ NON \_ \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

0x80420300
</dt> <dt>



EAPHost non è stato in grado di trovare un certificato in un archivio certificati radice attendibile per la convalida della certificazione utente.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**CERTIFICATO RADICE UTENTE EAP \_ \_ E NON \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

0x80420301
</dt> <dt>



L'autenticazione non è riuscita perché il certificato radice usato per questa rete non è valido.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**CERTIFICATO RADICE UTENTE EAP \_ \_ E \_ \_ \_ SCADUTO**
</dt> <dd> <dl> <dt>

0x80420302
</dt> <dt>



Il certificato radice attendibile necessario per la convalida del certificato utente è scaduto.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**EAP \_ E \_ SERVER \_ ROOT \_ CERT \_ FIRST**
</dt> <dd> <dl> <dt>

0x80420400L
</dt> <dt>



Definisce il limite delle segnalazioni errori. qualsiasi errore correlato al certificato radice del server si verificherà tra **EAP \_ E SERVER \_ ROOT \_ \_ CERT \_ FIRST** **e EAP E SERVER ROOT \_ \_ \_ \_ CERT \_ FIRST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**EAP \_ E \_ SERVER \_ ROOT \_ CERT \_ LAST**
</dt> <dd> <dl> <dt>

0x804204FFL
</dt> <dt>



Definisce il limite delle segnalazioni errori. qualsiasi errore correlato al certificato radice del server si verificherà tra **EAP \_ E SERVER \_ ROOT \_ \_ CERT \_ FIRST** **e EAP E SERVER ROOT \_ \_ \_ \_ CERT \_ FIRST**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**CERTIFICATO RADICE DEL SERVER EAP \_ E \_ NON \_ \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

0x80420400
</dt> <dt>



EAPHost non è stato in grado di trovare un certificato radice in un archivio certificati radice attendibile per la convalida della certificazione server.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**CERTIFICATO RADICE DEL SERVER EAP \_ E \_ NON \_ \_ \_ VALIDO** 
</dt> <dd> <dl> <dt>

0x80420401
</dt> <dt>



L'autenticazione non è riuscita perché il certificato del server necessario per questa rete nel computer server non è valido.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**NOME CERTIFICATO RADICE SERVER EAP \_ \_ \_ \_ \_ \_ EAP OBBLIGATORIO**
</dt> <dd> <dl> <dt>

0x80420406
</dt> <dt>



L'autenticazione non è riuscita perché per il certificato nel computer server non è specificato un nome di server.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Esistono nomi alternativi per determinati errori:

-   Un altro nome per **IL \_ METODO \_ EAP EAPHOST \_ PACCHETTO NON \_ \_ VALIDO** è **METODO EAP PACCHETTO NON \_ \_ \_ VALIDO**.
-   Un altro nome **per EAP \_ \_ EAPHOST \_ REMOTE INVALID \_ \_ PACKET** è **EAP INVALID \_ \_ PACKET**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Eaphosterror.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti EAPHost comuni](common-eap-host-error-constants.md)
</dt> </dl>

 

