---
title: Esempio di codice C/C++ creazione di un'attività con NewWorkItem
description: In questo esempio viene creata una singola attività.
ms.assetid: a96bae5d-fa36-41ab-8baf-144683fc6b52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8573c5d5d097bdbe58c14329a5029046eecfae8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955387"
---
# <a name="cc-code-example-creating-a-task-using-newworkitem"></a><span data-ttu-id="360f1-103">Esempio di codice C/C++: creazione di un'attività con NewWorkItem</span><span class="sxs-lookup"><span data-stu-id="360f1-103">C/C++ Code Example: Creating a Task Using NewWorkItem</span></span>

<span data-ttu-id="360f1-104">In questo esempio viene creata una singola attività.</span><span class="sxs-lookup"><span data-stu-id="360f1-104">This example creates a single task.</span></span>


```C++
#include <windows.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <objidl.h>
#include <wchar.h>
#include <stdio.h>


int main(int argc, char **argv)
{
  HRESULT hr = S_OK;
  ITaskScheduler *pITS;
  
  
  /////////////////////////////////////////////////////////////////
  // Call CoInitialize to initialize the COM library and then 
  // call CoCreateInstance to get the Task Scheduler object. 
  /////////////////////////////////////////////////////////////////
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
  
  
  /////////////////////////////////////////////////////////////////
  // Call ITaskScheduler::NewWorkItem to create new task.
  /////////////////////////////////////////////////////////////////
  LPCWSTR pwszTaskName;
  ITask *pITask;
  IPersistFile *pIPersistFile;
  pwszTaskName = L"Test Task";
  
  hr = pITS->NewWorkItem(pwszTaskName,         // Name of task
                         CLSID_CTask,          // Class identifier 
                         IID_ITask,            // Interface identifier
                         (IUnknown**)&pITask); // Address of task 
                                                                                                                                                                                            //  interface
  
  
  pITS->Release();                               // Release object
  if (FAILED(hr))
  {
     CoUninitialize();
     fprintf(stderr, "Failed calling NewWorkItem, error = 0x%x\n",hr);
     return 1;
  }
  
  
  /////////////////////////////////////////////////////////////////
  // Call IUnknown::QueryInterface to get a pointer to 
  // IPersistFile and IPersistFile::Save to save 
  // the new task to disk.
  /////////////////////////////////////////////////////////////////
  
  hr = pITask->QueryInterface(IID_IPersistFile,
                              (void **)&pIPersistFile);
  
  pITask->Release();
  if (FAILED(hr))
  {
     CoUninitialize();
     fprintf(stderr, "Failed calling QueryInterface, error = 0x%x\n",hr);
     return 1;
  }
  
  
  hr = pIPersistFile->Save(NULL,
                           TRUE);
  pIPersistFile->Release();
  if (FAILED(hr))
  {
     CoUninitialize();
     fprintf(stderr, "Failed calling Save, error = 0x%x\n",hr);
     return 1;
  }
  
  
  CoUninitialize();
  printf("Created task.\n");
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="360f1-105">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="360f1-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="360f1-106">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="360f1-106">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




