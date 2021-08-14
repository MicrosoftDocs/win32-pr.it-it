---
title: Interfacce NLM
description: Interfacce NLM
ms.assetid: 57cc2a07-4551-428c-a303-9b1a4510f225
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07751a3f28c713b699cf60aa391d7141b19db0fcafd3ef13437f951c944dcb04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117798508"
---
# <a name="nlm-interfaces"></a>Interfacce NLM

Di seguito sono riportate le interfacce NLM.

| Interfaccia                                                            | Descrizione                                                                                                                                                                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumNetworkConnections**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworkconnections)           | Fornisce un enumeratore standard per le connessioni di rete. Enumera le connessioni di rete attive, disconnesse o tutte all'interno di una rete. Questa interfaccia può essere ottenuta [**dall'interfaccia INetwork.**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) |
| [**IEnumNetworks**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-ienumnetworks)                               | Enumera tutte le reti disponibili nel server. Questa interfaccia può essere ottenuta [**dall'interfaccia INetwork.**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)                                                                                         |
| [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)                                         | Rappresenta una rete nel server. Può anche rappresentare una raccolta di connessioni di rete con una firma di rete simile.                                                                                          |
| [**INetworkConnection**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnection)                     | Rappresenta una singola connessione di rete.                                                                                                                                                                                  |
| [**INetworkConnectionCost**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncost)                | Consente di eseguire query sul costo di rete corrente e sullo stato del piano dati associato a una connessione.                                                                                                                                    |
| [**INetworkConnectionCostEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectioncostevents) | Usato per notificare a un'applicazione gli eventi di modifica dello stato del piano dati e dei costi per una connessione.                                                                                                                               |
| [**INetworkConnectionEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkconnectionevents)         | Interfaccia sink implementata da un client per ricevere eventi correlati alle connessioni di rete. Le applicazioni interessate a eventi di livello granulare inferiore, ad esempio le modifiche di autenticazione, implementano questa interfaccia.       |
| [**INetworkCostManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanager)                   | Consente di eseguire query sui costi a livello di computer e sullo stato del piano dati associati a una connessione usata per la connettività Internet a livello di computer o al primo hop di routing a una destinazione specifica in una connessione. |
| [**INetworkCostManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkcostmanagerevents)       | Usato per inviare una notifica a un'applicazione di eventi correlati a costi e piani dati a livello di computer.                                                                                                                                         |
| [**INetworkEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworkevents)                             | Interfaccia sink implementata da un client per ricevere eventi correlati alla rete. Queste API sono tutte funzioni di callback che vengono chiamate automaticamente quando vengono generati i rispettivi eventi.                                  |
| [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager)                   | Fornisce un set di metodi per eseguire funzioni di gestione degli elenchi di rete.                                                                                                                                                  |
| [**INetworkListManagerEvents**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanagerevents)       | Interfaccia sink implementata da un client per ricevere eventi correlati a Network List Manager. Le applicazioni interessate a eventi di livello granulare superiore, ad esempio la connettività Internet, implementano l'interfaccia .   |



 

 

 




