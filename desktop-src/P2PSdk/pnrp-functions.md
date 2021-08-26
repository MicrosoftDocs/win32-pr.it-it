---
description: L'API del provider dello spazio dei nomi PNRP usa le funzioni seguenti.
ms.assetid: 7c9f2dd7-8dbc-4bbe-b53c-8036c79faa8a
title: Funzioni PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f109684be61bf1a9a194acb89b22fd4a50be652a6615a18a789e157ca2a5d909
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034381"
---
# <a name="pnrp-functions"></a>Funzioni PNRP

L'API del provider dello spazio dei nomi PNRP usa le funzioni seguenti.



| Funzione                                                             | Descrizione                                                                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerNameToPeerHostName**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname)             | Codifica il nome peer fornito come formato che può essere usato con una chiamata successiva alla [**funzione getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows Sockets. |
| [**PeerHostNameToPeerName**](/windows/desktop/api/P2P/nf-p2p-peerhostnametopeername)             | Decodifica un nome host restituito da [**PeerNameToPeerHostName**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname) nella stringa del nome peer che rappresenta.                            |
| [**Avvio peerPnrp**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartup)                           | Avvia il Peer Name Resolution Protocol (PNRP) per il peer chiamante.                                                                                |
| [**PeerPnrpShutdown**](/windows/desktop/api/P2P/nf-p2p-peerpnrpshutdown)                         | Arresta un'istanza in esecuzione del servizio Peer Name Resolution Protocol (PNRP) e rilascia tutte le risorse associate.                             |
| [**PeerPnrpRegister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpregister)                         | Registra un peer con un cloud PNRP e restituisce un handle che può essere usato per gli aggiornamenti della registrazione.                                                           |
| [**PeerPnrpUpdateRegistration**](/windows/desktop/api/P2P/nf-p2p-peerpnrpupdateregistration)     | Aggiorna le informazioni di registrazione PNRP per un nome.                                                                                                        |
| [**PeerPnrpUnregister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpunregister)                     | Annulla la registrazione di un peer da un cloud PNRP.                                                                                                                        |
| [**PeerPnrpResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpresolve)                           | Ottiene gli indirizzi endpoint registrati per un nome peer specifico.                                                                                        |
| [**PeerPnrpStartResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve)                 | Avvia un'operazione asincrona di risoluzione dei nomi peer.                                                                                                       |
| [**PeerPnrpGetCloudInfo**](/windows/desktop/api/P2P/nf-p2p-peerpnrpgetcloudinfo)                 | Recupera informazioni sui cloud Peer Name Resolution Protocol (PNRP) a cui partecipa il peer chiamante.                                         |
| [**PeerPnrpEndResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpendresolve)                     | Chiude l'handle per un'operazione di risoluzione PNRP asincrona avviata con una precedente chiamata a [**PeerPnrpStartResolve.**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve)      |
| [PNRP e WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md) | Avvia il processo che consente a un'applicazione di risolvere i nomi ed enumerare i cloud di rete.                                                                 |
| [PNRP e WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)     | Termina una query avviata in una chiamata precedente a [**WSALookupServiceBegin.**](winsock-nsp-reference-links.md)                                             |
| [PNRP e WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)   | Corrisponde alle query specificate in una chiamata precedente a [**WSALookupServiceBegin.**](winsock-nsp-reference-links.md)                                                |
| [PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md)                     | Riceve notifiche sulle modifiche all'elenco del cloud di rete e sulla disponibilità dei risultati di una richiesta di risoluzione dei nomi.                                     |
| [PNRP e WSASetService](pnrp-and-wsasetservice.md)                 | Registra o rimuove i [nomi peer](peer-names.md).                                                                                                           |



 

 

 
