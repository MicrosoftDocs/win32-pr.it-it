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
# <a name="polling-for-the-status-of-the-job"></a>Polling dello stato del processo

Per impostazione predefinita, un'applicazione deve eseguire il polling delle modifiche allo stato di un processo. Per acquisire le modifiche nello stato del processo, chiamare il metodo [**Metodo ibackgroundcopyjob:: GetState**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) . Per acquisire le modifiche del numero di byte e di file trasferiti, chiamare il metodo [**Metodo ibackgroundcopyjob:: getProgress**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) . Per recuperare le informazioni sullo stato di avanzamento della parte di risposta di un processo di caricamento-risposta, chiamare il metodo [**IBackgroundCopyJob2:: GetReplyProgress**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) . Per un esempio in cui vengono utilizzate le informazioni sullo stato di avanzamento, vedere [determinare lo stato di avanzamento di un processo](determining-the-progress-of-a-job.md).

L' [**enumerazione \_ \_ dello stato del processo BG**](/windows/desktop/api/Bits/ne-bits-bg_job_state) definisce gli Stati di un processo e la struttura dello stato di [**\_ \_ avanzamento del processo BG**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) contiene informazioni sul numero di byte e file trasferiti.

Per utilizzare il polling, è necessario creare un meccanismo per avviare il polling. Ad esempio, creare un timer o usare un pulsante "Aggiorna" nell'interfaccia utente. Tuttavia, potrebbe essere più facile eseguire la registrazione per la notifica degli eventi e ricevere eventi quando lo stato o lo stato di avanzamento viene modificato. Per informazioni sulla notifica degli eventi, vedere la pagina relativa alla [registrazione di un callback com](registering-a-com-callback.md).

Nell'esempio seguente viene usato un timer per eseguire il polling dello stato di un processo. Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido.


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



 

 




