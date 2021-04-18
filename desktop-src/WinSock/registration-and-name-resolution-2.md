---
description: Windows Sockets 2 è un set di funzioni che standardizza il modo in cui le applicazioni accedono e usano i vari servizi di denominazione di rete.
ms.assetid: e245475c-26cc-491f-b335-b1b6a816dc3c
title: Registrazione e risoluzione dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8abc778c09fa2c0cc8de00db0edaa846ed2ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309940"
---
# <a name="registration-and-name-resolution"></a>Registrazione e risoluzione dei nomi

Windows Sockets 2 è un set di funzioni che standardizza il modo in cui le applicazioni accedono e usano i vari servizi di denominazione di rete. Quando si usano queste funzioni, le applicazioni non devono distinguere i protocolli molto diversi associati ai servizi nomi, ad esempio DNS, NIS, X. 500, SAP e così via. Per mantenere la compatibilità completa con Windows Sockets 1,1, le funzioni di ricerca di database **getXbyY** e asincrone **WSAAsyncGetXbyY** esistenti continuano a essere supportate, ma sono implementate nell'interfaccia del provider di servizi Windows Sockets in termini di nuove funzionalità di risoluzione dei nomi. Per ulteriori informazioni, vedere le funzioni [**GetServByName**](/windows/desktop/api/winsock/nf-winsock-getservbyname) e [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) . Vedere anche [risoluzione dei nomi compatibili per TCP/IP in Windows sockets 1,1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).

Questa sezione descrive le funzionalità di registrazione e risoluzione dei nomi disponibili per gli sviluppatori Winsock. Nell'elenco seguente vengono descritti gli argomenti di questa sezione:

-   [Risoluzione dei nomi indipendente dal protocollo](protocol-independent-name-resolution-2.md)
-   [Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Winsock](about-winsock.md)
</dt> <dt>

[Uso di Winsock](using-winsock.md)
</dt> </dl>

 

 



