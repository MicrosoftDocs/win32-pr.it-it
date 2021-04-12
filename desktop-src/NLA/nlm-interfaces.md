---
title: Interfacce NLM
description: Interfacce NLM
ms.assetid: 57cc2a07-4551-428c-a303-9b1a4510f225
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322086a2860ff9bade47c9971662931f9ecada60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471798"
---
# <a name="nlm-interfaces"></a>Interfacce NLM

Di seguito sono riportate le interfacce NLM.

| Interfaccia                                                            | Descrizione                                                                                                                                                                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumNetworkConnections**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworkconnections)           | Fornisce un enumeratore standard per le connessioni di rete. Enumera le connessioni di rete attive, disconnesse o tutte all'interno di una rete. Questa interfaccia può essere ottenuta dall'interfaccia [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) . |
| [**IEnumNetworks**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworks)                               | Enumera tutte le reti disponibili sul server. Questa interfaccia può essere ottenuta dall'interfaccia [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) .                                                                                         |
| [**Di INet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)                                         | Rappresenta una rete nel server. Può anche rappresentare una raccolta di connessioni di rete con una firma di rete simile.                                                                                          |
| [**INetworkConnection**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnection)                     | Rappresenta una singola connessione di rete.                                                                                                                                                                                  |
| [**INetworkConnectionCost**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncost)                | Utilizzato per eseguire una query sullo stato corrente dei costi di rete e del piano dati associato a una connessione.                                                                                                                                    |
| [**INetworkConnectionCostEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncostevents) | Utilizzato per notificare a un'applicazione i costi e gli eventi di modifica dello stato del piano dati per una connessione.                                                                                                                               |
| [**INetworkConnectionEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectionevents)         | Interfaccia di sink implementata da un client per ricevere eventi correlati alle connessioni di rete. Questa interfaccia viene implementata dalle applicazioni interessate a eventi a livello di granularità inferiore, ad esempio modifiche dell'autenticazione.       |
| [**INetworkCostManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanager)                   | Utilizzato per eseguire query sulle informazioni relative allo stato del piano dati e dei costi a livello di computer associate a una connessione utilizzata per la connettività Internet a livello di computer o al primo hop del routing a una destinazione specifica in una connessione. |
| [**INetworkCostManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanagerevents)       | Consente di notificare a un'applicazione di eventi relativi a costi e piani di dati a livello di computer.                                                                                                                                         |
| [**INetworkEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkevents)                             | Interfaccia di sink implementata da un client per ricevere eventi correlati alla rete. Queste API sono tutte funzioni di callback chiamate automaticamente quando vengono generati i rispettivi eventi.                                  |
| [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager)                   | Fornisce un set di metodi per eseguire le funzioni di gestione dell'elenco di rete.                                                                                                                                                  |
| [**INetworkListManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanagerevents)       | Interfaccia di sink implementata da un client per ricevere eventi correlati a gestione elenchi reti. Le applicazioni interessate a eventi di livello granulare più elevati, come la connettività Internet, implementano l'interfaccia.   |



 

 

 




