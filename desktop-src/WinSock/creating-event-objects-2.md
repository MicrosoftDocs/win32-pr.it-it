---
description: Il \_32.dll WS2 fornisce le funzionalità per la creazione di oggetti evento sia per le applicazioni che per i provider di servizi, anche se nella maggior parte dei casi gli oggetti evento verranno creati dalle applicazioni.
ms.assetid: 86da30ad-80bc-4982-9306-bbe29b1bab19
title: Creazione di oggetti evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec202f8f17790ed85979a8287005aa65374a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307000"
---
# <a name="creating-event-objects"></a><span data-ttu-id="d9362-103">Creazione di oggetti evento</span><span class="sxs-lookup"><span data-stu-id="d9362-103">Creating Event Objects</span></span>

<span data-ttu-id="d9362-104">Il \_32.dll WS2 fornisce le funzionalità per la creazione di oggetti evento sia per le applicazioni che per i provider di servizi, anche se nella maggior parte dei casi gli oggetti evento verranno creati dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d9362-104">The Ws2\_32.dll provides facilities for event object creation to both applications and service providers, although in most instances event objects will be created by applications.</span></span> <span data-ttu-id="d9362-105">I servizi oggetto evento vengono resi disponibili per i provider di servizi Windows Sockets tramite [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) semplicemente come un meccanismo pratico per qualsiasi elaborazione interna che può trarre vantaggio dallo stesso.</span><span class="sxs-lookup"><span data-stu-id="d9362-105">Event object services are made available to Windows Sockets service providers through [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) simply as a convenience mechanism for any internal processing that may benefit from same.</span></span> <span data-ttu-id="d9362-106">Si noti che l'handle dell'oggetto evento è valido solo nel contesto del processo chiamante.</span><span class="sxs-lookup"><span data-stu-id="d9362-106">Note that the event object handle is only valid in the context of the calling process.</span></span> <span data-ttu-id="d9362-107">Negli ambienti Windows la realizzazione degli oggetti evento avviene tramite i servizi eventi nativi forniti dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d9362-107">In Windows environments the realization of event objects is through the native event services provided by the operating system.</span></span>

 

 



