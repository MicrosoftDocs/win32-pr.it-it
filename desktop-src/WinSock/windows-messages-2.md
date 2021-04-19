---
description: Windows Sockets 1,1 ha introdotto il meccanismo di selezione asincrona per fornire indicazioni relative agli eventi di rete che non implicavano il polling o il blocco.
ms.assetid: d536f796-c532-4b57-8dc7-3415661b736b
title: Messaggi di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac0f60bb597a7dd92c0039dd805a971bb8587ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308870"
---
# <a name="windows-messages"></a><span data-ttu-id="e2f16-103">Messaggi di Windows</span><span class="sxs-lookup"><span data-stu-id="e2f16-103">Windows Messages</span></span>

<span data-ttu-id="e2f16-104">Windows Sockets 1,1 ha introdotto il meccanismo di selezione asincrona per fornire indicazioni relative agli eventi di rete che non implicavano il polling o il blocco.</span><span class="sxs-lookup"><span data-stu-id="e2f16-104">Windows Sockets 1.1 introduced the async-select mechanism to provide network event indications that did not involve either polling or blocking.</span></span> <span data-ttu-id="e2f16-105">La funzione [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) viene usata per registrare un interesse in uno o più eventi di rete, come elencato nell'esempio precedente, e fornire un handle di finestra da usare per la notifica.</span><span class="sxs-lookup"><span data-stu-id="e2f16-105">The [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) function is used to register an interest in one or more network events as listed in the preceding, and supply a window handle to be used for notification.</span></span> <span data-ttu-id="e2f16-106">Quando si verifica un evento di rete denominato, viene inviato un messaggio di Windows specificato dal client alla finestra indicata.</span><span class="sxs-lookup"><span data-stu-id="e2f16-106">When a nominated network event occurs, a client-specified Windows message is sent to the indicated window.</span></span> <span data-ttu-id="e2f16-107">Per eseguire questa operazione, il provider di servizi deve usare la funzione [**WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) .</span><span class="sxs-lookup"><span data-stu-id="e2f16-107">The service provider must use the [**WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) function to accomplish this.</span></span>

<span data-ttu-id="e2f16-108">In Windows questo potrebbe non essere il meccanismo di notifica più efficiente ed è poco pratico per i daemon e i servizi che non vogliono aprire alcuna finestra.</span><span class="sxs-lookup"><span data-stu-id="e2f16-108">In Windows, this may not be the most efficient notification mechanism, and is inconvenient for daemons and services that do not want to open any windows.</span></span> <span data-ttu-id="e2f16-109">Per risolvere il problema, è stato introdotto il meccanismo di segnalazione degli oggetti evento descritto nella seguente procedura.</span><span class="sxs-lookup"><span data-stu-id="e2f16-109">The event object signaling mechanism described in the following is introduced to solve this problem.</span></span>

 

 
