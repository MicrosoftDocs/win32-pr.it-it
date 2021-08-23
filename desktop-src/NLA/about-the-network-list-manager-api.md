---
title: Informazioni sull'API Network List Manager
description: Informazioni sull'API Network List Manager
ms.assetid: 675cf7ed-9f57-4d62-8091-1f4e8812f2ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704bedb3a1029c2be3c123c65a896b1765f191b886af9b354d747abd5e1698e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065175"
---
# <a name="about-the-network-list-manager-api"></a>Informazioni sull'API Network List Manager

L'Windows di rete microsoft consente ai computer multihomed di connettersi a più reti contemporaneamente. Potrebbero essere disponibili più reti wireless insieme alla rete LAN e alle connessioni remote. Network List Manager identifica le reti disponibili e restituisce i dati degli attributi di rete all'applicazione.

L'API network list manager interagisce con il servizio Network List Manager per identificare e recuperare le proprietà di ogni rete a cui si connette il PC. Ogni rete viene identificata in modo univoco con una firma di rete in base alle proprietà identificabili in modo univoco di tale rete. Quando un'applicazione si registra per le notifiche di Network List Manager, l'applicazione riceve notifiche sulla disponibilità di nuove connessioni di rete o sulle modifiche alle connessioni di rete esistenti. Le applicazioni possono modificare la logica a seconda della rete a cui sono connesse. a quale connessione di rete sono connessi; o le proprietà di rete. Con queste informazioni le applicazioni possono ottimizzare le azioni in base alle condizioni di rete correnti

Windows Vista introduce nuove interfacce che possono essere usate per ottenere informazioni dettagliate su queste caratteristiche di rete e altro ancora. Con [**l'interfaccia INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) è facile enumerare tutte le reti [**(INetwork)**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)che un computer ha mai visto, solo le reti connesse o solo le reti disconnesse. **L'interfaccia INetworkListManager** semplifica anche l'enumerazione delle interfacce di rete in un computer.

[**L'interfaccia INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) viene usata per determinare le proprietà di una connessione di rete: nome, descrizione, ID, gestito/autenticato, connesso/disconnesso e altro ancora. È possibile che una singola rete sia connessa a più interfacce, quindi tramite **un'interfaccia INetwork** è anche possibile enumerare le istanze dell'interfaccia **INetwork** in uso.

[**L'interfaccia INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) indica le proprietà pertinenti di un'interfaccia: ID, GUID, Tipo (gestito, autenticato) e Stato (connesso, disconnesso, V4 locale, V4 Internet, V6 Locale, V6 Internet). V4 Locale significa protocollo IP versione 4 (IPv4) locale. V4 Internet significa IPv4 con accesso a Internet. V6 Locale e V6 Internet significa IPv6.

La radice dell'albero di oggetti per Il percorso di rete è [**l'interfaccia INetworkListManager.**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) Questa interfaccia viene implementata nella **\_ coclasse NetworkListManager del CLSID.** Per usare questa interfaccia, è necessario creare l'oggetto **COM \_ NetworkListManager del CLSID** come illustrato:


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



 

 




