---
description: Un'applicazione utilizza la funzione WSAEnumProtocols per determinare quali protocolli di trasporto e catene di protocolli sono presenti e per ottenere informazioni su ciascuno di essi come contenuto nella \_ struttura di informazioni WSAPROTOCOL associata.
ms.assetid: 4f38cb07-d824-4d43-abd8-89d58dc15810
title: Uso di più protocolli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab9a37dcc90f1094126f701641539dd3f26a1a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129111"
---
# <a name="using-multiple-protocols"></a>Uso di più protocolli

Un'applicazione utilizza la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) per determinare quali protocolli di trasporto e catene di protocolli sono presenti e per ottenere informazioni su ciascuno di essi come contenuto nella struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) associata.

Nella maggior parte dei casi esiste una singola struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per ogni protocollo o catena di protocolli. Tuttavia, alcuni protocolli presentano più comportamenti. Il protocollo SPX, ad esempio, è orientato ai messaggi, ovvero i limiti dei messaggi del mittente vengono conservati dalla rete, ma il Socket ricevente può ignorare questi limiti dei messaggi e considerarli come un flusso di byte. Pertanto, per SPX possono esistere due diverse voci della struttura di **\_ informazioni WSAPROTOCOL** , una per ogni comportamento.

In Windows Sockets 2 sono visualizzati diversi nuovi valori di famiglia di indirizzi, tipo di socket e protocollo. Windows Sockets 1,1 supportava una famiglia di indirizzi singolo (AF \_ inet) per IPv4 costituito da un numero ridotto di tipi di socket noti e identificatori di protocollo. Windows Sockets 2 mantiene la famiglia di indirizzi, il tipo di socket e gli identificatori di protocollo esistenti per motivi di compatibilità, ma supporta anche i nuovi valori della famiglia di indirizzi per i nuovi protocolli di trasporto con nuovi tipi di supporto.

I nuovi identificatori univoci non sono necessariamente noti, ma questo non dovrebbe rappresentare un problema. Le applicazioni che devono essere indipendenti dal protocollo sono consigliate per selezionare un protocollo in base alla relativa idoneità anziché ai valori assegnati al *\_ tipo di socket* o ai parametri del *protocollo* . L'idoneità del protocollo è indicata dagli attributi di comunicazione, ad esempio il flusso di messaggi e di byte e da quelli affidabili, che sono contenuti nella struttura del protocollo [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . Se si selezionano i protocolli sulla base dell'idoneità, anziché i nomi di protocollo noti e i tipi di socket, le applicazioni indipendenti dal protocollo possono sfruttare i nuovi protocolli di trasporto e i tipi di supporto associati, man mano che diventano disponibili.

La metà del server di un'applicazione client/server si avvale stabilendo socket in ascolto su tutti i protocolli di trasporto appropriati. Il client può quindi stabilire la connessione utilizzando un protocollo appropriato. Questo consente, ad esempio, a un'applicazione client di non essere modificata se era in esecuzione su un sistema desktop connesso tramite LAN o su un computer portatile tramite una rete wireless.

 

 
