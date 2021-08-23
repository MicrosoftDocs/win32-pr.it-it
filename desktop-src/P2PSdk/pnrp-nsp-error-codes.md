---
description: Codici di errore NSP PNRP
ms.assetid: adf40b1a-c5d6-418d-a012-cf6ba7d4fa24
title: Codici di errore NSP PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acee7465a86d56af9b2e07a1ae6948dd1b1a1e9145cee2165b7dd4e90f2a5f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061350"
---
# <a name="pnrp-nsp-error-codes"></a>Codici di errore NSP PNRP

Se la funzione del provider dello spazio dei nomi restituisce un **errore SOCKET \_ ERROR,** è necessario usare [WSAGetLastError](winsock-nsp-reference-links.md) per ottenere altre informazioni sull'errore. L'NSP PNRP restituisce i codici di errore seguenti:



| Termine                                                                                                                                                                     | Descrizione                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>WSA \_ E \_ CANCELLED<br/>                                                                         | Un'operazione viene annullata.<br/>                                                                               |
| <span id="__WSA_E_NO_MORE"></span><span id="__wsa_e_no_more"></span> WSA \_ E \_ NON \_ PIÙ<br/>                                                                         | I risultati di una richiesta risolta non sono pronti. Potrebbe non trattarsi di un errore.<br/>                              |
| <span id="_WSA_IO_PENDING_"></span><span id="_wsa_io_pending_"></span> I/O WSA \_ \_ IN SOSPESO <br/>                                                                      | Operazione non completata.<br/>                                                                           |
| <span id="WSA_NOT_ENOUGH_MEMORY"></span><span id="wsa_not_enough_memory"></span>MEMORIA WSA \_ \_ INSUFFICIENTE \_<br/>                                                      | Memoria insufficiente per completare un'azione specificata.<br/>                                              |
| <span id="WSA_OPERATION_ABORTED"></span><span id="wsa_operation_aborted"></span>OPERAZIONE WSA \_ \_ INTERROTTA<br/>                                                       | Un'operazione viene annullata.<br/>                                                                               |
| <span id="WSA_PNRP_CLOUD_DISABLED"></span><span id="wsa_pnrp_cloud_disabled"></span>CLOUD WSA \_ PNRP \_ \_ DISABILITATO<br/>                                                | Un nome cloud specificato è disabilitato.<br/>                                                                     |
| <span id="WSA_PNRP_CLOUD_NOT_FOUND"></span><span id="wsa_pnrp_cloud_not_found"></span>CLOUD \_ WSA PNRP \_ NON \_ \_ TROVATO<br/>                                            | Un nome cloud specificato non è disponibile.<br/>                                                                |
| <span id="WSA_PNRP_CLOUD_IS_SEARCH_ONLY"></span><span id="wsa_pnrp_cloud_is_search_only"></span>WSA \_ PNRP \_ CLOUD È SOLO \_ \_ \_ RICERCA<br/>                            | Si è tentato di registrare un nome in un cloud configurato per la sola risoluzione.<br/>     |
| <span id="WSA_PNRP_CLIENT_INVALID_COMPARTMENT_ID"></span><span id="wsa_pnrp_client_invalid_compartment_id"></span>ID RAGGRUPPAMENTO \_ CLIENT WSA PNRP \_ NON \_ \_ \_ VALIDO<br/> | Uso di PNRP in un raggruppamento esterno all'impostazione predefinita. PNRP funzionerà solo nel raggruppamento predefinito.<br/>     |
| <span id="WSA_PNRP_INVALID_IDENTITY"></span><span id="wsa_pnrp_invalid_identity"></span>IDENTITÀ WSA \_ PNRP \_ NON \_ VALIDA<br/>                                          | Non è possibile accedere a un'identità specificata.<br/>                                                                |
| <span id="WSA_PNRP_TOO_MUCH_LOAD"></span><span id="wsa_pnrp_too_much_load"></span>WSA \_ PNRP \_ TOO \_ MUCH \_ LOAD<br/>                                                  | Non è possibile creare un nome peer perché il computer non dispone delle risorse necessarie per elaborare la richiesta. <br/> |
| <span id="WSAEFAULT"></span><span id="wsaefault"></span>WSAEFAULT<br/>                                                                                             | Un'operazione non è consentita nello stato corrente.<br/>                                                        |
| <span id="WSAEINVAL"></span><span id="wsaeinval"></span>WSAEINVAL<br/>                                                                                             | È stato specificato un parametro o una combinazione di parametri non valida.<br/>                                         |
| <span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>WSAENETUNREACH<br/>                                                                              | Una connessione alla rete viene persa.<br/>                                                                    |
| <span id="WSAENOTIMPLEMENTED"></span><span id="wsaenotimplemented"></span>WSAENOTIMPLEMENTED<br/>                                                                  | Una funzionalità specificata non viene implementata da PNRP.<br/>                                                   |
| <span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>WSAEOPNOTSUPP<br/>                                                                                 | Una funzionalità specificata non è supportata da PNRP.<br/>                                                     |
| <span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>WSAEWOULDBLOCK<br/>                                                                              | Operazione non completata.<br/>                                                                           |
| <span id="__WSASERVICE_NOT_FOUND"></span><span id="__wsaservice_not_found"></span> WSASERVICE \_ NON \_ TROVATO<br/>                                                     | Un provider, uno spazio dei nomi o un ID servizio specificato non sono supportati.<br/>                                       |
| <span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>WSASYSNOTREADY<br/>                                                                              | Il servizio non è stato avviato.<br/>                                                                             |



 

 

 




