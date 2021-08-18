---
title: Visualizzazione dei nomi e degli stati delle attività (C++)
description: Questi due esempi di C++ illustrano come enumerare le attività. Un esempio mostra come visualizzare le informazioni per le attività in una cartella di attività e gli altri esempi illustrano come visualizzare le informazioni per tutte le attività in esecuzione.
ms.assetid: 32037133-d3f3-4186-b035-ab01d37ed58d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b80ec17b71ae45c951a27ca582855936d73457401d878b0f21f69bcbaa71ca23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760186"
---
# <a name="displaying-task-names-and-states-c"></a>Visualizzazione dei nomi e degli stati delle attività (C++)

Questi due esempi di C++ illustrano come enumerare le attività. Un esempio mostra come visualizzare le informazioni per le attività in una cartella di attività e gli altri esempi illustrano come visualizzare le informazioni per tutte le attività in esecuzione.

La procedura seguente descrive come visualizzare i nomi e lo stato delle attività per tutte le attività in una cartella delle attività.

**Per visualizzare i nomi e lo stato delle attività per tutte le attività in una cartella di attività**

1.  Inizializzare COM e impostare la sicurezza COM generale.
2.  Creare [**l'oggetto ITaskService.**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)

    Questo oggetto consente di connettersi al servizio Utilità di pianificazione e accedere a una cartella di attività specifica.

3.  Ottenere una cartella di attività che contiene le attività su cui si vogliono ottenere informazioni.

    Usare il [**metodo ITaskService::GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) per ottenere la cartella.

4.  Ottenere la raccolta di attività dalla cartella.

    Usare il [**metodo ITaskFolder::GetTasks**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-gettasks) per ottenere la raccolta di attività ([**IRegisteredTaskCollection**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtaskcollection)).

5.  Ottenere il numero di attività nella raccolta ed enumerare ogni attività nella raccolta.

    Usare la [**proprietà Item di IRegisteredTaskCollection**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtaskcollection-get_item) per ottenere [**un'istanza di IRegisteredTask.**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) Ogni istanza conterrà un'attività nella raccolta. È quindi possibile visualizzare le informazioni (valori delle proprietà) di ogni attività registrata.

Nell'esempio C++ seguente viene illustrato come visualizzare il nome e lo stato di tutte le attività nella cartella delle attività radice.


```C++
/********************************************************************
 This sample enumerates through the tasks on the local computer and 
 displays their name and state. 
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
//  Include the task header file.
#include <taskschd.h>
#pragma comment(lib, "taskschd.lib")
#pragma comment(lib, "comsupp.lib")


using namespace std;

int __cdecl wmain()
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        printf("\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity(
        NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL,
        0,
        NULL);

    if( FAILED(hr) )
    {
        printf("\nCoInitializeSecurity failed: %x", hr );
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    ITaskService *pService = NULL;
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
          printf("Failed to CoCreate an instance of the TaskService class: %x", hr);
          CoUninitialize();
          return 1;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(),
        _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        printf("ITaskService::Connect failed: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.
    ITaskFolder *pRootFolder = NULL;
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    
    pService->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        CoUninitialize();
        return 1;
    }
    
    //  -------------------------------------------------------
    //  Get the registered tasks in the folder.
    IRegisteredTaskCollection* pTaskCollection = NULL;
    hr = pRootFolder->GetTasks( NULL, &pTaskCollection );

    pRootFolder->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get the registered tasks.: %x", hr);
        CoUninitialize();
        return 1;
    }

    LONG numTasks = 0;
    hr = pTaskCollection->get_Count(&numTasks);

    if( numTasks == 0 )
     {
        printf("\nNo Tasks are currently running" );
        pTaskCollection->Release();
        CoUninitialize();
        return 1;
     }

    printf("\nNumber of Tasks : %d", numTasks );

    TASK_STATE taskState;
    
    for(LONG i=0; i < numTasks; i++)
    {
        IRegisteredTask* pRegisteredTask = NULL;
        hr = pTaskCollection->get_Item( _variant_t(i+1), &pRegisteredTask );
        
        if( SUCCEEDED(hr) )
        {
            BSTR taskName = NULL;
            hr = pRegisteredTask->get_Name(&taskName);
            if( SUCCEEDED(hr) )
            {
                printf("\nTask Name: %S", taskName);
                SysFreeString(taskName);

                hr = pRegisteredTask->get_State(&taskState);
                if (SUCCEEDED (hr) )
                    printf("\n\tState: %d", taskState);
                else 
                    printf("\n\tCannot get the registered task state: %x", hr);
            }
            else
            {
                printf("\nCannot get the registered task name: %x", hr);
            }
            pRegisteredTask->Release();
        }
        else
        {
            printf("\nCannot get the registered task item at index=%d: %x", i+1, hr);
        }
    }

    pTaskCollection->Release();
    CoUninitialize();
    return 0;
}

```



La procedura seguente descrive come visualizzare i nomi e lo stato delle attività per tutte le attività in esecuzione.

**Per visualizzare i nomi e lo stato delle attività per tutte le attività in esecuzione**

1.  Inizializzare COM e impostare la sicurezza COM generale.
2.  Creare [**l'oggetto ITaskService.**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)

    Questo oggetto consente di connettersi al servizio Utilità di pianificazione e accedere a una cartella di attività specifica.

3.  Usare il [**metodo ITaskService::GetRunningTasks**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getrunningtasks) per ottenere una raccolta di tutte le attività in esecuzione ([**IRunningTaskCollection**](/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection)). È possibile specificare per ottenere istanze dell'attività in esecuzione, incluse o escluse le attività nascoste.
4.  Ottenere il numero di attività nella raccolta ed enumerare ogni attività nella raccolta.

    Usare la [**proprietà Item di IRunningTaskCollection**](/windows/desktop/api/taskschd/nf-taskschd-irunningtaskcollection-get_item) per ottenere [**un'istanza di IRunningTask.**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) Ogni istanza conterrà un'attività nella raccolta. È quindi possibile visualizzare le informazioni (valori delle proprietà) di ogni attività registrata.

Nell'esempio C++ seguente viene illustrato come visualizzare il nome e lo stato di tutte le attività in esecuzione, incluse le attività nascoste.


```C++
/********************************************************************
 This sample enumerates through all running tasks on the local computer and 
 displays their name and state. 
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
//  Include the task header file.
#include <taskschd.h>
#pragma comment(lib, "taskschd.lib")
#pragma comment(lib, "comsupp.lib")


using namespace std;

int __cdecl wmain()
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        printf("\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity(
        NULL,
        -1,
        NULL,
        NULL,
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,
        RPC_C_IMP_LEVEL_IMPERSONATE,
        NULL,
        0,
        NULL);

    if( FAILED(hr) )
    {
        printf("\nCoInitializeSecurity failed: %x", hr );
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    ITaskService *pService = NULL;
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
          printf("Failed to CoCreate an instance of the TaskService class: %x", hr);
          CoUninitialize();
          return 1;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(),
        _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        printf("ITaskService::Connect failed: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }

       // Get the running tasks.
       IRunningTaskCollection* pRunningTasks = NULL;
       hr = pService->GetRunningTasks(TASK_ENUM_HIDDEN, &pRunningTasks);

    pService->Release();
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        CoUninitialize();
        return 1;
    }
        
    LONG numTasks = 0;
    hr = pRunningTasks->get_Count(&numTasks);

    if( numTasks == 0 )
     {
        printf("\nNo Tasks are currently running" );
        pRunningTasks->Release();
        CoUninitialize();
        return 1;
     }

    printf("\nNumber of running tasks : %d", numTasks );

    TASK_STATE taskState;
    
    for(LONG i=0; i < numTasks; i++)
    {
        IRunningTask* pRunningTask = NULL;
        hr = pRunningTasks->get_Item( _variant_t(i+1), &pRunningTask );
        
        if( SUCCEEDED(hr) )
        {
            BSTR taskName = NULL;
            hr = pRunningTask->get_Name(&taskName);
            if( SUCCEEDED(hr) )
            {
                printf("\nTask Name: %S", taskName);
                SysFreeString(taskName);

                hr = pRunningTask->get_State(&taskState);
                if (SUCCEEDED (hr) )
                    printf("\n\tState: %d", taskState);
                else 
                    printf("\n\tCannot get the registered task state: %x", hr);
            }
            else
            {
                printf("\nCannot get the registered task name: %x", hr);
            }
            pRunningTask->Release();
        }
        else
        {
            printf("\nCannot get the registered task item at index=%d: %x", i+1, hr);
        }
    }

    pRunningTasks->Release();
    CoUninitialize();
    return 0;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




