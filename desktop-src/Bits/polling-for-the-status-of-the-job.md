---
title: Polling per lo stato del processo
description: Per impostazione predefinita, un'applicazione deve eseguire il polling delle modifiche nello stato di un processo.
ms.assetid: b12ee1e0-d3d9-4d31-b2af-7491480968f0
keywords:
- trasferimento di bit del processo, polling
- polling per lo stato del processo BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f1f47a891968e686ae1ffc083bfa9b00d79c8bdc22e2c78ea523ef7ec707e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701721"
---
# <a name="polling-for-the-status-of-the-job"></a>Polling per lo stato del processo

Per impostazione predefinita, un'applicazione deve eseguire il polling delle modifiche nello stato di un processo. Per acquisire le modifiche nello stato del processo, chiamare il [**metodo IBackgroundCopyJob::GetState.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getstate) Per acquisire le modifiche nel numero di byte e file trasferiti, chiamare il [**metodo IBackgroundCopyJob::GetProgress.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-getprogress) Per recuperare informazioni sullo stato sulla parte di risposta di un processo di caricamento-risposta, chiamare il metodo [**IBackgroundCopyJob2::GetReplyProgress.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyprogress) Per un esempio in cui vengono utilizzate le informazioni sullo stato, vedere [Determinazione dello stato di avanzamento di un processo](determining-the-progress-of-a-job.md).

[**L'enumerazione BG \_ JOB \_ STATE**](/windows/desktop/api/Bits/ne-bits-bg_job_state) definisce gli stati di un processo e la struttura [**BG JOB \_ \_ PROGRESS**](/windows/desktop/api/Bits/ns-bits-bg_job_progress) contiene informazioni sul numero di byte e file trasferiti.

Per usare il polling, è necessario creare un meccanismo per avviare il polling. Ad esempio, creare un timer o usare un pulsante "Aggiorna" nell'interfaccia utente. Tuttavia, potrebbe essere più semplice registrarsi per la notifica degli eventi e ricevere eventi quando lo stato o lo stato cambia. Per informazioni sulla notifica degli eventi, vedere [Registrazione di un callback COM](registering-a-com-callback.md).

Nell'esempio seguente viene utilizzato un timer per eseguire il polling dello stato di un processo. Nell'esempio si presuppone che il [**puntatore a interfaccia IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido.


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



 

 




