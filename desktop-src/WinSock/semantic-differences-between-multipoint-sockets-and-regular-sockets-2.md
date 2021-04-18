---
title: Differenze semantiche tra i socket multipoint e i socket normali
description: Differenze tra i \_ socket multipoint radice c e i socket da punto a punto regolari.
ms.assetid: fbadfde8-44dc-41ac-bd93-1a22c76ca321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04d95b2637a4f805cea5ee6f138cc6992080a238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310438"
---
# <a name="semantic-differences-between-multipoint-sockets-and-regular-sockets"></a><span data-ttu-id="05de6-103">Differenze semantiche tra i socket multipoint e i socket normali</span><span class="sxs-lookup"><span data-stu-id="05de6-103">Semantic differences between multipoint sockets and regular sockets</span></span>

<span data-ttu-id="05de6-104">Nel piano di controllo sono presenti alcune differenze semantiche significative tra un \_ socket radice c e un socket Point-to-Point normale:</span><span class="sxs-lookup"><span data-stu-id="05de6-104">In the control plane, there are some significant semantic differences between a c\_root socket and a regular point-to-point socket:</span></span>

-   <span data-ttu-id="05de6-105">Il \_ socket radice c può essere usato in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) per unire in join una nuova foglia.</span><span class="sxs-lookup"><span data-stu-id="05de6-105">The c\_root socket can be used in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to join a new a leaf.</span></span>
-   <span data-ttu-id="05de6-106">L'inserimento di un \_ socket radice c in modalità di ascolto (chiamando [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) non impedisce che il \_ socket radice c venga usato in una chiamata a [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) per aggiungere una nuova foglia o per l'invio e la ricezione di dati multipoint.</span><span class="sxs-lookup"><span data-stu-id="05de6-106">Placing a c\_root socket into listening mode (by calling [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen)) does not preclude the c\_root socket from being used in a call to [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add a new leaf, or for sending and receiving multipoint data.</span></span>
-   <span data-ttu-id="05de6-107">La chiusura di un \_ socket radice c causa la \_ notifica di chiusura FD a tutti i socket foglia c associati \_ .</span><span class="sxs-lookup"><span data-stu-id="05de6-107">The closing of a c\_root socket causes all of the associated c\_leaf sockets to get FD\_CLOSE notification.</span></span>

<span data-ttu-id="05de6-108">Non esistono differenze semantiche tra un \_ socket foglia c e un socket normale nel piano di controllo, ad eccezione del fatto che il \_ socket foglia c può essere usato in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf)e l'uso del \_ socket foglia c in [**ascolto**](/windows/desktop/api/Winsock2/nf-winsock2-listen) indica che devono essere accettate solo le richieste di connessione multipoint.</span><span class="sxs-lookup"><span data-stu-id="05de6-108">There are no semantic differences between a c\_leaf socket and a regular socket in the control plane, except that the c\_leaf socket can be used in [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), and the use of c\_leaf socket in [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) indicates that only multipoint connection requests should be accepted.</span></span>

<span data-ttu-id="05de6-109">Nel piano dati, le differenze semantiche tra il \_ socket radice d e un socket da punto a punto normale sono:</span><span class="sxs-lookup"><span data-stu-id="05de6-109">In the data plane, the semantic differences between the d\_root socket and a regular point-to-point socket are:</span></span>

-   <span data-ttu-id="05de6-110">I dati inviati sul \_ socket radice d vengono recapitati a tutte le foglie nella stessa sessione multipoint.</span><span class="sxs-lookup"><span data-stu-id="05de6-110">The data sent on the d\_root socket is delivered to all the leaves in the same multipoint session.</span></span>
-   <span data-ttu-id="05de6-111">I dati ricevuti nel \_ socket radice d possono provenire da una qualsiasi delle foglie.</span><span class="sxs-lookup"><span data-stu-id="05de6-111">The data received on the d\_root socket may be from any of the leaves.</span></span>

<span data-ttu-id="05de6-112">Il \_ socket foglia d nel piano dati radice non presenta alcuna differenza semantica rispetto al socket normale. Tuttavia, nel piano dati non radice, i dati inviati sul \_ socket foglia d passano a tutti gli altri nodi foglia e i dati ricevuti possono provenire da qualsiasi altro nodo foglia.</span><span class="sxs-lookup"><span data-stu-id="05de6-112">The d\_leaf socket in the rooted data plane has no semantic difference from the regular socket, however, in the nonrooted data plane, the data sent on the d\_leaf socket goes to all the other leaf nodes, and the data received could be from any other leaf nodes.</span></span> <span data-ttu-id="05de6-113">Come indicato in precedenza, le informazioni relative al fatto che il \_ socket foglia d si trovi in un piano dati radice o non radice è contenuto nella struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) corrispondente per il socket.</span><span class="sxs-lookup"><span data-stu-id="05de6-113">As mentioned earlier, the information about whether the d\_leaf socket is in a rooted or nonrooted data plane is contained in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the socket.</span></span>

 

 
