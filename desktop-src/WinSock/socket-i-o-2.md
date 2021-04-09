---
description: Utilizzo di I/o di blocco, I/o non di blocco con notifica asincrona degli eventi di rete e I/O sovrapposti con indicazione di completamento in Windows Sockets 2 (Winsock).
ms.assetid: 07f34177-72bc-4b2a-b655-57e53d1742b0
title: I/O socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efcd325a0a379671dd39709f37e2c6d2133ca27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129118"
---
# <a name="socket-io"></a><span data-ttu-id="144c5-103">I/O socket</span><span class="sxs-lookup"><span data-stu-id="144c5-103">Socket I/O</span></span>

<span data-ttu-id="144c5-104">Esistono tre modi principali per eseguire operazioni di I/O in Windows Sockets 2:</span><span class="sxs-lookup"><span data-stu-id="144c5-104">There are three primary ways of doing I/O in Windows Sockets 2:</span></span>

-   <span data-ttu-id="144c5-105">Blocco di I/O.</span><span class="sxs-lookup"><span data-stu-id="144c5-105">Blocking I/O.</span></span>
-   <span data-ttu-id="144c5-106">I/O non di blocco insieme alla notifica asincrona degli eventi di rete.</span><span class="sxs-lookup"><span data-stu-id="144c5-106">Nonblocking I/O along with asynchronous notification of network events.</span></span>
-   <span data-ttu-id="144c5-107">I/O sovrapposto con indicazione di completamento.</span><span class="sxs-lookup"><span data-stu-id="144c5-107">Overlapped I/O with completion indication.</span></span>

<span data-ttu-id="144c5-108">Ogni metodo viene descritto nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="144c5-108">We describe each method in the following sections.</span></span> <span data-ttu-id="144c5-109">L'I/O di blocco è il comportamento predefinito. è possibile utilizzare la modalità non di blocco in qualsiasi socket inserito in modalità non di blocco e I/O sovrapposti possono essere eseguiti solo su socket creati con l'attributo Overlapped.</span><span class="sxs-lookup"><span data-stu-id="144c5-109">Blocking I/O is the default behavior, nonblocking mode can be used on any socket that is placed into nonblocking mode, and overlapped I/O can only occur on sockets that are created with the overlapped attribute.</span></span> <span data-ttu-id="144c5-110">È anche interessante notare che le due chiamate per l'invio di: [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) e [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) e le due chiamate per la ricezione di: [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) e [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) implementano ogni tre metodi di i/O.</span><span class="sxs-lookup"><span data-stu-id="144c5-110">It is also interesting to note that the two calls for sending: [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) and the two calls for receiving: [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) and [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) each implement all three methods of I/O.</span></span> <span data-ttu-id="144c5-111">I provider di servizi stabiliscono come eseguire l'operazione di I/O in base alle modalità socket, agli attributi e ai valori dei parametri di input.</span><span class="sxs-lookup"><span data-stu-id="144c5-111">Service providers determine how to perform the I/O operation based on socket modes, attributes, and the input parameter values.</span></span>

 

 
