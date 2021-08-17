---
description: 'Messaggi di errore restituiti dai gestori di protocollo:'
ms.assetid: b5e99ad1-1698-483c-8173-796af33085c4
title: Messaggi di errore del gestore del protocollo di ricerca (Searchapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4473e3e235641e5b4bb5d86313b4154cd00ec029fe96d42d8964dab51f33780f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969730"
---
# <a name="search-protocol-handler-error-messages"></a>Messaggi di errore del gestore del protocollo di ricerca

Messaggi di errore restituiti dai gestori di protocollo:



| Costante/valore                                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRTH_E_ACCESS_DENIED"></span><span id="prth_e_access_denied"></span><dl> <dt>**PRTH \_ E \_ ACCESSO \_ NEGATO**</dt> <dt>0x80041205L</dt> </dl>             | L'accesso è stato negato. Se ciò si verifica durante una ricerca per indicizzazione incrementale, il file viene eliminato dalla coda url del gatherer.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_IS_READ_NONE"></span><span id="prth_e_acl_is_read_none"></span><dl> <dt>**PRTH \_ E \_ ACL \_ IS READ \_ \_ NONE**</dt> <dt>0x80041211L</dt> </dl>  | L'elemento non verrà indicizzato. Il relativo ACL non consente a nessuno di leggere l'elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_TOO_BIG"></span><span id="prth_e_acl_too_big"></span><dl> <dt>**PRTH \_ E \_ ACL \_ TOO \_ BIG**</dt> <dt>0x80041212L</dt> </dl>                  | ACL ha superato i 64 KB. La ricerca non indicizza l'elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_BAD_REQUEST"></span><span id="prth_e_bad_request"></span><dl> <dt>**PRTH \_ E \_ BAD \_ REQUEST**</dt> <dt>0x80041208L</dt> </dl>                   | La richiesta non è valida a causa di un errore nell'URL.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_COMM_ERROR"></span><span id="prth_e_comm_error"></span><dl> <dt>**PRTH \_ E \_ ERRORE \_ COMM**</dt> <dt>0x80041200L</dt> </dl>                      | Indica un errore di comunicazione o del server. Se sono presenti troppi errori per un server specifico, il gatherer contrassegna il server come non disponibile.<br/>                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_NOT_REDIRECTED"></span><span id="prth_e_not_redirected"></span><dl> <dt>**PRTH \_ E \_ NOT \_ REDIRECTED**</dt> <dt>0x80041207L</dt> </dl>          | L'URL reindirizzato non esiste.<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_E_OBJ_NOT_FOUND"></span><span id="prth_e_obj_not_found"></span><dl> <dt>**PRTH \_ E \_ OBJ \_ NOT \_ FOUND**</dt> <dt>0x80041201L</dt> </dl>            | Oggetto non trovato. Indica che il gatherer deve eliminare il documento dalla coda se non viene trovato durante una ricerca per indicizzazione incrementale.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_REQUEST_ERROR"></span><span id="prth_e_request_error"></span><dl> <dt>**PRTH \_ E \_ REQUEST \_ ERROR**</dt> <dt>0x80041202L</dt> </dl>             | Le opzioni usate non sono supportate.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="PRTH_E_SERVER_ERROR"></span><span id="prth_e_server_error"></span><dl> <dt>**PRTH \_ E \_ ERRORE \_ DEL SERVER**</dt> <dt>0x80041206L</dt> </dl>                | Errore di comunicazione o server. Se sono presenti troppi errori per un server specifico, il gatherer contrassegna il server come non disponibile.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PRTH_S_NOT_ALL_PARTS"></span><span id="prth_s_not_all_parts"></span><dl> <dt>**PRTH \_ S \_ NOT \_ ALL \_ PARTS**</dt> <dt>0x8004121BL</dt> </dl>            | Non è possibile accedere a parti di un elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="PRTH_S_NOT_MODIFIED"></span><span id="prth_s_not_modified"></span><dl> <dt>**PRTH \_ S \_ NOT \_ MODIFIED**</dt> <dt>0x00041203L</dt> </dl>                | Il contenuto dell'elemento non è stato modificato. Se questo errore si verifica durante una ricerca per indicizzazione incrementale, il gatherer ignora questo elemento perché l'elemento non è stato modificato.<br/>                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_S_TRY_IMPERSONATING"></span><span id="prth_s_try_impersonating"></span><dl> <dt>**PRTH \_ S \_ PROVARE \_ A RAPPRESENTARE**</dt> <dt>0x00041225L</dt> </dl> | È necessario accedere all'elemento durante la rappresentazione di un utente. Il gestore del protocollo deve implementare [**IUrlAccessor3::GetImpersonationSidBlobs**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor3-getimpersonationsidblobs) in modo che l'host del protocollo di ricerca possa recuperare un elenco di SID da usare per la rappresentazione e possa ripristinare l'uso [**di IUrlAccessor2,**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2)rappresentando uno degli utenti consentiti all'apertura dell'elemento. <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo app desktop di Vista \[\]<br/>                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                   |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3.0<br/>                                            |
| Intestazione<br/>                   | <dl> <dt>Searchapi.h</dt> </dl> |



 

 




