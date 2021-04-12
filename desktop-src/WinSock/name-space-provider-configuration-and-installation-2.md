---
description: WSCEnableNSProviderWSCEnableNSProvider32WSCInstallNameSpaceWSCInstallNameSpace32WSCInstallNameSpaceExWSCInstallNameSpaceEx32WSCUnInstallNameSpaceWSCUnInstallNameSpace32WSCWriteNameSpaceOrderWSCWriteNameSpaceOrder32
ms.assetid: 3dd289fb-eebb-48b2-a887-eeb60322ab09
title: Configurazione e installazione del provider dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c87de8fee4ccaea0fb6978037e1e41684b56267
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526142"
---
# <a name="namespace-provider-configuration-and-installation"></a>Configurazione e installazione del provider dello spazio dei nomi

-   [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider)
-   [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32)
-   [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace)
-   [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32)
-   [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex)
-   [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32)
-   [**WSCUnInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace)
-   [**WSCUnInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace32)
-   [**WSCWriteNameSpaceOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwritenamespaceorder)
-   [**WSCWriteNameSpaceOrder32**](/windows/desktop/api/Sporder/nf-sporder-wscwritenamespaceorder32)

Come indicato in precedenza, l'applicazione di installazione per un provider dello spazio dei nomi deve chiamare [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) o [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) per eseguire la registrazione con WS2 \_32.dll e fornire informazioni statiche sulla configurazione. Per eseguire l'installazione nel catalogo a 32 bit su una piattaforma a 64 bit, il provider dello spazio dei nomi deve chiamare [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) o [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32). Il \_32.dll WS2 utilizza queste informazioni per eseguire la funzione di routing e la relativa implementazione di [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) e [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa). La funzione [**WSCUnInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace) viene utilizzata per rimuovere un provider dello spazio dei nomi dal registro di sistema e la funzione [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) viene utilizzata per alternare un provider tra gli stati attivo e inattivo.

In una piattaforma a 64 bit, [**WSCUnInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace32) e [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) sono funzioni simili per gestire il catalogo a 32 bit.

I risultati di queste tre operazioni non sono visibili alle applicazioni attualmente caricate e in esecuzione. Verranno interessate solo le applicazioni che iniziano l'esecuzione dopo queste operazioni.

Questa architettura supporta in modo esplicito la creazione di un'istanza di più provider dello spazio dei nomi all'interno di una singola DLL, tuttavia ogni provider deve disporre di un identificatore univoco del provider di spazio dei nomi (GUID) allocato ed è necessario [**che venga**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32)eseguita una chiamata separata a [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) o [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) per ogni creazione di istanza (sulle piattaforme a 64 bit, le funzioni per il [**Catalogo a 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) Tale provider può determinare quale istanza viene richiamata perché l'identificatore del provider dello spazio dei nomi (NSP) viene visualizzato come parametro in ogni funzione NSP.

 

 



