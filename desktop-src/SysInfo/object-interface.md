---
description: 'Windows fornisce funzioni che eseguono le attività seguenti:'
ms.assetid: 437419c7-d6c5-4cae-b5d0-d552c75d4448
title: Interfaccia oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adc85eafdcfe4bb573d3e156b20f9b74dbf0652
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485245"
---
# <a name="object-interface"></a><span data-ttu-id="7bdeb-103">Interfaccia oggetto</span><span class="sxs-lookup"><span data-stu-id="7bdeb-103">Object Interface</span></span>

<span data-ttu-id="7bdeb-104">Windows fornisce funzioni che eseguono le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="7bdeb-104">Windows provides functions that perform the following tasks:</span></span>

-   <span data-ttu-id="7bdeb-105">Creare un oggetto</span><span class="sxs-lookup"><span data-stu-id="7bdeb-105">Create an object</span></span>
-   <span data-ttu-id="7bdeb-106">Ottenere un handle di oggetto</span><span class="sxs-lookup"><span data-stu-id="7bdeb-106">Get an object handle</span></span>
-   <span data-ttu-id="7bdeb-107">Ottenere informazioni sull'oggetto</span><span class="sxs-lookup"><span data-stu-id="7bdeb-107">Get information about the object</span></span>
-   <span data-ttu-id="7bdeb-108">Impostare le informazioni sull'oggetto</span><span class="sxs-lookup"><span data-stu-id="7bdeb-108">Set information about the object</span></span>
-   <span data-ttu-id="7bdeb-109">Chiudere l'handle dell'oggetto</span><span class="sxs-lookup"><span data-stu-id="7bdeb-109">Close the object handle</span></span>
-   <span data-ttu-id="7bdeb-110">Eliminare definitivamente l'oggetto</span><span class="sxs-lookup"><span data-stu-id="7bdeb-110">Destroy the object</span></span>

<span data-ttu-id="7bdeb-111">Alcune di queste attività non sono necessarie per ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-111">Some of these tasks are not necessary for each object.</span></span> <span data-ttu-id="7bdeb-112">Alcune di queste attività vengono combinate per determinati oggetti.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-112">Some of these tasks are combined for certain objects.</span></span> <span data-ttu-id="7bdeb-113">Ad esempio, un'applicazione può creare un oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-113">For example, an application can create an event object.</span></span> <span data-ttu-id="7bdeb-114">Altre applicazioni possono aprire l'evento per ottenere un handle univoco per questo oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-114">Other applications can open the event to obtain a unique handle to this event object.</span></span> <span data-ttu-id="7bdeb-115">Quando ogni applicazione termina utilizzando l'evento, chiude il relativo handle all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-115">As each application finishes using the event, it closes its handle to the object.</span></span> <span data-ttu-id="7bdeb-116">Quando non sono presenti handle aperti rimanenti per l'oggetto evento, il sistema elimina l'oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-116">When there are no remaining open handles to the event object, the system destroys the event object.</span></span> <span data-ttu-id="7bdeb-117">Un'applicazione può invece ottenere un handle per un oggetto finestra esistente.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-117">In contrast, an application can obtain a handle to an existing window object.</span></span> <span data-ttu-id="7bdeb-118">Quando l'oggetto finestra non è più necessario, l'applicazione deve eliminare definitivamente l'oggetto che invalida l'handle della finestra.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-118">When the window object is no longer needed, the application must destroy the object, which invalidates the window handle.</span></span>

<span data-ttu-id="7bdeb-119">Occasionalmente, un oggetto rimane in memoria dopo la chiusura di tutti gli handle degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-119">Occasionally, an object remains in memory after all object handles have been closed.</span></span> <span data-ttu-id="7bdeb-120">Un thread, ad esempio, può creare un oggetto evento e attendere l'handle dell'evento.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-120">For example, a thread could create an event object and wait on the event handle.</span></span> <span data-ttu-id="7bdeb-121">Mentre il thread è in attesa, è possibile che un altro thread chiuda lo stesso handle di oggetto evento.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-121">While the thread is waiting, another thread could close the same event object handle.</span></span> <span data-ttu-id="7bdeb-122">L'oggetto evento rimane in memoria, senza alcun handle di oggetto evento, fino a quando l'oggetto evento non viene impostato sullo stato segnalato e l'operazione di attesa viene completata.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-122">The event object remains in memory, without any event object handles, until the event object is set to the signaled state and the wait operation is completed.</span></span> <span data-ttu-id="7bdeb-123">A questo punto, il sistema rimuove l'oggetto dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-123">At this time, the system removes the object from memory.</span></span>

<span data-ttu-id="7bdeb-124">Handle e oggetti utilizzano la memoria.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-124">Handles and objects consume memory.</span></span> <span data-ttu-id="7bdeb-125">Pertanto, per mantenere le prestazioni del sistema, è necessario chiudere gli handle ed eliminare gli oggetti non appena non sono più necessari.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-125">Therefore, to preserve system performance, you should close handles and delete objects as soon as they are no longer needed.</span></span> <span data-ttu-id="7bdeb-126">In caso contrario, l'applicazione può influire negativamente sulle prestazioni del sistema, a causa dell'utilizzo eccessivo del file di paging.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-126">If you do not do this, your application can hurt system performance, due to excessive use of the paging file.</span></span>

<span data-ttu-id="7bdeb-127">Al termine di un processo, il sistema chiude automaticamente gli handle ed Elimina gli oggetti creati dal processo.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-127">When a process terminates, the system automatically closes handles and deletes objects created by the process.</span></span> <span data-ttu-id="7bdeb-128">Tuttavia, quando un thread termina, il sistema in genere non chiude gli handle o Elimina gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-128">However, when a thread terminates, the system usually does not close handles or delete objects.</span></span> <span data-ttu-id="7bdeb-129">Le uniche eccezioni sono finestra, Hook, posizione della finestra e oggetti di conversazione DDE (Dynamic Data Exchange); questi oggetti vengono eliminati definitivamente al termine del thread di creazione.</span><span class="sxs-lookup"><span data-stu-id="7bdeb-129">The only exceptions are window, hook, window position, and dynamic data exchange (DDE) conversation objects; these objects are destroyed when the creating thread terminates.</span></span>

 

 



