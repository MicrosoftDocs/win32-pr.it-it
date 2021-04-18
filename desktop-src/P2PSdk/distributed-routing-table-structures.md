---
description: Le strutture seguenti supportano le funzioni API della tabella di routing distribuita (DRT).
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: Strutture della tabella di routing distribuita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d454d2c28008422da897dc91ca9a3dc29db374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312284"
---
# <a name="distributed-routing-table-structures"></a>Strutture della tabella di routing distribuita

Le strutture seguenti supportano le funzioni API della tabella di routing distribuita (DRT).



| Struttura                                                  | Descrizione                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_dati DRT**](/windows/desktop/api/drt/ns-drt-drt_data)                              | Contiene un BLOB di dati. Questa struttura viene utilizzata da diverse funzioni DRT.                                                                                                                   |
| [**\_registrazione DRT**](/windows/desktop/api/drt/ns-drt-drt_registration)              | Contiene la registrazione della chiave. Si tratta di un membro della struttura dei [**\_ \_ risultati di ricerca DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) e è un argomento passato a [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey). |
| [**\_Indirizzo DRT**](/windows/desktop/api/drt/ns-drt-drt_address)                        | Contiene informazioni sull'endpoint di un nodo DRT che ha partecipato a una ricerca. Queste informazioni sono destinate all'uso nel debug di problemi di connettività.                                   |
| [**\_elenco indirizzi \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_address_list)             | Contiene un set di strutture di [**\_ indirizzi DRT**](/windows/desktop/api/drt/ns-drt-drt_address) che rappresentano i nodi contattati durante la ricerca di una chiave.                                                             |
| [**\_provider di sicurezza DRT \_**](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | Definisce l'interfaccia che deve essere implementata da un provider di sicurezza.                                                                                                                   |
| [**\_provider bootstrap \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | Definisce l'interfaccia che deve essere implementata da un provider bootstrap.                                                                                                                  |
| [**\_Impostazioni DRT**](/windows/desktop/api/drt/ns-drt-drt_settings)                      | Definisce le impostazioni di DRT durante l'inizializzazione. Questa struttura viene passata come argomento a [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).                                                                           |
| [**\_informazioni di ricerca DRT \_**](/windows/desktop/api/drt/ns-drt-drt_search_info)               | Definisce una query di ricerca. Questa struttura viene passata come argomento a [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch).                                                                             |
| [**\_risultato della ricerca DRT \_**](/windows/desktop/api/drt/ns-drt-drt_search_result)           | Contiene un risultato della ricerca. Questa struttura viene restituita da [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult).                                                                                |
| [**\_dati evento \_ DRT**](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | Contiene i dati dell'evento restituiti chiamando [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) dopo che un'applicazione ha ricevuto un segnale di evento.                                                    |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazioni tabella di routing distribuita](distributed-routing-table-enumerations.md)
</dt> <dt>

[Funzioni della tabella di routing distribuita](distributed-routing-table-functions.md)
</dt> <dt>

[Riferimento API Tabella routing distribuito](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



