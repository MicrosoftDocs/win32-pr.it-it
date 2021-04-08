---
description: L'ordine di installazione iniziale dei provider di servizi di trasporto determina l'ordine in cui vengono enumerate tramite WSCEnumProtocols e WSCEnumProtocols32 nell'interfaccia del provider di servizi o tramite WSAEnumProtocols nell'interfaccia dell'applicazione. In particolare, questo ordine regola anche l'ordine in cui i protocolli e i provider di servizi vengono considerati quando un client richiede la creazione di un socket in base alla famiglia di indirizzi, al tipo e all'identificatore del protocollo.
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: Ordinamento del provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c23d9357d30c94b084bf6288013c38a2d46a4b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880454"
---
# <a name="service-provider-ordering"></a>Ordinamento del provider di servizi

L'ordine di installazione iniziale dei provider di servizi di trasporto determina l'ordine in cui vengono enumerate tramite [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) e [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) nell'interfaccia del provider di servizi o tramite [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) nell'interfaccia dell'applicazione. In particolare, questo ordine regola anche l'ordine in cui i protocolli e i provider di servizi vengono considerati quando un client richiede la creazione di un socket in base alla famiglia di indirizzi, al tipo e all'identificatore del protocollo.

Windows Sockets 2 include un'applet denominata Sporder.exe che consente di riordinare i protocolli installati in modo interattivo dopo che i protocolli sono già stati installati. Winsock include anche una DLL ausiliaria, Sporder.dll, che esporta un'interfaccia procedurale per i protocolli di riordinamento. Questa interfaccia procedurale è costituita da una singola procedura denominata [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).

La definizione dell'interfaccia può essere importata in un programma C o C++ per mezzo del file di inclusione sporder. h. Il punto di ingresso può essere collegato tramite il file lib sporder. lib.

 

 



