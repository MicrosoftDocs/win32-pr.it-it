---
description: L'helper IP consente di accedere alle informazioni sui protocolli di rete utilizzati nel computer locale.
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: Recupero di informazioni sul Transmission Control Protocol e sul protocollo del datagramma utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a73893bf379dda6a58f86854028967da806863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760844"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a><span data-ttu-id="c9029-103">Recupero di informazioni sul Transmission Control Protocol e sul protocollo del datagramma utente</span><span class="sxs-lookup"><span data-stu-id="c9029-103">Retrieving Information About the Transmission Control Protocol and the User Datagram Protocol</span></span>

<span data-ttu-id="c9029-104">L'helper IP consente di accedere alle informazioni sui protocolli di rete utilizzati nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="c9029-104">IP Helper makes it possible to access information about network protocols that are used on the local computer.</span></span> <span data-ttu-id="c9029-105">Utilizzare le funzioni descritte nei paragrafi seguenti per recuperare informazioni sul Transmission Control Protocol (TCP) e sul protocollo UDP (User Datagram Protocol) nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="c9029-105">Use the functions described in the following paragraphs to retrieve information about the Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) on the local computer.</span></span>

<span data-ttu-id="c9029-106">La funzione [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) recupera le statistiche correnti per TCP.</span><span class="sxs-lookup"><span data-stu-id="c9029-106">The [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function retrieves the current statistics for TCP.</span></span> <span data-ttu-id="c9029-107">Per esempi di codice che coinvolgono **GetTcpStatistics** , vedere [recupero di informazioni con GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="c9029-107">For code samples involving **GetTcpStatistics** see [Retrieving Information Using GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).</span></span>

<span data-ttu-id="c9029-108">La funzione [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) recupera le statistiche correnti per UDP.</span><span class="sxs-lookup"><span data-stu-id="c9029-108">The [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) function retrieves the current statistics for UDP.</span></span>

<span data-ttu-id="c9029-109">La funzione [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) recupera la tabella di connessione TCP.</span><span class="sxs-lookup"><span data-stu-id="c9029-109">The [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) function retrieves the TCP connection table.</span></span> <span data-ttu-id="c9029-110">[**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) recupera la tabella del listener UDP.</span><span class="sxs-lookup"><span data-stu-id="c9029-110">The [**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) retrieves the UDP listener table.</span></span>

<span data-ttu-id="c9029-111">La funzione [**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) consente a uno sviluppatore di impostare lo stato di una connessione TCP specificata su MIB \_ TCP \_ state \_ Delete \_ TCB.</span><span class="sxs-lookup"><span data-stu-id="c9029-111">The [**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) function enables a developer to set the state of a specified TCP connection to MIB\_TCP\_STATE\_DELETE\_TCB.</span></span>

 

 



