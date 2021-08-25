---
description: Perché un protocollo di trasporto sia accessibile tramite Windows Socket, deve essere installato correttamente nel sistema e registrato con Windows Socket.
ms.assetid: 0f0b22e4-81b7-43a7-bc2f-7124fa32d925
title: Configurazione e installazione del trasporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1ec75810790df0d9373e8f3ee184f2dbd51d9bb5c37d7721097febe23a8aee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733241"
---
# <a name="transport-configuration-and-installation"></a>Configurazione e installazione del trasporto

Perché un protocollo di trasporto sia accessibile tramite Windows Socket, deve essere installato correttamente nel sistema e registrato con Windows Socket. Quando un provider del servizio di trasporto viene installato richiamando il programma di installazione di un fornitore, le informazioni di configurazione devono essere aggiunte a un database di configurazione per fornire al32.dll Ws2 le informazioni necessarie relative al provider di \_ servizi. Il32.dll Ws2 esporta diverse funzioni di \_ installazione, [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider) e [**WSCInstallProviderAndChains,**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains)per il programma di installazione del fornitore per fornire le informazioni pertinenti sul provider di servizi da installare. Queste informazioni includono, ad esempio, il nome e il percorso della DLL del provider di servizi e un elenco di strutture [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) che il provider può supportare. Il32.dll Ws2 fornisce anche una \_ funzione, [**WSCDeinstallProvider,**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider)per il programma di installazione di un fornitore per rimuovere tutte le informazioni rilevanti dal database di configurazione gestito dal32.dll \_ Ws2. La posizione e il formato esatti di queste informazioni di configurazione sono privati per il32.dll Ws2 e possono essere manipolati solo dalle funzioni indicate \_ in precedenza.

Nelle piattaforme a 64 bit sono disponibili funzioni simili che operano su cataloghi a 32 bit e a 64 bit. Queste funzioni includono [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32), [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32)e [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32).

L'ordine in cui i provider del servizio di trasporto vengono installati inizialmente determina l'ordine in cui vengono enumerati tramite [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) e [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) nell'interfaccia del provider di servizi o [**tramite WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) nell'interfaccia dell'applicazione. Ancora più importante, questo ordine determina anche l'ordine in cui i protocolli e i provider di servizi vengono considerati quando un client richiede la creazione di un socket in base alla famiglia di indirizzi, al tipo e all'identificatore di protocollo. Windows Sockets 2 include un'applet denominata Sporder.exe che consente al catalogo dei protocolli installati di essere riordinato in modo interattivo dopo che i protocolli sono già stati installati. Windows Sockets 2 include anche una DLL ausiliaria, Sporder.dll, che esporta un'interfaccia procedurale per il riordinamento dei protocolli. Questa interfaccia procedurale è costituita da una singola procedura [**denominata WSCWriteProviderOrder.**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder)

## <a name="installing-layered-protocols-and-protocol-chains"></a>Installazione di protocolli a più livelli e catene di protocolli

La [**struttura WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) fornita con ogni protocollo da installare indica se il protocollo è un protocollo di base, un protocollo a più livelli o una catena di protocolli. Il valore del *parametro ProtocolChain.ChainLen* viene interpretato come illustrato nella tabella seguente.

| Valore | Significato                                           |
|-------|---------------------------------------------------|
| 0     | Protocollo a più livelli.                                 |
| 1     | Protocollo di base (o catena con un solo componente). |
| >1 | Catena di protocolli.                                   |



 

L'installazione delle catene di protocolli può essere eseguita solo dopo la corretta installazione di tutti i componenti costitutivi (protocolli di base e protocolli a più livelli). La [**struttura WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per una catena di protocolli usa il parametro *ProtocolChain* per descrivere la lunghezza della catena e l'identità di ogni componente. I singoli protocolli che costituiscono una catena sono elencati in ordine nella matrice ProtocolChain.ChainEntries, con l'zero elemento della matrice corrispondente al primo provider a livelli. I protocolli vengono identificati dai relativi valori *CatalogEntryID,* assegnati dal32.dll Ws2 in fase di installazione del protocollo, e sono disponibili nella struttura \_ **WSAPROTOCOL \_ INFO** per ogni protocollo.

I valori per i parametri rimanenti nella struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) della catena di protocolli devono essere scelti per riflettere gli attributi e gli identificatori che meglio caratterizzano l'intera catena di protocolli. Quando si selezionano questi valori, gli sviluppatori devono tenere presente che le comunicazioni sulle catene di protocollo possono verificarsi solo quando entrambi gli endpoint hanno catene di protocollo compatibili installate e che le applicazioni devono essere in grado di riconoscere la struttura **WSAPROTOCOL \_ INFO** corrispondente.

Quando viene installato un protocollo di base, non è necessario creare voci nella matrice *ProtocolChain.ChainEntries.* È implicitamente comprensibile che l'unico componente di questa catena sia già identificato nel parametro *CatalogEntryID* della stessa [**struttura WSAPROTOCOL \_ INFO.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) Si noti anche che le catene di protocolli potrebbero non includere più istanze dello stesso protocollo a più livelli.

 

 
