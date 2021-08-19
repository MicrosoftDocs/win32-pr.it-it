---
title: Bluetooth e getsockopt
description: Bluetooth usa la funzione getsockopt per eseguire query su vari parametri associati al canale del server o alla connessione.
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- getsockopt
- Bluetooth e getsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee63d8dc1665868023967dd88c5ba223cce538c1fa1d41dd151329f6bf52f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081085"
---
# <a name="bluetooth-and-getsockopt"></a>Bluetooth e getsockopt

Bluetooth usa la [**funzione getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) per eseguire query su vari parametri associati al canale del server o alla connessione. **L'uso di getsockopt** con Bluetooth presenta i requisiti seguenti:

-   Il *parametro s* di [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) deve essere un socket Bluetooth valido.
-   Il *parametro level* di [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) deve essere SOL \_ RFCOMM.

Per un elenco delle opzioni Bluetooth socket disponibili, vedere [Bluetooth e Opzioni socket](bluetooth-and-socket-options.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 