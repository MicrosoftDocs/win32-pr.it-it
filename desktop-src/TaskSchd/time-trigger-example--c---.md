---
title: Esempio di trigger temporale (C++)
description: In questo esempio C++ viene illustrato come creare un'attività pianificata per l'Blocco note all'ora specificata.
ms.assetid: e45b18b0-5a7f-4283-b42f-15e9ffcfaff7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 227d6fe24aa63b430376a7ce50d23b4b8ecd282f807315384b42175b9903d1b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059651"
---
# <a name="time-trigger-example-c"></a>Esempio di trigger temporale (C++)

In questo esempio C++ viene illustrato come creare un'attività pianificata per l'Blocco note all'ora specificata. L'attività contiene un trigger basato sul tempo che specifica un limite di inizio e un limite finale per l'attività. L'attività contiene anche un'azione che specifica l'attività da eseguire Blocco note. L'attività viene registrata usando un tipo di accesso interattivo, ovvero l'attività viene eseguita nel contesto di sicurezza dell'utente che esegue l'applicazione. L'attività contiene anche le impostazioni di inattività, che specificano Utilità di pianificazione attività quando il computer è in una condizione di inattività.

Nella procedura seguente viene descritto come pianificare un'attività per avviare un eseguibile in un determinato momento.

**Per pianificare Blocco note l'avvio a un'ora specifica**

1.  Inizializzare COM e impostare la sicurezza COM generale.
2.  Creare [**l'oggetto ITaskService.**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)

    Questo oggetto consente di creare attività in una cartella specificata.

3.  Ottiene una cartella di attività in cui creare un'attività.

    Usare il [**metodo ITaskService::GetFolder**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-getfolder) per ottenere la cartella e il metodo [**ITaskService::NewTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskservice-newtask) per creare [**l'oggetto ITaskDefinition.**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)

4.  Definire le informazioni sull'attività usando [**l'oggetto ITaskDefinition,**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) ad esempio le informazioni di registrazione per l'attività.

    Usare la [**proprietà RegistrationInfo di ITaskDefinition e**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo) altre proprietà dell'interfaccia [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) per definire le informazioni sull'attività.

5.  Creare un trigger basato sul tempo usando la [**proprietà Triggers di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers) per accedere a [**ITriggerCollection per**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection) l'attività.

    Usare il [**metodo ITriggerCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-create) (che specifica il tipo di trigger da creare) per creare un trigger basato sul tempo. In questo modo è possibile impostare il limite iniziale e il limite finale per il trigger in modo che le azioni dell'attività verranno pianificate per l'esecuzione a un'ora specificata.

6.  Creare un'azione per l'attività da eseguire usando la [**proprietà Actions di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) per accedere [**all'interfaccia IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection) per l'attività.

    Usare il [**metodo IActionCollection::Create**](/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-create) per specificare il tipo di azione che si vuole creare. Questo esempio usa un [**oggetto IExecAction,**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) che rappresenta un'azione che esegue un'operazione della riga di comando.

7.  Registrare l'attività [**usando il metodo ITaskFolder::RegisterTaskDefinition.**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition)

Nell'esempio C++ seguente viene illustrato come pianificare un'attività da eseguire Blocco note minuto dopo la registrazione dell'attività.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




