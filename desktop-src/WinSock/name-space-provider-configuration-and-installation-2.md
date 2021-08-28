---
description: WSCEnableNSProviderWSCEnableNSProvider32WSCInstallNameSpaceWSCInstallNameSpace32WSCInstallNameSpaceExWSCInstallNameSpaceEx32WSCUnInstallNameSpaceWSCUnInstallNameSpace32WSCWriteNameSpaceOrderWSCWriteNameSpaceOrder32
ms.assetid: 3dd289fb-eebb-48b2-a887-eeb60322ab09
title: Configurazione e installazione del provider dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d420e9322d1d39816cdb9b3812b23b1e7e72e945c3d0f2ef95e7edff77f12276
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121371"
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

Come accennato in precedenza, l'applicazione di installazione per un provider dello spazio dei nomi deve chiamare [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) o [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) per eseguire la registrazione con il32.dll Ws2 e fornire informazioni di configurazione \_ statiche. Per eseguire l'installazione nel catalogo a 32 bit in una piattaforma a 64 bit, il provider dello spazio dei nomi deve chiamare [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) o [**WSCInstallNameSpaceEx32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) Il32.dll WS2 usa queste informazioni per eseguire la funzione di routing e nell'implementazione di \_ [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) e [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa). La [**funzione WSCUnInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace) viene usata per rimuovere un provider dello spazio dei nomi dal Registro di sistema e la funzione [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) viene usata per alternare un provider tra gli stati attivo e inattivo.

In una piattaforma a 64 [**bit, WSCUnInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace32) e [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) sono funzioni simili per gestire il catalogo a 32 bit.

I risultati di queste tre operazioni non sono visibili alle applicazioni attualmente caricate e in esecuzione. Solo le applicazioni che iniziano l'esecuzione dopo l'esecuzione di queste operazioni saranno interessate da tali operazioni.

Questa architettura supporta in modo esplicito la creazione di istanze di più provider di spazi dei nomi all'interno di una singola DLL, tuttavia ogni provider deve avere un identificatore univoco del provider dello spazio dei nomi (GUID) allocato e deve essere eseguita una chiamata separata a [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) o [**WSCInstallNameSpaceEx**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex) per ogni creazione di istanza .Nelle piattaforme a 64 bit le funzioni per il catalogo a 32 bit [**sono WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) e [**WSCInstallNameSpaceEx32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) Tale provider può determinare quale istanza viene richiamata perché l'identificatore del provider di spazi dei nomi (NSP) viene visualizzato come parametro in ogni funzione del provider di servizi di rete.

 

 



