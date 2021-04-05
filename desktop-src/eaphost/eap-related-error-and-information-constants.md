---
title: Costanti di errore e informazioni correlate a EAP (Eaphosterror. h)
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
ms.openlocfilehash: 8bd7b829cd4c5ba550fd88242ffb8c34572648d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048454"
---
# <a name="eap-related-error-and-information-constants"></a>Costanti di errore e informazioni correlate a EAP

Singoli gruppi di costanti di errore e informazioni correlate a EAP comuni a tutte le tecnologie API EAPHost.

<dl> <dt>

<span id="EAP_E_EAPHOST_FIRST"></span><span id="eap_e_eaphost_first"></span>**\_prima EAP E \_ EAPHost \_**
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



Definisce il limite dei report di errore. si verificherà un errore relativo a EAPHost tra **EAP e \_ \_ EAPHost \_ prima** e **EAP e EAPHost per \_ \_ \_ ultimo**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_LAST___"></span><span id="eap_e_eaphost_last___"></span>**EAP \_ E \_ EAPHOST per \_ ultimi** 
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



Definisce il limite dei report di errore. si verificherà un errore relativo a EAPHost tra **EAP e \_ \_ EAPHost \_ prima** e **EAP e EAPHost per \_ \_ \_ ultimo**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_FIRST_"></span><span id="eap_i_eaphost_first_"></span>**EAP \_ I \_ EAPHost \_ prima** 
</dt> <dd> <dl> <dt>

0x80420000L
</dt> <dt>



Definisce il limite dei report informazioni; eventuali registrazioni di eventi informativi correlati a EAPHost si verificheranno **prima tra EAP \_ i \_ EAPHost \_** e **EAP \_ i \_ EAPHost \_**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_LAST"></span><span id="eap_i_eaphost_last"></span>**EAP \_ I \_ EAPHost per \_ ultimi**
</dt> <dd> <dl> <dt>

0x804200FFL
</dt> <dt>



Definisce il limite dei report informazioni; eventuali registrazioni di eventi informativi correlati a EAPHost si verificheranno **prima tra EAP \_ i \_ EAPHost \_** e **EAP \_ i \_ EAPHost \_**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_CERT_STORE_INACCESSIBLE"></span><span id="eap_e_cert_store_inaccessible"></span>**\_archivio certificati EAP E non \_ \_ \_ accessibile**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



L'autenticatore o il peer non è in grado di accedere all'archivio certificati.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_NOT_INSTALLED"></span><span id="eap_e_eaphost_method_not_installed"></span>**\_metodo EAP \_ E \_ EAPHost \_ non \_ installato**
</dt> <dd> <dl> <dt>

0x80420011
</dt> <dt>



Il metodo EAP richiesto non è installato.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_THIRDPARTY_METHOD_HOST_RESET"></span><span id="eap_e_eaphost_thirdparty_method_host_reset"></span>**\_reimpostazione \_ \_ \_ host metodo thirdparty \_ EAP E EAPHOST \_**
</dt> <dd> <dl> <dt>

0x80420012
</dt> <dt>



L'host del metodo di terze parti non risponde ed è stato riavviato automaticamente.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_EAPQEC_INACCESSIBLE"></span><span id="eap_e_eaphost_eapqec_inaccessible"></span>**\_EAPQEC EAP \_ E \_ EAPHOST \_ inaccessibili**
</dt> <dd> <dl> <dt>

0x80420013
</dt> <dt>



EAPHost non è in grado di comunicare con il [client di imposizione di quarantena](/windows/desktop/NAP/nap-client-architecture) EAP (QeC) in un client abilitato per [Protezione accesso alla rete](/windows/desktop/NAP/network-access-protection-start-page) (NAP).


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_IDENTITY_UNKNOWN"></span><span id="eap_e_eaphost_identity_unknown"></span>**\_identità EAP \_ E \_ EAPHOST \_ sconosciuta**
</dt> <dd> <dl> <dt>

0x80420014
</dt> <dt>



EAPHost restituisce questo errore se l'autenticatore non riesce a eseguire l'autenticazione dopo l'invio dell'identità peer.


</dt> </dl> </dd> <dt>

<span id="EAP_E_AUTHENTICATION_FAILED"></span><span id="eap_e_authentication_failed"></span>**\_autenticazione EAP \_ E \_ non riuscita**
</dt> <dd> <dl> <dt>

0x80420015 
</dt> <dt>



EAPHost restituisce questo errore in caso di errore di autenticazione.


</dt> </dl> </dd> <dt>

<span id="EAP_I_EAPHOST_EAP_NEGOTIATION_FAILED"></span><span id="eap_i_eaphost_eap_negotiation_failed"></span>**\_ \_ \_ negoziazione EAP EAP EAPHost \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

0x40420016
</dt> <dt>



EAPHost registra questo evento informativo quando il client e il server non sono configurati con tipi EAP compatibili.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_INVALID_PACKET"></span><span id="eap_e_eaphost_method_invalid_packet"></span>**\_ \_ \_ \_ pacchetto non valido nel metodo EAP E EAPHost \_**
</dt> <dd> <dl> <dt>

0x80420017
</dt> <dt>



Un metodo EAP ha ricevuto un pacchetto EAP che non può essere elaborato. Un altro nome per il **\_ pacchetto EAP E \_ EAPHOST \_ Method \_ non valido \_** è il **\_ \_ \_ pacchetto EAP non valido**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_REMOTE_INVALID_PACKET"></span><span id="eap_e_eaphost_remote_invalid_packet"></span>**\_ \_ pacchetto remoto EAP E EAPHost \_ \_ non valido \_**
</dt> <dd> <dl> <dt>

0x80420018
</dt> <dt>



EAPHost ha ricevuto un pacchetto che non può essere elaborato. Un altro nome per **EAP \_ E \_ EAPHOST \_ Remote \_ \_ Packet** è un **\_ \_ pacchetto EAP non valido**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_XML_MALFORMED_"></span><span id="eap_e_eaphost_xml_malformed_"></span>**\_ \_ formato XML EAP E EAPHost non \_ \_ valido** 
</dt> <dd> <dl> <dt>

0x80420019
</dt> <dt>



Convalida dello schema di configurazione EAPHost non riuscita.


</dt> </dl> </dd> <dt>

<span id="EAP_E_METHOD_CONFIG_DOES_NOT_SUPPORT_SSO"></span><span id="eap_e_method_config_does_not_support_sso"></span>**\_la configurazione del metodo EAP E non \_ \_ \_ \_ \_ supporta \_ SSO**
</dt> <dd> <dl> <dt>

0x8042001A
</dt> <dt>



Windows 7 o versioni successive: il metodo EAP non supporta Single Sign-on (SSO) per la configurazione specificata.


</dt> </dl> </dd> <dt>

<span id="EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="eap_e_eaphost_method_operation_not_supported"></span>**\_operazione del metodo EAP E \_ EAPHost \_ \_ \_ non \_ supportata**
</dt> <dd> <dl> <dt>

0x80420020
</dt> <dt>



EAPHost restituisce questo errore quando un metodo EAP configurato non supporta un'operazione richiesta (chiamata di procedura).


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_FIRST"></span><span id="eap_e_user_first"></span>**\_ \_ prima utente EAP \_ E**
</dt> <dd> <dl> <dt>

0x80420100L
</dt> <dt>



Definisce il limite dei report di errore. si verificherà un errore correlato all'utente tra il **\_ \_ \_ primo utente** e EAP e **\_ \_ \_ l'** utente.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_LAST_"></span><span id="eap_e_user_last_"></span>**\_ \_ ultimo utente EAP \_ E** 
</dt> <dd> <dl> <dt>

0x804201FFL
</dt> <dt>



Definisce il limite dei report di errore. si verificherà un errore correlato all'utente tra il **\_ \_ \_ primo utente** e EAP e **\_ \_ \_ l'** utente.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_FIRST"></span><span id="eap_i_user_first"></span>**\_ \_ prima utente EAP \_ I**
</dt> <dd> <dl> <dt>

0x40420100L
</dt> <dt>



Definisce il limite dei report informazioni; eventuali registrazioni di eventi informativi correlati a EAP si verificheranno tra l' **\_ \_ utente EAP \_ prima** e **\_ \_ \_ l'ultimo utente EAP i**.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_LAST"></span><span id="eap_i_user_last"></span>**\_ \_ ultimo utente EAP \_ I**
</dt> <dd> <dl> <dt>

0x404201FFL
</dt> <dt>



Definisce il limite dei report informazioni; eventuali registrazioni di eventi informativi correlati a EAP si verificheranno tra l' **\_ \_ utente EAP \_ prima** e **\_ \_ \_ l'ultimo utente EAP i**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_NOT_FOUND"></span><span id="eap_e_user_cert_not_found"></span>**\_ \_ certificato utente EAP \_ E \_ non \_ trovato**
</dt> <dd> <dl> <dt>

0x80420100
</dt> <dt>



EAPHost non è riuscito a trovare un certificato utente per l'autenticazione.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_INVALID"></span><span id="eap_e_user_cert_invalid"></span>**\_ \_ certificato utente EAP \_ E \_ non valido**
</dt> <dd> <dl> <dt>

0x80420101
</dt> <dt>



Per il certificato utente utilizzato per l'autenticazione non è impostato l'utilizzo chiavi avanzato (EKU) appropriato.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_EXPIRED"></span><span id="eap_e_user_cert_expired"></span>**\_ \_ certificato utente EAP \_ E \_ scaduto**
</dt> <dd> <dl> <dt>

0x80420102
</dt> <dt>



EAPhost ha rilevato un certificato utente scaduto.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REVOKED"></span><span id="eap_e_user_cert_revoked"></span>**\_ \_ certificato utente EAP \_ E \_ revocato**
</dt> <dd> <dl> <dt>

0x80420103
</dt> <dt>



Il certificato utente usato per l'autenticazione è stato revocato.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_OTHER_ERROR"></span><span id="eap_e_user_cert_other_error"></span>**\_errore del \_ \_ certificato utente \_ EAP \_ E**
</dt> <dd> <dl> <dt>

0x80420104
</dt> <dt>



Si è verificato un errore sconosciuto con la certificazione utente utilizzata per l'autenticazione.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CERT_REJECTED_"></span><span id="eap_e_user_cert_rejected_"></span>**\_ \_ certificato utente EAP \_ E \_ rifiutato** 
</dt> <dd> <dl> <dt>

0x80420105
</dt> <dt>



L'autenticatore ha rifiutato la certificazione utente.


</dt> </dl> </dd> <dt>

<span id="EAP_I_USER_ACCOUNT_OTHER_ERROR"></span><span id="eap_i_user_account_other_error"></span>**\_ \_ \_ errore dell'account utente \_ EAP I \_**
</dt> <dd> <dl> <dt>

0x40420110
</dt> <dt>



Si è verificato un errore EAP dopo uno scambio di identità, che indica la probabilità di un problema con l'account dell'utente che esegue l'autenticazione.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_CREDENTIALS_REJECTED"></span><span id="eap_e_user_credentials_rejected"></span>**\_ \_ credenziali utente EAP \_ E \_ rifiutate**
</dt> <dd> <dl> <dt>

0x80420111
</dt> <dt>



L'autenticatore ha rifiutato le credenziali utente per l'autenticazione.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_NAME_PASSWORD_REJECTED"></span><span id="eap_e_user_name_password_rejected"></span>**\_ \_ password nome utente EAP E \_ \_ \_ rifiutata**
</dt> <dd> <dl> <dt>

0x80420112
</dt> <dt>



Windows 7 o versioni successive: autenticazione non riuscita. L'autenticatore ha rifiutato le credenziali utente.


</dt> </dl> </dd> <dt>

<span id="EAP_E_NO_SMART_CARD_READER"></span><span id="eap_e_no_smart_card_reader"></span>**EAP \_ E \_ nessun \_ lettore di Smart \_ card \_**
</dt> <dd> <dl> <dt>

0x80420113
</dt> <dt>



Windows 7 o versioni successive: non è stato trovato alcun lettore di smart card.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_FIRST"></span><span id="eap_e_server_first"></span>**\_server EAP \_ E \_ prima**
</dt> <dd> <dl> <dt>

0x80420200L
</dt> <dt>



Definisce il limite dei report di errore. si verificherà un errore relativo al server tra il **\_ \_ \_ primo** e il server EAP e il server per **\_ \_ \_ ultimo**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_LAST"></span><span id="eap_e_server_last"></span>**\_ \_ ultimo server EAP \_ E**
</dt> <dd> <dl> <dt>

0x804202FFL
</dt> <dt>



Definisce il limite dei report di errore. si verificherà un errore relativo al server tra il **\_ \_ \_ primo** e il server EAP e il server per **\_ \_ \_ ultimo**.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_NOT_FOUND"></span><span id="eap_e_server_cert_not_found"></span>**\_ \_ certificato server EAP \_ E \_ non \_ trovato**
</dt> <dd> <dl> <dt>

0x80420200
</dt> <dt>



EAPHost non è stato in grado di trovare il certificato del server per l'autenticazione.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_INVALID"></span><span id="eap_e_server_cert_invalid"></span>**\_ \_ certificato server EAP \_ E \_ non valido**
</dt> <dd> <dl> <dt>

0x80420201
</dt> <dt>



Il certificato del server utilizzato per l'autenticazione non dispone di un set di utilizzo chiavi avanzato (EKU) appropriato.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_EXPIRED"></span><span id="eap_e_server_cert_expired"></span>**\_ \_ certificato server EAP \_ E \_ scaduto**
</dt> <dd> <dl> <dt>

0x80420202
</dt> <dt>



EAPhost ha rilevato un certificato server scaduto.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_REVOKED"></span><span id="eap_e_server_cert_revoked"></span>**\_ \_ certificato server EAP \_ E \_ revocato**
</dt> <dd> <dl> <dt>

0x80420203
</dt> <dt>



Il certificato server usato per l'autenticazione è stato revocato.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_CERT_OTHER_ERROR"></span><span id="eap_e_server_cert_other_error"></span>**\_errore del \_ certificato del server EAP E \_ \_ altro \_**
</dt> <dd> <dl> <dt>

0x80420204
</dt> <dt>



Si è verificato un errore sconosciuto con il certificato del server.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_FIRST"></span><span id="eap_e_user_root_cert_first"></span>**\_ \_ \_ \_ primo certificato radice utente EAP E \_**
</dt> <dd> <dl> <dt>

0x80420300L
</dt> <dt>



Definisce il limite dei report di errore. qualsiasi errore relativo al certificato radice utente si verificherà prima tra il certificato **\_ \_ \_ radice utente \_ \_ EAP** e e il certificato **\_ \_ \_ radice \_ \_ utente EAP** e.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_LAST"></span><span id="eap_e_user_root_cert_last"></span>**\_ \_ \_ \_ ultimo certificato radice utente EAP E \_**
</dt> <dd> <dl> <dt>

0x804203FFL
</dt> <dt>



Definisce il limite dei report di errore. qualsiasi errore relativo al certificato radice utente si verificherà prima tra il certificato **\_ \_ \_ radice utente \_ \_ EAP** e e il certificato **\_ \_ \_ radice \_ \_ utente EAP** e.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_user_root_cert_not_found"></span>**\_ \_ certificato radice utente EAP E \_ \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

0x80420300
</dt> <dt>



EAPHost non è riuscito a trovare un certificato in un archivio certificati radice attendibile per la convalida della certificazione utente.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_INVALID"></span><span id="eap_e_user_root_cert_invalid"></span>**\_ \_ certificato radice utente EAP E \_ \_ \_ non valido**
</dt> <dd> <dl> <dt>

0x80420301
</dt> <dt>



L'autenticazione non è riuscita perché il certificato radice usato per la rete non è valido.


</dt> </dl> </dd> <dt>

<span id="EAP_E_USER_ROOT_CERT_EXPIRED"></span><span id="eap_e_user_root_cert_expired"></span>**\_ \_ \_ certificato radice utente EAP \_ E \_ scaduto**
</dt> <dd> <dl> <dt>

0x80420302
</dt> <dt>



Il certificato radice attendibile necessario per la convalida del certificato utente è scaduto.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_FIRST"></span><span id="eap_e_server_root_cert_first"></span>**\_ \_ \_ \_ primo certificato radice del server EAP E \_**
</dt> <dd> <dl> <dt>

0x80420400L
</dt> <dt>



Definisce il limite dei report di errore. si verificherà un errore relativo al certificato radice del server tra il certificato **radice del server EAP e \_ \_ \_ \_ \_ prima** e il certificato **\_ \_ \_ radice \_ \_** del server EAP e.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_LAST"></span><span id="eap_e_server_root_cert_last"></span>**\_ \_ \_ \_ ultimo certificato radice server EAP E \_**
</dt> <dd> <dl> <dt>

0x804204FFL
</dt> <dt>



Definisce il limite dei report di errore. si verificherà un errore relativo al certificato radice del server tra il certificato **radice del server EAP e \_ \_ \_ \_ \_ prima** e il certificato **\_ \_ \_ radice \_ \_** del server EAP e.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="eap_e_server_root_cert_not_found"></span>**\_ \_ certificato radice del server EAP E \_ \_ \_ non \_ trovato**
</dt> <dd> <dl> <dt>

0x80420400
</dt> <dt>



EAPHost non è riuscito a trovare un certificato radice in un archivio certificati radice attendibile per la convalida della certificazione server.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_INVALID__________"></span><span id="eap_e_server_root_cert_invalid__________"></span>**\_ \_ certificato radice del server EAP E \_ \_ \_ non valido** 
</dt> <dd> <dl> <dt>

0x80420401
</dt> <dt>



L'autenticazione non è riuscita perché il certificato server richiesto per la rete nel computer server non è valido.


</dt> </dl> </dd> <dt>

<span id="EAP_E_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="eap_e_server_root_cert_name_required"></span>**\_ \_ \_ nome certificato radice server EAP E \_ \_ \_ obbligatorio**
</dt> <dd> <dl> <dt>

0x80420406
</dt> <dt>



L'autenticazione non è riuscita perché il certificato nel computer server non ha un nome di server specificato.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Esistono nomi alternativi per determinati errori:

-   Un altro nome per il **\_ pacchetto EAP E \_ EAPHOST \_ Method \_ non valido \_** è il **\_ \_ \_ pacchetto EAP non valido**.
-   Un altro nome per **EAP \_ E \_ EAPHOST \_ Remote \_ \_ Packet** è un **\_ \_ pacchetto EAP non valido**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Eaphosterror. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti EAPHost comuni](common-eap-host-error-constants.md)
</dt> </dl>

 

