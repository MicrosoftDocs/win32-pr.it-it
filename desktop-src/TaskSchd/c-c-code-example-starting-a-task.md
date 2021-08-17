---
title: Esempio di codice C/C++ avvio di un'attività
description: Questo esempio tenta di eseguire un'attività esistente. In questo esempio si presuppone che l'attività e l'attività di test esistano già nel computer locale.
ms.assetid: e4f38f8a-3488-4802-913b-f627ecca8bb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11abcbd4581db306b8ca60f478e9b2927e531b7dd2fd8461742f4dc1c93a169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139624"
---
# <a name="cc-code-example-starting-a-task"></a>Esempio di codice C/C++: avvio di un'attività

Questo esempio tenta di eseguire un'attività esistente. In questo esempio si presuppone che l'attività e l'attività di test esistano già nel computer locale.


```C++
#include <windows.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <wchar.h>
#include<stdio.h>


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
     wprintf(L"Failed calling ITaskScheduler::Activate; error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::Run to start the execution of "Test Task".
  ///////////////////////////////////////////////////////////////////
  
  hr = pITask->Run();
  pITask->Release();

  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::Run, error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }

  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione 1.0 Esempi](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




