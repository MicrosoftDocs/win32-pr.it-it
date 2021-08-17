---
description: In un'applicazione viene utilizzata la funzione WSAEnumProtocols per determinare quali protocolli di trasporto e catene di protocolli sono presenti e per ottenere informazioni su ognuno di essi come contenuto nella struttura INFO WSAPROTOCOL \_ associata.
ms.assetid: 4f38cb07-d824-4d43-abd8-89d58dc15810
title: Uso di più protocolli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf9e1641c8e1ed308561b9e85425005933fceac17b156d1161895f13ad06d55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739961"
---
# <a name="using-multiple-protocols"></a>Uso di più protocolli

In un'applicazione viene utilizzata la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) per determinare quali protocolli di trasporto e catene di protocolli sono presenti e per ottenere informazioni su ognuno di essi come contenuto nella struttura [**INFO WSAPROTOCOL associata. \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)

Nella maggior parte dei casi è presente una singola [**struttura WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per ogni protocollo o catena di protocolli. Tuttavia, alcuni protocolli presentano più comportamenti. Ad esempio, il protocollo SPX è orientato ai messaggi, ovvero i limiti dei messaggi del mittente vengono mantenuti dalla rete, ma il socket di ricezione può ignorare questi limiti del messaggio e considerarli come un flusso di byte. Per SPX potrebbero quindi esistere due voci di struttura **\_ INFO WSAPROTOCOL** diverse, una per ogni comportamento.

In Windows Sockets 2 vengono visualizzati diversi nuovi valori relativi a famiglia di indirizzi, tipo di socket e protocollo. Windows I socket 1.1 supportano una famiglia di indirizzi singoli (AF INET) per IPv4 costituita da un numero ridotto di tipi di socket noti e identificatori \_ di protocollo. Windows Sockets 2 mantiene la famiglia di indirizzi, il tipo di socket e gli identificatori di protocollo esistenti per motivi di compatibilità, ma supporta anche i nuovi valori della famiglia di indirizzi per i nuovi protocolli di trasporto con nuovi tipi di supporto.

Gli identificatori univoci nuovi non sono necessariamente noti, ma questo non dovrebbe costituire un problema. Le applicazioni che devono essere indipendenti dal protocollo sono invitate a selezionare un protocollo in base alla relativa idoneità anziché ai valori assegnati al tipo *di \_ socket* o ai *parametri di* protocollo. L'idoneità del protocollo è indicata dagli attributi di comunicazione, ad esempio il flusso di messaggi e byte e reliable-versus-unreliable, contenuti nella struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) del protocollo. La selezione di protocolli in base all'idoneità rispetto ai nomi di protocollo noti e ai tipi di socket consente alle applicazioni indipendenti dal protocollo di sfruttare i nuovi protocolli di trasporto e i relativi tipi di supporti associati non appena diventano disponibili.

La metà server di un'applicazione client/server offre vantaggi grazie alla definizione di socket di ascolto su tutti i protocolli di trasporto adatti. Il client può quindi stabilire la connessione usando qualsiasi protocollo appropriato. In questo modo, ad esempio, un'applicazione client potrebbe non essere modificata indipendentemente dal fatto che sia in esecuzione in un sistema desktop connesso tramite LAN o in un portatile che usa una rete wireless.

 

 
