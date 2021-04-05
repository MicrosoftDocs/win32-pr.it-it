---
title: Esempio di codice C/C++ recupero di stringhe di trigger
description: In questo esempio viene recuperata una stringa di trigger per tutti i trigger associati a un'attività nota.
ms.assetid: cd605c68-efaa-4ce7-9e44-59f516d85627
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b99f986692c3bfb1297a98e9afdcea65606446
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711731"
---
# <a name="cc-code-example-retrieving-trigger-strings"></a>Esempio di codice C/C++: recupero di stringhe di trigger

In questo esempio viene recuperata una stringa di trigger per tutti i trigger associati a un'attività nota.


```C++
#include <windows.h>
#include <winbase.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <wchar.h>


int main(int argc, char **argv)
{
  HRESULT hr = S_OK;
  ITaskScheduler *pITS;
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoInitialize to initialize the COM library and then
  // call CoCreateInstance to get the Task Scheduler object.
  ///////////////////////////////////////////////////////////////////
  hr = CoInitialize(NULL);
  if (SUCCEEDED(hr))
  {
    hr = CoCreateInstance(CLSID_CTaskScheduler,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_ITaskScheduler,
                          (void **) &pITS);
    if (FAILED(hr))
    {
      CoUninitialize();
      return 1;
    }
  }
  else
  {
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITaskScheduler::Activate to get the Task object.
  ///////////////////////////////////////////////////////////////////
  
  ITask *pITask;
  LPCWSTR lpcwszTaskName = L"Test Task";
  hr = pITS->Activate(lpcwszTaskName,
                      IID_ITask,
                      (IUnknown**) &pITask);
  
  pITS->Release();
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::TriggerCount to retrieve the number of triggers
  // associated with the task.
  ///////////////////////////////////////////////////////////////////
  
  WORD plTriggerCount;
  hr = pITask->GetTriggerCount (&plTriggerCount);
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetTriggerCount: ");
    wprintf(L"error = 0x%x\n",hr);
    pTask->Release();
    CoUninitialize();
    return 1;
  } 
  
  
  ///////////////////////////////////////////////////////////////////
  // Display the trigger stings, calling ITask::GetTriggerString for 
  // each trigger associated with the task.
  ///////////////////////////////////////////////////////////////////
  
  wprintf(L"There are %i triggers with Test Task.\n",plTriggerCount);
  wprintf(L"They are:\n");  
   
  WORD CurrentTrigger=0;
  LPWSTR ppwszTrigger;
  
  for (CurrentTrigger=0; CurrentTrigger<plTriggerCount; CurrentTrigger++)
  {  
    pITask->GetTriggerString (CurrentTrigger,
                              &ppwszTrigger); 
    if (FAILED(hr))
    {
      wprintf(L"Failed calling ITask::GetTriggerString: ");
      wprintf(L"error = 0x%x\n",hr);
      pTask->Release();
      CoUninitialize();
      return 1;
    }
    
    wprintf(L"%i) %s\n",CurrentTrigger+1, ppwszTrigger);
  } 
  
  
  ///////////////////////////////////////////////////////////////////
  // Release resources.
  ///////////////////////////////////////////////////////////////////
  
  CoTaskMemFree(ppwszTrigger);
  pITask->Release();
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Utilità di pianificazione 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




