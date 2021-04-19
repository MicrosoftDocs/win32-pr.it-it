---
description: Gli esempi di applicazioni WMI in questa sezione sono scritti in C++.
ms.assetid: 5c4c4c4c-adbc-4702-a6fe-5f98a6db3ba1
ms.tgt_platform: multiple
title: Esempi di applicazioni WMI C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883b51bd00de5e3938fef8467c68d299ac60683a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309753"
---
# <a name="wmi-c-application-examples"></a><span data-ttu-id="5f587-103">Esempi di applicazioni WMI C++</span><span class="sxs-lookup"><span data-stu-id="5f587-103">WMI C++ Application Examples</span></span>

<span data-ttu-id="5f587-104">Gli esempi di applicazioni WMI in questa sezione sono scritti in C++.</span><span class="sxs-lookup"><span data-stu-id="5f587-104">The WMI application examples in this section are written in C++.</span></span> <span data-ttu-id="5f587-105">Illustrano una serie di attività che possono essere completate usando i componenti WMI e offrono un'alternativa rispetto all'uso di Visual Basic script.</span><span class="sxs-lookup"><span data-stu-id="5f587-105">They demonstrate a range of tasks that can be completed using WMI components and offer an alternative over using Visual Basic scripts.</span></span> <span data-ttu-id="5f587-106">Ogni applicazione è suddivisa in una serie di passaggi in modo analogo, in modo che le sezioni di codice di esempi diversi possano essere facilmente combinate per formare applicazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="5f587-106">Each application is separated into a series of steps in a similar way so that code sections from different examples can easily be combined to form customized applications.</span></span>

<span data-ttu-id="5f587-107">La tabella seguente elenca gli esempi di C++ in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="5f587-107">The following table lists the C++ examples in this section.</span></span>



| <span data-ttu-id="5f587-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="5f587-108">Example</span></span>                                                                                                                                  | <span data-ttu-id="5f587-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f587-109">Description</span></span>                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f587-110">Esempio: recupero di dati WMI dal computer locale</span><span class="sxs-lookup"><span data-stu-id="5f587-110">Example: Getting WMI Data from the Local Computer</span></span>](example--getting-wmi-data-from-the-local-computer.md)                               | <span data-ttu-id="5f587-111">Questo esempio consente di connettersi allo spazio dei nomi WMI nel computer locale e di ottenere i dati da una query nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="5f587-111">This example connects to the WMI namespace on the local computer and gets data from a query on the local computer.</span></span> <span data-ttu-id="5f587-112">I dati vengono raccolti semisincrona.</span><span class="sxs-lookup"><span data-stu-id="5f587-112">The data is gathered semisynchronously.</span></span> |
| [<span data-ttu-id="5f587-113">Esempio: recupero di dati WMI dal computer locale in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="5f587-113">Example: Getting WMI Data from the Local Computer Asynchronously</span></span>](example--getting-wmi-data-from-the-local-computer-asynchronously.md) | <span data-ttu-id="5f587-114">Questo esempio consente di connettersi allo spazio dei nomi WMI nel computer locale e di ottenere i dati da una query nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="5f587-114">This example connects to the WMI namespace on the local computer and gets data from a query on the local computer.</span></span> <span data-ttu-id="5f587-115">I dati vengono raccolti in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="5f587-115">The data is gathered asynchronously.</span></span>    |
| [<span data-ttu-id="5f587-116">Esempio: recupero di dati WMI da un computer remoto</span><span class="sxs-lookup"><span data-stu-id="5f587-116">Example: Getting WMI Data from a Remote Computer</span></span>](example--getting-wmi-data-from-a-remote-computer.md)                                 | <span data-ttu-id="5f587-117">Questo esempio consente di connettersi allo spazio dei nomi WMI in un computer remoto e di ottenere i dati da una query nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="5f587-117">This example connects to the WMI namespace on a remote computer and gets data from a query on the remote computer.</span></span> <span data-ttu-id="5f587-118">I dati vengono raccolti semisincrona.</span><span class="sxs-lookup"><span data-stu-id="5f587-118">The data is gathered semisynchronously.</span></span> |
| [<span data-ttu-id="5f587-119">Esempio: chiamata a un metodo del provider</span><span class="sxs-lookup"><span data-stu-id="5f587-119">Example: Calling a Provider Method</span></span>](example--calling-a-provider-method.md)                                                             | <span data-ttu-id="5f587-120">In questo esempio viene eseguita la connessione allo spazio dei nomi WMI nel computer locale e viene chiamato un metodo in WMI.</span><span class="sxs-lookup"><span data-stu-id="5f587-120">This example connects to the WMI namespace on the local computer and calls a method in WMI.</span></span> <span data-ttu-id="5f587-121">Il metodo viene eseguito in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="5f587-121">The method is executed synchronously.</span></span>                          |
| [<span data-ttu-id="5f587-122">Esempio: ricezione di notifiche di eventi tramite WMI</span><span class="sxs-lookup"><span data-stu-id="5f587-122">Example: Receiving Event Notifications Through WMI</span></span>](example--receiving-event-notifications-through-wmi-.md)                            | <span data-ttu-id="5f587-123">Questo esempio consente di connettersi allo spazio dei nomi WMI nel computer locale e riceve un evento dal computer locale.</span><span class="sxs-lookup"><span data-stu-id="5f587-123">This example connects to the WMI namespace on the local computer and receives an event from the local computer.</span></span> <span data-ttu-id="5f587-124">L'evento viene ricevuto semisincrona.</span><span class="sxs-lookup"><span data-stu-id="5f587-124">The event is received semisynchronously.</span></span>   |



 

 

 



