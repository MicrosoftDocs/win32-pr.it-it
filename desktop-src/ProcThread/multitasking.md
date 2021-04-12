---
description: Un sistema operativo multitasking divide il tempo di elaborazione disponibile tra i processi o i thread che lo richiedono.
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: Multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d06c1d8d44f397f06923c793971bcb20f35b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345466"
---
# <a name="multitasking"></a><span data-ttu-id="f0155-103">Multitasking</span><span class="sxs-lookup"><span data-stu-id="f0155-103">Multitasking</span></span>

<span data-ttu-id="f0155-104">Un sistema operativo multitasking divide il tempo di elaborazione disponibile tra i processi o i thread che lo richiedono.</span><span class="sxs-lookup"><span data-stu-id="f0155-104">A multitasking operating system divides the available processor time among the processes or threads that need it.</span></span> <span data-ttu-id="f0155-105">Il sistema è progettato per il multitasking preemptive. alloca un *intervallo di tempo* del processore a ogni thread che esegue.</span><span class="sxs-lookup"><span data-stu-id="f0155-105">The system is designed for preemptive multitasking; it allocates a processor *time slice* to each thread it executes.</span></span> <span data-ttu-id="f0155-106">Il thread attualmente in esecuzione viene sospeso al termine del periodo di tempo specificato, consentendo l'esecuzione di un altro thread.</span><span class="sxs-lookup"><span data-stu-id="f0155-106">The currently executing thread is suspended when its time slice elapses, allowing another thread to run.</span></span> <span data-ttu-id="f0155-107">Quando il sistema passa da un thread a un altro, Salva il contesto del thread con precedenza e ripristina il contesto salvato del thread successivo nella coda.</span><span class="sxs-lookup"><span data-stu-id="f0155-107">When the system switches from one thread to another, it saves the context of the preempted thread and restores the saved context of the next thread in the queue.</span></span>

<span data-ttu-id="f0155-108">L'entità della porzione di tempo dipende dal sistema operativo e dal processore.</span><span class="sxs-lookup"><span data-stu-id="f0155-108">The length of the time slice depends on the operating system and the processor.</span></span> <span data-ttu-id="f0155-109">Poiché ogni intervallo di tempo è ridotto (circa 20 millisecondi), più thread sembrano essere in esecuzione nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="f0155-109">Because each time slice is small (approximately 20 milliseconds), multiple threads appear to be executing at the same time.</span></span> <span data-ttu-id="f0155-110">Questa situazione si verifica essenzialmente nei sistemi a più processori, in cui i thread eseguibili vengono distribuiti tra i vari processori disponibili.</span><span class="sxs-lookup"><span data-stu-id="f0155-110">This is actually the case on multiprocessor systems, where the executable threads are distributed among the available processors.</span></span> <span data-ttu-id="f0155-111">Tuttavia, è necessario prestare attenzione quando si usano più thread in un'applicazione, perché le prestazioni del sistema possono diminuire se sono presenti troppi thread.</span><span class="sxs-lookup"><span data-stu-id="f0155-111">However, you must use caution when using multiple threads in an application, because system performance can decrease if there are too many threads.</span></span>

<span data-ttu-id="f0155-112">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="f0155-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="f0155-113">Vantaggi del multitasking</span><span class="sxs-lookup"><span data-stu-id="f0155-113">Advantages of Multitasking</span></span>](advantages-of-multitasking.md)
-   [<span data-ttu-id="f0155-114">Quando usare il multitasking</span><span class="sxs-lookup"><span data-stu-id="f0155-114">When to Use Multitasking</span></span>](when-to-use-multitasking.md)
-   [<span data-ttu-id="f0155-115">Considerazioni sul multitasking</span><span class="sxs-lookup"><span data-stu-id="f0155-115">Multitasking Considerations</span></span>](multitasking-considerations.md)

 

 



