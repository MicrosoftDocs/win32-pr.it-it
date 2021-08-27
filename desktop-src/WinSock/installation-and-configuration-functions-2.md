---
description: Le funzioni seguenti vengono implementate nel32.dll Ws2 e devono essere utilizzate dalle applicazioni che installano i provider di servizi dello spazio dei nomi e del trasporto \_ Windows Sockets in un computer.
ms.assetid: 3289737a-77b6-45d1-9c0a-3ed05b3475c2
title: Funzioni di installazione e configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0731eff882c614c19c20d8323d012a7656fc2d8c15072aaafef3d7c91e46e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097861"
---
# <a name="installation-and-configuration-functions"></a>Funzioni di installazione e configurazione

Le funzioni seguenti vengono implementate nel32.dll Ws2 e devono essere utilizzate dalle applicazioni che installano i provider di servizi dello spazio dei nomi e del trasporto \_ Windows Sockets in un computer. Queste funzioni non influiscono sulle applicazioni attualmente in esecuzione, né le modifiche apportate da queste funzioni sono visibili alle applicazioni attualmente in esecuzione.

Per tutti i provider, un identificatore di provider è un GUID generato dallo sviluppatore del provider (tramite l'utilità Uuidgen.exe) e fornito a Ws2 \_32.dll.



| Funzione                                                                      | Descrizione                                                                                                                                              |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSCDeinstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider)                        | Rimuove un provider del servizio di trasporto dal Registro di sistema.                                                                                                  |
| [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32)                      | Rimuove il provider del servizio di trasporto a 32 bit specificato dal Registro di sistema in una piattaforma a 64 bit.                                                          |
| [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)                                | Recupera informazioni sui protocolli di trasporto disponibili.                                                                                               |
| [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)                              | Recupera informazioni sui protocolli di trasporto disponibili nel catalogo a 32 bit nelle piattaforme a 64 bit.                                                     |
| [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider)                            | Registra un nuovo provider del servizio di trasporto.                                                                                                              |
| [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32)                   | Registra un nuovo provider del servizio di trasporto nei database di configurazione di sistema a 32 bit e a 64 bit su una piattaforma a 64 bit.                               |
| [**WSCInstallProviderAndChains**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains)            | Registra un nuovo provider di servizi di trasporto a 32 bit e le catene di protocolli specifiche nel database di configurazione del sistema su una piattaforma a 32 bit.   |
| [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32) | Registra un nuovo provider di trasporto e il relativo protocollo specifico concatena nei database di configurazione di sistema a 32 bit e a 64 bit su una piattaforma a 64 bit. |



 

 

 



