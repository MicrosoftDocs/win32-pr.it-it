---
title: Polling dello stato del processo
description: Per impostazione predefinita, un'applicazione deve eseguire il polling delle modifiche allo stato di un processo.
ms.assetid: b12ee1e0-d3d9-4d31-b2af-7491480968f0
keywords:
- trasferimento BITS processo, polling
- polling dei bit di stato del processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df7fcde49d7359ff8cfa38326eba1e1e0bfeac5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855530"
---
# <a name="polling-for-the-status-of-the-job"></a><span data-ttu-id="3ac87-105">Polling dello stato del processo</span><span class="sxs-lookup"><span data-stu-id="3ac87-105">Polling for the Status of the Job</span></span>

<span data-ttu-id="3ac87-106">Per impostazione predefinita, un'applicazione deve eseguire il polling delle modifiche allo stato di un processo.</span><span class="sxs-lookup"><span data-stu-id="3ac87-106">By default, an application must poll for changes in the status of a job.</span></span> <span data-ttu-id="3ac87-107">Per acquisire le modifiche nello stato del processo, chiamare il metodo [**Metodo ibackgroundcopyjob:: GetState**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) .</span><span class="sxs-lookup"><span data-stu-id="3ac87-107">To capture changes in the job's state, call the [**IBackgroundCopyJob::GetState**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) method.</span></span> <span data-ttu-id="3ac87-108">Per acquisire le modifiche del numero di byte e di file trasferiti, chiamare il metodo [**Metodo ibackgroundcopyjob:: getProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) .</span><span class="sxs-lookup"><span data-stu-id="3ac87-108">To capture changes in the number of bytes and files transferred, call the [**IBackgroundCopyJob::GetProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) method.</span></span> <span data-ttu-id="3ac87-109">Per recuperare le informazioni sullo stato di avanzamento della parte di risposta di un processo di caricamento-risposta, chiamare il metodo [**IBackgroundCopyJob2:: GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) .</span><span class="sxs-lookup"><span data-stu-id="3ac87-109">To retrieve progress information on the reply portion of an upload-reply job, call the [**IBackgroundCopyJob2::GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) method.</span></span> <span data-ttu-id="3ac87-110">Per un esempio in cui vengono utilizzate le informazioni sullo stato di avanzamento, vedere [determinare lo stato di avanzamento di un processo](determining-the-progress-of-a-job.md).</span><span class="sxs-lookup"><span data-stu-id="3ac87-110">For an example that uses the progress information, see [Determining the Progress of a Job](determining-the-progress-of-a-job.md).</span></span>

<span data-ttu-id="3ac87-111">L' [**enumerazione \_ \_ dello stato del processo BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) definisce gli Stati di un processo e la struttura dello stato di [**\_ \_ avanzamento del processo BG**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) contiene informazioni sul numero di byte e file trasferiti.</span><span class="sxs-lookup"><span data-stu-id="3ac87-111">The [**BG\_JOB\_STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state) enumeration defines the states of a job, and the [**BG\_JOB\_PROGRESS**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) structure contains information on the number of bytes and files transferred.</span></span>

<span data-ttu-id="3ac87-112">Per utilizzare il polling, è necessario creare un meccanismo per avviare il polling.</span><span class="sxs-lookup"><span data-stu-id="3ac87-112">To use polling, you need to create a mechanism to initiate polling.</span></span> <span data-ttu-id="3ac87-113">Ad esempio, creare un timer o usare un pulsante "Aggiorna" nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="3ac87-113">For example, create a timer or use an "Update" button on the user interface.</span></span> <span data-ttu-id="3ac87-114">Tuttavia, potrebbe essere più facile eseguire la registrazione per la notifica degli eventi e ricevere eventi quando lo stato o lo stato di avanzamento viene modificato.</span><span class="sxs-lookup"><span data-stu-id="3ac87-114">However, it might be easier to register for event notification and receive events when the state or progress changes.</span></span> <span data-ttu-id="3ac87-115">Per informazioni sulla notifica degli eventi, vedere la pagina relativa alla [registrazione di un callback com](registering-a-com-callback.md).</span><span class="sxs-lookup"><span data-stu-id="3ac87-115">For information on event notification, see [Registering a COM Callback](registering-a-com-callback.md).</span></span>

<span data-ttu-id="3ac87-116">Nell'esempio seguente viene usato un timer per eseguire il polling dello stato di un processo.</span><span class="sxs-lookup"><span data-stu-id="3ac87-116">The following example uses a timer to poll for the state of a job.</span></span> <span data-ttu-id="3ac87-117">Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido.</span><span class="sxs-lookup"><span data-stu-id="3ac87-117">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
BG_JOB_STATE State;
HANDLE hTimer = NULL;
LARGE_INTEGER liDueTime;
//IBackgroundCopyError* pError = NULL;
//BG_JOB_PROGRESS Progress;
//WCHAR *JobStates[] = { L"Queued", L"Connecting", L"Transferring",
//                       L"Suspended", L"Error", L"Transient Error",
//                       L"Transferred", L"Acknowledged", L"Canceled"
//                     };

liDueTime.QuadPart = -10000000;  //Poll every 1 second
hTimer = CreateWaitableTimer(NULL, FALSE, L"MyTimer");
SetWaitableTimer(hTimer, &liDueTime, 1000, NULL, NULL, 0);

do
{
  WaitForSingleObject(hTimer, INFINITE);

  //Use JobStates[State] to set the window text in a user interface.
  hr = pJob->GetState(&State);
  if (FAILED(hr))
  {
    //Handle error
  }

  if (BG_JOB_STATE_TRANSFERRED == State)
    //Call pJob->Complete(); to acknowledge that the transfer is complete
    //and make the file available to the client.
  else if (BG_JOB_STATE_ERROR == State || BG_JOB_STATE_TRANSIENT_ERROR == State)
    //Call pJob->GetError(&pError); to retrieve an IBackgroundCopyError interface 
    //pointer which you use to determine the cause of the error.
  else if (BG_JOB_STATE_TRANSFERRING == State)
    //Call pJob->GetProgress(&Progress); to determine the number of bytes 
    //and files transferred.
} while (BG_JOB_STATE_TRANSFERRED != State && 
         BG_JOB_STATE_ERROR != State &&
         BG_JOB_STATE_TRANSIENT_ERROR != State);
CancelWaitableTimer(hTimer);
CloseHandle(hTimer);
```



 

 




