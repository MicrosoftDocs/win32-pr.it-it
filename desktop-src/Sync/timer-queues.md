---
description: La funzione CreateTimerQueue ha provocato crea una coda per i timer.
ms.assetid: ee85a6c3-3a1d-4f94-9112-cb8247b2a189
title: Code timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ad2f94612c234b3ec0d1d75fa723c4e86e6fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312745"
---
# <a name="timer-queues"></a><span data-ttu-id="5c779-103">Code timer</span><span class="sxs-lookup"><span data-stu-id="5c779-103">Timer Queues</span></span>

<span data-ttu-id="5c779-104">La funzione [**CreateTimerQueue ha provocato**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) crea una coda per i timer.</span><span class="sxs-lookup"><span data-stu-id="5c779-104">The [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) function creates a queue for timers.</span></span> <span data-ttu-id="5c779-105">I timer in questa coda, detti timer della *coda del timer*, sono oggetti leggeri che consentono di specificare una funzione di callback da chiamare quando arriva il tempo di scadenza specificato.</span><span class="sxs-lookup"><span data-stu-id="5c779-105">Timers in this queue, known as *timer-queue timers*, are lightweight objects that enable you to specify a callback function to be called when the specified due time arrives.</span></span> <span data-ttu-id="5c779-106">L'operazione Wait viene eseguita da un thread nel [pool di thread](../procthread/thread-pooling.md).</span><span class="sxs-lookup"><span data-stu-id="5c779-106">The wait operation is performed by a thread in the [thread pool](../procthread/thread-pooling.md).</span></span>

<span data-ttu-id="5c779-107">Per aggiungere un timer alla coda, chiamare la funzione [**CreateTimerQueueTimer ha provocato**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="5c779-107">To add a timer to the queue, call the [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function.</span></span> <span data-ttu-id="5c779-108">Per aggiornare un timer della coda del timer, chiamare la funzione [**ChangeTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="5c779-108">To update a timer-queue timer, call the [**ChangeTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) function.</span></span> <span data-ttu-id="5c779-109">È possibile specificare una funzione di callback che deve essere eseguita da un thread di lavoro dal pool di thread quando il timer scade.</span><span class="sxs-lookup"><span data-stu-id="5c779-109">You can specify a callback function to be executed by a worker thread from the thread pool when the timer expires.</span></span>

<span data-ttu-id="5c779-110">Per annullare un timer in sospeso, chiamare la funzione [**DeleteTimerQueueTimer ha provocato**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="5c779-110">To cancel a pending timer, call the [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) function.</span></span> <span data-ttu-id="5c779-111">Al termine della coda di timer, chiamare la funzione [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) per eliminare la coda del timer.</span><span class="sxs-lookup"><span data-stu-id="5c779-111">When you are finished with the queue of timers, call the [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) function to delete the timer queue.</span></span> <span data-ttu-id="5c779-112">Eventuali timer in sospeso nella coda vengono annullati ed eliminati.</span><span class="sxs-lookup"><span data-stu-id="5c779-112">Any pending timers in the queue are canceled and deleted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c779-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5c779-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c779-114">Uso delle code timer</span><span class="sxs-lookup"><span data-stu-id="5c779-114">Using Timer Queues</span></span>](using-timer-queues.md)
</dt> </dl>

 

 
