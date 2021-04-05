---
title: Bluetooth e socket
description: Crea un socket per le connessioni in ingresso o in uscita.
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- Bluetooth Bluetooth
- connettore Bluetooth
- Bluetooth e connettore Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2c2085ee0c61941bab93ed25dd86f5c102d0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727650"
---
# <a name="bluetooth-and-socket"></a>Bluetooth e socket

La funzione [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) crea un socket per le connessioni in ingresso o in uscita.:

Per creare un socket usando Bluetooth, usare le impostazioni seguenti:

-   Il parametro *AF* della funzione [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) è sempre impostato su **AF \_ BTH** per i Socket Bluetooth.
-   Il parametro di *tipo* della funzione [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) è sempre **\_ Stream Sock**; **Calzino \_** I socket DGRAM non sono supportati da Bluetooth.
-   Per il parametro del *protocollo* , **BTHPROTO \_ rfcomm** è il protocollo supportato.

Per ulteriori informazioni, vedere [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**presa**](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 