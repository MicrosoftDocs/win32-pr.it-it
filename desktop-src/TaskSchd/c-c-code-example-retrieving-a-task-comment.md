---
title: Esempio di codice C/C++ durante il recupero di un commento di attività
description: In questo esempio viene recuperata la stringa di commento di un'attività nota e viene visualizzata la stringa di commento sullo schermo. In questo esempio si presuppone che l'attività e l'attività di test esistano già nel computer locale.
ms.assetid: f6f558d8-2e34-4314-9583-f815921aac7e
keywords:
- recupero del commento dell'attività Utilità di pianificazione
- recupero delle proprietà degli elementi di lavoro Utilità di pianificazione, commento dell'attività
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89ada9b135e42e25a81baf9bee60910b4e1a483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330183"
---
# <a name="cc-code-example-retrieving-a-task-comment"></a><span data-ttu-id="550ba-106">Esempio di codice C/C++: recupero di un commento di attività</span><span class="sxs-lookup"><span data-stu-id="550ba-106">C/C++ Code Example: Retrieving a Task Comment</span></span>

<span data-ttu-id="550ba-107">In questo esempio viene recuperata la stringa di commento di un'attività nota e viene visualizzata la stringa di commento sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="550ba-107">This example retrieves the comment string of a known task and displays the comment string on the screen.</span></span> <span data-ttu-id="550ba-108">In questo esempio si presuppone che l'attività e l'attività di test esistano già nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="550ba-108">This example assumes that the task and the test task already exist on the local computer.</span></span>


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
  // Call ITask::GetComment. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  LPWSTR ppwszComment;
  
  hr = pITask->GetComment(&ppwszComment);
  
  // Release the ITask interface.
  pITask->Release();
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetComment: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  wprintf(L"The comment for Test Task is: ");
  wprintf(L"  %s\n",ppwszComment);
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoTaskMemFree to free the string.
  ///////////////////////////////////////////////////////////////////
  CoTaskMemFree(ppwszComment);
  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="550ba-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="550ba-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="550ba-110">Esempi di Utilità di pianificazione 1,0</span><span class="sxs-lookup"><span data-stu-id="550ba-110">Task Scheduler 1.0 Examples</span></span>](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




