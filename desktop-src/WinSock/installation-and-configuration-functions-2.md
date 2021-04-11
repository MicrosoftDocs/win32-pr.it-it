---
description: Le funzioni seguenti sono implementate nel \_32.dll WS2 e sono progettate per essere utilizzate dalle applicazioni che installano i provider di servizi di trasporto e spazio dei nomi Windows Sockets in un computer.
ms.assetid: 3289737a-77b6-45d1-9c0a-3ed05b3475c2
title: Funzioni di installazione e configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c72bb3ddaedb0b1d97c52d961293c161fe63c7ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226086"
---
# <a name="installation-and-configuration-functions"></a>Funzioni di installazione e configurazione

Le funzioni seguenti sono implementate nel \_32.dll WS2 e sono progettate per essere utilizzate dalle applicazioni che installano i provider di servizi di trasporto e spazio dei nomi Windows Sockets in un computer. Queste funzioni non influiscono sulle applicazioni attualmente in esecuzione, né le modifiche apportate da queste funzioni sono visibili alle applicazioni attualmente in esecuzione.

Per tutti i provider, un identificatore del provider è un GUID generato dallo sviluppatore del provider (tramite l'utilità Uuidgen.exe) e fornito a WS2 \_32.dll.



| Funzione                                                                      | Descrizione                                                                                                                                              |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSCDeinstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider)                        | Rimuove un provider di servizi di trasporto dal registro di sistema.                                                                                                  |
| [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32)                      | Rimuove il provider di servizi di trasporto a 32 bit specificato dal registro di sistema in una piattaforma a 64 bit.                                                          |
| [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)                                | Recupera le informazioni sui protocolli di trasporto disponibili.                                                                                               |
| [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)                              | Recupera le informazioni sui protocolli di trasporto disponibili nel catalogo a 32 bit sulle piattaforme a 64 bit.                                                     |
| [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider)                            | Registra un nuovo provider di servizi di trasporto.                                                                                                              |
| [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32)                   | Registra un nuovo provider di servizi di trasporto nei database di configurazione di sistema a 32 bit e a 64 bit in una piattaforma a 64 bit.                               |
| [**WSCInstallProviderAndChains**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains)            | Registra un nuovo provider di servizi di trasporto a 32 bit, nonché le catene di protocolli specifiche nel database di configurazione di sistema in una piattaforma a 32 bit.   |
| [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32) | Registra un nuovo provider di trasporto e le catene di protocolli specifiche nei database di configurazione di sistema a 32 bit e a 64 bit in una piattaforma a 64 bit. |



 

 

 



