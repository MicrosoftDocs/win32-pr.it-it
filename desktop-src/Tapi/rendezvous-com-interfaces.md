---
description: Nella tabella seguente sono elencati gli oggetti e le interfacce COM associati ai controlli conferenza Rendezvous.
ms.assetid: d9634586-8315-46d3-9ffc-bfa9a4d7738e
title: Interfacce COM Rendezvous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6df7fbdac45480ae7aa9d5968209f22fabe9a4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311885"
---
# <a name="rendezvous-com-interfaces"></a>Interfacce COM Rendezvous

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Nella tabella seguente sono elencati gli oggetti e le interfacce COM associati ai controlli conferenza Rendezvous.

Per ulteriori informazioni sul Component Object Model (COM), consultare le sezioni pertinenti della piattaforma Software Development Kit (SDK).



| Interfacce                                                         | Descrizione                                                                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**IEnumDialableAddrs**](/windows/desktop/api/Rend/nn-rend-ienumdialableaddrs)                   | Enumera gli indirizzi dialable disponibili nella directory corrente.                                                     |
| [**IEnumDirectory**](/windows/desktop/api/Rend/nn-rend-ienumdirectory)                           | Enumera gli oggetti [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) .                                                                    |
| [**IEnumDirectoryObject**](/windows/desktop/api/Rend/nn-rend-ienumdirectoryobject)               | Enumera gli oggetti [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) .                                                        |
| [**IEnumMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)                         | Enumera gli oggetti [**IMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope) .                                                                    |
| [**IEnumMedia**](ienummedia.md)                                   | Enumera gli oggetti [**ITmedia**](itmedia.md) .                                                                            |
| [**IEnumTime**](ienumtime.md)                                     | Enumera gli oggetti [**ITTime**](ittime.md) .                                                                              |
| [**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)         | Interfaccia principale per il wrapper COM dell'allocazione di indirizzi multicast.                                                           |
| [**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)                         | Fornisce metodi per recuperare e impostare informazioni sul lease degli indirizzi.                                                           |
| [**IMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)                                 | Incapsula tutte le proprietà di un ambito multicast e fornisce i metodi per ottenere informazioni sull'ambito.             |
| [**ITAttributeList**](itattributelist.md)                         | Consente di ottenere e impostare gli attributi non interpretati.                                                                   |
| [**ITConferenceBlob**](itconferenceblob.md)                       | Fornisce l'accesso alle informazioni di conferenza specifiche del provider.                                                              |
| [**ITConnection**](itconnection.md)                               | Fornisce metodi per modificare i fattori di connessione, ad esempio l'indirizzo, l'ambito e la larghezza di banda della conferenza.                       |
| [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)                                 | Ottiene e imposta le informazioni sulla directory e fornisce l'accesso a un determinato oggetto directory.                                |
| [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)                     | Ottiene e imposta informazioni generiche per una conferenza o un utente all'interno di una directory.                                            |
| [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) | Ottiene e imposta informazioni generiche specifiche per una conferenza, ad esempio l'ora di inizio e di fine.                                 |
| [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)             | Ottiene e imposta informazioni generiche specifiche per un utente, ad esempio il nome di un computer che corrisponde al telefono IP primario dell'utente. |
| [**ITILSConfig**](/windows/desktop/api/Rend/nn-rend-itilsconfig)                                 | Ottiene e imposta le informazioni specifiche per il server di una directory ILS specificata.                                                |
| [**ITMedia**](itmedia.md)                                         | Ottiene e imposta le proprietà del supporto di base, ad esempio il nome del supporto e il protocollo di trasporto.                                       |
| [**ITMediaCollection**](itmediacollection.md)                     | Consente l'accesso ai file multimediali in base all'indice. Consente la creazione e l'eliminazione di supporti.                                                     |
| [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous)                               | Interfaccia principale per il controllo Rendezvous.                                                                                |
| [**ITSdp**](itsdp.md)                                             | Modifica il BLOB SDP (Session Description Protocol). Riferimento: RFC 2327.                                             |
| [**ITTime**](ittime.md)                                           | Consente di accedere a un set di orari di attivazione per la sessione.                                                             |
| [**ITTimeCollection**](ittimecollection.md)                       | Consente l'accesso ai componenti temporali in base all'indice. Consente la creazione e l'eliminazione di componenti temporali.                                  |



 

 

 



