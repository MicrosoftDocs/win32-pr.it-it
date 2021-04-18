---
description: Per ricevere notifiche dal provider del registro di sistema, un'applicazione di gestione deve registrarsi come consumer di eventi temporanei.
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: Registrazione per eventi registro di sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 886046f5ffef366cdba2efb86629019f2ee0b5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318540"
---
# <a name="registering-for-system-registry-events"></a><span data-ttu-id="c6968-103">Registrazione per eventi registro di sistema</span><span class="sxs-lookup"><span data-stu-id="c6968-103">Registering for System Registry Events</span></span>

<span data-ttu-id="c6968-104">Per ricevere notifiche dal provider [del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) , un'applicazione di gestione deve registrarsi come consumer di eventi temporanei.</span><span class="sxs-lookup"><span data-stu-id="c6968-104">To receive notifications from the [System Registry](/previous-versions/windows/desktop/regprov/system-registry-provider) provider, a management application must register as a temporary event consumer.</span></span> <span data-ttu-id="c6968-105">La maggior parte dei requisiti per la registrazione per il provider del registro di sistema è identica a quella di qualsiasi altra registrazione di eventi, ad eccezione del fatto che è necessario eseguire anche la procedura riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="c6968-105">Most of the requirements to register for the System Registry provider are the same as any other event registration, except you must also perform the following procedure.</span></span>

<span data-ttu-id="c6968-106">Il provider del registro di sistema fornisce le classi di evento per gli eventi nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6968-106">The registry provider supplies event classes for events in the system registry.</span></span> <span data-ttu-id="c6968-107">Per ulteriori informazioni sulla registrazione di eventi generali, vedere [ricezione di un evento WMI](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="c6968-107">For more information about general event registration, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="c6968-108">Nella procedura seguente viene descritto come eseguire la registrazione per gli eventi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6968-108">The following procedure describes how to register for system registry events.</span></span>

<span data-ttu-id="c6968-109">**Per eseguire la registrazione per gli eventi del registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="c6968-109">**To register for system registry events**</span></span>

1.  <span data-ttu-id="c6968-110">Chiamare un metodo di query di notifica.</span><span class="sxs-lookup"><span data-stu-id="c6968-110">Call a notification query method.</span></span>

    <span data-ttu-id="c6968-111">In uno script o in C++ usare una query di notifica, ad esempio [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) o [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync).</span><span class="sxs-lookup"><span data-stu-id="c6968-111">In either script or C++, use a notification query such as [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) or [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync).</span></span> <span data-ttu-id="c6968-112">Creare una stringa di query per il parametro *bstrQuery* di **IWbemServices:: ExecNotificationQueryAsync** o *strQuery* nello script.</span><span class="sxs-lookup"><span data-stu-id="c6968-112">Create a query string for the *bstrQuery* parameter of **IWbemServices::ExecNotificationQueryAsync** or the *strQuery* in script.</span></span>

2.  <span data-ttu-id="c6968-113">Determinare il tipo di evento che si desidera ricevere e creare la query.</span><span class="sxs-lookup"><span data-stu-id="c6968-113">Determine which type of event you want to receive and create the query.</span></span>

    <span data-ttu-id="c6968-114">Nella tabella seguente sono elencate le classi di eventi del registro di sistema che è possibile utilizzare.</span><span class="sxs-lookup"><span data-stu-id="c6968-114">The following table lists the registry event classes that you can use.</span></span>

    

    | <span data-ttu-id="c6968-115">classe di evento</span><span class="sxs-lookup"><span data-stu-id="c6968-115">Event class</span></span>                                                      | <span data-ttu-id="c6968-116">Posizione hive</span><span class="sxs-lookup"><span data-stu-id="c6968-116">Hive location</span></span>        | <span data-ttu-id="c6968-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6968-117">Description</span></span>                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [<span data-ttu-id="c6968-118">**RegistryEvent**</span><span class="sxs-lookup"><span data-stu-id="c6968-118">**RegistryEvent**</span></span>](/previous-versions/windows/desktop/regprov/registryevent)                       | <span data-ttu-id="c6968-119">N/D</span><span class="sxs-lookup"><span data-stu-id="c6968-119">N/A</span></span><br/>       | <span data-ttu-id="c6968-120">Classe di base astratta per le modifiche nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6968-120">Abstract base class for changes in the registry.</span></span><br/> |
    | [<span data-ttu-id="c6968-121">**RegistryTreeChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="c6968-121">**RegistryTreeChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | <span data-ttu-id="c6968-122">RootPath</span><span class="sxs-lookup"><span data-stu-id="c6968-122">RootPath</span></span><br/>  | <span data-ttu-id="c6968-123">Monitora le modifiche apportate a una gerarchia di chiavi.</span><span class="sxs-lookup"><span data-stu-id="c6968-123">Monitors changes to a hierarchy of keys.</span></span><br/>         |
    | [<span data-ttu-id="c6968-124">**RegistryKeyChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="c6968-124">**RegistryKeyChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | <span data-ttu-id="c6968-125">KeyPath</span><span class="sxs-lookup"><span data-stu-id="c6968-125">KeyPath</span></span><br/>   | <span data-ttu-id="c6968-126">Monitora le modifiche apportate a una singola chiave.</span><span class="sxs-lookup"><span data-stu-id="c6968-126">Monitors changes to a single key.</span></span><br/>                |
    | [<span data-ttu-id="c6968-127">**RegistryValueChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="c6968-127">**RegistryValueChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | <span data-ttu-id="c6968-128">ValueName</span><span class="sxs-lookup"><span data-stu-id="c6968-128">ValueName</span></span><br/> | <span data-ttu-id="c6968-129">Monitora le modifiche apportate a un singolo valore.</span><span class="sxs-lookup"><span data-stu-id="c6968-129">Monitors changes to a single value.</span></span><br/>              |

    

     

    <span data-ttu-id="c6968-130">Queste classi hanno una proprietà denominata **hive** che identifica la gerarchia delle chiavi da monitorare per la modifica, ad esempio **il \_ \_ computer locale HKEY**.</span><span class="sxs-lookup"><span data-stu-id="c6968-130">These classes have a property called **Hive** that identifies the hierarchy of keys to be monitored for change, such as **HKEY\_LOCAL\_MACHINE**.</span></span>

    <span data-ttu-id="c6968-131">Le modifiche apportate alle **\_ classi HKEY \_ radice** e HKEY gli hive **\_ correnti \_ dell'utente** non sono supportate da [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) o dalle classi derivate, ad esempio [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).</span><span class="sxs-lookup"><span data-stu-id="c6968-131">Changes to the **HKEY\_CLASSES\_ROOT** and **HKEY\_CURRENT\_USER** hives are not supported by [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) or classes derived from it, such as [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).</span></span>

3.  <span data-ttu-id="c6968-132">Creare la clausola WHERE per la registrazione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="c6968-132">Create the WHERE clause for your event registration.</span></span>

    <span data-ttu-id="c6968-133">Il provider del registro di sistema ha regole specifiche per le clausole WHERE.</span><span class="sxs-lookup"><span data-stu-id="c6968-133">The System Registry provider has specific rules for WHERE clauses.</span></span> <span data-ttu-id="c6968-134">Per ulteriori informazioni, vedere [creazione di una clausola WHERE corretta per il provider del registro di sistema](creating-a-proper-where-clause-for-the-registry-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c6968-134">For more information, see [Creating a Proper WHERE Clause for the Registry Provider](creating-a-proper-where-clause-for-the-registry-provider.md).</span></span> <span data-ttu-id="c6968-135">Per informazioni generali sulla creazione di una clausola WHERE, vedere [esecuzione di query con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="c6968-135">For more general information about creating a WHERE clause, see [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="c6968-136">Determinare se il consumer riceve gli eventi.</span><span class="sxs-lookup"><span data-stu-id="c6968-136">Determine whether your consumer is receiving events.</span></span>

    <span data-ttu-id="c6968-137">Il provider del registro di sistema non garantisce che tutti gli eventi inviati vengano recapitati.</span><span class="sxs-lookup"><span data-stu-id="c6968-137">The System Registry provider does not guarantee that all sent events are delivered.</span></span> <span data-ttu-id="c6968-138">Per ulteriori informazioni, vedere [ricezione degli eventi del registro di sistema](receiving-registry-events.md).</span><span class="sxs-lookup"><span data-stu-id="c6968-138">For more information, see [Receiving Registry Events](receiving-registry-events.md).</span></span>

<span data-ttu-id="c6968-139">Nell'esempio di codice VBScript seguente viene illustrato come rilevare una modifica del registro di sistema nel software del **\_ \_ computer locale HKEY** \\  \\ **Microsoft** hive o sottoalbero.</span><span class="sxs-lookup"><span data-stu-id="c6968-139">The following VBScript code example shows how to detect a registry change in the **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft** hive or subtree.</span></span> <span data-ttu-id="c6968-140">Si tratta di uno script di monitoraggio che, a scopo dimostrativo, viene eseguito in un processo denominato Wscript.exe fino a quando non viene terminato in **Gestione attività**, WMI viene arrestato o il sistema operativo viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="c6968-140">This is a monitoring script that, for demonstration purposes, runs in a process named Wscript.exe until it is terminated in **Task Manager**, WMI is stopped, or the operating system is rebooted.</span></span> <span data-ttu-id="c6968-141">Lo script usa una chiamata [*semisincrono*](gloss-s.md) per [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span><span class="sxs-lookup"><span data-stu-id="c6968-141">The script uses a [*semisynchronous*](gloss-s.md) call to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span> <span data-ttu-id="c6968-142">Per ulteriori informazioni sulle chiamate semisincrono, vedere [creazione di una chiamata semisincrono con VBScript](making-a-semisynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="c6968-142">For more information about semisynchronous calls, see [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>


```VB
Set wmiServices = GetObject("winmgmts:root/default") 
Set colTreeChanges = wmiServices.ExecNotificationQuery _
    ("SELECT * FROM RegistryTreeChangeEvent " _
    & "WHERE Hive='HKEY_LOCAL_MACHINE' " _
    & "AND RootPath='SOFTWARE\\Microsoft'")

While (True)
   Set TreeChange = colTreeChanges.NextEvent
   TreeChange.GetObjectText_()
   Wscript.Echo  "Hive = " & TreeChange.Hive & VBNewLine _
      & "RootPath = "& TreeChange.RootPath _
      & TreeChange.GetObjectText_()      
Wend
```



Nell'esempio di codice VBScript seguente viene illustrato come monitorare la modifica nei valori di una chiave eseguendo la registrazione per il tipo di evento del provider del registro di sistema [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). Lo script chiama un metodo asincrono, [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). <span data-ttu-id="c6968-145">Per ulteriori informazioni sulle chiamate asincrone e sulla sicurezza, vedere [creazione di una chiamata asincrona con VBScript](making-an-asynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="c6968-145">For more information about asynchronous calls and security, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="c6968-146">Lo script seguente viene eseguito a tempo indefinito fino a quando il computer non viene riavviato, WMI viene arrestato o lo script viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="c6968-146">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="c6968-147">Per arrestare manualmente lo script, utilizzare Gestione attività per arrestare il processo.</span><span class="sxs-lookup"><span data-stu-id="c6968-147">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="c6968-148">Per arrestarla a livello di codice, usare il metodo [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) nella \_ classe del processo Win32.</span><span class="sxs-lookup"><span data-stu-id="c6968-148">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span>


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:root/default") 
Set wmiSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink", "SINK_") 
Set ObjRegistry = GetObject("winmgmts:_
    {impersonationLevel = impersonate}!\\" _
    & strComputer & "\root\default:StdRegProv")

' Create a new key
strPath = "SOFTWARE\MyKey\MySubKey\"
Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

' Start listening for change in key
objWMIServices.ExecNotificationQueryAsync wmiSink, _ 
    "SELECT * FROM RegistryKeyChangeEvent " _ 
    & "WHERE Hive='HKEY_LOCAL_MACHINE' AND " _ 
    & "KeyPath='SOFTWARE\\MyKey\\MySubKey\\'" 
WScript.Echo "Listening for Registry Change Events..." 

While(True) 
    WScript.Sleep 1000
' You can use Regedit to make a change in the key 
' HKEY_LOCAL_MACHINE\SOFTWARE\MyKey\MySubKey\ 
'    to see an event generated.
Wend 

Sub SINK_OnObjectReady(EventObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Change Event" & vbCrLf & _
      EventObject.GetObjectText_() 
End Sub
```



 

