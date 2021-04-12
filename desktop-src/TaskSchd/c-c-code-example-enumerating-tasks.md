---
title: Esempio di codice C/C++ enumerazione delle attività
description: In questo esempio vengono enumerate tutte le attività nella cartella delle attività pianificate del computer locale e viene stampato il nome di ogni attività sullo schermo.
ms.assetid: 3a6a2262-cc5e-469e-b9f0-981879beb4ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f7bd88f0e16cee7c3557154a4343671babf279
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221570"
---
# <a name="cc-code-example-enumerating-tasks"></a>Esempio di codice C/C++: enumerazione delle attività

In questo esempio vengono enumerate tutte le attività nella cartella delle attività pianificate del computer locale e viene stampato il nome di ogni attività sullo schermo.


```C++
#include <windows.h>
#include <initguid.h>
#include <ole2.h>
#include <mstask.h>
#include <msterr.h>
#include <wchar.h>

#define TASKS_TO_RETRIEVE          5


int main(int argc, char **argv)
{
  HRESULT hr = S_OK;
  ITaskScheduler *pITS;
  
  
  /////////////////////////////////////////////////////////////////
  // Call CoInitialize to initialize the COM library and 
  // then call CoCreateInstance to get the Task Scheduler object. 
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
      return hr;
    }
  }
  else
  {
    return hr;
  }
  
  /////////////////////////////////////////////////////////////////
  // Call ITaskScheduler::Enum to get an enumeration object.
  /////////////////////////////////////////////////////////////////
  IEnumWorkItems *pIEnum;
  hr = pITS->Enum(&pIEnum);
  pITS->Release();
  if (FAILED(hr))
  {
    CoUninitialize();
    return hr;
  }
  
  /////////////////////////////////////////////////////////////////
  // Call IEnumWorkItems::Next to retrieve tasks. Note that 
  // this example tries to retrieve five tasks for each call.
  /////////////////////////////////////////////////////////////////
  LPWSTR *lpwszNames;
  DWORD dwFetchedTasks = 0;
  while (SUCCEEDED(pIEnum->Next(TASKS_TO_RETRIEVE,
                                &lpwszNames,
                                &dwFetchedTasks))
                  && (dwFetchedTasks != 0))
  {
    ///////////////////////////////////////////////////////////////
    // Process each task. Note that this example prints the 
    // name of each task to the screen.
    //////////////////////////////////////////////////////////////
    while (dwFetchedTasks)
    {
       wprintf(L"%s\n", lpwszNames[--dwFetchedTasks]);
       CoTaskMemFree(lpwszNames[dwFetchedTasks]);
    }
    CoTaskMemFree(lpwszNames);
  }
  
  pIEnum->Release();
  CoUninitialize();
  return S_OK;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Utilità di pianificazione 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




