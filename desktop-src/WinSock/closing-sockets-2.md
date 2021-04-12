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
# <a name="closing-sockets"></a><span data-ttu-id="0f6a4-103">Chiusura di socket</span><span class="sxs-lookup"><span data-stu-id="0f6a4-103">Closing Sockets</span></span>

<span data-ttu-id="0f6a4-104">[**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) rilascia il descrittore di socket in modo che tutte le operazioni in sospeso in tutti i thread dello stesso processo vengano interrotte e qualsiasi altro riferimento a esso avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0f6a4-104">[**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) releases the socket descriptor so that any pending operations in any threads of the same process will be aborted, and any further reference to it will fail.</span></span> <span data-ttu-id="0f6a4-105">Si noti che è necessario utilizzare un conteggio dei riferimenti per i socket condivisi e solo se si tratta dell'ultimo riferimento a un socket sottostante, se le informazioni associate a questo socket vengono scartate, purché la chiusura normale non sia richiesta (ovvero, \_ DONTLINGER non è impostato).</span><span class="sxs-lookup"><span data-stu-id="0f6a4-105">Note that a reference count should be employed for shared sockets, and only if this is the last reference to an underlying socket, should the information associated with this socket be discarded, provided graceful close is not requested (that is, SO\_DONTLINGER is not set).</span></span> <span data-ttu-id="0f6a4-106">Nel caso in cui \_ venga impostato DONTLINGER, i dati in coda per la trasmissione verranno inviati, se possibile, prima del rilascio delle informazioni associate al socket.</span><span class="sxs-lookup"><span data-stu-id="0f6a4-106">In the case of SO\_DONTLINGER being set, any data queued for transmission will be sent, if possible, before information associated with the socket is released.</span></span> <span data-ttu-id="0f6a4-107">Per ulteriori informazioni, vedere **WSPCloseSocket** .</span><span class="sxs-lookup"><span data-stu-id="0f6a4-107">See **WSPCloseSocket** for more information.</span></span>

<span data-ttu-id="0f6a4-108">Per i provider di servizi nonIFS, è necessario richiamare [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) per rilasciare nuovamente il punto di controllo del socket alla DLL di Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="0f6a4-108">For nonIFS service providers, [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle) must be invoked to release the socket handle back to the Windows Sockets 2 DLL.</span></span>

 

 
