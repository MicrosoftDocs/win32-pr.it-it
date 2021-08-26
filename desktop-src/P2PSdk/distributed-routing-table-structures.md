---
description: Le strutture seguenti supportano le funzioni API DRT (Distributed Routing Table).
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: Strutture delle tabelle di routing distribuito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7613b63559eadd2b19229228b9d57fb438b6bd2bbb1b5a9d335a6513c1e8bfee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978941"
---
# <a name="distributed-routing-table-structures"></a>Strutture delle tabelle di routing distribuito

Le strutture seguenti supportano le funzioni API DRT (Distributed Routing Table).



| Struttura                                                  | Descrizione                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATI \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_data)                              | Contiene un BLOB di dati. Questa struttura viene usata da diverse funzioni DRT.                                                                                                                   |
| [**REGISTRAZIONE \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_registration)              | Contiene la registrazione della chiave. Questo è un membro della struttura [**DRT \_ SEARCH \_ RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) ed è un argomento passato [**a DrtRegisterKey.**](/windows/desktop/api/drt/nf-drt-drtregisterkey) |
| [**INDIRIZZO \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_address)                        | Contiene informazioni sull'endpoint su un nodo DRT che ha partecipato a una ricerca. Queste informazioni sono destinate all'uso nel debug dei problemi di connettività.                                   |
| [**ELENCO DI \_ INDIRIZZI \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_address_list)             | Contiene un set di [**strutture \_ ADDRESS DRT**](/windows/desktop/api/drt/ns-drt-drt_address) che rappresentano i nodi contattati durante una ricerca di una chiave.                                                             |
| [**PROVIDER DI SICUREZZA DRT \_ \_**](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | Definisce l'interfaccia che deve essere implementata da un provider di sicurezza.                                                                                                                   |
| [**DRT \_ BOOTSTRAP \_ PROVIDER**](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | Definisce l'interfaccia che deve essere implementata da un provider bootstrap.                                                                                                                  |
| [**IMPOSTAZIONI \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_settings)                      | Definisce le impostazioni DRT in fase di inizializzazione. Questa struttura viene passata come argomento a [**DrtOpen.**](/windows/desktop/api/drt/nf-drt-drtopen)                                                                           |
| [**INFORMAZIONI DI \_ RICERCA \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info)               | Definisce una query di ricerca. Questa struttura viene passata come argomento a [**DrtStartSearch.**](/windows/desktop/api/drt/nf-drt-drtstartsearch)                                                                             |
| [**RISULTATO DELLA \_ RICERCA \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result)           | Contiene un risultato della ricerca. Questa struttura viene restituita [**da DrtGetSearchResult.**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)                                                                                |
| [**DATI \_ DELL'EVENTO \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | Contiene i dati dell'evento restituiti chiamando [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) dopo che un'applicazione riceve un segnale di evento.                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazioni di tabelle di routing distribuito](distributed-routing-table-enumerations.md)
</dt> <dt>

[Funzioni delle tabelle di routing distribuito](distributed-routing-table-functions.md)
</dt> <dt>

[Informazioni di riferimento API Tabella routing distribuito](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



