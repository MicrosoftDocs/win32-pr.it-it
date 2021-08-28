---
title: Esempio di codice C/C++ che enumera le attività
description: Questo esempio enumera tutte le attività nella cartella Attività pianificate del computer locale e stampa il nome di ogni attività sullo schermo.
ms.assetid: 3a6a2262-cc5e-469e-b9f0-981879beb4ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52a1dc50d8289418b230e4f65154f23bbf2fc601de2215eb132153e22703619
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738901"
---
# <a name="cc-code-example-enumerating-tasks"></a>Esempio di codice C/C++: enumerazione di attività

Questo esempio enumera tutte le attività nella cartella Attività pianificate del computer locale e stampa il nome di ogni attività sullo schermo.


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

[Utilità di pianificazione 1.0 Esempi](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 




