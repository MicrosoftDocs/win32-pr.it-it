---
description: Codici di errore PNRP NSP
ms.assetid: adf40b1a-c5d6-418d-a012-cf6ba7d4fa24
title: Codici di errore PNRP NSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47b02959c921c8e3a468cadfa87dba6fb8d3c29d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881786"
---
# <a name="pnrp-nsp-error-codes"></a>Codici di errore PNRP NSP

Se la funzione del provider dello spazio dei nomi (NSP) restituisce un **\_ errore socket**, è necessario utilizzare [WSAGetLastError](winsock-nsp-reference-links.md) per ottenere ulteriori informazioni sull'errore. Il NSP PNRP restituisce i codici di errore seguenti:



| Termine                                                                                                                                                                     | Descrizione                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>WSA \_ E \_ annullato<br/>                                                                         | Un'operazione è stata annullata.<br/>                                                                               |
| <span id="__WSA_E_NO_MORE"></span><span id="__wsa_e_no_more"></span> WSA \_ E \_ nient' \_ altro<br/>                                                                         | I risultati di una richiesta risolta non sono pronti. Questo potrebbe non essere un errore.<br/>                              |
| <span id="_WSA_IO_PENDING_"></span><span id="_wsa_io_pending_"></span>\_io WSA \_ in sospeso <br/>                                                                      | Operazione non completata.<br/>                                                                           |
| <span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span>\_ \_ memoria insufficiente per WSA \_<br/>                                                      | Memoria insufficiente per completare un'azione specificata.<br/>                                              |
| <span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span>\_operazione WSA \_ interrotta<br/>                                                       | Un'operazione è stata annullata.<br/>                                                                               |
| <span id="WSA_PNRP_CLOUD_DISABLED"></span><span id="wsa_pnrp_cloud_disabled"></span>\_Cloud PNRP \_ cloud \_ disabilitato<br/>                                                | Un nome di cloud specificato è disabilitato.<br/>                                                                     |
| <span id="WSA_PNRP_CLOUD_NOT_FOUND"></span><span id="wsa_pnrp_cloud_not_found"></span>\_Cloud PNRP \_ PNRP \_ non \_ trovato<br/>                                            | Il nome cloud specificato non è disponibile.<br/>                                                                |
| <span id="WSA_PNRP_CLOUD_IS_SEARCH_ONLY"></span><span id="wsa_pnrp_cloud_is_search_only"></span>il \_ Cloud PNRP WSA \_ \_ è \_ solo di ricerca \_<br/>                            | Si è tentato di registrare un nome in un cloud configurato per la sola risoluzione.<br/>     |
| <span id="WSA_PNRP_CLIENT_INVALID_COMPARTMENT_ID"></span><span id="wsa_pnrp_client_invalid_compartment_id"></span>\_ \_ \_ ID raggruppamento non valido del client \_ PNRP WSA \_<br/> | Uso di PNRP in un raggruppamento esterno al valore predefinito. PNRP funzionerà solo nel raggruppamento predefinito.<br/>     |
| <span id="WSA_PNRP_INVALID_IDENTITY"></span><span id="wsa_pnrp_invalid_identity"></span>\_Identity PNRP \_ non valida \_<br/>                                          | Non è possibile accedere A un'identità specificata.<br/>                                                                |
| <span id="WSA_PNRP_TOO_MUCH_LOAD"></span><span id="wsa_pnrp_too_much_load"></span>\_ \_ caricamento troppo elevato di PNRP PNRP \_ \_<br/>                                                  | Non è possibile creare un nome peer perché il computer non dispone delle risorse necessarie per elaborare la richiesta. <br/> |
| <span id="WSAEFAULT"></span><span id="wsaefault"></span>WSAEFAULT<br/>                                                                                             | Operazione non consentita nello stato corrente.<br/>                                                        |
| <span id="WSAEINVAL"></span><span id="wsaeinval"></span>WSAEINVAL<br/>                                                                                             | È stato specificato un parametro o una combinazione di parametri non valida.<br/>                                         |
| <span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>WSAENETUNREACH<br/>                                                                              | Una connessione alla rete va persa.<br/>                                                                    |
| <span id="WSAENOTIMPLEMENTED"></span><span id="wsaenotimplemented"></span>WSAENOTIMPLEMENTED<br/>                                                                  | Una funzionalità specificata non è implementata da PNRP.<br/>                                                   |
| <span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>ILWSAEOPNOTSUPP<br/>                                                                                 | Una funzionalità specificata non è supportata da PNRP.<br/>                                                     |
| <span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>WSAEWOULDBLOCK<br/>                                                                              | Operazione non completata.<br/>                                                                           |
| <span id="__WSASERVICE_NOT_FOUND"></span><span id="__wsaservice_not_found"></span> WSASERVICE \_ non \_ trovato<br/>                                                     | Un provider, uno spazio dei nomi o un ID servizio specificato non è supportato.<br/>                                       |
| <span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>WSASYSNOTREADY<br/>                                                                              | Il servizio non è stato avviato.<br/>                                                                             |



 

 

 




