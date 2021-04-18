---
title: Esempio di trigger di registrazione (C++)
description: In questo esempio di C++ viene illustrato come creare un'attività pianificata per l'esecuzione del blocco note quando un'attività viene registrata.
ms.assetid: 5e2e8fa6-66c7-4356-8fd6-22f7974791b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090a690601e24e1245040d0e7b394123afa94b07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298513"
---
# <a name="registration-trigger-example-c"></a><span data-ttu-id="4329b-103">Esempio di trigger di registrazione (C++)</span><span class="sxs-lookup"><span data-stu-id="4329b-103">Registration Trigger Example (C++)</span></span>

<span data-ttu-id="4329b-104">In questo esempio di C++ viene illustrato come creare un'attività pianificata per l'esecuzione del blocco note quando un'attività viene registrata.</span><span class="sxs-lookup"><span data-stu-id="4329b-104">This C++ example shows how to create a task that is scheduled to execute Notepad when a task is registered.</span></span> <span data-ttu-id="4329b-105">L'attività contiene un trigger di registrazione che specifica un limite iniziale e un limite finale per l'attività e anche un ritardo per l'attività.</span><span class="sxs-lookup"><span data-stu-id="4329b-105">The task contains a registration trigger that specifies a start boundary and an end boundary for the task and also a delay for the task.</span></span> <span data-ttu-id="4329b-106">Il limite iniziale specifica quando viene attivato il trigger e il ritardo imposta la quantità di tempo tra il momento in cui l'attività viene registrata e l'avvio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="4329b-106">The start boundary specifies when the trigger is activated, and the delay sets the amount of time between when the task is registered and when the task is started.</span></span> <span data-ttu-id="4329b-107">L'attività contiene anche un'azione che specifica l'attività per l'esecuzione del blocco note.</span><span class="sxs-lookup"><span data-stu-id="4329b-107">The task also contains an action that specifies the task to execute Notepad.</span></span>

> [!Note]  
> <span data-ttu-id="4329b-108">Quando si aggiorna un'attività con un trigger di registrazione, l'attività verrà eseguita dopo l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="4329b-108">When a task with a registration trigger is updated, the task will execute after the update occurs.</span></span>

 

<span data-ttu-id="4329b-109">Nella procedura seguente viene descritto come pianificare un'attività per avviare un eseguibile quando l'attività è registrata.</span><span class="sxs-lookup"><span data-stu-id="4329b-109">The following procedure describes how to schedule a task to start an executable when the task is registered.</span></span>

<span data-ttu-id="4329b-110">**Per pianificare l'avvio del blocco note quando viene registrata un'attività**</span><span class="sxs-lookup"><span data-stu-id="4329b-110">**To schedule Notepad to start when a task is registered**</span></span>

1.  <span data-ttu-id="4329b-111">Inizializzare COM e impostare la sicurezza generale COM.</span><span class="sxs-lookup"><span data-stu-id="4329b-111">Initialize COM and set general COM security.</span></span>
2.  <span data-ttu-id="4329b-112">Creare l'oggetto [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .</span><span class="sxs-lookup"><span data-stu-id="4329b-112">Create the [**ITaskService**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) object.</span></span> <span data-ttu-id="4329b-113">Questo oggetto consente di creare attività in una cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="4329b-113">This object allows you to create tasks in a specified folder.</span></span>
3.  <span data-ttu-id="4329b-114">Ottenere una cartella attività per la creazione di un'attività in.</span><span class="sxs-lookup"><span data-stu-id="4329b-114">Get a task folder to create a task in.</span></span> <span data-ttu-id="4329b-115">Usare il metodo [**ITaskService:: GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) per ottenere la cartella e il metodo [**ITaskService:: newTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) per creare l'oggetto [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="4329b-115">Use the [**ITaskService::GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) method to get the folder, and the [**ITaskService::NewTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) method to create the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object.</span></span>
4.  <span data-ttu-id="4329b-116">Definire le informazioni sull'attività usando l'oggetto [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) , ad esempio le informazioni di registrazione per l'attività.</span><span class="sxs-lookup"><span data-stu-id="4329b-116">Define information about the task using the [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) object, such as the registration information for the task.</span></span> <span data-ttu-id="4329b-117">Utilizzare la [**Proprietà RegistrationInfo di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) e altre proprietà dell'interfaccia **ITaskDefinition** per definire le informazioni sull'attività.</span><span class="sxs-lookup"><span data-stu-id="4329b-117">Use the [**RegistrationInfo property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) and other properties of the **ITaskDefinition** interface to define the task information.</span></span>
5.  <span data-ttu-id="4329b-118">Creare un trigger di registrazione usando la [**Proprietà Triggers di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) per accedere al [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) per l'attività.</span><span class="sxs-lookup"><span data-stu-id="4329b-118">Create a registration trigger using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) to access the [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) for the task.</span></span> <span data-ttu-id="4329b-119">Usare il metodo [**ITriggerCollection:: create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) (specificando il tipo di trigger che si vuole creare) per creare un trigger di registrazione.</span><span class="sxs-lookup"><span data-stu-id="4329b-119">Use the [**ITriggerCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) method (specifying the type of trigger you want to create) to create a registration trigger.</span></span>
6.  <span data-ttu-id="4329b-120">Creare un'azione per l'attività da eseguire usando la [**Proprietà Actions di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) per accedere all'interfaccia [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) per l'attività.</span><span class="sxs-lookup"><span data-stu-id="4329b-120">Create an action for the task to execute by using the [**Actions property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) to access the [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) interface for the task.</span></span> <span data-ttu-id="4329b-121">Usare il metodo [**IActionCollection:: create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) per specificare il tipo di azione che si vuole creare.</span><span class="sxs-lookup"><span data-stu-id="4329b-121">Use the [**IActionCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) method to specify the type of action that you want to create.</span></span> <span data-ttu-id="4329b-122">In questo esempio viene utilizzato un oggetto [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) , che rappresenta un'azione che esegue un'operazione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4329b-122">This example uses an [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) object, which represents an action that executes a command-line operation.</span></span>
7.  <span data-ttu-id="4329b-123">Registrare l'attività usando il metodo [**ITaskFolder:: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) .</span><span class="sxs-lookup"><span data-stu-id="4329b-123">Register the task using the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method.</span></span>

<span data-ttu-id="4329b-124">Nell'esempio C++ riportato di seguito viene illustrato come pianificare un'attività per eseguire il blocco note 30 secondi dopo la registrazione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="4329b-124">The following C++ example shows how to schedule a task to execute Notepad 30 seconds after the task is registered.</span></span>


```C++
/********************************************************************
 This sample schedules a task to start notepad.exe 30 seconds after
 the task is registered. 
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
    LPCWSTR wszTaskName = L"Registration Trigger Test Task";

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
        printf("Cannot get Root Folder pointer: %x", hr );
        pService->Release();
        CoUninitialize();
        return 1;
    }
    
    //  If the same task exists, remove it.
    hr = pRootFolder->DeleteTask( _bstr_t( wszTaskName), 0  );
    
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
    //  Create the principal for the task
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
    
    //  Set up principal information: 
    hr = pPrincipal->put_Id( _bstr_t(L"Principal1") ); 
    if( FAILED(hr) )
        printf("\nCannot put the principal ID: %x", hr);

    hr = pPrincipal->put_LogonType( TASK_LOGON_INTERACTIVE_TOKEN );
    if( FAILED(hr) )
        printf("\nCannot put principal logon type: %x", hr);

    //  Run the task with the least privileges (LUA) 
    hr = pPrincipal->put_RunLevel( TASK_RUNLEVEL_LUA ); 
    pPrincipal->Release();  
    if( FAILED(hr) )
    {
        printf("\nCannot put principal run level: %x", hr );
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
    //  Get the trigger collection to insert the registration trigger.
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

    //  Add the registration trigger to the task.
    ITrigger *pTrigger = NULL;    
    hr = pTriggerCollection->Create( TASK_TRIGGER_REGISTRATION, &pTrigger );
    pTriggerCollection->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot create a registration trigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }     
    
    IRegistrationTrigger *pRegistrationTrigger = NULL;
    hr = pTrigger->QueryInterface( 
        IID_IRegistrationTrigger, (void**) &pRegistrationTrigger );
    pTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nQueryInterface call failed on IRegistrationTrigger: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }
    
    hr = pRegistrationTrigger->put_Id( _bstr_t( L"Trigger1" ) );
    if( FAILED(hr) )
        printf("\nCannot put trigger ID: %x", hr);
    
    //  Define the delay for the registration trigger.
    hr = pRegistrationTrigger->put_Delay( L"PT30S" );
    pRegistrationTrigger->Release();
    if( FAILED(hr) )
    {
        printf("\nCannot put registration trigger delay: %x", hr );
        pRootFolder->Release();
        pTask->Release();
        CoUninitialize();
        return 1;
    }   
    

    //  ------------------------------------------------------
    //  Add an Action to the task. This task will execute notepad.exe.     
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
        printf("\nCannot create action: %x", hr );
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
        printf("\nCannot put the action executable path: %x", hr );
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



## <a name="related-topics"></a><span data-ttu-id="4329b-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4329b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4329b-126">Uso della Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="4329b-126">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




