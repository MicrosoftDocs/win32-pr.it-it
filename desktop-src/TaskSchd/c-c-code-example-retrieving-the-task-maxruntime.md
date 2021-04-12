---
title: Esempio di codice C/C++ durante il recupero dell'attività MaxRunTime
description: In questo esempio viene recuperata la quantità massima di tempo che l'attività può eseguire (in millisecondi) e viene visualizzato tale numero sullo schermo. In questo esempio si presuppone che l'attività e l'attività di test esistano già nel computer locale.
ms.assetid: 33873fef-1b67-4010-8bda-b75e1dfa80d5
keywords:
- recupero dell'attività MaxRunTime Utilità di pianificazione
- recupero delle proprietà dell'attività Utilità di pianificazione, MaxRunTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fcf442e2936de48a11aea4d81de6e0bac18f92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395443"
---
# <a name="cc-code-example-retrieving-the-task-maxruntime"></a>Esempio di codice C/C++: recupero dell'attività MaxRunTime

In questo esempio viene recuperata la quantità massima di tempo che l'attività può eseguire (in millisecondi) e viene visualizzato tale numero sullo schermo. In questo esempio si presuppone che l'attività e l'attività di test esistano già nel computer locale.


```C++
#include <windows.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <wchar.h>


int main(int argc, char **argv)
{
  HRESULT hr = S_OK;
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoInitialize to initialize the COM library and then
  // call CoCreateInstance to get the Task Scheduler object.
  ///////////////////////////////////////////////////////////////////

  ITaskScheduler *pITS;
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
  LPCWSTR lpcwszTaskName;
  lpcwszTaskName = L"Test Task";
  hr = pITS->Activate(lpcwszTaskName,
                      IID_ITask,
                      (IUnknown**) &pITask);
  
  pITS->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITaskScheduler::Activate;\n");
     wprintf(L"error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetMaxRunTime to display the maximum time Test Task
  // is allowed to run.
  ///////////////////////////////////////////////////////////////////
  
  DWORD pdwRunTime;
  hr = pITask->GetMaxRunTime(&pdwRunTime);
  pITask->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::GetMaxRunTime: \n");
     wprintf(L"error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  wprintf(L"Test Task can run for %d milliseconds\n", pdwRunTime);
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Utilità di pianificazione 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




