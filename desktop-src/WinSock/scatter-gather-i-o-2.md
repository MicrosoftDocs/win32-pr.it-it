---
description: Le funzioni WSARecv, WSARecvFrom, WSARecvMsg, WSASend, WSASendMsg e WSASendTo accettano una matrice di buffer dell'applicazione come parametri di input e possono essere usate per l'I/O a dispersione/raccolta (o vettoriali).
ms.assetid: c42e6cea-3b40-44ad-8715-09ce57e82217
title: I/O a dispersione/raccolta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c572892a75b3532d68a39e2fabdcc971f0a3327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310439"
---
# <a name="scattergather-io"></a><span data-ttu-id="d0162-103">I/O a dispersione/raccolta</span><span class="sxs-lookup"><span data-stu-id="d0162-103">Scatter/Gather I/O</span></span>

<span data-ttu-id="d0162-104">Le funzioni [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)e [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) accettano una matrice di buffer dell'applicazione come parametri di input e possono essere usate per l'I/o a dispersione/raccolta (o vettoriali).</span><span class="sxs-lookup"><span data-stu-id="d0162-104">The [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg), [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg), and [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) functions all take an array of application buffers as input parameters and can be used for scatter/gather (or vectored) I/O.</span></span> <span data-ttu-id="d0162-105">Questo può essere molto utile nelle istanze in cui le parti di ogni messaggio trasmesso sono costituite da uno o più componenti di intestazione a lunghezza fissa oltre al corpo del messaggio.</span><span class="sxs-lookup"><span data-stu-id="d0162-105">This can be very useful in instances where portions of each message being transmitted consist of one or more fixed-length header components in addition to the message body.</span></span> <span data-ttu-id="d0162-106">Tali componenti di intestazione non devono essere concatenati dall'applicazione in un singolo buffer contiguo prima dell'invio.</span><span class="sxs-lookup"><span data-stu-id="d0162-106">Such header components need not be concatenated by the application into a single contiguous buffer prior to sending.</span></span> <span data-ttu-id="d0162-107">Analogamente alla ricezione, i componenti dell'intestazione possono essere suddivisi automaticamente in buffer distinti, lasciando il corpo del messaggio da solo.</span><span class="sxs-lookup"><span data-stu-id="d0162-107">Likewise on receiving, the header components can be automatically split off into separate buffers, leaving the message body by itself.</span></span>

<span data-ttu-id="d0162-108">Quando si ricevono più buffer, il completamento si verifica quando i dati arrivano dalla rete, indipendentemente dal fatto che vengano utilizzati tutti i buffer forniti.</span><span class="sxs-lookup"><span data-stu-id="d0162-108">When receiving into multiple buffers, completion occurs as data arrives from the network, regardless of whether all the supplied buffers are utilized.</span></span>

 

 
