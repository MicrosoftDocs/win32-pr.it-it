---
title: Esempio di codice C/C++ - Impostazione del nome dell'applicazione
description: In questo esempio viene impostato il nome dell'applicazione associata a un'attività nota. Questo esempio presuppone che l'attività \ 0034;test task \ 0034; esiste già nel computer locale e il servizio Utilità di pianificazione è in esecuzione.
ms.assetid: 1d86f945-0f13-4a7f-8123-df7e63a02238
keywords:
- impostazione delle proprietà delle attività Utilità di pianificazione , nome dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7861a62360ef97fdb9be5c691084cad98d594fc44030467e16058f7a8efd2c7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943842"
---
# <a name="cc-code-example-setting-application-name"></a>Esempio di codice C/C++: impostazione del nome dell'applicazione

In questo esempio viene impostato il nome dell'applicazione associata a un'attività nota. In questo esempio si presuppone che l'attività "test task" esista già nel computer locale e che il servizio Utilità di pianificazione sia in esecuzione.


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
  // Call ITask::SetApplicationName to specify the Application name
  // for Test Task.
  ///////////////////////////////////////////////////////////////////
  LPCWSTR pwszApplicationName = L"C:\\Windows\\System32\\notepad.exe";
 
  hr = pITask->SetApplicationName(pwszApplicationName);

  if (FAILED(hr))
  {
    wprintf(L"Failed calling ITask::SetApplicationName: ");
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
  
  wprintf(L"Set the application name for Test Task.\n");  
  CoUninitialize();
  return 0;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilità di pianificazione 1.0 Esempi](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




