---
title: Codici restituiti di TBS (TBS. h)
description: TBS usa i codici seguenti per indicare il risultato di una chiamata di funzione.
ms.assetid: a3888263-aa00-4b31-b51d-c6d448c1edb7
topic_type:
- apiref
api_name:
- TBS_SUCCESS
- TBS_E_INTERNAL_ERROR
- TBS_E_BAD_PARAMETER
- TBS_E_INVALID_OUTPUT_POINTER
- TBS_E_INVALID_CONTEXT
- TBS_E_INSUFFICIENT_BUFFER
- TBS_E_IOERROR
- TBS_E_INVALID_CONTEXT_PARAM
- TBS_E_SERVICE_NOT_RUNNING
- TBS_E_TOO_MANY_TBS_CONTEXTS
- TBS_E_TOO_MANY_RESOURCES
- TBS_E_SERVICE_START_PENDING
- TBS_E_PPI_NOT_SUPPORTED
- TBS_E_COMMAND_CANCELED
- TBS_E_BUFFER_TOO_LARGE
- TBS_E_TPM_NOT_FOUND
- TBS_E_SERVICE_DISABLED
- TBS_E_NO_EVENT_LOG
- TBS_E_ACCESS_DENIED
- TBS_E_PROVISIONING_NOT_ALLOWED
- TBS_E_PPI_FUNCTION_UNSUPPORTED
- TBS_E_OWNERAUTH_NOT_FOUND
- TBS_E_PROVISIONING_INCOMPLETE
api_location:
- Tbs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0271c323e4ea300f45817aa59d4f5f9779f9981
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400645"
---
# <a name="tbs-return-codes"></a>Codici restituiti di TBS

TBS usa i codici seguenti per indicare il risultato di una chiamata di funzione.



| Costante/valore                                                                                                                                                                                                                                                                                   | Descrizione                                                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_SUCCESS"></span><span id="tbs_success"></span><dl> <dt>**TBS \_ Operazione riuscita**</dt> <dt>0 (0x0)</dt> </dl>                                                                             | Funzione completata.<br/>                                                                                                                                                                                                         |
| <span id="TBS_E_INTERNAL_ERROR"></span><span id="tbs_e_internal_error"></span><dl> <dt>**TBS \_ E \_ \_ errore interno**</dt> <dt>2150121473 (0x80284001)</dt> </dl>                                | Si è verificato un errore interno del software.<br/>                                                                                                                                                                                            |
| <span id="TBS_E_BAD_PARAMETER"></span><span id="tbs_e_bad_parameter"></span><dl> <dt>**TBS \_ E \_ \_ parametro non valido**</dt> <dt>2150121474 (0x80284002)</dt> </dl>                                   | Uno o più valori di parametro non sono validi.<br/>                                                                                                                                                                                     |
| <span id="TBS_E_INVALID_OUTPUT_POINTER"></span><span id="tbs_e_invalid_output_pointer"></span><dl> <dt>**TBS \_ \_Puntatore di \_ output \_ E non valido**</dt> <dt>2150121475 (0x80284003)</dt> </dl>       | Un puntatore di output specificato non è valido.<br/>                                                                                                                                                                                              |
| <span id="TBS_E_INVALID_CONTEXT"></span><span id="tbs_e_invalid_context"></span><dl> <dt>**TBS \_ E \_ \_ contesto non valido**</dt> <dt>2150121476 (0x80284004)</dt> </dl>                             | L'handle del contesto specificato non fa riferimento a un contesto valido.<br/>                                                                                                                                                                 |
| <span id="TBS_E_INSUFFICIENT_BUFFER"></span><span id="tbs_e_insufficient_buffer"></span><dl> <dt>**TBS \_ E \_ \_ buffer insufficiente**</dt> <dt>2150121477 (0x80284005)</dt> </dl>                 | Il buffer di output specificato è troppo piccolo.<br/>                                                                                                                                                                                       |
| <span id="TBS_E_IOERROR"></span><span id="tbs_e_ioerror"></span><dl> <dt>**TBS \_ E \_ IOERROR**</dt> <dt>2150121478 (0x80284006)</dt> </dl>                                                      | Si è verificato un errore durante la comunicazione con il TPM.<br/>                                                                                                                                                                             |
| <span id="TBS_E_INVALID_CONTEXT_PARAM"></span><span id="tbs_e_invalid_context_param"></span><dl> <dt>**TBS \_ E \_ \_ \_ parametro di contesto non valido**</dt> <dt>2150121479 (0x80284007)</dt> </dl>          | È stato passato un parametro di contesto non valido durante il tentativo di creare un contesto di TBS.<br/>                                                                                                                                       |
| <span id="TBS_E_SERVICE_NOT_RUNNING"></span><span id="tbs_e_service_not_running"></span><dl> <dt>**TBS \_ \_Servizio E \_ non \_ in esecuzione**</dt> <dt>2150121480 (0x80284008)</dt> </dl>                | Il servizio TBS non è in esecuzione e non può essere avviato.<br/>                                                                                                                                                                        |
| <span id="TBS_E_TOO_MANY_TBS_CONTEXTS"></span><span id="tbs_e_too_many_tbs_contexts"></span><dl> <dt>**TBS \_ E \_ troppi \_ \_ \_ contesti TBS**</dt> <dt>2150121481 (0x80284009)</dt> </dl>         | Non è stato possibile creare un nuovo contesto perché troppi contesti aperti.<br/>                                                                                                                                                    |
| <span id="TBS_E_TOO_MANY_RESOURCES"></span><span id="tbs_e_too_many_resources"></span><dl> <dt>**TBS \_ E \_ troppe \_ \_ risorse**</dt> <dt>2150121482 (0x8028400A)</dt> </dl>                   | Non è stato possibile creare una nuova risorsa virtuale perché troppe risorse virtuali aperte.<br/>                                                                                                                                  |
| <span id="TBS_E_SERVICE_START_PENDING"></span><span id="tbs_e_service_start_pending"></span><dl> <dt>**TBS \_ \_Avvio del servizio E \_ \_ in sospeso**</dt> <dt>2150121483 (0x8028400B)</dt> </dl>          | Il servizio TBS è stato avviato ma non è ancora in esecuzione.<br/>                                                                                                                                                                        |
| <span id="TBS_E_PPI_NOT_SUPPORTED"></span><span id="tbs_e_ppi_not_supported"></span><dl> <dt>**TBS \_ E \_ PPI \_ non \_ supportati**</dt> <dt>2150121484 (0x8028400C)</dt> </dl>                      | L'interfaccia di presenza fisica non è supportata.<br/>                                                                                                                                                                               |
| <span id="TBS_E_COMMAND_CANCELED"></span><span id="tbs_e_command_canceled"></span><dl> <dt>**TBS \_ \_Comando E \_ annullato**</dt> <dt>2150121485 (0x8028400D)</dt> </dl>                          | Il comando è stato annullato.<br/>                                                                                                                                                                                                       |
| <span id="TBS_E_BUFFER_TOO_LARGE"></span><span id="tbs_e_buffer_too_large"></span><dl> <dt>**TBS \_ \_Buffer E \_ troppo \_ grande**</dt> <dt>2150121486 (0x8028400E)</dt> </dl>                         | Il buffer di input o di output è troppo grande.<br/>                                                                                                                                                                                        |
| <span id="TBS_E_TPM_NOT_FOUND"></span><span id="tbs_e_tpm_not_found"></span><dl> <dt>**TBS \_ E \_ TPM \_ non \_ trovato**</dt> <dt>2150121487 (0x8028400F)</dt> </dl>                                  | Non è possibile trovare un dispositivo di sicurezza con Trusted Platform Module compatibili (TPM) nel computer.<br/>                                                                                                                                    |
| <span id="TBS_E_SERVICE_DISABLED"></span><span id="tbs_e_service_disabled"></span><dl> <dt>**TBS \_ \_Servizio E \_ disattivato**</dt> <dt>2150121488 (0x80284010)</dt> </dl>                          | Il servizio TBS è stato disabilitato.<br/>                                                                                                                                                                                              |
| <span id="TBS_E_NO_EVENT_LOG"></span><span id="tbs_e_no_event_log"></span><dl> <dt>**TBS \_ E \_ nessun \_ \_ registro eventi**</dt> <dt>2150121489 (0x80284011)</dt> </dl>                                     | Il registro eventi di TBS non è disponibile.<br/>                                                                                                                                                                                             |
| <span id="TBS_E_ACCESS_DENIED"></span><span id="tbs_e_access_denied"></span><dl> <dt>**TBS \_ E \_ accesso \_ negato**</dt> <dt>2150121490 (0x80284012)</dt> </dl>                                   | Il chiamante non dispone dei diritti appropriati per eseguire l'operazione richiesta.<br/>                                                                                                                                             |
| <span id="TBS_E_PROVISIONING_NOT_ALLOWED"></span><span id="tbs_e_provisioning_not_allowed"></span><dl> <dt>**TBS \_ \_PROvisioning E \_ non \_ consentito**</dt> <dt>2150121491 (0x80284013)</dt> </dl> | L'azione di provisioning TPM non è consentita dai flag specificati.<br/>                                                                                                                                                              |
| <span id="TBS_E_PPI_FUNCTION_UNSUPPORTED"></span><span id="tbs_e_ppi_function_unsupported"></span><dl> <dt>**TBS \_ \_Funzione E PPI non \_ \_ supportata**</dt> <dt>2150121492 (0x80284014)</dt> </dl> | L'interfaccia di presenza fisica del firmware non supporta il metodo richiesto.<br/>                                                                                                                                         |
| <span id="TBS_E_OWNERAUTH_NOT_FOUND"></span><span id="tbs_e_ownerauth_not_found"></span><dl> <dt>**TBS \_ E \_ OWNERAUTH \_ non \_ trovato**</dt> <dt>2150121493 (0x80284015)</dt> </dl>                | Il valore OwnerAuth TPM richiesto non è stato trovato.<br/>                                                                                                                                                                                |
| <span id="TBS_E_PROVISIONING_INCOMPLETE"></span><span id="tbs_e_provisioning_incomplete"></span><dl> <dt>**TBS \_ E \_ PROvisioning \_ incompleto**</dt> <dt>2150121493 (0x80284015)</dt> </dl>     | Il provisioning del TPM non è stato completato. Per ulteriori informazioni sul completamento del provisioning, chiamare il metodo WMI [**\_ TPM Win32**](/windows/desktop/SecProv/win32-tpm) per il provisioning del TPM (' Provision ') e verificare le informazioni restituite.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                             |
| Intestazione<br/>                   | <dl> <dt>TBS. h</dt> </dl> |



 

