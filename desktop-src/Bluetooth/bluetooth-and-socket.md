---
title: Bluetooth e socket
description: Crea un socket per le connessioni in ingresso o in uscita.
ms.assetid: 21b9cf1f-1a85-4a4b-9557-faa4f32c3696
keywords:
- Bluetooth Bluetooth
- Socket Bluetooth
- Bluetooth e socket Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afaf61e307ce8d5001c2ba5402607b63b1ad6d19317aee044d7a2cac31259b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004301"
---
# <a name="bluetooth-and-socket"></a>Bluetooth e socket

La [**funzione socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) crea un socket per le connessioni in ingresso o in uscita:

Per creare un socket usando Bluetooth, usare le impostazioni seguenti:

-   Il *parametro af* della funzione [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) è sempre impostato su AF **\_ BTH** per Bluetooth socket.
-   Il *parametro di* tipo della funzione [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) è sempre **SOCK \_ STREAM;** **SOCK \_ I** socket DGRAM non sono supportati da Bluetooth.
-   Per il *parametro* del protocollo, **BTHPROTO \_ RFCOMM** è il protocollo supportato.

Per altre informazioni, [vedere Windows Socket.](/windows/desktop/WinSock/windows-sockets-start-page-2)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket)
</dt> </dl>

 

 