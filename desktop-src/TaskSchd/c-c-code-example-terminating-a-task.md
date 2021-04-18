---
title: Esempio di codice C/C++ che termina un'attività
description: Questo esempio verifica lo stato di un'attività nota e termina l'attività se è in esecuzione.
ms.assetid: 2131b966-6179-4a80-a3f1-ebb8967a7a90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2ea8adf901d417db13eb8c4f840acf0f283d3cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297991"
---
# <a name="cc-code-example-terminating-a-task"></a><span data-ttu-id="bcb8d-103">Esempio di codice C/C++: terminazione di un'attività</span><span class="sxs-lookup"><span data-stu-id="bcb8d-103">C/C++ Code Example: Terminating a Task</span></span>

<span data-ttu-id="bcb8d-104">Questo esempio verifica lo stato di un'attività nota e termina l'attività se è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="bcb8d-104">This example verifies the status of a known task and terminates the task if it is running.</span></span>


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
  
  //Release ITaskScheduler interface.
  pITS->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetStatus. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  HRESULT phrStatus;
  
  hr = pITask->GetStatus(&phrStatus);
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetStatus: ");
    wprintf(L"error = 0x%x\n",hr);
    pITask->Release();
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::Terminate if the status is SCHED_S_TASK_RUNNING.
  ///////////////////////////////////////////////////////////////////
  
  if(phrStatus==SCHED_S_TASK_RUNNING)
  {
    hr = pITask->Terminate();
    if (FAILED(hr))
    {
      wprintf(L"Failed calling ITask::Terminate: ");
      wprintf(L"error = 0x%x\n",hr);
      pITask->Release();
      CoUninitialize();
      return 1;
    }
  wprintf(L"Test Task is terminated.\n");
  }
  else
  {
    wprintf(L"Test Task is not running.\n");
  }

  // Release the ITask interface.
  pITask->Release();
  
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="bcb8d-105">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bcb8d-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcb8d-106">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="bcb8d-106">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




