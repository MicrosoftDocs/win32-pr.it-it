---
title: Esempio di codice C/C++ durante il recupero del nome dell'applicazione dell'attività
description: In questo esempio viene recuperato il nome dell'applicazione associata a una determinata attività e viene visualizzato tale nome sullo schermo. In questo esempio si presuppone che l'attività e l'attività di test esistano già nel computer locale.
ms.assetid: 7cf20a14-fee3-4507-83a9-4a081a9783fc
keywords:
- recupero dei nomi delle applicazioni Utilità di pianificazione
- recupero delle proprietà dell'attività Utilità di pianificazione, nome applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb590900cf7b4c6d8821560e91e2f05c21c0f73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298159"
---
# <a name="cc-code-example-retrieving-the-task-application-name"></a>Esempio di codice C/C++: recupero del nome dell'applicazione dell'attività

In questo esempio viene recuperato il nome dell'applicazione associata a una determinata attività e viene visualizzato tale nome sullo schermo. In questo esempio si presuppone che l'attività e l'attività di test esistano già nel computer locale.


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
     wprintf(L"Failed calling ITaskScheduler::Activate; error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Call ITask::GetApplicationName to display the name of the 
  // application associated with "Test Task".
  ///////////////////////////////////////////////////////////////////
  
  LPWSTR lpwszApplicationName;
  hr = pITask->GetApplicationName(&lpwszApplicationName);
  pITask->Release();
  if (FAILED(hr))
  {
     wprintf(L"Failed calling ITask::GetApplicationName\n");
     wprintf(L" error = 0x%x\n",hr);
     CoUninitialize();
     return 1;
  }
  
  
  ///////////////////////////////////////////////////////////////////
  // Process the returned string. 
  ///////////////////////////////////////////////////////////////////
  
  wprintf(L"Test Task is associated with: %s\n", lpwszApplicationName);
  
  
  ///////////////////////////////////////////////////////////////////
  // Call CoTaskMemFree to free resources.
  ///////////////////////////////////////////////////////////////////
  
  CoTaskMemFree(lpwszApplicationName);
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Utilità di pianificazione 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




