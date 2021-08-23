---
description: L'API di Peer Identity Manager usa le funzioni seguenti.
ms.assetid: 7621d26b-92e3-40c9-b0ce-94647d67f2c4
title: Funzioni di Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a640aa7250cdf34fed7440d955a8de8ac7ac1a58316bef3f6e97b3564ac7fd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518571"
---
# <a name="identity-manager-functions"></a>Funzioni di Identity Manager

L'API di Peer Identity Manager usa le funzioni seguenti.



| Funzione                                                           | Descrizione                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerCreatePeerName**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)                   | Crea un nuovo nome in base al nome esistente dell'identità peer e del classificatore specificati. Tuttavia, una nuova identità non viene creata da una chiamata a [**PeerCreatePeerName.**](/windows/desktop/api/P2P/nf-p2p-peercreatepeername)                                                                                                     |
| [**PeerEnumGroups**](/windows/desktop/api/P2P/nf-p2p-peerenumgroups)                           | Crea e restituisce un handle di enumerazione peer utilizzato per enumerare tutti i gruppi peer associati a un'identità peer specifica.                                                                                                                                                                          |
| [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities)                   | Crea e restituisce un handle di enumerazione peer utilizzato per enumerare tutte le identità peer che appartengono a un utente specifico.                                                                                                                                                                                |
| [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration)                   | Rilascia un'enumerazione, ad esempio un record o un'enumerazione di membri, e dealloca tutte le risorse associate all'enumerazione.                                                                                                                                                                   |
| [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)                               | Dealloca un blocco di dati e lo restituisce al pool di memoria.                                                                                                                                                                                                                                         |
| [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount)                       | Restituisce un conteggio degli elementi in un'enumerazione peer.                                                                                                                                                                                                                                                    |
| [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem)                         | Restituisce un numero specifico di elementi da un'enumerazione peer.                                                                                                                                                                                                                                            |
| [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)                   | Crea una nuova identità peer e ne restituisce il nome. Il nome dell'identità peer deve essere passato in tutte le chiamate successive alle funzioni Peer Identity Manager, Peer Grouping o PNRP che operano per conto dell'identità peer. Il nome dell'identità peer specifica l'identità peer in uso. |
| [**PeerIdentityDelete**](/windows/desktop/api/P2P/nf-p2p-peeridentitydelete)                   | Elimina un'identità peer. Ciò include la rimozione di tutti i certificati, le chiavi private e tutte le informazioni sul gruppo associate a un'identità peer specificata.                                                                                                                                                   |
| [**PeerIdentityExport**](/windows/desktop/api/P2P/nf-p2p-peeridentityexport)                   | Consente a un utente di esportare un'identità peer. L'utente può quindi trasferire l'identità peer in un computer diverso.                                                                                                                                                                                       |
| [**PeerIdentityGetCryptKey**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetcryptkey)         | Recupera un handle per un provider del servizio di crittografia (CSP).                                                                                                                                                                                                                                          |
| [**PeerIdentityGetDefault**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetdefault)           | Recupera il nome peer predefinito impostato per l'utente corrente.                                                                                                                                                                                                                                              |
| [**PeerIdentityGetFriendlyName**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetfriendlyname) | Restituisce il nome descrittivo dell'identità peer.                                                                                                                                                                                                                                                        |
| [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml)                   | Restituisce una descrizione dell'identità peer, che può quindi essere passata a terze parti e usata per invitare un'identità peer in un gruppo peer. Queste informazioni vengono restituite come frammento XML.                                                                                                           |
| [**PeerIdentityImport**](/windows/desktop/api/P2P/nf-p2p-peeridentityimport)                   | Importa un'identità peer. Se l'identità peer esiste in un computer, **viene restituito PEER \_ E ALREADY \_ \_ EXISTS.**                                                                                                                                                                                        |
| [**PeerIdentitySetFriendlyName**](/windows/desktop/api/P2P/nf-p2p-peeridentitysetfriendlyname) | Modifica il nome descrittivo per un'identità peer specificata. Il nome descrittivo è il nome leggibile dall'utente.                                                                                                                                                                                                |



 

 

 



