---
title: Esempio di trigger time (C++)
description: In questo esempio di C++ viene illustrato come creare un'attività pianificata per l'esecuzione del blocco note a un'ora specificata.
ms.assetid: e45b18b0-5a7f-4283-b42f-15e9ffcfaff7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f7f8d3c8bd1f179b0def9be069d710a2e126a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708908"
---
# <a name="time-trigger-example-c"></a><span data-ttu-id="7dbd6-103">Esempio di trigger time (C++)</span><span class="sxs-lookup"><span data-stu-id="7dbd6-103">Time Trigger Example (C++)</span></span>

<span data-ttu-id="7dbd6-104">In questo esempio di C++ viene illustrato come creare un'attività pianificata per l'esecuzione del blocco note a un'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-104">This C++ example shows how to create a task that is scheduled to execute Notepad at a specified time.</span></span> <span data-ttu-id="7dbd6-105">L'attività contiene un trigger basato sul tempo che specifica un limite iniziale e un limite finale per l'attività.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-105">The task contains a time-based trigger that specifies a start boundary and an end boundary for the task.</span></span> <span data-ttu-id="7dbd6-106">L'attività contiene anche un'azione che specifica l'attività per l'esecuzione del blocco note.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-106">The task also contains an action that specifies the task to execute Notepad.</span></span> <span data-ttu-id="7dbd6-107">L'attività viene registrata utilizzando un tipo di accesso interattivo, ovvero l'attività viene eseguita nel contesto di sicurezza dell'utente che esegue l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-107">The task is registered using an interactive logon type, which means the task runs under the security context of the user who runs the application.</span></span> <span data-ttu-id="7dbd6-108">L'attività contiene anche impostazioni inattive, che specificano il modo in cui Utilità di pianificazione esegue le attività quando il computer si trova in una condizione di inattività.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-108">The task also contains idle settings, which specifies how Task Scheduler performs tasks when the computer is in an idle condition.</span></span>

<span data-ttu-id="7dbd6-109">Nella procedura seguente viene descritto come pianificare un'attività per avviare un eseguibile in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-109">The following procedure describes how to schedule a task to start an executable at a certain time.</span></span>

<span data-ttu-id="7dbd6-110">**Per pianificare l'avvio del blocco note a un'ora specifica**</span><span class="sxs-lookup"><span data-stu-id="7dbd6-110">**To schedule Notepad to start at a specific time**</span></span>

1.  <span data-ttu-id="7dbd6-111">Inizializzare COM e impostare la sicurezza generale COM.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-111">Initialize COM and set general COM security.</span></span>
2.  <span data-ttu-id="7dbd6-112">Creare l'oggetto [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="7dbd6-112">Create the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) object.</span></span>

    <span data-ttu-id="7dbd6-113">Questo oggetto consente di creare attività in una cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-113">This object allows you to create tasks in a specified folder.</span></span>

3.  <span data-ttu-id="7dbd6-114">Ottenere una cartella attività per la creazione di un'attività in.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-114">Get a task folder to create a task in.</span></span>

    <span data-ttu-id="7dbd6-115">Usare il metodo [**ITaskService:: GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) per ottenere la cartella e il metodo [**ITaskService:: newTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) per creare l'oggetto [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="7dbd6-115">Use the [**ITaskService::GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) method to get the folder, and the [**ITaskService::NewTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) method to create the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object.</span></span>

4.  <span data-ttu-id="7dbd6-116">Definire le informazioni sull'attività usando l'oggetto [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) , ad esempio le informazioni di registrazione per l'attività.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-116">Define information about the task using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object, such as the registration information for the task.</span></span>

    <span data-ttu-id="7dbd6-117">Utilizzare la [**Proprietà RegistrationInfo di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) e altre proprietà dell'interfaccia [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) per definire le informazioni sull'attività.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-117">Use the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) and other properties of the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) interface to define the task information.</span></span>

5.  <span data-ttu-id="7dbd6-118">Creare un trigger basato sul tempo usando la [**Proprietà Triggers di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) per accedere al [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) per l'attività.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-118">Create a time-based trigger using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) to access the [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) for the task.</span></span>

    <span data-ttu-id="7dbd6-119">Usare il metodo [**ITriggerCollection:: create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) (specificando il tipo di trigger che si vuole creare) per creare un trigger basato sul tempo.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-119">Use the [**ITriggerCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) method (specifying the type of trigger you want to create) to create a time-based trigger.</span></span> <span data-ttu-id="7dbd6-120">Questo consente di impostare il limite iniziale e il limite finale per il trigger in modo che le azioni dell'attività verranno pianificate per l'esecuzione a un'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-120">This allows you to set the start boundary and the end boundary for the trigger so that the task's actions will be scheduled to execute at a specified time.</span></span>

6.  <span data-ttu-id="7dbd6-121">Creare un'azione per l'attività da eseguire usando la [**Proprietà Actions di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) per accedere all'interfaccia [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) per l'attività.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-121">Create an action for the task to execute by using the [**Actions property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) to access the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) interface for the task.</span></span>

    <span data-ttu-id="7dbd6-122">Usare il metodo [**IActionCollection:: create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) per specificare il tipo di azione che si vuole creare.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-122">Use the [**IActionCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="7dbd6-123">In questo esempio viene utilizzato un oggetto [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) , che rappresenta un'azione che esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-123">This example uses an [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) object, which represents an action that executes a command-line operation.</span></span>

7.  <span data-ttu-id="7dbd6-124">Registrare l'attività usando il metodo [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="7dbd6-124">Register the task using the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method.</span></span>

<span data-ttu-id="7dbd6-125">Nell'esempio C++ riportato di seguito viene illustrato come pianificare un'attività per eseguire il blocco note un minuto dopo la registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="7dbd6-125">The following C++ example shows how to schedule a task to execute Notepad one minute after the task is registered.</span></span>


```C++
/********************************************************************
 This sample schedules a task to start notepad.exe 1 minute from the
 time the task is registered. 
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
#include <wincred.h>
//  Include the task header file.
#include <taskschd.h>
#pragma comment(lib, "taskschd.lib")
#pragma comment(lib, "comsupp.lib")
#pragma comment(lib, "credui.lib")

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
    LPCWSTR wszTaskName = L"Time Trigger Test Task";

    //  Get the windows directory and set the path to notepad.exe.
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
    //  Get the pointer to the root task folder.  This folder will hold the
    //  new task that is registered.
    ITaskFolder *pRootFolder = NULL;
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        printf("Cannot get Root folder pointer: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }
    
    //  If the same task exists, remove it.
    pRootFolder->DeleteTask( _bstr_t( wszTaskName), 0  );
    
    //  Create the task definition object to create the task.
    ITaskDefinition *pTask = NULL;
    hr = pService->NewTask( 0, &pTask );

    pService->Release();  // COM clean up.  Pointer is no longer used.
    if (FAILED(hr))
    {
        printf("Failed to CoCreate an instance of the TaskService class: %x", hr);
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
    
    hr = pRegInfo->put_Author( L"Author Name" );    
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
    //  Create the principal for the task - these credentials
    //  are overwritten with the credentials passed to RegisterTaskDefinition
    IPrincipal *pPrincipal = NULL;
    hr = pTask->get_Principal( &pPrincipal );
    if( FAILED(hr) )
    {
        printf("\nCannot get principal pointer: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    //  Set up principal logon type to interactive logon
    hr = pPrincipal->put_LogonType( TASK_LOGON_INTERACTIVE_TOKEN );
    pPrincipal->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put principal info: %x", hr );
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
        printf("\nCannot put setting information: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    // Set the idle settings for the task.
    IIdleSettings *pIdleSettings = NULL;
    hr = pSettings->get_IdleSettings( &pIdleSettings );
    if( FAILED(hr) )
    {
        printf("\nCannot get idle setting information: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    hr = pIdleSettings->put_WaitTimeout(L"PT5M");
    pIdleSettings->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put idle setting information: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    

    //  ------------------------------------------------------
    //  Get the trigger collection to insert the time trigger.
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

    //  Add the time trigger to the task.
    ITrigger *pTrigger = NULL;    
    hr = pTriggerCollection->Create( TASK_TRIGGER_TIME, &pTrigger );     
    pTriggerCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    ITimeTrigger *pTimeTrigger = NULL;
    hr = pTrigger->QueryInterface( 
        IID_ITimeTrigger, (void**) &pTimeTrigger );
    pTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed for ITimeTrigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }

    hr = pTimeTrigger->put_Id( _bstr_t( L"Trigger1" ) );
    if( FAILED(hr) )
        printf("\nCannot put trigger ID: %x", hr);

    hr = pTimeTrigger->put_EndBoundary( _bstr_t(L"2015-05-02T08:00:00") );
    if( FAILED(hr) )
        printf("\nCannot put end boundary on trigger: %x", hr);

    //  Set the task to start at a certain time. The time 
    //  format should be YYYY-MM-DDTHH:MM:SS(+-)(timezone).
    //  For example, the start boundary below
    //  is January 1st 2005 at 12:05
    hr = pTimeTrigger->put_StartBoundary( _bstr_t(L"2005-01-01T12:05:00") );
    pTimeTrigger->Release();    
    if( FAILED(hr) )
    {
        printf("\nCannot add start boundary to trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    

    //  ------------------------------------------------------
    //  Add an action to the task. This task will execute notepad.exe.     
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
    
    //  Create the action, specifying that it is an executable action.
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

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t( wstrExecutablePath.c_str() ) );
    pExecAction->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put action path: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }  
    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    IRegisteredTask *pRegisteredTask = NULL;
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t( wszTaskName ),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(), 
            _variant_t(), 
            TASK_LOGON_INTERACTIVE_TOKEN,
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



## <a name="related-topics"></a><span data-ttu-id="7dbd6-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7dbd6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dbd6-127">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="7dbd6-127">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




