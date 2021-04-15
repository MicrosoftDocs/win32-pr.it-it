---
title: Manutenzione automatica (Cookbook per la compatibilità per Windows)
description: Manutenzione automatica
ms.assetid: D3B61105-D118-42A4-8F3D-ED92EFAF597F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320625fa0ac8e56368396a7f1be88def0ac3c526
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104474502"
---
# <a name="automatic-maintenance"></a>Manutenzione automatica

## <a name="platforms"></a>Piattaforme

**Client** -Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

Windows dipende dall'esecuzione della posta in arrivo e dall'attività di manutenzione di terze parti per gran parte del suo valore aggiunto, inclusi Windows Update e la deframmentazione automatica del disco, nonché gli aggiornamenti e le analisi antivirus. Inoltre, le aziende utilizzano spesso attività di manutenzione, ad esempio l'analisi di protezione accesso alla rete (NAP), per consentire l'applicazione degli standard di sicurezza in tutte le workstation aziendali.

L'attività di manutenzione in Windows è progettata per essere eseguita in background con un'interazione utente limitata e un minimo effetto sulle prestazioni e sull'efficienza energetica. Tuttavia, in Windows 7 e versioni precedenti, le prestazioni e l'efficienza energetica sono ancora interessate a causa della pianificazione non deterministica e molto variegata delle diverse attività di manutenzione di Windows. La velocità di risposta agli utenti viene ridotta quando viene eseguita l'attività di manutenzione mentre gli utenti usano attivamente il computer. Spesso le app richiedono inoltre all'utente di aggiornare il software e di eseguire la manutenzione in background e indirizzare gli utenti a più esperienze, tra cui centro operativo, pannello di controllo, Windows Update, Utilità di pianificazione snap-in MMC e controlli di terze parti.

L'obiettivo della manutenzione automatica è combinare tutte le attività di manutenzione in background in Windows e aiutare gli sviluppatori di terze parti ad aggiungere le attività di manutenzione a Windows senza influire negativamente sulle prestazioni e sull'efficienza energetica. Inoltre, la manutenzione automatica consente agli utenti e alle aziende di controllare la pianificazione e la configurazione delle attività di manutenzione.

**Problemi principali**

La manutenzione automatica è progettata per risolvere i problemi relativi alle attività di manutenzione in Windows:

-   Pianificazione scadenza
-   Conflitti di utilizzo delle risorse
-   Efficienza energetica
-   Trasparenza per l'utente

## <a name="functionality"></a>Funzionalità

La manutenzione automatica facilita l'efficienza di inattività e consente l'esecuzione di tutte le attività in modo tempestivo e in ordine di priorità. Consente inoltre di abilitare la visibilità e il controllo unificato delle attività di manutenzione e consente agli sviluppatori di terze parti di aggiungere le attività di manutenzione a Windows senza influire negativamente sulle prestazioni e sull'efficienza energetica. A tale scopo, offre una modalità completamente automatica, la modalità avviata dall'utente, l'arresto automatico, le scadenze e le notifiche e il controllo aziendale. Ognuno di essi è descritto di seguito.

**Modalità completamente automatica**

Questa modalità predefinita consente la pianificazione intelligente durante il tempo di inattività del PC e in orari pianificati, ovvero l'esecuzione e la sospensione automatica delle attività di manutenzione senza alcun intervento da parte dell'utente. L'utente può impostare una pianificazione settimanale o giornaliera. Tutte le attività di manutenzione non sono interattive ed eseguite in modo invisibile all'utente.

Il computer viene ripreso automaticamente dalla modalità di sospensione quando non è probabile che il sistema sia in uso, rispettando i criteri di risparmio energia, che nel caso dei portatili, per impostazione predefinita è possibile abilitare la riattivazione solo se si trova in alimentazione AC. Le risorse di sistema complete a potenza elevata vengono usate per completare l'attività di manutenzione nel minor tempo possibile. Se il sistema è stato ripreso dalla sospensione per la manutenzione automatica, viene richiesto di tornare alla modalità sospensione.

Eventuali interazioni utente richieste correlate a attività come la configurazione vengono eseguite al di fuori dell'esecuzione automatica della manutenzione.

**Modalità avviata dall'utente**

Se gli utenti devono prepararsi per la corsa, prevedere un tempo di alimentazione della batteria per un tempo prolungato o voler ottimizzare le prestazioni e la velocità di risposta, hanno la possibilità di avviare la manutenzione automatica su richiesta. Gli utenti possono configurare gli attributi di manutenzione automatica, inclusa la pianificazione di esecuzione automatica. Possono visualizzare lo stato corrente dell'esecuzione di manutenzione automatica e possono arrestare la manutenzione automatica, se necessario.

**Arresto automatico**

La manutenzione automatica interrompe automaticamente le attività di manutenzione in corso se l'utente inizia a interagire con il computer. L'attività di manutenzione viene ripresa quando il sistema torna allo stato inattivo.

> [!Note]  
> Tutte le attività nella manutenzione automatica devono supportare l'arresto in 2 secondi o meno. L'utente deve ricevere una notifica che indica che l'attività è stata arrestata.

 

**Scadenze e notifiche**

L'attività di manutenzione critica deve essere eseguita all'interno di un intervallo di tempo predefinito. Se non è stato possibile eseguire attività critiche nell'intervallo di tempo specificato, la manutenzione automatica verrà avviata automaticamente alla successiva opportunità di inattività del sistema disponibile. Tuttavia, se lo stato dell'attività resta dietro la scadenza, la manutenzione automatica invierà una notifica all'utente sull'attività e fornirà un'opzione per un'esecuzione manuale della manutenzione automatica. Tutte le attività pianificate per la manutenzione verranno eseguite, sebbene le attività più affamate abbiano la precedenza. Questa attività può influisca sulle prestazioni e sulla velocità di risposta del sistema; Pertanto, la manutenzione automatica invierà una notifica all'utente dell'esecuzione dell'attività di manutenzione critica.

**Controllo Enterprise**

I professionisti IT aziendali dovrebbero essere in grado di determinare quando viene eseguita la manutenzione automatica sui sistemi Windows, applicare tale pianificazione tramite interfacce di gestione standardizzate e recuperare i dati degli eventi sullo stato dei tentativi di esecuzione automatica della manutenzione. Inoltre, i professionisti IT devono essere in grado di richiamare attività di manutenzione automatica specifiche in modalità remota tramite interfacce di gestione standard. Ogni volta che viene eseguita la manutenzione automatica, la creazione di rapporti di stato, incluse le notifiche quando non è stato possibile eseguire la manutenzione automatica perché l'utente ha sospeso manualmente l'attività, viene eseguito. I professionisti IT dovrebbero prendere in considerazione la possibilità di trasferire gli script di accesso alla manutenzione automatica per semplificare l'esperienza di accesso dell'utente.

## <a name="creating-an-automatic-maintenance-task"></a>Creazione di un'attività di manutenzione automatica

In questa sezione viene illustrato in dettaglio come gli sviluppatori possono creare un'attività utilizzando una definizione di attività in linguaggio XML o C. Tenere presente che l'attività di manutenzione non deve avviare alcuna interfaccia utente che richiede l'interazione dell'utente, perché la manutenzione automatica è completamente invisibile e viene eseguita quando l'utente non è presente. Infatti, se l'utente interagisce con il computer durante la manutenzione automatica, le attività in corso verranno terminate fino al periodo di inattività successivo.

**Utilizzo di XML**

Utilità di pianificazione include uno strumento da riga di comando incorporato, schtasks.exe, che consente di importare una definizione di attività in formato XML. Lo schema per la definizione di attività è documentato in https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx . Di seguito è riportato un esempio di un'attività di manutenzione automatica definita in XML.


```
<?xml version="1.0" encoding="UTF-16"?>
<Task version="1.4" xmlns="http://schemas.microsoft.com/windows/2004/02/mit/task">
  <RegistrationInfo>
    <Date>2011-07-01T11:34:31</Date>
    <Author>IT Deptartment</Author>
  </RegistrationInfo>
  <Principals>
    <Principal id="Author">
      <RunLevel>LeastPrivilege</RunLevel>
      <GroupId>NT AUTHORITY\SYSTEM</GroupId>
    </Principal>
  </Principals>
  <Settings>
    <MultipleInstancesPolicy>IgnoreNew</MultipleInstancesPolicy>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
    <AllowHardTerminate>true</AllowHardTerminate>
    <StartWhenAvailable>false</StartWhenAvailable>
    <RunOnlyIfNetworkAvailable>false</RunOnlyIfNetworkAvailable>
    <MaintenanceSettings>
      <Period>P2D</Period>
      <Deadline>P14D</Deadline>
    </MaintenanceSettings>
    <AllowStartOnDemand>true</AllowStartOnDemand>
    <Enabled>true</Enabled>
    <Hidden>false</Hidden>
    <RunOnlyIfIdle>false</RunOnlyIfIdle>
    <DisallowStartOnRemoteAppSession>false</DisallowStartOnRemoteAppSession>
    <UseUnifiedSchedulingEngine>true</UseUnifiedSchedulingEngine>
    <WakeToRun>false</WakeToRun>
    <ExecutionTimeLimit>P3D</ExecutionTimeLimit>
    <Priority>7</Priority>
  </Settings>
  <Actions Context="Author">
    <Exec>
      <Command>cmd</Command>
      <Arguments>/c timeout -t 60</Arguments>
    </Exec>
  </Actions>
</Task> 
```



Per salvare l'attività in un computer Windows, salvare il codice XML precedente come file di testo e usare la riga di comando seguente:

`Schtasks.exe /create /tn <task name> /xml <text file name>`

**Utilizzo di C**

È anche possibile creare un'attività di manutenzione automatica usando il codice C. Di seguito è riportato un esempio di codice che può essere usato per configurare le impostazioni di manutenzione automatica di un'attività:


```
/********************************************************************
This sample creates a maintenance task to start cmd window during maintenance opportunities with periodicity of 2 days and deadline 0f 14 days.
********************************************************************/

#define _WIN32_DCOM

#include <windows.h>
#include <iostream>
#include <stdio.h>
#include <comdef.h>
#include <wincred.h>
//  Include the task header file.
#include <taskschd.h>
//#pragma comment(lib, "taskschd.lib")
//#pragma comment(lib, "comsupp.lib")

int __cdecl 
MainteanceTask( )
{
    //  ------------------------------------------------------
    //  Initialize COM.
    HRESULT hr;

    //  ------------------------------------------------------
    //  Create a name for the task.
    LPCWSTR wszTaskName = L"MaintenanceTask";

    ITaskService *pService = NULL;
    ITaskFolder *pRootFolder = NULL;
    ITaskDefinition *pTask = NULL;
    ITaskSettings *pSettings = NULL;
    IRegistrationInfo *pRegInfo= NULL;
    IPrincipal *pPrincipal = NULL;
    ITaskSettings3 *pSettings3 = NULL;
    IMaintenanceSettings* pMaintenanceSettings = NULL;
    IActionCollection *pActionCollection = NULL;
    IAction *pAction = NULL;
    IExecAction *pExecAction = NULL;
    IRegisteredTask *pRegisteredTask = NULL;

    wprintf(L"\nCreate Maintenance Task %ws", wszTaskName );

    hr = CoInitializeEx( NULL, COINIT_MULTITHREADED);
    if( FAILED(hr) )
    {
        wprintf(L"\nCoInitializeEx failed: %x", hr );
        return 1;
    }

    //  Set general COM security levels.
    hr = CoInitializeSecurity( NULL,
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
        wprintf(L"\nCoInitializeSecurity failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create an instance of the Task Service. 
    hr = CoCreateInstance( CLSID_TaskScheduler,
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_ITaskService,
                           (void**)&pService );  
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to create an instance of ITaskService: %x", hr);
        goto CleanUp;
    }
        
    //  Connect to the task service.
    hr = pService->Connect(_variant_t(), _variant_t(), _variant_t(), _variant_t());
    if( FAILED(hr) )
    {
        wprintf(L"\nITaskService::Connect failed: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Get the pointer to the root task folder.  This folder will hold the
    //  new task that is registered.
    hr = pService->GetFolder( _bstr_t( L"\\") , &pRootFolder );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Root folder pointer: %x", hr );
        goto CleanUp;
    }
    
    //  If the same task exists, remove it.
    ( void ) pRootFolder->DeleteTask( _bstr_t(wszTaskName), 0  );
    
    //  Create the task definition object to create the task.
    hr = pService->NewTask( 0, &pTask );
    if (FAILED(hr))
    {
        wprintf(L"\nFailed to CoCreate an instance of the TaskService class: %x", hr);
        goto CleanUp;
    }
        
    //  ------------------------------------------------------
    //  Get the registration info for setting the identification.
    hr = pTask->get_RegistrationInfo( &pRegInfo );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get identification pointer: %x", hr );
        goto CleanUp;
    }
    
    hr = pRegInfo->put_Author( _bstr_t(L"Author Name") );    
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put identification info: %x", hr );
        goto CleanUp;
    }

    // The task needs to grant explicit FRFX to LOCAL SERVICE (A;;FRFX;;;LS)
    hr = pRegInfo->put_SecurityDescriptor( _variant_t(L"D:P(A;;FA;;;BA)(A;;FA;;;SY)(A;;FRFX;;;LS)") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put security descriptor: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Create the principal for the task - these credentials
    //  are overwritten with the credentials passed to RegisterTaskDefinition
    hr = pTask->get_Principal( &pPrincipal );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get principal pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Set up principal logon type to interactive logon
    hr = pPrincipal->put_LogonType( TASK_LOGON_INTERACTIVE_TOKEN );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put principal info: %x", hr );
        goto CleanUp;
    }  

    //  ------------------------------------------------------
    //  Create the settings for the task
    hr = pTask->get_Settings( &pSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get settings pointer: %x", hr );
        goto CleanUp;
    }

    hr = pSettings->QueryInterface( __uuidof(ITaskSettings3), (void**) &pSettings3 );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot query ITaskSettings3 interface: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->put_UseUnifiedSchedulingEngine( VARIANT_TRUE );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_UseUnifiedSchedulingEngine: %x", hr );
        goto CleanUp;
    }

    hr = pSettings3->CreateMaintenanceSettings( &pMaintenanceSettings );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot CreateMaintenanceSettings: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Period ( _bstr_t(L"P2D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    hr = pMaintenanceSettings->put_Deadline ( _bstr_t(L"P14D") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put_Period: %x", hr );
        goto CleanUp;
    }

    //  ------------------------------------------------------
    //  Add an action to the task. This task will execute notepad.exe.     
    //  Get the task action collection pointer.
    hr = pTask->get_Actions( &pActionCollection );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot get Task collection pointer: %x", hr );
        goto CleanUp;
    }
    
    //  Create the action, specifying that it is an executable action.
    hr = pActionCollection->Create( TASK_ACTION_EXEC, &pAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot create the action: %x", hr );
        goto CleanUp;
    }

    //  QI for the executable task pointer.
    hr = pAction->QueryInterface( IID_IExecAction, (void**) &pExecAction );
    if( FAILED(hr) )
    {
        wprintf(L"\nQueryInterface call failed for IExecAction: %x", hr );
        goto CleanUp;
    }

    //  Set the path of the executable to notepad.exe.
    hr = pExecAction->put_Path( _bstr_t(L"cmd") );
    if( FAILED(hr) )
    {
        wprintf(L"\nCannot put action path: %x", hr );
        goto CleanUp;
    }  
    
    //  ------------------------------------------------------
    //  Save the task in the root folder.
    hr = pRootFolder->RegisterTaskDefinition(
            _bstr_t(wszTaskName),
            pTask,
            TASK_CREATE_OR_UPDATE, 
            _variant_t(), 
            _variant_t(), 
            TASK_LOGON_INTERACTIVE_TOKEN,
            _variant_t(L""),
            &pRegisteredTask);
    if( FAILED(hr) )
    {
        wprintf(L"\nError saving the Task : %x", hr );
        goto CleanUp;
    }
    
    wprintf(L"\nSuccess!\n----------------------------------" );

CleanUp:

    if ( pService != NULL ) pService->Release();
    if ( pRootFolder != NULL ) pRootFolder->Release();
    if ( pTask != NULL ) pTask->Release();
    if ( pSettings != NULL ) pSettings->Release();
    if ( pRegInfo != NULL ) pRegInfo->Release();
    if ( pPrincipal != NULL ) pPrincipal->Release();
    if ( pSettings3 != NULL ) pSettings3->Release();
    if ( pMaintenanceSettings != NULL ) pMaintenanceSettings->Release();
    if ( pActionCollection != NULL ) pActionCollection->Release();
    if ( pAction != NULL ) pAction->Release();
    if ( pExecAction != NULL ) pExecAction->Release();
    if ( pRegisteredTask != NULL ) pRegisteredTask->Release();

    CoUninitialize();
    return SUCCEEDED ( hr ) ? 0 : 1;
}
```



## <a name="validating-tasks"></a>Convalida di attività

Verificare che l'attività sia stata creata correttamente e venga eseguita come parte della manutenzione.

**Convalida della creazione di attività**

Usare questa riga di comando per esportare la definizione di attività in un file e assicurarsi che la definizione di attività sia come previsto:

`Schtasks.exe /Query /tn<task name> /xml <text file name>`

**Convalida dell'esecuzione dell'attività**

Eseguire questa riga di comando per avviare l'attività e verificare che l'interfaccia utente di Utilità di pianificazione (taskschd. msc) indichi che l'attività è stata eseguita:

`Schtasks.exe /Run /tn<task name>`

## <a name="resources"></a>Risorse

-   [Pianificazione attività 2,0](/previous-versions/bb756979(v=msdn.10))

 

 