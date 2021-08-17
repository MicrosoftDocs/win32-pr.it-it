---
description: L'ordine di installazione iniziale dei provider di servizi di trasporto determina l'ordine in cui vengono enumerati tramite WSCEnumProtocols e WSCEnumProtocols32 nell'interfaccia del provider di servizi o tramite WSAEnumProtocols nell'interfaccia dell'applicazione. Ancora più importante, questo ordine determina anche l'ordine in cui i protocolli e i provider di servizi vengono considerati quando un client richiede la creazione di un socket in base alla famiglia di indirizzi, al tipo e all'identificatore di protocollo.
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: Ordinamento del provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 445fcc0cadafae8fd61ee2e34a872485b67466037c1dc71e34ab173156c8d9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740582"
---
# <a name="service-provider-ordering"></a>Ordinamento del provider di servizi

L'ordine di installazione iniziale dei provider di servizi di trasporto determina l'ordine in cui vengono enumerati tramite [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) e [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) nell'interfaccia del provider di servizi o [**tramite WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) nell'interfaccia dell'applicazione. Ancora più importante, questo ordine determina anche l'ordine in cui i protocolli e i provider di servizi vengono considerati quando un client richiede la creazione di un socket in base alla famiglia di indirizzi, al tipo e all'identificatore di protocollo.

Windows Sockets 2 include un'applet denominata Sporder.exe che consente al catalogo dei protocolli installati di essere riordinato in modo interattivo dopo che i protocolli sono già stati installati. Winsock include anche una DLL ausiliaria, Sporder.dll, che esporta un'interfaccia procedurale per il riordino dei protocolli. Questa interfaccia procedurale è costituita da una singola routine [**denominata WSCWriteProviderOrder.**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder)

La definizione dell'interfaccia può essere importata in un programma C o C++ tramite il file di inclusione Sporder.h. Il punto di ingresso può essere collegato tramite il file lib Sporder.lib.

 

 



