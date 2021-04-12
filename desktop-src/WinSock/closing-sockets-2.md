---
description: WSPCloseSocket rilascia il descrittore di socket in modo che tutte le operazioni in sospeso in tutti i thread dello stesso processo vengano interrotte e qualsiasi altro riferimento a esso avrà esito negativo.
ms.assetid: 658d0c35-05d4-4b51-a4d3-a3b441a2c735
title: Chiusura di socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d0c877767925f67e07427a77dc8ec8445f30c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526190"
---
# <a name="closing-sockets"></a>Chiusura di socket

[**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) rilascia il descrittore di socket in modo che tutte le operazioni in sospeso in tutti i thread dello stesso processo vengano interrotte e qualsiasi altro riferimento a esso avrà esito negativo. Si noti che è necessario utilizzare un conteggio dei riferimenti per i socket condivisi e solo se si tratta dell'ultimo riferimento a un socket sottostante, se le informazioni associate a questo socket vengono scartate, purché la chiusura normale non sia richiesta (ovvero, \_ DONTLINGER non è impostato). Nel caso in cui \_ venga impostato DONTLINGER, i dati in coda per la trasmissione verranno inviati, se possibile, prima del rilascio delle informazioni associate al socket. Per ulteriori informazioni, vedere **WSPCloseSocket** .

Per i provider di servizi nonIFS, è necessario richiamare [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) per rilasciare nuovamente il punto di controllo del socket alla DLL di Windows Sockets 2.

 

 
