---
description: L'API del provider dello spazio dei nomi PNRP usa le funzioni seguenti.
ms.assetid: 7c9f2dd7-8dbc-4bbe-b53c-8036c79faa8a
title: Funzioni PNRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0e811c2d10927064e380970456c76f30730ee4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312228"
---
# <a name="pnrp-functions"></a>Funzioni PNRP

L'API del provider dello spazio dei nomi PNRP usa le funzioni seguenti.



| Funzione                                                             | Descrizione                                                                                                                                                  |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerNameToPeerHostName**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname)             | Codifica il nome peer fornito come formato che può essere utilizzato con una chiamata successiva alla funzione [**funzione getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows Sockets. |
| [**PeerHostNameToPeerName**](/windows/desktop/api/P2P/nf-p2p-peerhostnametopeername)             | Decodifica un nome host restituito da [**PeerNameToPeerHostName**](/windows/desktop/api/P2P/nf-p2p-peernametopeerhostname) nella stringa del nome peer che rappresenta.                            |
| [**PeerPnrpStartup**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartup)                           | Avvia il servizio PNRP (Peer Name Resolution Protocol) per il peer chiamante.                                                                                |
| [**PeerPnrpShutdown**](/windows/desktop/api/P2P/nf-p2p-peerpnrpshutdown)                         | Arresta un'istanza in esecuzione del servizio PNRP (Peer Name Resolution Protocol) e rilascia tutte le risorse a esso associate.                             |
| [**PeerPnrpRegister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpregister)                         | Registra un peer con un Cloud PNRP e restituisce un handle che può essere usato per gli aggiornamenti della registrazione.                                                           |
| [**PeerPnrpUpdateRegistration**](/windows/desktop/api/P2P/nf-p2p-peerpnrpupdateregistration)     | Aggiorna le informazioni di registrazione PNRP per un nome.                                                                                                        |
| [**PeerPnrpUnregister**](/windows/desktop/api/P2P/nf-p2p-peerpnrpunregister)                     | Annulla la registrazione di un peer da un Cloud PNRP.                                                                                                                        |
| [**PeerPnrpResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpresolve)                           | Ottiene gli indirizzi endpoint registrati per un nome peer specifico.                                                                                        |
| [**PeerPnrpStartResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve)                 | Avvia un'operazione asincrona di risoluzione del nome peer.                                                                                                       |
| [**PeerPnrpGetCloudInfo**](/windows/desktop/api/P2P/nf-p2p-peerpnrpgetcloudinfo)                 | Recupera informazioni sui Cloud PNRP (Peer Name Resolution Protocol) a cui partecipa il peer chiamante.                                         |
| [**PeerPnrpEndResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpendresolve)                     | Chiude l'handle per un'operazione di risoluzione PNRP asincrona avviata con una precedente chiamata a [**PeerPnrpStartResolve**](/windows/desktop/api/P2P/nf-p2p-peerpnrpstartresolve).      |
| [PNRP e WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md) | Avvia il processo che consente a un'applicazione di risolvere i nomi ed enumerare i cloud di rete.                                                                 |
| [PNRP e WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)     | Termina una query avviata in una chiamata precedente a [**WSALookupServiceBegin**](winsock-nsp-reference-links.md).                                             |
| [PNRP e WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)   | Corrisponde alle query specificate in una chiamata precedente a [**WSALookupServiceBegin**](winsock-nsp-reference-links.md).                                                |
| [PNRP e WSANSPIoctl](pnrp-and-wsanspioctl.md)                     | Riceve le notifiche relative alle modifiche apportate all'elenco di cloud di rete e alla disponibilità dei risultati di una richiesta di risoluzione dei nomi.                                     |
| [PNRP e WSASetService](pnrp-and-wsasetservice.md)                 | Registra o rimuove [i nomi dei peer](peer-names.md).                                                                                                           |



 

 

 
