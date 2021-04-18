---
description: Affinché un protocollo di trasporto sia accessibile tramite Windows Sockets, è necessario che sia installato correttamente nel sistema e registrato con Windows Sockets.
ms.assetid: 0f0b22e4-81b7-43a7-bc2f-7124fa32d925
title: Configurazione e installazione del trasporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea980740f727e39338c7568f4cc30a961b5484df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306892"
---
# <a name="transport-configuration-and-installation"></a>Configurazione e installazione del trasporto

Affinché un protocollo di trasporto sia accessibile tramite Windows Sockets, è necessario che sia installato correttamente nel sistema e registrato con Windows Sockets. Quando un provider di servizi di trasporto viene installato richiamando il programma di installazione di un fornitore, le informazioni di configurazione devono essere aggiunte a un database di configurazione per fornire al WS2 \_32.dll le informazioni necessarie relative al provider di servizi. Il \_32.dll WS2 Esporta diverse funzioni di installazione, [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider) e [**WSCInstallProviderAndChains**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains), affinché il programma di installazione del fornitore fornisca le informazioni rilevanti sul provider di servizi da installare. Queste informazioni includono, ad esempio, il nome e il percorso della DLL del provider di servizi e un elenco di strutture di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) che questo provider è in grado di supportare. Il \_32.dll WS2 fornisce anche una funzione, [**WSCDeinstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider), per il programma di disinstallazione di un fornitore per rimuovere tutte le informazioni rilevanti dal database di configurazione gestito dall' \_32.dll WS2. Il percorso esatto e il formato di queste informazioni di configurazione sono privati per la \_32.dll WS2 e possono essere modificati solo dalle funzioni sopra indicate.

Sulle piattaforme a 64 bit sono disponibili funzioni simili che operano su cataloghi a 32 bit e 64 bit. Queste funzioni includono [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32), [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32)e [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32).

L'ordine di installazione iniziale dei provider di servizi di trasporto determina l'ordine in cui vengono enumerate tramite [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) e [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) nell'interfaccia del provider di servizi o tramite [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) nell'interfaccia dell'applicazione. In particolare, questo ordine regola anche l'ordine in cui i protocolli e i provider di servizi vengono considerati quando un client richiede la creazione di un socket in base alla famiglia di indirizzi, al tipo e all'identificatore del protocollo. Windows Sockets 2 include un'applet denominata Sporder.exe che consente di riordinare i protocolli installati in modo interattivo dopo che i protocolli sono già stati installati. Windows Sockets 2 include anche una DLL ausiliaria, Sporder.dll, che esporta un'interfaccia procedurale per i protocolli di riordinamento. Questa interfaccia procedurale è costituita da una singola procedura denominata [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).

## <a name="installing-layered-protocols-and-protocol-chains"></a>Installazione di protocolli e catene di protocolli a più livelli

La struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) fornita con ogni protocollo da installare indica se il protocollo è un protocollo di base, un protocollo sovrapposto o una catena di protocolli. Il valore del parametro *ProtocolChain. ChainLen* viene interpretato come illustrato nella tabella seguente.

| Valore | Significato                                           |
|-------|---------------------------------------------------|
| 0     | Protocollo sovrapposto.                                 |
| 1     | Protocollo di base (o catena con un solo componente). |
| >1 | Catena di protocolli.                                   |



 

L'installazione delle catene di protocollo può verificarsi solo dopo l'installazione corretta di tutti i componenti costitutivi (protocolli di base e protocolli a livelli). La struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per una catena di protocolli usa il parametro *ProtocolChain* per descrivere la lunghezza della catena e l'identità di ogni componente. I singoli protocolli che costituiscono una catena vengono elencati in ordine nella matrice ProtocolChain. ChainEntries, con l'elemento zero della matrice corrispondente al primo provider a livelli. I protocolli sono identificati dai relativi valori *CatalogEntryID* , che vengono assegnati da WS2 \_32.dll al momento dell'installazione del protocollo e sono disponibili nella struttura di **\_ informazioni WSAPROTOCOL** per ogni protocollo.

I valori per i parametri rimanenti nella struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) della catena di protocolli devono essere scelti per riflettere gli attributi e gli identificatori che meglio caratterizzano la catena di protocolli nel suo complesso. Quando si selezionano questi valori, gli sviluppatori devono tenere presente che le comunicazioni sulle catene di protocollo possono verificarsi solo quando entrambi gli endpoint dispongono di catene di protocolli compatibili installate e che le applicazioni devono essere in grado di riconoscere la struttura di **\_ informazioni WSAPROTOCOL** corrispondente.

Quando viene installato un protocollo di base, non è necessario eseguire alcuna voce nella matrice *ProtocolChain. ChainEntries* . Viene implicitamente compreso che l'unico componente di questa catena è già identificato nel parametro *CatalogEntryID* della stessa struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . Si noti inoltre che le catene di protocollo non possono includere più istanze dello stesso protocollo a più livelli.

 

 
