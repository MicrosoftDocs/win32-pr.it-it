---
description: Gli oggetti evento Windows Sockets sono semplici costrutti che è possibile creare e chiudere, impostare e cancellare, attendere e sottoporre a polling.
ms.assetid: 65a7627e-150e-4ca3-bc17-d2b380ee02d1
title: Utilizzo di oggetti evento (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26a9b70ff49bf7d46f2907c04fd8911d55dd623
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306888"
---
# <a name="using-event-objects-windows-sockets-2"></a><span data-ttu-id="d2591-103">Utilizzo di oggetti evento (Windows Sockets 2)</span><span class="sxs-lookup"><span data-stu-id="d2591-103">Using Event Objects (Windows Sockets 2)</span></span>

<span data-ttu-id="d2591-104">Gli oggetti evento Windows Sockets sono semplici costrutti che è possibile creare e chiudere, impostare e cancellare, attendere e sottoporre a polling.</span><span class="sxs-lookup"><span data-stu-id="d2591-104">Windows Sockets event objects are simple constructs that can be created and closed, set and cleared, waited upon and polled.</span></span> <span data-ttu-id="d2591-105">Il modello accettato prevede che i client creino un oggetto evento e forniscano l'handle come parametro (o come componente di una struttura di parametri) in funzioni quali [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) e [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d2591-105">The accepted model is for clients to create an event object and supply the handle as a parameter (or as a component of a parameter structure) in functions such as [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="d2591-106">Quando si è verificata la condizione candidata, il provider di servizi utilizza l'handle per impostare l'oggetto evento chiamando [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent).</span><span class="sxs-lookup"><span data-stu-id="d2591-106">When the nominated condition has occurred, the service provider uses the handle to set the event object by calling [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent).</span></span> <span data-ttu-id="d2591-107">Nel frattempo, il client Winsock SPI può bloccarsi e attendere o eseguire il polling finché l'oggetto evento non viene impostato (segnalato).</span><span class="sxs-lookup"><span data-stu-id="d2591-107">Meanwhile, the Winsock SPI client may either block and wait or poll until the event object becomes set (signaled).</span></span> <span data-ttu-id="d2591-108">Il client può successivamente cancellare o reimpostare l'oggetto evento e usarlo di nuovo.</span><span class="sxs-lookup"><span data-stu-id="d2591-108">The client may subsequently clear or reset the event object and use it again.</span></span>

 

 
