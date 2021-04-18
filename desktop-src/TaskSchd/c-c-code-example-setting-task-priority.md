---
title: Esempio di codice C/C++ impostazione della priorità delle attività
description: In questo esempio viene impostata la priorità di un'attività di test e quindi viene salvata l'attività. In questo esempio si presuppone che l'attività di test esista già nel computer locale.
ms.assetid: 498dc438-3703-4d5c-a8b1-609d5776942d
keywords:
- impostazione delle proprietà dell'attività Utilità di pianificazione, priorità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540405ebe3544d6fad9418533957ddcda8a567c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297992"
---
# <a name="cc-code-example-setting-task-priority"></a><span data-ttu-id="3bea4-105">Esempio di codice C/C++: impostazione della priorità delle attività</span><span class="sxs-lookup"><span data-stu-id="3bea4-105">C/C++ Code Example: Setting Task Priority</span></span>

<span data-ttu-id="3bea4-106">In questo esempio viene impostata la priorità di un'attività di test e quindi viene salvata l'attività.</span><span class="sxs-lookup"><span data-stu-id="3bea4-106">This example sets the priority of a test task and then saves the task.</span></span> <span data-ttu-id="3bea4-107">In questo esempio si presuppone che l'attività di test esista già nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="3bea4-107">This example assumes that the test task already exists on the local computer.</span></span>


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
  
  // Release the ITaskScheduler interface.
  pITS->Release();  
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITaskScheduler::Activate: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::SetPriority to specify the priority level of 
  // Test Task.
  ///////////////////////////////////////////////////////////////////
  DWORD dwPriority = HIGH_PRIORITY_CLASS;
  
  hr = pITask->SetPriority(dwPriority);
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::SetPriority: ");
    wprintf(L"error = 0x%x\n",hr);
    pITask->Release();
    CoUninitialize();
    return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call IPersistFile::Save to save the modified task to disk.
  ///////////////////////////////////////////////////////////////////
  IPersistFile *pIPersistFile;
  
  hr = pITask->QueryInterface(IID_IPersistFile,
                              (void **)&pIPersistFile);
  
  // Release the ITask interface.
  pITask->Release();  
  
  hr = pIPersistFile->Save(NULL,
                           TRUE);
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling IPersistFile::Save: ");
    wprintf(L"error = 0x%x\n",hr);
    pIPersistFile->Release();
    CoUninitialize();
    return 1;
  }

  // Release the IPersistFile interface.
  pIPersistFile->Release();
  
  wprintf(L"Set the priority of TestTask to HIGH_PRIORITY_CLASS.\n");
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="3bea4-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3bea4-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bea4-109">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="3bea4-109">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




