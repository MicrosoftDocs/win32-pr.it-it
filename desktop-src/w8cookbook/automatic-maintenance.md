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
# <a name="automatic-maintenance"></a><span data-ttu-id="d48f4-103">Manutenzione automatica</span><span class="sxs-lookup"><span data-stu-id="d48f4-103">Automatic Maintenance</span></span>

## <a name="platforms"></a><span data-ttu-id="d48f4-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="d48f4-104">Platforms</span></span>

<span data-ttu-id="d48f4-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="d48f4-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="d48f4-106">**Server** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d48f4-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="d48f4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d48f4-107">Description</span></span>

<span data-ttu-id="d48f4-108">Windows dipende dall'esecuzione della posta in arrivo e dall'attività di manutenzione di terze parti per gran parte del suo valore aggiunto, inclusi Windows Update e la deframmentazione automatica del disco, nonché gli aggiornamenti e le analisi antivirus.</span><span class="sxs-lookup"><span data-stu-id="d48f4-108">Windows depends on execution of inbox and third party maintenance activity for much of its value-add, including Windows Update, and automatic disk defragmentation, as well as antivirus updates and scans.</span></span> <span data-ttu-id="d48f4-109">Inoltre, le aziende utilizzano spesso attività di manutenzione, ad esempio l'analisi di protezione accesso alla rete (NAP), per consentire l'applicazione degli standard di sicurezza in tutte le workstation aziendali.</span><span class="sxs-lookup"><span data-stu-id="d48f4-109">Additionally, enterprises frequently use maintenance activity such as Network Access Protection (NAP) scanning to help enforce security standards on all enterprise workstations.</span></span>

<span data-ttu-id="d48f4-110">L'attività di manutenzione in Windows è progettata per essere eseguita in background con un'interazione utente limitata e un minimo effetto sulle prestazioni e sull'efficienza energetica.</span><span class="sxs-lookup"><span data-stu-id="d48f4-110">Maintenance activity in Windows is designed to run in the background with limited user interaction and minimal impact to performance and energy efficiency.</span></span> <span data-ttu-id="d48f4-111">Tuttavia, in Windows 7 e versioni precedenti, le prestazioni e l'efficienza energetica sono ancora interessate a causa della pianificazione non deterministica e molto variegata delle diverse attività di manutenzione di Windows.</span><span class="sxs-lookup"><span data-stu-id="d48f4-111">However, in Windows 7 and earlier versions, performance and energy efficiency are still impacted due to the non-deterministic and widely varied schedule of the multiple maintenance activities in Windows.</span></span> <span data-ttu-id="d48f4-112">La velocità di risposta agli utenti viene ridotta quando viene eseguita l'attività di manutenzione mentre gli utenti usano attivamente il computer.</span><span class="sxs-lookup"><span data-stu-id="d48f4-112">Responsiveness to users is reduced when maintenance activity runs while users are actively using the computer.</span></span> <span data-ttu-id="d48f4-113">Spesso le app richiedono inoltre all'utente di aggiornare il software e di eseguire la manutenzione in background e indirizzare gli utenti a più esperienze, tra cui centro operativo, pannello di controllo, Windows Update, Utilità di pianificazione snap-in MMC e controlli di terze parti.</span><span class="sxs-lookup"><span data-stu-id="d48f4-113">Apps also frequently ask the user to update their software and run background maintenance, and direct users to multiple experiences, including Action Center, Control Panel, Windows Update, Task Scheduler MMC snap-in, and third-party controls.</span></span>

<span data-ttu-id="d48f4-114">L'obiettivo della manutenzione automatica è combinare tutte le attività di manutenzione in background in Windows e aiutare gli sviluppatori di terze parti ad aggiungere le attività di manutenzione a Windows senza influire negativamente sulle prestazioni e sull'efficienza energetica.</span><span class="sxs-lookup"><span data-stu-id="d48f4-114">The goal of Automatic Maintenance is to combine all background maintenance activity in Windows and help third-party developers add their maintenance activity to Windows without negatively impacting performance and energy efficiency.</span></span> <span data-ttu-id="d48f4-115">Inoltre, la manutenzione automatica consente agli utenti e alle aziende di controllare la pianificazione e la configurazione delle attività di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="d48f4-115">Additionally, Automatic Maintenance enables users as well as enterprises to be in control of maintenance activity scheduling and configuration.</span></span>

<span data-ttu-id="d48f4-116">**Problemi principali**</span><span class="sxs-lookup"><span data-stu-id="d48f4-116">**Key problems**</span></span>

<span data-ttu-id="d48f4-117">La manutenzione automatica è progettata per risolvere i problemi relativi alle attività di manutenzione in Windows:</span><span class="sxs-lookup"><span data-stu-id="d48f4-117">Automatic Maintenance is designed to address these problems with maintenance activity in Windows:</span></span>

-   <span data-ttu-id="d48f4-118">Pianificazione scadenza</span><span class="sxs-lookup"><span data-stu-id="d48f4-118">Deadline scheduling</span></span>
-   <span data-ttu-id="d48f4-119">Conflitti di utilizzo delle risorse</span><span class="sxs-lookup"><span data-stu-id="d48f4-119">Resource utilization conflicts</span></span>
-   <span data-ttu-id="d48f4-120">Efficienza energetica</span><span class="sxs-lookup"><span data-stu-id="d48f4-120">Energy efficiency</span></span>
-   <span data-ttu-id="d48f4-121">Trasparenza per l'utente</span><span class="sxs-lookup"><span data-stu-id="d48f4-121">Transparency to the user</span></span>

## <a name="functionality"></a><span data-ttu-id="d48f4-122">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="d48f4-122">Functionality</span></span>

<span data-ttu-id="d48f4-123">La manutenzione automatica facilita l'efficienza di inattività e consente l'esecuzione di tutte le attività in modo tempestivo e in ordine di priorità.</span><span class="sxs-lookup"><span data-stu-id="d48f4-123">Automatic Maintenance facilitates idle efficiency and permits all activity to run in a timely and prioritized fashion.</span></span> <span data-ttu-id="d48f4-124">Consente inoltre di abilitare la visibilità e il controllo unificato delle attività di manutenzione e consente agli sviluppatori di terze parti di aggiungere le attività di manutenzione a Windows senza influire negativamente sulle prestazioni e sull'efficienza energetica.</span><span class="sxs-lookup"><span data-stu-id="d48f4-124">It also helps enable unified visibility and control over maintenance activity, and allows third-party developers to add their maintenance activity to Windows without negatively impacting performance and energy efficiency.</span></span> <span data-ttu-id="d48f4-125">A tale scopo, offre una modalità completamente automatica, la modalità avviata dall'utente, l'arresto automatico, le scadenze e le notifiche e il controllo aziendale.</span><span class="sxs-lookup"><span data-stu-id="d48f4-125">To do this, it provides a fully automatic mode, user-initiated mode, automatic stop, deadlines and notification, and enterprise control.</span></span> <span data-ttu-id="d48f4-126">Ognuno di essi è descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="d48f4-126">These are each described below.</span></span>

<span data-ttu-id="d48f4-127">**Modalità completamente automatica**</span><span class="sxs-lookup"><span data-stu-id="d48f4-127">**Fully automatic mode**</span></span>

<span data-ttu-id="d48f4-128">Questa modalità predefinita consente la pianificazione intelligente durante il tempo di inattività del PC e in orari pianificati, ovvero l'esecuzione e la sospensione automatica delle attività di manutenzione senza alcun intervento da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d48f4-128">This default mode enables intelligent scheduling during PC idle-time and at scheduled times—the execution and automatic pausing of maintenance activity without any user intervention.</span></span> <span data-ttu-id="d48f4-129">L'utente può impostare una pianificazione settimanale o giornaliera.</span><span class="sxs-lookup"><span data-stu-id="d48f4-129">The user can set a weekly or daily schedule.</span></span> <span data-ttu-id="d48f4-130">Tutte le attività di manutenzione non sono interattive ed eseguite in modo invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="d48f4-130">All maintenance activity is non-interactive and executes silently.</span></span>

<span data-ttu-id="d48f4-131">Il computer viene ripreso automaticamente dalla modalità di sospensione quando non è probabile che il sistema sia in uso, rispettando i criteri di risparmio energia, che nel caso dei portatili, per impostazione predefinita è possibile abilitare la riattivazione solo se si trova in alimentazione AC.</span><span class="sxs-lookup"><span data-stu-id="d48f4-131">The computer automatically is resumed from sleep when the system is not likely to be in use, respecting the Power Management policy, which in the case of laptops, defaults to allow wake-up only if it is on AC power.</span></span> <span data-ttu-id="d48f4-132">Le risorse di sistema complete a potenza elevata vengono usate per completare l'attività di manutenzione nel minor tempo possibile.</span><span class="sxs-lookup"><span data-stu-id="d48f4-132">Full system resources at high power are used to complete the maintenance activity as quickly as possible.</span></span> <span data-ttu-id="d48f4-133">Se il sistema è stato ripreso dalla sospensione per la manutenzione automatica, viene richiesto di tornare alla modalità sospensione.</span><span class="sxs-lookup"><span data-stu-id="d48f4-133">If the system was resumed from sleep for Automatic Maintenance, it is requested to return to sleep.</span></span>

<span data-ttu-id="d48f4-134">Eventuali interazioni utente richieste correlate a attività come la configurazione vengono eseguite al di fuori dell'esecuzione automatica della manutenzione.</span><span class="sxs-lookup"><span data-stu-id="d48f4-134">Any required user interactions related to activities such as configuration are performed outside of Automatic Maintenance execution.</span></span>

<span data-ttu-id="d48f4-135">**Modalità avviata dall'utente**</span><span class="sxs-lookup"><span data-stu-id="d48f4-135">**User-initiated mode**</span></span>

<span data-ttu-id="d48f4-136">Se gli utenti devono prepararsi per la corsa, prevedere un tempo di alimentazione della batteria per un tempo prolungato o voler ottimizzare le prestazioni e la velocità di risposta, hanno la possibilità di avviare la manutenzione automatica su richiesta.</span><span class="sxs-lookup"><span data-stu-id="d48f4-136">If users need to prepare for travel, expect to be on battery power for a prolonged time, or wish to optimize for performance and responsiveness, they have the option of initiating Automatic Maintenance on demand.</span></span> <span data-ttu-id="d48f4-137">Gli utenti possono configurare gli attributi di manutenzione automatica, inclusa la pianificazione di esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="d48f4-137">Users can configure Automatic Maintenance attributes, including the automatic run schedule.</span></span> <span data-ttu-id="d48f4-138">Possono visualizzare lo stato corrente dell'esecuzione di manutenzione automatica e possono arrestare la manutenzione automatica, se necessario.</span><span class="sxs-lookup"><span data-stu-id="d48f4-138">They can view the current status of Automatic Maintenance execution, and they can stop Automatic Maintenance if needed.</span></span>

<span data-ttu-id="d48f4-139">**Arresto automatico**</span><span class="sxs-lookup"><span data-stu-id="d48f4-139">**Automatic stop**</span></span>

<span data-ttu-id="d48f4-140">La manutenzione automatica interrompe automaticamente le attività di manutenzione in corso se l'utente inizia a interagire con il computer.</span><span class="sxs-lookup"><span data-stu-id="d48f4-140">Automatic Maintenance automatically stops currently running maintenance activities if the user starts interacting with the computer.</span></span> <span data-ttu-id="d48f4-141">L'attività di manutenzione viene ripresa quando il sistema torna allo stato inattivo.</span><span class="sxs-lookup"><span data-stu-id="d48f4-141">Maintenance activity will resume when the system returns to idle status.</span></span>

> [!Note]  
> <span data-ttu-id="d48f4-142">Tutte le attività nella manutenzione automatica devono supportare l'arresto in 2 secondi o meno.</span><span class="sxs-lookup"><span data-stu-id="d48f4-142">All activities in Automatic Maintenance must support stopping in 2 seconds or less.</span></span> <span data-ttu-id="d48f4-143">L'utente deve ricevere una notifica che indica che l'attività è stata arrestata.</span><span class="sxs-lookup"><span data-stu-id="d48f4-143">The user should be notified that the activity has been stopped.</span></span>

 

<span data-ttu-id="d48f4-144">**Scadenze e notifiche**</span><span class="sxs-lookup"><span data-stu-id="d48f4-144">**Deadlines and notification**</span></span>

<span data-ttu-id="d48f4-145">L'attività di manutenzione critica deve essere eseguita all'interno di un intervallo di tempo predefinito.</span><span class="sxs-lookup"><span data-stu-id="d48f4-145">Critical maintenance activity must execute within a pre-defined time window.</span></span> <span data-ttu-id="d48f4-146">Se non è stato possibile eseguire attività critiche nell'intervallo di tempo specificato, la manutenzione automatica verrà avviata automaticamente alla successiva opportunità di inattività del sistema disponibile.</span><span class="sxs-lookup"><span data-stu-id="d48f4-146">If critical tasks have not been able to run within their designated time, Automatic Maintenance will automatically start executing at the next available system idle opportunity.</span></span> <span data-ttu-id="d48f4-147">Tuttavia, se lo stato dell'attività resta dietro la scadenza, la manutenzione automatica invierà una notifica all'utente sull'attività e fornirà un'opzione per un'esecuzione manuale della manutenzione automatica.</span><span class="sxs-lookup"><span data-stu-id="d48f4-147">However, if the task state remains behind deadline, Automatic Maintenance will notify the user about the activity and provide an option for a manual run of Automatic Maintenance.</span></span> <span data-ttu-id="d48f4-148">Tutte le attività pianificate per la manutenzione verranno eseguite, sebbene le attività più affamate abbiano la precedenza.</span><span class="sxs-lookup"><span data-stu-id="d48f4-148">All tasks scheduled for maintenance will run, although the most starved tasks take precedence.</span></span> <span data-ttu-id="d48f4-149">Questa attività può influisca sulle prestazioni e sulla velocità di risposta del sistema; Pertanto, la manutenzione automatica invierà una notifica all'utente dell'esecuzione dell'attività di manutenzione critica.</span><span class="sxs-lookup"><span data-stu-id="d48f4-149">This activity may impact system responsiveness and performance; therefore, Automatic Maintenance will notify the user that critical maintenance activity is executing.</span></span>

<span data-ttu-id="d48f4-150">**Controllo Enterprise**</span><span class="sxs-lookup"><span data-stu-id="d48f4-150">**Enterprise control**</span></span>

<span data-ttu-id="d48f4-151">I professionisti IT aziendali dovrebbero essere in grado di determinare quando viene eseguita la manutenzione automatica sui sistemi Windows, applicare tale pianificazione tramite interfacce di gestione standardizzate e recuperare i dati degli eventi sullo stato dei tentativi di esecuzione automatica della manutenzione.</span><span class="sxs-lookup"><span data-stu-id="d48f4-151">Enterprise IT professionals should be able to determine when Automatic Maintenance executes on their Windows systems, enforce that schedule via standardized management interfaces, and retrieve event data about the status of Automatic Maintenance execution attempts.</span></span> <span data-ttu-id="d48f4-152">Inoltre, i professionisti IT devono essere in grado di richiamare attività di manutenzione automatica specifiche in modalità remota tramite interfacce di gestione standard.</span><span class="sxs-lookup"><span data-stu-id="d48f4-152">Additionally, IT professionals should be able to invoke specific Automatic Maintenance activity remotely via standard management interfaces.</span></span> <span data-ttu-id="d48f4-153">Ogni volta che viene eseguita la manutenzione automatica, la creazione di rapporti di stato, incluse le notifiche quando non è stato possibile eseguire la manutenzione automatica perché l'utente ha sospeso manualmente l'attività, viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d48f4-153">Each time Automatic Maintenance executes, status reporting, including notifications when Automatic Maintenance could not be executed because the user has manually paused the activity, runs.</span></span> <span data-ttu-id="d48f4-154">I professionisti IT dovrebbero prendere in considerazione la possibilità di trasferire gli script di accesso alla manutenzione automatica per semplificare l'esperienza di accesso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d48f4-154">IT professionals should consider moving logon scripts to Automatic Maintenance to help make the user’s logon experience quicker.</span></span>

## <a name="creating-an-automatic-maintenance-task"></a><span data-ttu-id="d48f4-155">Creazione di un'attività di manutenzione automatica</span><span class="sxs-lookup"><span data-stu-id="d48f4-155">Creating an Automatic Maintenance task</span></span>

<span data-ttu-id="d48f4-156">In questa sezione viene illustrato in dettaglio come gli sviluppatori possono creare un'attività utilizzando una definizione di attività in linguaggio XML o C.</span><span class="sxs-lookup"><span data-stu-id="d48f4-156">This section details how developers can create a task using a task definition in XML or C language.</span></span> <span data-ttu-id="d48f4-157">Tenere presente che l'attività di manutenzione non deve avviare alcuna interfaccia utente che richiede l'interazione dell'utente, perché la manutenzione automatica è completamente invisibile e viene eseguita quando l'utente non è presente.</span><span class="sxs-lookup"><span data-stu-id="d48f4-157">Keep in mind that maintenance activity should not launch any user interface that requires user interaction, as Automatic Maintenance is completely silent and runs when the user is not present.</span></span> <span data-ttu-id="d48f4-158">Infatti, se l'utente interagisce con il computer durante la manutenzione automatica, le attività in corso verranno terminate fino al periodo di inattività successivo.</span><span class="sxs-lookup"><span data-stu-id="d48f4-158">Indeed, if the user interacts with the computer during Automatic Maintenance, any tasks in process will be ended until the next idle period.</span></span>

<span data-ttu-id="d48f4-159">**Utilizzo di XML**</span><span class="sxs-lookup"><span data-stu-id="d48f4-159">**Using XML**</span></span>

<span data-ttu-id="d48f4-160">Utilità di pianificazione include uno strumento da riga di comando incorporato, schtasks.exe, che consente di importare una definizione di attività in formato XML.</span><span class="sxs-lookup"><span data-stu-id="d48f4-160">Task Scheduler includes a built-in command-line tool, schtasks.exe, that can import a task definition in XML format.</span></span> <span data-ttu-id="d48f4-161">Lo schema per la definizione di attività è documentato in https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx .</span><span class="sxs-lookup"><span data-stu-id="d48f4-161">The schema for task definition is documented at https://msdn.microsoft.com/library/aa383609(v=VS.85).aspx.</span></span> <span data-ttu-id="d48f4-162">Di seguito è riportato un esempio di un'attività di manutenzione automatica definita in XML.</span><span class="sxs-lookup"><span data-stu-id="d48f4-162">Below is an example of an Automatic Maintenance task defined in XML.</span></span>


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



<span data-ttu-id="d48f4-163">Per salvare l'attività in un computer Windows, salvare il codice XML precedente come file di testo e usare la riga di comando seguente:</span><span class="sxs-lookup"><span data-stu-id="d48f4-163">To save the task on a Windows computer, save the above XML as a text file and use this command line:</span></span>

`Schtasks.exe /create /tn <task name> /xml <text file name>`

<span data-ttu-id="d48f4-164">**Utilizzo di C**</span><span class="sxs-lookup"><span data-stu-id="d48f4-164">**Using C**</span></span>

<span data-ttu-id="d48f4-165">È anche possibile creare un'attività di manutenzione automatica usando il codice C.</span><span class="sxs-lookup"><span data-stu-id="d48f4-165">An Automatic Maintenance task also can be created using C code.</span></span> <span data-ttu-id="d48f4-166">Di seguito è riportato un esempio di codice che può essere usato per configurare le impostazioni di manutenzione automatica di un'attività:</span><span class="sxs-lookup"><span data-stu-id="d48f4-166">Below is a code sample that can be used to configure a task’s Automatic Maintenance settings:</span></span>


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



## <a name="validating-tasks"></a><span data-ttu-id="d48f4-167">Convalida di attività</span><span class="sxs-lookup"><span data-stu-id="d48f4-167">Validating tasks</span></span>

<span data-ttu-id="d48f4-168">Verificare che l'attività sia stata creata correttamente e venga eseguita come parte della manutenzione.</span><span class="sxs-lookup"><span data-stu-id="d48f4-168">Validate that the task has been created successfully and runs as part of maintenance.</span></span>

<span data-ttu-id="d48f4-169">**Convalida della creazione di attività**</span><span class="sxs-lookup"><span data-stu-id="d48f4-169">**Validating task creation**</span></span>

<span data-ttu-id="d48f4-170">Usare questa riga di comando per esportare la definizione di attività in un file e assicurarsi che la definizione di attività sia come previsto:</span><span class="sxs-lookup"><span data-stu-id="d48f4-170">Use this command line to export the task definition to a file and ensure that the task definition is as expected:</span></span>

`Schtasks.exe /Query /tn<task name> /xml <text file name>`

<span data-ttu-id="d48f4-171">**Convalida dell'esecuzione dell'attività**</span><span class="sxs-lookup"><span data-stu-id="d48f4-171">**Validating task execution**</span></span>

<span data-ttu-id="d48f4-172">Eseguire questa riga di comando per avviare l'attività e verificare che l'interfaccia utente di Utilità di pianificazione (taskschd. msc) indichi che l'attività è stata eseguita:</span><span class="sxs-lookup"><span data-stu-id="d48f4-172">Run this command line to launch the task and validate that the Task Scheduler UI (taskschd.msc) shows the task has run:</span></span>

`Schtasks.exe /Run /tn<task name>`

## <a name="resources"></a><span data-ttu-id="d48f4-173">Risorse</span><span class="sxs-lookup"><span data-stu-id="d48f4-173">Resources</span></span>

-   <span data-ttu-id="d48f4-174">[Pianificazione attività 2,0](/previous-versions/bb756979(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="d48f4-174">[Task Schedule 2.0](/previous-versions/bb756979(v=msdn.10))</span></span>

 

 