---
title: Manutenzione automatica (Guida di cookbook sulla compatibilità per Windows)
description: Manutenzione automatica
ms.assetid: D3B61105-D118-42A4-8F3D-ED92EFAF597F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a839191d84f3f20fcc598b42433c888b090b2b174dd6891c0b5b9fc72f0af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028869"
---
# <a name="automatic-maintenance"></a>Manutenzione automatica

## <a name="platforms"></a>Piattaforme

**Client** : Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

Windows dipende dall'esecuzione della posta in arrivo e dalle attività di manutenzione di terze parti per gran parte del valore aggiunto, tra cui l'aggiornamento di Windows e la deframmentazione automatica del disco, nonché gli aggiornamenti e le analisi antivirus. Inoltre, le aziende usano spesso attività di manutenzione come l'analisi di Protezione accesso alla rete (NAP) per applicare gli standard di sicurezza in tutte le workstation aziendali.

L'attività di Windows è progettata per essere eseguita in background con interazione utente limitata e impatto minimo sulle prestazioni e sull'efficienza energetica. Tuttavia, in Windows 7 e versioni precedenti, le prestazioni e l'efficienza energetica sono ancora interessate dalla pianificazione non deterministica e ampiamente variata delle diverse attività di manutenzione in Windows. La velocità di risposta agli utenti si riduce quando viene eseguita un'attività di manutenzione mentre gli utenti usano attivamente il computer. Le app spesso chiedono spesso all'utente di aggiornare il software ed eseguire la manutenzione in background e indirizzano gli utenti a più esperienze, tra cui Centro notifiche, Pannello di controllo, aggiornamento Windows, snap-in MMC Utilità di pianificazione e controlli di terze parti.

L'obiettivo di Manutenzione automatica è combinare tutte le attività di manutenzione in background in Windows e aiutare gli sviluppatori di terze parti ad aggiungere la propria attività di manutenzione a Windows senza influire negativamente sulle prestazioni e sull'efficienza energetica. Inoltre, Manutenzione automatica utenti e aziende di avere il controllo della pianificazione e della configurazione delle attività di manutenzione.

**Problemi principali**

Manutenzione automatica è progettato per risolvere questi problemi relativi all'attività di manutenzione in Windows:

-   Pianificazione delle scadenze
-   Conflitti di utilizzo delle risorse
-   Efficienza energetica
-   Trasparenza per l'utente

## <a name="functionality"></a>Funzionalità

Manutenzione automatica agevola l'efficienza di inattività e consente l'esecuzione di tutte le attività in modo ordinato e prioritario. Consente inoltre di abilitare visibilità unificata e controllo sulle attività di manutenzione e consente agli sviluppatori di terze parti di aggiungere la propria attività di manutenzione Windows senza influire negativamente sulle prestazioni e sull'efficienza energetica. A tale scopo, offre una modalità completamente automatica, la modalità avviata dall'utente, l'arresto automatico, le scadenze e le notifiche e il controllo aziendale. Queste sono descritte di seguito.

**Modalità completamente automatica**

Questa modalità predefinita consente la pianificazione intelligente durante il tempo di inattività del PC e in orari pianificati, ovvero l'esecuzione e la sospensione automatica dell'attività di manutenzione senza alcun intervento dell'utente. L'utente può impostare una pianificazione settimanale o giornaliera. Tutte le attività di manutenzione non sono interattive e vengono eseguite in modo invisibile all'utente.

Il computer viene ripreso automaticamente dalla sospensione quando è probabile che il sistema non sia in uso, rispettando i criteri di risparmio energia, che nel caso dei portatili consentono per impostazione predefinita la riattivazione solo se è alimentato da CA. Le risorse di sistema complete a potenza elevata vengono usate per completare l'attività di manutenzione il più rapidamente possibile. Se il sistema è stato ripreso dalla sospensione per Manutenzione automatica, viene richiesto di tornare in sospensione.

Tutte le interazioni utente necessarie correlate ad attività quali la configurazione vengono eseguite al di fuori Manutenzione automatica esecuzione.

**Modalità avviata dall'utente**

Se gli utenti devono prepararsi per il viaggio, aspettarsi di essere alimentato a batteria per un periodo prolungato o di voler ottimizzare le prestazioni e la velocità di risposta, hanno la possibilità di avviare Manutenzione automatica su richiesta. Gli utenti possono configurare Manutenzione automatica, inclusa la pianificazione dell'esecuzione automatica. Possono visualizzare lo stato corrente dell'esecuzione Manutenzione automatica e arrestare l Manutenzione automatica se necessario.

**Arresto automatico**

Manutenzione automatica automaticamente le attività di manutenzione in esecuzione se l'utente inizia a interagire con il computer. L'attività di manutenzione riprenderà quando il sistema torna allo stato di inattività.

> [!Note]  
> Tutte le attività in Manutenzione automatica devono supportare l'arresto in un massimo di 2 secondi. All'utente deve essere notificato che l'attività è stata arrestata.

 

**Scadenze e notifica**

L'attività di manutenzione critica deve essere eseguita all'interno di un intervallo di tempo predefinito. Se le attività critiche non sono state in grado di essere eseguite entro il tempo designato, Manutenzione automatica l'esecuzione verrà avviata automaticamente alla successiva opportunità di inattività del sistema disponibile. Tuttavia, se lo stato dell'attività rimane entro la scadenza, Manutenzione automatica notifica all'utente l'attività e fornisce un'opzione per un'esecuzione manuale di Manutenzione automatica. Tutte le attività pianificate per la manutenzione verranno eseguite, anche se le attività più care hanno la precedenza. Questa attività può influire sulla velocità di risposta e sulle prestazioni del sistema. Pertanto, Manutenzione automatica notifica all'utente che è in esecuzione un'attività di manutenzione critica.

**Enterprise controllo**

Enterprise I professionisti IT devono essere in grado di determinare quando Manutenzione automatica viene eseguito nei propri sistemi Windows, applicare tale pianificazione tramite interfacce di gestione standardizzate e recuperare i dati degli eventi sullo stato dei tentativi di Manutenzione automatica'esecuzione. Inoltre, i professionisti IT devono essere in grado di richiamare attività Manutenzione automatica in remoto tramite interfacce di gestione standard. Ogni volta Manutenzione automatica, viene eseguita la segnalazione dello stato, incluse le notifiche Manutenzione automatica non è stato possibile eseguire l'attività perché l'utente ha sospeso manualmente l'attività. I professionisti IT devono prendere in considerazione lo spostamento degli script di accesso Manutenzione automatica per rendere più rapida l'esperienza di accesso dell'utente.

## <a name="creating-an-automatic-maintenance-task"></a>Creazione di un'Manutenzione automatica lavoro

Questa sezione illustra in dettaglio come gli sviluppatori possono creare un'attività usando una definizione di attività in linguaggio XML o C. Tenere presente che le attività di manutenzione non devono avviare alcuna interfaccia utente che richieda l'interazione dell'utente, perché Manutenzione automatica è completamente invisibile all'utente e viene eseguita quando l'utente non è presente. In effetti, se l'utente interagisce con il computer durante Manutenzione automatica, tutte le attività in corso verranno terminate fino al periodo di inattività successivo.

**Uso di XML**

Utilità di pianificazione include uno strumento da riga di comando predefinito, schtasks.exe, che può importare una definizione di attività in formato XML. Lo schema per la definizione dell'attività è documentato in https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx . Di seguito è riportato un esempio di Manutenzione automatica attività definita in XML.


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



Per salvare l'attività in un computer Windows, salvare il codice XML precedente come file di testo e usare questa riga di comando:

`Schtasks.exe /create /tn <task name> /xml <text file name>`

**Uso di C**

È Manutenzione automatica possibile creare un'attività usando il codice C. Di seguito è riportato un esempio di codice che può essere usato per configurare le impostazioni Manutenzione automatica attività:


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



## <a name="validating-tasks"></a>Convalida delle attività

Verificare che l'attività sia stata creata correttamente ed eseguita come parte della manutenzione.

**Convalida della creazione di attività**

Usare questa riga di comando per esportare la definizione dell'attività in un file e assicurarsi che la definizione dell'attività sia quella prevista:

`Schtasks.exe /Query /tn<task name> /xml <text file name>`

**Convalida dell'esecuzione dell'attività**

Eseguire questa riga di comando per avviare l'attività e verificare che l'interfaccia utente di Utilità di pianificazione (taskschd.msc) mostra che l'attività è stata eseguita:

`Schtasks.exe /Run /tn<task name>`

## <a name="resources"></a>Risorse

-   [Pianificazione attività 2.0](/previous-versions/bb756979(v=msdn.10))

 

 