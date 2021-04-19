---
title: Esempio di codice C/C++ creazione di un trigger di attività
description: Questo esempio crea un nuovo trigger per un'attività esistente denominata attività di test.
ms.assetid: 94755ec0-4b65-4adb-8074-9a0990e26e3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f7f846992d9d5a149230414a9b954198c06b2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298255"
---
# <a name="cc-code-example-creating-a-task-trigger"></a><span data-ttu-id="26a11-103">Esempio di codice C/C++: creazione di un trigger di attività</span><span class="sxs-lookup"><span data-stu-id="26a11-103">C/C++ Code Example: Creating a Task Trigger</span></span>

<span data-ttu-id="26a11-104">Questo esempio crea un nuovo trigger per un'attività esistente denominata attività di test.</span><span class="sxs-lookup"><span data-stu-id="26a11-104">This example creates a new trigger for an existing task named Test Task.</span></span>


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
  LPCWSTR lpcwszTaskName;
  lpcwszTaskName = L"Test Task";
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
  // Call ITask::CreateTrigger to create new trigger.
  ///////////////////////////////////////////////////////////////////
  
  ITaskTrigger *pITaskTrigger;
  WORD piNewTrigger;
  hr = pITask->CreateTrigger(&piNewTrigger,
                             &pITaskTrigger);
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::CreatTrigger: ");
    wprintf(L"error = 0x%x\n",hr);
    pITask->Release();
    CoUninitialize();
    return 1;
  }
  
  
  //////////////////////////////////////////////////////
  // Define TASK_TRIGGER structure. Note that wBeginDay,
  // wBeginMonth, and wBeginYear must be set to a valid 
  // day, month, and year respectively.
  //////////////////////////////////////////////////////
  
  TASK_TRIGGER pTrigger;
  ZeroMemory(&pTrigger, sizeof (TASK_TRIGGER));
  
  // Add code to set trigger structure?
  pTrigger.wBeginDay =1;                  // Required
  pTrigger.wBeginMonth =1;                // Required
  pTrigger.wBeginYear =1999;              // Required
  pTrigger.cbTriggerSize = sizeof (TASK_TRIGGER); 
  pTrigger.wStartHour = 13;
  pTrigger.TriggerType = TASK_TIME_TRIGGER_DAILY;
  pTrigger.Type.Daily.DaysInterval = 1;
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITaskTrigger::SetTrigger to set trigger criteria.
  ///////////////////////////////////////////////////////////////////
  
  hr = pITaskTrigger->SetTrigger (&pTrigger);
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskTrigger::SetTrigger: ");
    wprintf(L"error = 0x%x\n",hr);
    pITask->Release();
    pITaskTrigger->Release();
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call IPersistFile::Save to save trigger to disk.
  ///////////////////////////////////////////////////////////////////
  
  IPersistFile *pIPersistFile;
  hr = pITask->QueryInterface(IID_IPersistFile,
                              (void **)&pIPersistFile);
  hr = pIPersistFile->Save(NULL,
                           TRUE);

  if (FAILED(hr))
  {
    wprintf(L"Failed calling IPersistFile::Save: ");
    wprintf(L"error = 0x%x\n",hr);
    pITask->Release();
    pITaskTrigger->Release();
    pIPersistFile->Release();
    CoUninitialize();
    return 1;
  }
  
  wprintf(L"The trigger was created and IPersistFile::Save was \n");
  wprintf(L"called to save the new trigger to disk.\n"); 
  
  
  ///////////////////////////////////////////////////////////////////
  // Release resources.
  ///////////////////////////////////////////////////////////////////
  
  pITask->Release();
  pITaskTrigger->Release();
  pIPersistFile->Release();
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="26a11-105">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26a11-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26a11-106">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="26a11-106">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




