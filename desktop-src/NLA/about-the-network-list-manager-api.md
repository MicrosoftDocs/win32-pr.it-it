---
title: Informazioni sull'API di Network List Manager
description: Informazioni sull'API di Network List Manager
ms.assetid: 675cf7ed-9f57-4d62-8091-1f4e8812f2ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6230251e627671b7fd33adbf50b3904703bc9847
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713588"
---
# <a name="about-the-network-list-manager-api"></a>Informazioni sull'API di Network List Manager

L'ambiente di rete di Microsoft Windows consente ai computer multihomed di connettersi contemporaneamente a più reti. È possibile che siano disponibili più reti wireless insieme alle connessioni LAN e remote. Network List Manager identifica le reti disponibili e restituisce i dati degli attributi di rete per l'applicazione.

L'API Network List Manager interagisce con il servizio Network List Manager per identificare e recuperare le proprietà di ogni rete a cui il PC si connette. Ogni rete viene identificata in modo univoco con una firma di rete basata sulle proprietà identificabili in modo univoco della rete. Quando un'applicazione viene registrata per le notifiche di Network List Manager, l'applicazione riceve notifiche sulla disponibilità di nuove connessioni di rete o modifiche alle connessioni di rete esistenti. Le applicazioni possono regolare la logica a seconda della rete a cui sono connesse. connessione di rete a cui sono connesse. o le proprietà di rete. Con queste informazioni le applicazioni possono ottimizzare le proprie azioni in base alle condizioni correnti della rete

In Windows Vista sono state introdotte nuove interfacce che è possibile utilizzare per ottenere informazioni dettagliate su queste caratteristiche di rete e altro ancora. Con l'interfaccia [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) è facile enumerare tutte le reti ([**inett**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) visualizzate da un computer o solo le reti connesse o solo le reti disconnesse. L'interfaccia **INetworkListManager** consente inoltre di enumerare facilmente le interfacce di rete in un computer.

Per determinare le proprietà di una connessione di rete, viene utilizzata l'interfaccia di [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) , ovvero nome, descrizione, ID, gestito/autenticato, connesso/disconnesso e altro ancora. È possibile che una singola rete sia connessa a diverse interfacce, quindi tramite un'interfaccia di **inet** è possibile anche enumerare **le istanze dell'interfaccia di** questo sistema.

L'interfaccia di tipo [**inet**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) indica le proprietà pertinenti di un'interfaccia: ID, Guid, tipo (gestito, autenticato) e stato (connesso, disconnesso, V4 locale, V4 Internet, V6 locale, V6 Internet). V4 local indica l'accesso locale IPv4 (Internet Protocol versione 4). V4 Internet significa IPv4 con accesso a Internet. Il protocollo Internet V6 locale e V6 media sono IPv6.

La radice della struttura ad albero di oggetti per il percorso di rete è l'interfaccia [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) . Questa interfaccia è implementata nella coclasse **CLSID \_ NetworkListManager** . Per utilizzare questa interfaccia, è necessario creare l'oggetto com **CLSID \_ NetworkListManager** come dimostrato:


```C++
#include <windows.h>
#include <netlistmgr.h>

#pragma comment(lib, "ole32.lib")

void main()
{
    INetworkListManager *pNetworkListManager = NULL; 
    HRESULT hr = CoCreateInstance(CLSID_NetworkListManager, NULL,
            CLSCTX_ALL, IID_INetworkListManager,
            (LPVOID *)&pNetworkListManager);
}
```



 

 




