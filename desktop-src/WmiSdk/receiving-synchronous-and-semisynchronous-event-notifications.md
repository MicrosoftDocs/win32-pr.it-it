---
description: Usare SWbemServices.ExecQuery per richiedere tutti gli eventi esistenti.
ms.assetid: bc99719a-7e33-4e2d-8355-f8fc97c66f71
ms.tgt_platform: multiple
title: Ricezione di notifiche di eventi sincroni e semisincrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15327c66f7ba3e59824c94d54a206ec348c85952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314584"
---
# <a name="receiving-synchronous-and-semisynchronous-event-notifications"></a><span data-ttu-id="908d9-103">Ricezione di notifiche di eventi sincroni e semisincrono</span><span class="sxs-lookup"><span data-stu-id="908d9-103">Receiving Synchronous and Semisynchronous Event Notifications</span></span>

<span data-ttu-id="908d9-104">Usare [**SWbemServices.ExecQuery**](swbemservices-execquery.md) per richiedere tutti gli eventi esistenti.</span><span class="sxs-lookup"><span data-stu-id="908d9-104">Use [**SWbemServices.ExecQuery**](swbemservices-execquery.md) to request all existing events.</span></span>

<span data-ttu-id="908d9-105">Nell'esempio di codice seguente viene illustrato come eseguire una query per gli eventi in un log.</span><span class="sxs-lookup"><span data-stu-id="908d9-105">The following code example shows how to query for the events in a log.</span></span>

`Select * from Win32_NTLogEvent`

<span data-ttu-id="908d9-106">Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md), [ricezione di notifiche degli eventi](receiving-event-notifications.md)e [WQL (SQL per WMI)](wql-sql-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="908d9-106">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md), [Receiving Event Notifications](receiving-event-notifications.md), and [WQL (SQL for WMI)](wql-sql-for-wmi.md).</span></span>

<span data-ttu-id="908d9-107">La chiamata predefinita a [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) usa la comunicazione semisincrono.</span><span class="sxs-lookup"><span data-stu-id="908d9-107">The default call to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) uses semisynchronous communication.</span></span> <span data-ttu-id="908d9-108">Il parametro *iFlags* include i flag **wbemFlagForwardOnly** e **wbemFlagReturnImmediately** impostati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="908d9-108">The *iflags* parameter has the **wbemFlagForwardOnly** and **wbemFlagReturnImmediately** flags set by default.</span></span> <span data-ttu-id="908d9-109">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="908d9-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="908d9-110">Nella procedura seguente viene descritto come ricevere una notifica degli eventi semisincrono tramite VBScript.</span><span class="sxs-lookup"><span data-stu-id="908d9-110">The following procedure describes how to receive semisynchronous event notification using VBScript.</span></span>

<span data-ttu-id="908d9-111">**Per ricevere la notifica degli eventi semisincrono in VBScript**</span><span class="sxs-lookup"><span data-stu-id="908d9-111">**To receive semisynchronous event notification in VBScript**</span></span>

1.  <span data-ttu-id="908d9-112">Creare una query per il tipo di evento che si desidera ricevere.</span><span class="sxs-lookup"><span data-stu-id="908d9-112">Create a query for the type of event that you want to receive.</span></span> <span data-ttu-id="908d9-113">Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="908d9-113">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

2.  <span data-ttu-id="908d9-114">Se si richiede un tipo di istanza di un evento come [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md), indicare nella query un tipo di istanza di destinazione, ad esempio [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="908d9-114">If you request an instance type of event such as [**\_\_InstanceCreationEvent**](--instancecreationevent.md), indicate in the query a type of target instance, for example, [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span>

3.  <span data-ttu-id="908d9-115">Se necessario, specificare un'istanza, ad esempio, il nome di uno spazio dei nomi quando si richiedono istanze [**\_ \_ NamespaceModificationEvent**](--namespacemodificationevent.md) future per uno spazio dei nomi specifico.</span><span class="sxs-lookup"><span data-stu-id="908d9-115">If necessary, specify an instance, for example, the name of a namespace when requesting future [**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md) instances for a specific namespace.</span></span>

4.  <span data-ttu-id="908d9-116">Specificare un intervallo di polling per Strumentazione gestione Windows (WMI) in una query, ad esempio "entro 10", per eseguire il polling ogni 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="908d9-116">Specify a polling interval for Windows Management Instrumentation (WMI) in a query, such as "WITHIN 10"—to poll every 10 seconds.</span></span> <span data-ttu-id="908d9-117">Per ulteriori informazioni, vedere [clausola all'interno](within-clause.md)di.</span><span class="sxs-lookup"><span data-stu-id="908d9-117">For more information, see [WITHIN Clause](within-clause.md).</span></span>

5.  <span data-ttu-id="908d9-118">Chiamare [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) utilizzando la query.</span><span class="sxs-lookup"><span data-stu-id="908d9-118">Call [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) using the query.</span></span>

6.  <span data-ttu-id="908d9-119">Esegue il ciclo della raccolta ricevuta.</span><span class="sxs-lookup"><span data-stu-id="908d9-119">Loop through the collection you receive.</span></span>

<span data-ttu-id="908d9-120">Nell'esempio seguente viene illustrato come monitorare l'inserimento e la rimozione di dischi da un'unità disco floppy in un computer locale.</span><span class="sxs-lookup"><span data-stu-id="908d9-120">The following example shows how to monitor insertion and removal of disks from a floppy disk drive on a local machine.</span></span> <span data-ttu-id="908d9-121">Lo script richiede \_ istanze di [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) per l'istanza [**di \_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) dell'unità floppy ed esegue il polling ogni 10 secondi per le nuove istanze.</span><span class="sxs-lookup"><span data-stu-id="908d9-121">The script requests \_[**\_\_InstanceModificationEvent**](--instancemodificationevent.md) instances for the floppy drive [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instance and polls every 10 seconds for new instances.</span></span> <span data-ttu-id="908d9-122">Questo script è un esempio di consumer di eventi temporanei e continua l'esecuzione fino a quando non viene arrestato in Gestione attività o il sistema non viene riavviato.</span><span class="sxs-lookup"><span data-stu-id="908d9-122">This script is an example of a temporary event consumer, and continues running until it is stopped in Task Manager or the system is rebooted.</span></span> <span data-ttu-id="908d9-123">Per ulteriori informazioni, vedere [ricezione di eventi per la durata dell'applicazione](receiving-events-for-the-duration-of-your-application.md).</span><span class="sxs-lookup"><span data-stu-id="908d9-123">For more information, see [Receiving Events for the Duration of your Application](receiving-events-for-the-duration-of-your-application.md).</span></span>


```VB
Const FLOPPY_DISK = 2
Set colMonitoredDisks = GetObject("Winmgmts:").ExecNotificationQuery _
    ("Select * from __InstanceModificationEvent within 10 WHERE " _
        & "TargetInstance ISA 'Win32_LogicalDisk'")
i = 0
Do While i = 0
    Set strDiskChange = colMonitoredDisks.NextEvent
    If strDiskChange.TargetInstance.DriveType = FLOPPY_DISK Then
        If strDiskChange.TargetInstance.Size > 0 Then
            Wscript.Echo "A disk has been inserted" & _
                " into the floppy drive."
    Else
            Wscript.Echo "A disk has been removed" & _
                " from the floppy drive."
        End If
    End If
Loop
```



<span data-ttu-id="908d9-124">Nella procedura seguente viene descritto come ricevere una notifica degli eventi semisincrono utilizzando C++.</span><span class="sxs-lookup"><span data-stu-id="908d9-124">The following procedure describes how to receive semisynchronous event notification using C++.</span></span>

<span data-ttu-id="908d9-125">**Per ricevere la notifica degli eventi semisincrono in C++**</span><span class="sxs-lookup"><span data-stu-id="908d9-125">**To receive semisynchronous event notification in C++**</span></span>

1.  <span data-ttu-id="908d9-126">Configurare l'applicazione con le chiamate alle funzioni [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="908d9-126">Set up the application with calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions.</span></span>

    <span data-ttu-id="908d9-127">Poiché WMI è basato su COM, chiamare [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) è un passaggio obbligatorio per un'applicazione WMI.</span><span class="sxs-lookup"><span data-stu-id="908d9-127">Because WMI is COM based, calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) is a required step for a WMI application.</span></span> <span data-ttu-id="908d9-128">Per ulteriori informazioni, vedere [creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="908d9-128">For more information, see [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span>

2.  <span data-ttu-id="908d9-129">Determinare il tipo di eventi che si desidera ricevere.</span><span class="sxs-lookup"><span data-stu-id="908d9-129">Determine the kind of events that you want to receive.</span></span>

    <span data-ttu-id="908d9-130">WMI supporta eventi intrinseci ed estrinseci.</span><span class="sxs-lookup"><span data-stu-id="908d9-130">WMI supports intrinsic and extrinsic events.</span></span> <span data-ttu-id="908d9-131">Un evento intrinseco è un evento predefinito da WMI.</span><span class="sxs-lookup"><span data-stu-id="908d9-131">An intrinsic event is an event predefined by WMI.</span></span> <span data-ttu-id="908d9-132">Un evento estrinseco è un evento definito da un provider di terze parti.</span><span class="sxs-lookup"><span data-stu-id="908d9-132">An extrinsic event is an event defined by a third party provider.</span></span> <span data-ttu-id="908d9-133">Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="908d9-133">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

3.  <span data-ttu-id="908d9-134">Eseguire la registrazione per ricevere una classe specifica di eventi con una chiamata al metodo [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) .</span><span class="sxs-lookup"><span data-stu-id="908d9-134">Register to receive a specific class of events with a call to the [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) method.</span></span>

    <span data-ttu-id="908d9-135">Eseguire ogni query in modo molto specifico.</span><span class="sxs-lookup"><span data-stu-id="908d9-135">Make each query very specific.</span></span> <span data-ttu-id="908d9-136">L'obiettivo della registrazione è registrarsi per ricevere solo le notifiche richieste.</span><span class="sxs-lookup"><span data-stu-id="908d9-136">The goal of registration is to register to receive only the required notifications.</span></span> <span data-ttu-id="908d9-137">Notifiche che non sono necessarie per l'elaborazione e il tempo di recapito.</span><span class="sxs-lookup"><span data-stu-id="908d9-137">Notifications that are not required waste processing and delivery time.</span></span>

    <span data-ttu-id="908d9-138">È possibile progettare un consumer di eventi per la ricezione di più eventi.</span><span class="sxs-lookup"><span data-stu-id="908d9-138">You can design an event consumer to receive multiple events.</span></span> <span data-ttu-id="908d9-139">Ad esempio, un consumer potrebbe richiedere la notifica degli eventi di modifica dell'istanza per una classe specifica di eventi di violazione della sicurezza e del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="908d9-139">For example, a consumer might require notification of instance modification events for a specific class of device and security violation events.</span></span> <span data-ttu-id="908d9-140">In questo caso, le attività eseguite da un consumer durante la ricezione di un evento di modifica dell'istanza sono diverse per i due eventi.</span><span class="sxs-lookup"><span data-stu-id="908d9-140">In this case, the tasks a consumer performs when receiving an instance modification event are different for the two events.</span></span> <span data-ttu-id="908d9-141">Pertanto, il consumer deve effettuare una chiamata a [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) per registrare gli eventi di modifica dell'istanza e un'altra chiamata a **ExecNotificationQuery** per la registrazione degli eventi di violazione della sicurezza.</span><span class="sxs-lookup"><span data-stu-id="908d9-141">Thus, the consumer should make one call to [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) to register for instance modification events, and another call to **ExecNotificationQuery** to register for security violation events.</span></span>

    <span data-ttu-id="908d9-142">Nella chiamata a [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)impostare il parametro *è* sul **\_ flag WBEM \_ return \_ immediatamente** e il **flag WBEM \_ \_ \_ solo in futuro**.</span><span class="sxs-lookup"><span data-stu-id="908d9-142">In the call to [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery), set the *lFlags* parameter to **WBEM\_FLAG\_RETURN\_IMMEDIATELY** and **WBEM\_FLAG\_FORWARD\_ONLY**.</span></span> <span data-ttu-id="908d9-143">Il **\_ flag WBEM \_ restituisce \_ immediatamente** un flag per l'elaborazione di semisincrono e il flag **WBEM di \_ \_ \_ sola trasmissione** richiede un enumeratore di solo inoltri.</span><span class="sxs-lookup"><span data-stu-id="908d9-143">The **WBEM\_FLAG\_RETURN\_IMMEDIATELY** flag requests semisynchronous processing, and the **WBEM\_FLAG\_FORWARD\_ONLY** flag requests a forward-only enumerator.</span></span> <span data-ttu-id="908d9-144">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="908d9-144">For more information, see [Calling a Method](calling-a-method.md).</span></span> <span data-ttu-id="908d9-145">La funzione **ExecNotificationQuery** restituisce un puntatore a un'interfaccia [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="908d9-145">The **ExecNotificationQuery** function returns a pointer to an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface.</span></span>

4.  <span data-ttu-id="908d9-146">Eseguire il polling per le notifiche degli eventi registrati eseguendo chiamate ripetute al metodo [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) .</span><span class="sxs-lookup"><span data-stu-id="908d9-146">Poll for registered event notifications by making repeated calls to the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) method.</span></span>
5.  <span data-ttu-id="908d9-147">Al termine, rilasciare l'enumeratore che fa riferimento all'oggetto [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="908d9-147">When finished, release the enumerator that points to the [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) object.</span></span>

    <span data-ttu-id="908d9-148">È possibile rilasciare il puntatore [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) associato alla registrazione.</span><span class="sxs-lookup"><span data-stu-id="908d9-148">You can release the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer associated with the registration.</span></span> <span data-ttu-id="908d9-149">Il rilascio del puntatore **IWbemServices** fa sì che WMI interrompa la distribuzione degli eventi a tutti i consumer temporanei associati.</span><span class="sxs-lookup"><span data-stu-id="908d9-149">Releasing the **IWbemServices** pointer causes WMI to stop delivering events to all associated temporary consumers.</span></span>

 

 
