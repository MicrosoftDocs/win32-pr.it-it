---
description: 'Messaggi di errore restituiti dai gestori del protocollo:'
ms.assetid: b5e99ad1-1698-483c-8173-796af33085c4
title: Messaggi di errore del gestore di protocollo di ricerca (searchapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 297ea44c367069a5558355cf6fe81cd9db57ee53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128559"
---
# <a name="search-protocol-handler-error-messages"></a>Cerca nei messaggi di errore del gestore del protocollo

Messaggi di errore restituiti dai gestori del protocollo:



| Costante/valore                                                                                                                                                                                                                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRTH_E_ACCESS_DENIED"></span><span id="prth_e_access_denied"></span><dl> <dt>**PRTH \_ E \_ accesso \_ negato**</dt> <dt>0x80041205L</dt> </dl>             | Accesso negato. Se questo errore si verifica durante una ricerca per indicizzazione incrementale, il file viene eliminato dalla coda URL del Gatherer.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_IS_READ_NONE"></span><span id="prth_e_acl_is_read_none"></span><dl> <dt>**PRTH \_ E \_ ACL \_ is \_ Read \_ None**</dt> <dt>0x80041211L</dt> </dl>  | L'elemento non verrà indicizzato. Il relativo ACL non consente a nessuno di leggere l'elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_TOO_BIG"></span><span id="prth_e_acl_too_big"></span><dl> <dt>**PRTH \_ E \_ ACL \_ troppo \_ grande**</dt> <dt>0x80041212L</dt> </dl>                  | L'ACL ha superato 64 KB. La ricerca non indicizza l'elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_BAD_REQUEST"></span><span id="prth_e_bad_request"></span><dl> <dt>**PRTH \_ 0x80041208L \_ \_ richiesta non valida**</dt> <dt></dt> </dl>                   | La richiesta non è valida a causa di un errore nell'URL.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_COMM_ERROR"></span><span id="prth_e_comm_error"></span><dl> <dt>**PRTH \_ 0x80041200L \_ \_ errore di comunicazione E**</dt> <dt></dt> </dl>                      | Indica un errore di comunicazione o del server. Se sono presenti troppi errori per un determinato server, il Gatherer contrassegna il server come non disponibile.<br/>                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_NOT_REDIRECTED"></span><span id="prth_e_not_redirected"></span><dl> <dt>**PRTH \_ E \_ non \_ reindirizzato**</dt> <dt>0x80041207L</dt> </dl>          | L'URL reindirizzato non esiste.<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_E_OBJ_NOT_FOUND"></span><span id="prth_e_obj_not_found"></span><dl> <dt>**PRTH \_ E \_ obj \_ non \_ trovato**</dt> <dt>0x80041201L</dt> </dl>            | Oggetto non trovato. Indica che il Gatherer deve eliminare il documento dalla coda se non viene trovato durante una ricerca per indicizzazione incrementale.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_REQUEST_ERROR"></span><span id="prth_e_request_error"></span><dl> <dt>**PRTH \_ \_ \_ Errore di richiesta E**</dt> <dt>0x80041202L</dt> </dl>             | Le opzioni utilizzate non sono supportate.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="PRTH_E_SERVER_ERROR"></span><span id="prth_e_server_error"></span><dl> <dt>**PRTH \_ \_ \_ Errore del server E**</dt> <dt>0x80041206L</dt> </dl>                | Errore di comunicazione o del server. Se sono presenti troppi errori per un determinato server, il Gatherer contrassegna il server come non disponibile.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PRTH_S_NOT_ALL_PARTS"></span><span id="prth_s_not_all_parts"></span><dl> <dt>**PRTH \_ \_Non \_ tutti i \_ componenti**</dt> <dt>0x8004121BL</dt> </dl>            | Non è possibile accedere alle parti di un elemento.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="PRTH_S_NOT_MODIFIED"></span><span id="prth_s_not_modified"></span><dl> <dt>**PRTH \_ Il 0x00041203L non è stato \_ \_ modificato**</dt> <dt></dt> </dl>                | Il contenuto dell'elemento non è stato modificato. Se questo errore si verifica durante una ricerca per indicizzazione incrementale, il Gatherer ignora questo elemento perché l'elemento non è stato modificato.<br/>                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_S_TRY_IMPERSONATING"></span><span id="prth_s_try_impersonating"></span><dl> <dt>**PRTH \_ S \_ provare a \_ rappresentare**</dt> <dt>0x00041225L</dt> </dl> | È necessario accedere all'elemento durante la rappresentazione di un utente. Il gestore di protocollo deve implementare [**IUrlAccessor3:: GetImpersonationSidBlobs**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor3-getimpersonationsidblobs) in modo che l'host del protocollo di ricerca possa recuperare un elenco di SID da usare per la rappresentazione e può ripristinare l'uso di [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2), rappresentando uno degli utenti consentiti all'apertura dell'elemento. <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, \[ solo app desktop di Windows Vista\]<br/>                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                   |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                            |
| Intestazione<br/>                   | <dl> <dt>Searchapi. h</dt> </dl> |



 

 




