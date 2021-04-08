---
title: Esempio di trigger di avvio (C++)
description: Questo argomento contiene un esempio di codice C++ che Mostra come creare un'attività pianificata per l'esecuzione Notepad.exe all'avvio del sistema.
ms.assetid: d4dbbfe5-bde9-4a1c-8e11-24cd1e14646c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdbd5a5a73d100394b90e91f8b9c30c1bd495ac0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856450"
---
# <a name="boot-trigger-example-c"></a><span data-ttu-id="bf9ee-103">Esempio di trigger di avvio (C++)</span><span class="sxs-lookup"><span data-stu-id="bf9ee-103">Boot Trigger Example (C++)</span></span>

<span data-ttu-id="bf9ee-104">Questo argomento contiene un esempio di codice C++ che Mostra come creare un'attività pianificata per l'esecuzione Notepad.exe all'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-104">This topic contains a C++ code example that shows how to create a task that is scheduled to execute Notepad.exe when the system is started.</span></span> <span data-ttu-id="bf9ee-105">L'attività contiene un trigger di avvio che specifica un limite iniziale e un tempo di ritardo per l'avvio dell'attività dopo l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-105">The task contains a boot trigger that specifies a start boundary and delay time for the task to start after the system is started.</span></span> <span data-ttu-id="bf9ee-106">L'attività contiene anche un'azione che specifica l'esecuzione dell'attività Notepad.exe.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-106">The task also contains an action that specifies the task execute Notepad.exe.</span></span> <span data-ttu-id="bf9ee-107">L'attività viene registrata utilizzando l'account del servizio locale come contesto di sicurezza per l'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-107">The task is registered using the Local Service account as a security context to run the task.</span></span>

<span data-ttu-id="bf9ee-108">Nella procedura seguente viene descritto come pianificare un'attività per avviare un eseguibile all'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-108">The following procedure describes how to schedule a task to start an executable when the system is started.</span></span>

<span data-ttu-id="bf9ee-109">**Per pianificare l'avvio del blocco note al momento dell'avvio del sistema**</span><span class="sxs-lookup"><span data-stu-id="bf9ee-109">**To schedule Notepad to start when the system is started**</span></span>

1.  <span data-ttu-id="bf9ee-110">Inizializzare COM e impostare la sicurezza generale COM.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-110">Initialize COM and set general COM security.</span></span>
2.  <span data-ttu-id="bf9ee-111">Creare l'oggetto [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="bf9ee-111">Create the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) object.</span></span>

    <span data-ttu-id="bf9ee-112">Questo oggetto consente di creare attività in una cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-112">This object enables you to create tasks in a specified folder.</span></span>

3.  <span data-ttu-id="bf9ee-113">Ottenere una cartella attività per la creazione di un'attività in.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-113">Get a task folder to create a task in.</span></span>

    <span data-ttu-id="bf9ee-114">Usare il metodo [**ITaskService:: GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) per ottenere la cartella e il metodo [**ITaskService:: newTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) per creare l'oggetto [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="bf9ee-114">Use the [**ITaskService::GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) method to get the folder, and the [**ITaskService::NewTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) method to create the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object.</span></span>

4.  <span data-ttu-id="bf9ee-115">Definire le informazioni sull'attività usando l'oggetto [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) , ad esempio le informazioni di registrazione per l'attività.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-115">Define information about the task using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object, such as the registration information for the task.</span></span>

    <span data-ttu-id="bf9ee-116">Utilizzare la [**Proprietà RegistrationInfo di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) e altre proprietà dell'interfaccia [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) per definire le informazioni sull'attività.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-116">Use the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) and other properties of the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface to define the task information.</span></span>

5.  <span data-ttu-id="bf9ee-117">Creare un trigger di avvio usando la [**Proprietà Triggers di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) per accedere al [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) per l'attività.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-117">Create a boot trigger using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) to access the [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) for the task.</span></span>

    <span data-ttu-id="bf9ee-118">Usare il metodo [**ITriggerCollection:: create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) per specificare che si vuole creare un trigger di avvio.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-118">Use the [**ITriggerCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) method to specify that you want to create a boot trigger.</span></span> <span data-ttu-id="bf9ee-119">È possibile impostare il limite di inizio e il ritardo per il trigger in modo che le azioni dell'attività vengano pianificate per l'esecuzione a un'ora specificata all'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-119">You can set the start boundary and delay for the trigger so that the task actions will be scheduled to execute at a specified time when the system is started.</span></span>

6.  <span data-ttu-id="bf9ee-120">Creare un'azione per l'attività da eseguire usando la [**Proprietà Actions di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) per accedere alla raccolta [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) per l'attività.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-120">Create an action for the task to execute by using the [**Actions property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) to access the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) collection for the task.</span></span>

    <span data-ttu-id="bf9ee-121">Usare il metodo [**IActionCollection:: create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) per specificare il tipo di azione che si vuole creare.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-121">Use the [**IActionCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) method to specify the type of action you want to create.</span></span> <span data-ttu-id="bf9ee-122">In questo esempio viene utilizzato un oggetto [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) , che rappresenta un'azione che esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-122">This example uses an [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) object, which represents an action that executes a command-line operation.</span></span>

7.  <span data-ttu-id="bf9ee-123">Registrare l'attività usando il metodo [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="bf9ee-123">Register the task using the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method.</span></span>

<span data-ttu-id="bf9ee-124">Nell'esempio di codice C++ riportato di seguito viene illustrato come pianificare un'attività da eseguire Notepad.exe 30 secondi dopo l'avvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="bf9ee-124">The following C++ code example shows how to schedule a task to execute Notepad.exe 30 seconds after the system is started.</span></span>


```C++
/********************************************************************
 This sample schedules a task to start Notepad.exe 30 seconds after
 the system is started. 
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
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"Boot Trigger Test Task";

    //  Get the Windows directory and set the path to Notepad.exe.
    wstring wstrExecutablePath = _wgetenv( L"WINDIR");
    wstrExecutablePath += L"\\SYSTEM32\\NOTEPAD.EXE";


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
          printf("Failed to create an instance of ITaskService: %x", hr);
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
    //  This folder will hold the new task that is registered.
    ITaskFolder *pRootFolder = NULL;
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        printf("Cannot get Root Folder pointer: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }
    
    //  If the same task exists, remove it.
    pRootFolder->DeleteTask( _bstr_t( wszTaskName), 0  );
    
    //  Create the task builder object to create the task.
    ITaskDefinition *pTask = NULL;
    hr = pService->NewTask( 0, &pTask );

    pService->Release();  // COM clean up.  Pointer is no longer used.
    if (FAILED(hr))
    {
          printf("Failed to create a task definition: %x", hr);
          pRootFolder->Release();
          CoUninitialize();
          return 1;
    }
    
        
    //  ------------------------------------------------------
    //  Get the registration info for setting the identification.
    IRegistrationInfo *pRegInfo= NULL;
    hr = pTask->get_RegistrationInfo( &pRegInfo );
    if( FAILED(hr) )
    {
        printf("\nCannot get identification pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    hr = pRegInfo->put_Author(L"Author Name");
    pRegInfo->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put identification info: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  ------------------------------------------------------
    //  Create the settings for the task
    ITaskSettings *pSettings = NULL;
    hr = pTask->get_Settings( &pSettings );
    if( FAILED(hr) )
    {
        printf("\nCannot get settings pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    //  Set setting values for the task. 
    hr = pSettings->put_StartWhenAvailable(VARIANT_TRUE);
    pSettings->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put setting info: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
       

    //  ------------------------------------------------------
    //  Get the trigger collection to insert the boot trigger.
    ITriggerCollection *pTriggerCollection = NULL;
    hr = pTask->get_Triggers( &pTriggerCollection );
    if( FAILED(hr) )
    {
        printf("\nCannot get trigger collection: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  Add the boot trigger to the task.
    ITrigger *pTrigger = NULL;
    hr = pTriggerCollection->Create( TASK_TRIGGER_BOOT, &pTrigger ); 
    pTriggerCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create the trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    IBootTrigger *pBootTrigger = NULL;
    hr = pTrigger->QueryInterface( 
        IID_IBootTrigger, (void**) &pBootTrigger );
    pTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed for IBootTrigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    hr = pBootTrigger->put_Id( _bstr_t( L"Trigger1" ) );
    if( FAILED(hr) )
       printf("\nCannot put the trigger ID: %x", hr);
    
    //  Set the task to start at a certain time. The time 
    //  format should be YYYY-MM-DDTHH:MM:SS(+-)(timezone).
    //  For example, the start boundary below
    //  is January 1st 2005 at 12:05
    hr = pBootTrigger->put_StartBoundary( _bstr_t(L"2005-01-01T12:05:00") );
    if( FAILED(hr) )
       printf("\nCannot put the start boundary: %x", hr);
  
    hr = pBootTrigger->put_EndBoundary( _bstr_t(L"2015-05-02T08:00:00") );
    if( FAILED(hr) )
       printf("\nCannot put the end boundary: %x", hr);

    // Delay the task to start 30 seconds after system start. 
    hr = pBootTrigger->put_Delay( L"PT30S" );
    pBootTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put delay for boot trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    } 
       

    //  ------------------------------------------------------
    //  Add an Action to the task. This task will execute Notepad.exe.     
    IActionCollection *pActionCollection = NULL;

    //  Get the task action collection pointer.
    hr = pTask->get_Actions( &pActionCollection );
    if( FAILED(hr) )
    {
        printf("\nCannot get Task collection pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
        
    //  Create the action, specifying it as an executable action.
    IAction *pAction = NULL;
    hr = pActionCollection->Create( TASK_ACTION_EXEC, &pAction );
    pActionCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create the action: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    IExecAction *pExecAction = NULL;
    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( 
        IID_IExecAction, (void**) &pExecAction );
    pAction->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed for IExecAction: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    //  Set the path of the executable to Notepad.exe.
    hr = pExecAction->put_Path( _bstr_t( wstrExecutablePath.c_str() ) ); 
    pExecAction->Release(); 
    if( FAILED(hr) )
    {
        printf("\nCannot set path of executable: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
      
    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    IRegisteredTask *pRegisteredTask = NULL;
    VARIANT varPassword;
    varPassword.vt = VT_EMPTY;
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t( wszTaskName ),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(L"Local Service"), 
            varPassword, 
            TASK_LOGON_SERVICE_ACCOUNT,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        printf("\nError saving the Task : %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    printf("\n Success! Task successfully registered. " );

    //  Clean up.
    pRootFolder->Release();
    pTask->Release();
    pRegisteredTask->Release();
    CoUninitialize();
    return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="bf9ee-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bf9ee-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf9ee-126">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="bf9ee-126">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




