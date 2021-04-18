---
description: Differenze tra i socket Point-to-Point regolari e \_ i socket multipoint radice c in Windows Sockets (Winsock) SPI.
ms.assetid: 5476933b-70f2-4dcf-a6e9-f9f4a537c29f
title: Differenze semantiche tra i socket multipoint e i socket normali in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd9e4e94583ee653a8ec0bf19c743dddd3e16253
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309934"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets-in-the-spi"></a><span data-ttu-id="d1ea5-103">Differenze semantiche tra i socket multipoint e i socket normali in SPI</span><span class="sxs-lookup"><span data-stu-id="d1ea5-103">Semantic Differences Between Multipoint Sockets and Regular Sockets in the SPI</span></span>

<span data-ttu-id="d1ea5-104">Nel piano di controllo sono presenti alcune differenze semantiche significative tra un \_ socket radice c e un socket Point-to-Point normale:</span><span class="sxs-lookup"><span data-stu-id="d1ea5-104">In the control plane, there are some significant semantic differences between a c\_root socket and a regular point-to-point socket:</span></span>

-   <span data-ttu-id="d1ea5-105">Il \_ socket radice c può essere usato in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) per aggiungere una nuova foglia.</span><span class="sxs-lookup"><span data-stu-id="d1ea5-105">The c\_root socket can be used in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) to join a new leaf.</span></span>
-   <span data-ttu-id="d1ea5-106">L'inserimento di un \_ socket radice c in modalità di ascolto (chiamando [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) non impedisce che il \_ socket radice c venga utilizzato in una chiamata a [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) per aggiungere una nuova foglia o per l'invio e la ricezione di dati multipoint.</span><span class="sxs-lookup"><span data-stu-id="d1ea5-106">Placing a c\_root socket into the listening mode (by calling [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))) does not preclude the c\_root socket from being used in a call to [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf) to add a new leaf, or for sending and receiving multipoint data.</span></span>
-   <span data-ttu-id="d1ea5-107">La chiusura di un socket radice c provocherà \_ la \_ notifica di chiusura FD a tutti i socket foglia c associati \_ .</span><span class="sxs-lookup"><span data-stu-id="d1ea5-107">The closing of a c\_root socket will cause all the associated c\_leaf sockets to get FD\_CLOSE notification.</span></span>

<span data-ttu-id="d1ea5-108">Non esistono differenze semantiche tra un \_ socket foglia c e un socket normale nel piano di controllo, ad eccezione del fatto che il \_ socket foglia c può essere usato in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)e l'uso del \_ socket foglia c in [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indica che devono essere accettate solo le richieste di connessione multipoint.</span><span class="sxs-lookup"><span data-stu-id="d1ea5-108">There are no semantic differences between a c\_leaf socket and a regular socket in the control plane, except that the c\_leaf socket can be used in [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), and the use of c\_leaf socket in [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) indicates that only multipoint connection requests should be accepted.</span></span>

<span data-ttu-id="d1ea5-109">Nel piano dati, le differenze semantiche tra il \_ socket radice d e un socket da punto a punto normale sono</span><span class="sxs-lookup"><span data-stu-id="d1ea5-109">In the data plane, the semantic differences between the d\_root socket and a regular point-to-point socket are</span></span>

-   <span data-ttu-id="d1ea5-110">I dati inviati nel \_ socket radice d verranno recapitati a tutte le foglie nella stessa sessione multipoint.</span><span class="sxs-lookup"><span data-stu-id="d1ea5-110">The data sent on the d\_root socket will be delivered to all the leaves in the same multipoint session.</span></span>
-   <span data-ttu-id="d1ea5-111">I dati ricevuti nel \_ socket radice d possono provenire da una qualsiasi delle foglie.</span><span class="sxs-lookup"><span data-stu-id="d1ea5-111">The data received on the d\_root socket may be from any of the leaves.</span></span>

<span data-ttu-id="d1ea5-112">Il \_ socket foglia d nel piano dati radice non presenta alcuna differenza semantica rispetto al socket normale. Tuttavia, nel piano dati non radice, i dati inviati sul socket foglia d andranno \_ a tutti gli altri nodi foglia e i dati ricevuti potrebbero provenire da qualsiasi altro nodo foglia.</span><span class="sxs-lookup"><span data-stu-id="d1ea5-112">The d\_leaf socket in the rooted data plane has no semantic difference from the regular socket, however, in the nonrooted data plane, the data sent on the d\_leaf socket will go to all of the other leaf nodes, and the data received could be from any of the other leaf nodes.</span></span> <span data-ttu-id="d1ea5-113">Come indicato in precedenza, le informazioni relative al fatto che il \_ socket foglia d si trovi in un piano dati radice o non radice è contenuto nella struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente per il socket.</span><span class="sxs-lookup"><span data-stu-id="d1ea5-113">As mentioned earlier, the information about whether the d\_leaf socket is in a rooted or nonrooted data plane is contained in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the socket.</span></span>

 

 
