---
title: Esempio di codice C/C++ recupero delle informazioni sull'account dell'attività
description: Questo esempio di codice recupera le informazioni sull'account di un'attività nota e visualizza il nome dell'account sullo schermo. In questo esempio si presuppone che l'attività e l'attività di test esistano già nel computer locale e che il Utilità di pianificazione sia in esecuzione.
ms.assetid: ef330276-a063-42c6-a837-fddb4723091b
keywords:
- recupero delle informazioni sull'account dell'attività Utilità di pianificazione
- recupero delle proprietà degli elementi di lavoro Utilità di pianificazione, informazioni sull'account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1102ce0c2a2a98e66c1ac943eeab0593fe75e189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955549"
---
# <a name="cc-code-example-retrieving-task-account-information"></a>Esempio di codice C/C++: recupero delle informazioni sull'account attività

Questo esempio di codice recupera le informazioni sull'account di un'attività nota e visualizza il nome dell'account sullo schermo. In questo esempio si presuppone che l'attività e l'attività di test esistano già nel computer locale e che il Utilità di pianificazione sia in esecuzione.


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
  // Call ITask::GetAccountInformation. Note that this method is 
  // inherited from IScheduledWorkItem.
  ///////////////////////////////////////////////////////////////////
  LPWSTR pwszAccountName;
  
  hr = pITask->GetAccountInformation(&pwszAccountName);
  
  // Release the ITask interface.
  pITask->Release();

  if(hr == SCHED_E_NO_SECURITY_SERVICES)
  {
    wprintf(L"Error: SCHED_E_NO_SECURITY_SERVICES");
    wprintf(L"Security services are available only on Windows Server 2003");
    wprintf(L", Windows XP, and Windows 2000.");
    CoUninitialize();
    return 1;

  }
  
  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::GetAccountInformation: ");
    wprintf(L"error = 0x%x\n",hr);
    CoUninitialize();
    return 1;
  }
  
  
  wprintf(L"The account name for Test Task is: ");
  wprintf(L"  %s\n",pwszAccountName);
  
  CoTaskMemFree(pwszAccountName);
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Utilità di pianificazione 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




