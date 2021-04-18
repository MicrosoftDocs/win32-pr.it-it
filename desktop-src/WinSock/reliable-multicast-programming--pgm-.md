---
description: In questa sezione viene descritta l'implementazione del protocollo multicast PGM (Pragmatic General Multicast) in Windows, spesso definita multicast affidabile. Il multicast affidabile viene implementato tramite Windows Sockets in Windows Server 2003 e versioni successive.
ms.assetid: 81c203ed-739f-4a06-99a1-9a99c6164edc
title: Programmazione multicast affidabile (PGM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce57fcce7bf2faf471604bed97d345971801ca1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310452"
---
# <a name="reliable-multicast-programming-pgm"></a><span data-ttu-id="277fa-104">Programmazione multicast affidabile (PGM)</span><span class="sxs-lookup"><span data-stu-id="277fa-104">Reliable Multicast Programming (PGM)</span></span>

<span data-ttu-id="277fa-105">In questa sezione viene descritta l'implementazione del protocollo multicast PGM (Pragmatic General Multicast) in Windows, spesso definita multicast affidabile.</span><span class="sxs-lookup"><span data-stu-id="277fa-105">This section describes the Pragmatic General Multicast (PGM) multicast protocol implementation in Windows, often referred to as reliable multicast.</span></span> <span data-ttu-id="277fa-106">Il multicast affidabile viene implementato tramite Windows Sockets in Windows Server 2003 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="277fa-106">Reliable multicast is implemented through Windows Sockets in Windows Server 2003 and later.</span></span>

<span data-ttu-id="277fa-107">**Windows XP:** Il protocollo PGM è supportato solo quando è installato Microsoft Message Queuing (MSMQ) 3,0.</span><span class="sxs-lookup"><span data-stu-id="277fa-107">**Windows XP:** PGM is only supported when Microsoft Message Queuing (MSMQ) 3.0 is installed.</span></span>

<span data-ttu-id="277fa-108">PGM è un protocollo multicast affidabile e scalabile che consente ai destinatari di rilevare la perdita, richiedere la ritrasmissione di dati persi o notificare a un'applicazione una perdita irreversibile.</span><span class="sxs-lookup"><span data-stu-id="277fa-108">PGM is a reliable and scalable multicast protocol that enables receivers to detect loss, request retransmission of lost data, or notify an application of unrecoverable loss.</span></span> <span data-ttu-id="277fa-109">PGM è un protocollo ricevitore-affidabile, che indica che il ricevitore è responsabile di garantire la ricezione di tutti i dati, assolvere il mittente della responsabilità della ricezione.</span><span class="sxs-lookup"><span data-stu-id="277fa-109">PGM is a receiver-reliable protocol, which means the receiver is responsible for ensuring all data is received, absolving the sender of reception responsibility.</span></span>

<span data-ttu-id="277fa-110">PGM è adatto per le applicazioni che richiedono il recapito di dati multicast senza duplicazione da più origini a più ricevitori.</span><span class="sxs-lookup"><span data-stu-id="277fa-110">PGM is appropriate for applications that require duplicate-free multicast data delivery from multiple sources to multiple receivers.</span></span> <span data-ttu-id="277fa-111">Il protocollo PGM non supporta il recapito riconosciuto né garantisce l'ordine dei pacchetti da più mittenti.</span><span class="sxs-lookup"><span data-stu-id="277fa-111">PGM does not support acknowledged delivery, nor does it guarantee ordering of packets from multiple senders.</span></span>

<span data-ttu-id="277fa-112">Per ulteriori informazioni su PGM, vedere la specifica RFC 3208 disponibile all'indirizzo [www.ietf.org](https://www.ietf.org/).</span><span class="sxs-lookup"><span data-stu-id="277fa-112">For more information about PGM, refer to RFC 3208 available at [www.ietf.org](https://www.ietf.org/).</span></span>

<span data-ttu-id="277fa-113">Questa sezione descrive come usare Reliable Multicast in Windows.</span><span class="sxs-lookup"><span data-stu-id="277fa-113">This section describes how to use reliable multicast on Windows.</span></span> <span data-ttu-id="277fa-114">Negli argomenti seguenti vengono illustrati i vari aspetti della creazione di un'applicazione multicast affidabile mediante Windows Sockets:</span><span class="sxs-lookup"><span data-stu-id="277fa-114">The following topics explain the various aspects of creating a reliable multicast application using Windows Sockets:</span></span>

-   [<span data-ttu-id="277fa-115">Mittenti e ricevitori PGM</span><span class="sxs-lookup"><span data-stu-id="277fa-115">PGM Senders and Receivers</span></span>](pgm-senders-and-receivers.md)
-   [<span data-ttu-id="277fa-116">Opzioni mittente PGM</span><span class="sxs-lookup"><span data-stu-id="277fa-116">PGM Sender Options</span></span>](pgm-sender-options.md)
-   [<span data-ttu-id="277fa-117">Invio e ricezione di dati PGM</span><span class="sxs-lookup"><span data-stu-id="277fa-117">Sending and Receiving PGM Data</span></span>](sending-and-receiving-pgm-data.md)
-   [<span data-ttu-id="277fa-118">Multihoming e PGM</span><span class="sxs-lookup"><span data-stu-id="277fa-118">Multihoming and PGM</span></span>](multihoming-and-pgm.md)
-   [<span data-ttu-id="277fa-119">Opzioni socket PGM</span><span class="sxs-lookup"><span data-stu-id="277fa-119">PGM Socket Options</span></span>](pgm-socket-options.md)

 

 



