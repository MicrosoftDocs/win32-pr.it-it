---
description: Negli argomenti seguenti viene descritto come utilizzare l'API ETW per la traccia eventi.
ms.assetid: 7362874a-8206-4973-bb79-a9eaff55feb4
title: Utilizzo di traccia eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5141c19838796c0ec29f9eb20add689d56b97757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226359"
---
# <a name="using-event-tracing"></a><span data-ttu-id="ae1b4-103">Utilizzo di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="ae1b4-103">Using Event Tracing</span></span>

<span data-ttu-id="ae1b4-104">Negli argomenti seguenti viene descritto come utilizzare l'API ETW per la traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="ae1b4-104">The following topics describe how to use the ETW API for event tracing.</span></span>



| <span data-ttu-id="ae1b4-105">Argomento</span><span class="sxs-lookup"><span data-stu-id="ae1b4-105">Topic</span></span>                                                                          | <span data-ttu-id="ae1b4-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae1b4-106">Description</span></span>                                                                                                             |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae1b4-107">Controllo delle sessioni di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="ae1b4-107">Controlling Event Tracing Sessions</span></span>](controlling-event-tracing-sessions.md)   | <span data-ttu-id="ae1b4-108">Viene descritto come gestire le sessioni di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="ae1b4-108">Describes how to manage event tracing sessions.</span></span>                                                                         |
| [<span data-ttu-id="ae1b4-109">Invio di eventi</span><span class="sxs-lookup"><span data-stu-id="ae1b4-109">Providing Events</span></span>](providing-events.md)                                       | <span data-ttu-id="ae1b4-110">Viene descritto come registrare e instrumentare un provider di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="ae1b4-110">Describes how to register and instrument an event trace provider.</span></span>                                                       |
| [<span data-ttu-id="ae1b4-111">Utilizzo di eventi</span><span class="sxs-lookup"><span data-stu-id="ae1b4-111">Consuming Events</span></span>](consuming-events.md)                                       | <span data-ttu-id="ae1b4-112">Viene descritto come implementare funzioni di callback utilizzate per utilizzare ed elaborare eventi da un file di log di traccia o in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="ae1b4-112">Describes how to implement callback functions used to consume and process events from a trace log file or in real time.</span></span> |
| [<span data-ttu-id="ae1b4-113">Preprocessore traccia software Windows</span><span class="sxs-lookup"><span data-stu-id="ae1b4-113">Windows Software Trace Preprocessor</span></span>](windows-software-trace-preprocessor.md) | <span data-ttu-id="ae1b4-114">Fornisce un meccanismo efficiente per registrare e utilizzare gli eventi che si verificano durante l'esecuzione di un'applicazione o di un driver.</span><span class="sxs-lookup"><span data-stu-id="ae1b4-114">Provides an efficient mechanism to log and consume events that occur during the execution of an application or driver.</span></span>  |



 

<span data-ttu-id="ae1b4-115">Includere il file di intestazione Wmistr. h prima di includere il file di intestazione Evntrace. h.</span><span class="sxs-lookup"><span data-stu-id="ae1b4-115">Include the Wmistr.h header file before including the Evntrace.h header file.</span></span>

 

 



