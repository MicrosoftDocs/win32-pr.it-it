---
description: In Gestione autorizzazioni un'attività è un'azione di alto livello che gli utenti di un'applicazione devono completare. Le attività sono costituite da operazioni, ovvero funzioni di basso livello e metodi dell'applicazione.
ms.assetid: a9a0202e-44c9-4192-8ff8-e22bddf26cfe
title: Raggruppamento di operazioni in attività in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c869db5dc5acbd4a7e7f9401ebbf97dea481c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884478"
---
# <a name="grouping-operations-into-tasks-in-c"></a><span data-ttu-id="3a8e4-104">Raggruppamento di operazioni in attività in C++</span><span class="sxs-lookup"><span data-stu-id="3a8e4-104">Grouping Operations into Tasks in C++</span></span>

<span data-ttu-id="3a8e4-105">In Gestione autorizzazioni un'attività è un'azione di alto livello che gli utenti di un'applicazione devono completare.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-105">In Authorization Manager, a task is a high-level action that users of an application need to complete.</span></span> <span data-ttu-id="3a8e4-106">Le attività sono costituite da operazioni, ovvero funzioni di basso livello e metodi dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-106">Tasks are made up of operations, which are low-level functions and methods of the application.</span></span> <span data-ttu-id="3a8e4-107">Viene quindi assegnata un'attività ai ruoli che devono eseguire tale attività.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-107">A task is then assigned to those roles that must perform that task.</span></span> <span data-ttu-id="3a8e4-108">Un'attività è rappresentata da un oggetto [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) .</span><span class="sxs-lookup"><span data-stu-id="3a8e4-108">A task is represented by an [**IAzTask**](/windows/desktop/api/Azroles/nn-azroles-iaztask) object.</span></span> <span data-ttu-id="3a8e4-109">Per ulteriori informazioni sulle operazioni e sulle attività, vedere [operazioni e attività](operations-and-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="3a8e4-109">For more information about operations and tasks, see [Operations and Tasks](operations-and-tasks.md).</span></span>

<span data-ttu-id="3a8e4-110">Nell'esempio seguente viene illustrato come raggruppare le operazioni per creare un'attività.</span><span class="sxs-lookup"><span data-stu-id="3a8e4-110">The following example shows how to group operations to create a task.</span></span> <span data-ttu-id="3a8e4-111">Nell'esempio si presuppone che esista un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C, che questo archivio contiene un'applicazione denominata Expense e che l'applicazione contenga operazioni definite nell'argomento [definizione di operazioni in C++](defining-operations-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="3a8e4-111">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C, that this store contains an application named Expense, and that this application contains operations defined in the topic [Defining Operations in C++](defining-operations-in-c--.md).</span></span>


```C++
#ifndef _WIN32_WINNT
#define _WIN32_WINNT 0x0502
#endif
#pragma comment(lib, "duser.lib")

#include <windows.h>
#include <stdio.h>
#include <azroles.h>
#include <objbase.h>

void main(void){
    IAzAuthorizationStore* pStore = NULL;
    IAzApplication* pApp = NULL;
    IAzTask* pTask = NULL;
    HRESULT hr;
    void MyHandleError(char *s);
    BSTR storeName = NULL;
    BSTR appName = NULL;
    BSTR taskName = NULL;
    BSTR opName = NULL;
    
    //  Initialize COM.
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize COM.");

    //  Create the AzAuthorizationStore object.
    hr = CoCreateInstance(
   /*"b2bcff59-a757-4b0b-a1bc-ea69981da69e"*/
         __uuidof(AzAuthorizationStore),
         NULL,
         CLSCTX_ALL,
   /*"edbd9ca9-9b82-4f6a-9e8b-98301e450f14"*/
         __uuidof(IAzAuthorizationStore),
         (void**)&pStore);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create AzAuthorizationStore object.");
    
    //  Create null VARIANT for parameters.
    VARIANT myVar; 
    VariantInit(&myVar);

    //  Allocate a string for the name of the store.
    if(!(storeName = SysAllocString(L"msxml://c:\\MyStore.xml")))
        MyHandleError("Could not allocate string.");
    
    //  Initialize the store.
    hr = pStore->Initialize(AZ_AZSTORE_FLAG_MANAGE_STORE_ONLY,
  storeName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not initialize store.");

    //  Create an application object.
    if (!(appName = SysAllocString(L"Expense")))
        MyHandleError("Could not allocate application name string.");
    hr = pStore->OpenApplication(appName, myVar, &pApp);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not open application.");

    //  Create a task object.
    if (!(taskName = SysAllocString(L"Submit Expense")))
        MyHandleError("Could not allocate task name string.");
    hr = pApp->CreateTask(taskName, myVar, &pTask);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not create task.");

    //  Add operations to the task.
    if (!(opName = SysAllocString(L"RetrieveForm")))
        MyHandleError("Could not allocate operation name string.");
    hr = pTask->AddOperation(opName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add 1st operation to the task.");
    SysFreeString(opName);

    if (!(opName = SysAllocString(L"EnqueRequest")))
        MyHandleError("Could not allocate operation name string.");
    hr = pTask->AddOperation(opName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add 2nd operation to the task.");
    SysFreeString(opName);

    if (!(opName = SysAllocString(L"UseFormControl")))
        MyHandleError("Could not allocate operation name string.");
    hr = pTask->AddOperation(opName, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not add 3rd operation to the task.");
    SysFreeString(opName);

    //  Save information to the store.
    hr = pTask->Submit(0, myVar);
    if (!(SUCCEEDED(hr)))
        MyHandleError("Could not save task data to the store.");

    //  Clean up resources.
    pStore->Release();
    pApp->Release();
    pTask->Release();
    SysFreeString(storeName);
    SysFreeString(appName);
    VariantClear(&myVar);
    CoUninitialize();
}

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 



