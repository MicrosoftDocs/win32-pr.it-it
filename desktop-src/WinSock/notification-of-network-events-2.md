---
description: Una delle responsabilità più importanti di un provider di servizi di trasporto dati è quella di fornire indicazioni al client quando si verificano determinati eventi di rete.
ms.assetid: 7b60a775-ed20-4048-bd0b-9d43d090f82c
title: Notifica degli eventi di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090d3adda7d34c0fe49eb14936bc01bf20878b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879193"
---
# <a name="notification-of-network-events"></a><span data-ttu-id="3c935-103">Notifica degli eventi di rete</span><span class="sxs-lookup"><span data-stu-id="3c935-103">Notification of Network Events</span></span>

<span data-ttu-id="3c935-104">Una delle responsabilità più importanti di un provider di servizi di trasporto dati è quella di fornire indicazioni al client quando si verificano determinati eventi di rete.</span><span class="sxs-lookup"><span data-stu-id="3c935-104">One of the most important responsibilities of a data transport service provider is that of providing indications to the client when certain network events have occurred.</span></span> <span data-ttu-id="3c935-105">L'elenco degli eventi di rete definiti è costituito dagli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="3c935-105">The list of defined network events consists of the following:</span></span>

-   <span data-ttu-id="3c935-106">**FD \_ Connetti**: è stata completata una connessione a un host remoto o a una sessione multicast.</span><span class="sxs-lookup"><span data-stu-id="3c935-106">**FD\_CONNECT**— A connection to a remote host or to a multicast session has been completed.</span></span>
-   <span data-ttu-id="3c935-107">**FD \_ ACCEPT**: un host remoto sta effettuando una richiesta di connessione.</span><span class="sxs-lookup"><span data-stu-id="3c935-107">**FD\_ACCEPT**— A remote host is making a connection request.</span></span>
-   <span data-ttu-id="3c935-108">**FD \_ READ**: sono arrivati i dati di rete che è possibile leggere.</span><span class="sxs-lookup"><span data-stu-id="3c935-108">**FD\_READ**— Network data has arrived which is available to be read.</span></span>
-   <span data-ttu-id="3c935-109">**FD \_ WRITE**: lo spazio è diventato disponibile nei buffer del provider di servizi, in modo che ora possano essere inviati dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="3c935-109">**FD\_WRITE**— Space has become available in the service provider's buffers so that additional data may now be sent.</span></span>
-   <span data-ttu-id="3c935-110">**FD \_ OOB**: i dati fuori banda sono disponibili per la lettura.</span><span class="sxs-lookup"><span data-stu-id="3c935-110">**FD\_OOB**— Out of band data is available to be read.</span></span>
-   <span data-ttu-id="3c935-111">**FD \_ CLOSE**: l'host remoto ha chiuso la connessione.</span><span class="sxs-lookup"><span data-stu-id="3c935-111">**FD\_CLOSE**— The remote host has closed down the connection.</span></span>
-   <span data-ttu-id="3c935-112">**FD \_ QOS**: si è verificata una modifica nei livelli QoS negoziato.</span><span class="sxs-lookup"><span data-stu-id="3c935-112">**FD\_QOS**— A change has occurred in negotiated QoS levels.</span></span>
-   <span data-ttu-id="3c935-113">**FD \_ \_QoS del gruppo**: riservato.</span><span class="sxs-lookup"><span data-stu-id="3c935-113">**FD\_GROUP\_QOS**— Reserved.</span></span>
-   <span data-ttu-id="3c935-114">**FD \_ \_ \_ Modifica dell'interfaccia di routing**: un'interfaccia locale da usare per raggiungere la destinazione specificata nell' **interfaccia di \_ routing sio \_ \_ modificare IOCTL** è cambiata.</span><span class="sxs-lookup"><span data-stu-id="3c935-114">**FD\_ROUTING\_INTERFACE\_CHANGE**— A local interface that should be used to reach the destination specified in **SIO\_ROUTING\_INTERFACE\_CHANGE IOCTL** has changed.</span></span>
-   <span data-ttu-id="3c935-115">**FD \_ \_ \_ Modifica elenco indirizzi**: l'elenco degli indirizzi locali a cui è possibile associare l'applicazione è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="3c935-115">**FD\_ADDRESS\_LIST\_CHANGE**— The list of local addresses to which application can bind has changed.</span></span>

<span data-ttu-id="3c935-116">Il set di eventi di rete enumerato in precedenza viene talvolta indicato come evento **FD \_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="3c935-116">The set of network events enumerated above is sometimes referred to as the **FD\_XXX** events.</span></span> <span data-ttu-id="3c935-117">L'indicazione dell'occorrenza di uno o più eventi di rete di questo tipo può essere fornita in diversi modi, a seconda del modo in cui il client richiede la notifica.</span><span class="sxs-lookup"><span data-stu-id="3c935-117">Indication of the occurrence of one or more of such network events may be given in a number of ways depending on how the client requests notification.</span></span>

 

 



