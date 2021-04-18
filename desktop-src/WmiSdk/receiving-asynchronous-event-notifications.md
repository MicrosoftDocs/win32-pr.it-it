---
description: La notifica asincrona degli eventi è una tecnica che consente a un'applicazione di monitorare costantemente gli eventi senza monopolizzare le risorse di sistema.
ms.assetid: 69ec8ead-9073-4689-bc66-5134728ab147
ms.tgt_platform: multiple
title: Ricezione di notifiche di eventi asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d883908475c796a6bcf31895f2928345541c940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314587"
---
# <a name="receiving-asynchronous-event-notifications"></a><span data-ttu-id="1c977-103">Ricezione di notifiche di eventi asincroni</span><span class="sxs-lookup"><span data-stu-id="1c977-103">Receiving Asynchronous Event Notifications</span></span>

<span data-ttu-id="1c977-104">La notifica asincrona degli eventi è una tecnica che consente a un'applicazione di monitorare costantemente gli eventi senza monopolizzare le risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="1c977-104">Asynchronous event notification is a technique that allows an application to constantly monitor events without monopolizing system resources.</span></span> <span data-ttu-id="1c977-105">Le notifiche degli eventi asincroni presentano le stesse limitazioni di sicurezza di altre chiamate asincrone.</span><span class="sxs-lookup"><span data-stu-id="1c977-105">Asynchronous event notifications have the same security limitations that other asynchronous calls have.</span></span> <span data-ttu-id="1c977-106">In alternativa, è possibile eseguire chiamate semisincrono.</span><span class="sxs-lookup"><span data-stu-id="1c977-106">You can make semisynchronous calls instead.</span></span> <span data-ttu-id="1c977-107">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="1c977-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="1c977-108">La coda di eventi asincroni indirizzati a un client può aumentare eccezionalmente le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="1c977-108">The queue of asynchronous events routed to a client has the potential to grow exceptionally large.</span></span> <span data-ttu-id="1c977-109">Pertanto, WMI implementa un criterio a livello di sistema per evitare di esaurire la memoria.</span><span class="sxs-lookup"><span data-stu-id="1c977-109">Therefore, WMI implements a system-wide policy to avoid running out of memory.</span></span> <span data-ttu-id="1c977-110">WMI rallenta gli eventi o inizia a eliminare gli eventi dalla coda quando la coda cresce oltre una determinata dimensione.</span><span class="sxs-lookup"><span data-stu-id="1c977-110">WMI either slows down events, or starts dropping events from the queue when the queue grows past a certain size.</span></span>

<span data-ttu-id="1c977-111">WMI utilizza le proprietà [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) e [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) della classe [**\_ WMISetting Win32**](/windows/desktop/CIMWin32Prov/win32-wmisetting) per impostare limiti di prevenzione della memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="1c977-111">WMI uses the [**LowThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) and [**HighThresholdOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) properties of the [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) class to set limits on out-of-memory avoidance.</span></span> <span data-ttu-id="1c977-112">Il valore minimo indica quando WMI deve iniziare a rallentare la notifica degli eventi e il valore massimo indica quando iniziare a eliminare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="1c977-112">The minimum value indicates when WMI should start slowing event notification, and the maximum value indicates when to start dropping events.</span></span> <span data-ttu-id="1c977-113">I valori predefiniti per le soglie bassa e massima sono 1 milione (10 MB) e 2 milioni (20 MB).</span><span class="sxs-lookup"><span data-stu-id="1c977-113">The default values for the low and high thresholds are 1000000 (10 MB) and 2000000 (20 MB).</span></span> <span data-ttu-id="1c977-114">Inoltre, è possibile impostare la proprietà [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) per descrivere l'intervallo di tempo in cui WMI deve attendere prima di eliminare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="1c977-114">In addition, you can set the [**MaxWaitOnEvents**](/windows/desktop/CIMWin32Prov/win32-wmisetting) property to describe the amount of time WMI should wait before dropping events.</span></span> <span data-ttu-id="1c977-115">Il valore predefinito per **MaxWaitOnEvents** è 2000 o 2 secondi.</span><span class="sxs-lookup"><span data-stu-id="1c977-115">The default value for **MaxWaitOnEvents** is 2000, or 2 seconds.</span></span>

## <a name="receiving-asynchronous-event-notifications-in-vbscript"></a><span data-ttu-id="1c977-116">Ricezione di notifiche di eventi asincroni in VBScript</span><span class="sxs-lookup"><span data-stu-id="1c977-116">Receiving Asynchronous Event Notifications in VBScript</span></span>

<span data-ttu-id="1c977-117">Le chiamate di scripting per ricevere notifiche degli eventi sono essenzialmente le stesse di tutte le chiamate asincrone con gli stessi problemi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1c977-117">The scripting calls to receive event notifications are essentially the same as all asynchronous calls with the same security issues.</span></span> <span data-ttu-id="1c977-118">Per ulteriori informazioni, vedere [creazione di una chiamata asincrona con VBScript](making-an-asynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="1c977-118">For more information, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="1c977-119">**Per ricevere notifiche di eventi asincroni in VBScript**</span><span class="sxs-lookup"><span data-stu-id="1c977-119">**To receive asynchronous event notifications in VBScript**</span></span>

1.  <span data-ttu-id="1c977-120">Creare un oggetto sink chiamando [WScript. CreateObject](/previous-versions//xzysf6hc(v=vs.85)) e specificando il ProgID di "WbemScripting" e il tipo di oggetto di [**SWbemSink**](swbemsink.md).</span><span class="sxs-lookup"><span data-stu-id="1c977-120">Create a sink object by calling [WScript.CreateObject](/previous-versions//xzysf6hc(v=vs.85)) and specifying the progid of "WbemScripting" and the object type of [**SWbemSink**](swbemsink.md).</span></span> <span data-ttu-id="1c977-121">L'oggetto sink riceve le notifiche.</span><span class="sxs-lookup"><span data-stu-id="1c977-121">The sink object receives the notifications.</span></span>
2.  <span data-ttu-id="1c977-122">Scrivere una subroutine per ogni evento che si desidera gestire.</span><span class="sxs-lookup"><span data-stu-id="1c977-122">Write a subroutine for each event you want to handle.</span></span> <span data-ttu-id="1c977-123">La tabella seguente elenca gli eventi [**SWbemSink**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="1c977-123">The following table lists the [**SWbemSink**](swbemsink.md) events.</span></span>

    

    | <span data-ttu-id="1c977-124">Evento</span><span class="sxs-lookup"><span data-stu-id="1c977-124">Event</span></span>                                            | <span data-ttu-id="1c977-125">Significato</span><span class="sxs-lookup"><span data-stu-id="1c977-125">Meaning</span></span>                                                                                                                         |
    |--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
    | [<span data-ttu-id="1c977-126">**OnObjectReady**</span><span class="sxs-lookup"><span data-stu-id="1c977-126">**OnObjectReady**</span></span>](swbemsink-onobjectready.md) | <span data-ttu-id="1c977-127">Segnala i ritorni di un oggetto al sink.</span><span class="sxs-lookup"><span data-stu-id="1c977-127">Reports the returns of an object to the sink.</span></span> <span data-ttu-id="1c977-128">L'utilizzo di questa chiamata restituisce un oggetto ogni volta fino al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1c977-128">Using this call returns one object each time until the operation is complete.</span></span>     |
    | [<span data-ttu-id="1c977-129">**OnCompleted**</span><span class="sxs-lookup"><span data-stu-id="1c977-129">**OnCompleted**</span></span>](swbemsink-oncompleted.md)     | <span data-ttu-id="1c977-130">Segnala il completamento di una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="1c977-130">Reports when an asynchronous call is complete.</span></span> <span data-ttu-id="1c977-131">Questo evento non si verifica mai se l'operazione è indefinita.</span><span class="sxs-lookup"><span data-stu-id="1c977-131">This event never occurs if the operation is indefinite.</span></span>                          |
    | [<span data-ttu-id="1c977-132">**OnObjectPut**</span><span class="sxs-lookup"><span data-stu-id="1c977-132">**OnObjectPut**</span></span>](swbemsink-onobjectput.md)     | <span data-ttu-id="1c977-133">Segnala il completamento di un'operazione Put asincrona.</span><span class="sxs-lookup"><span data-stu-id="1c977-133">Reports the completion of an asynchronous put operation.</span></span> <span data-ttu-id="1c977-134">Questo evento restituisce il percorso dell'oggetto dell'istanza o della classe salvata.</span><span class="sxs-lookup"><span data-stu-id="1c977-134">This event returns the object path of the instance or the saved class.</span></span> |
    | [<span data-ttu-id="1c977-135">**OnProgress**</span><span class="sxs-lookup"><span data-stu-id="1c977-135">**OnProgress**</span></span>](swbemsink-onprogress.md)       | <span data-ttu-id="1c977-136">Segnala lo stato di una chiamata asincrona in corso.</span><span class="sxs-lookup"><span data-stu-id="1c977-136">Reports the status of an asynchronous call that is in progress.</span></span> <span data-ttu-id="1c977-137">Non tutti i provider supportano i report di stato provvisori.</span><span class="sxs-lookup"><span data-stu-id="1c977-137">Not all providers support interim progress reports.</span></span>             |
    | [<span data-ttu-id="1c977-138">**Annulla**</span><span class="sxs-lookup"><span data-stu-id="1c977-138">**Cancel**</span></span>](swbemsink-cancel.md)               | <span data-ttu-id="1c977-139">Annulla tutte le operazioni asincrone in attesa associate a questo sink dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1c977-139">Cancels all of the outstanding asynchronous operations associated with this object sink.</span></span>                                        |

    

     

<span data-ttu-id="1c977-140">Nell'esempio di codice VBScript seguente viene notificata l'eliminazione di processi con un intervallo di polling di 10 secondi.</span><span class="sxs-lookup"><span data-stu-id="1c977-140">The following VBScript code example notifies the deletion of processes with a 10 second polling interval.</span></span> <span data-ttu-id="1c977-141">In questo script, il SINK della subroutine \_ OnObjectReady gestisce l'occorrenza dell'evento.</span><span class="sxs-lookup"><span data-stu-id="1c977-141">In this script, the subroutine SINK\_OnObjectReady handles the event occurrence.</span></span> <span data-ttu-id="1c977-142">Nell'esempio, l'oggetto sink è denominato "sink", tuttavia è possibile assegnare un nome a questo oggetto come scelto.</span><span class="sxs-lookup"><span data-stu-id="1c977-142">In the example, the sink object is named "Sink", however you can name this object as you choose.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set MySink = WScript.CreateObject( _
    "WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, _
    "SELECT * FROM __InstanceDeletionEvent" _
    & " WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'"


WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    Wscript.Echo "__InstanceDeletionEvent event has occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub
```



## <a name="receiving-asynchronous-event-notifications-in-c"></a><span data-ttu-id="1c977-143">Ricezione di notifiche di eventi asincroni in C++</span><span class="sxs-lookup"><span data-stu-id="1c977-143">Receiving Asynchronous Event Notifications in C++</span></span>

<span data-ttu-id="1c977-144">Per eseguire una notifica asincrona, è necessario creare un thread separato esclusivamente per il monitoraggio e la ricezione di eventi da Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1c977-144">To perform asynchronous notification, you create a separate thread solely to monitor and receive events from Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="1c977-145">Quando il thread riceve un messaggio, il thread invia una notifica all'applicazione principale.</span><span class="sxs-lookup"><span data-stu-id="1c977-145">When that thread receives a message, the thread notifies your main application.</span></span>

<span data-ttu-id="1c977-146">Dedicando un thread separato, si consente al processo principale di eseguire altre attività in attesa dell'arrivo di un evento.</span><span class="sxs-lookup"><span data-stu-id="1c977-146">By dedicating a separate thread, you permit your main process to perform other activities while waiting for an event to arrive.</span></span> <span data-ttu-id="1c977-147">Il recapito asincrono delle notifiche migliora le prestazioni, ma può garantire una minore sicurezza del necessario.</span><span class="sxs-lookup"><span data-stu-id="1c977-147">Asynchronous delivery of notifications improves performance but may provide less security than you want.</span></span> <span data-ttu-id="1c977-148">In C++ è possibile usare l'interfaccia [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) o eseguire controlli di accesso sui descrittori di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="1c977-148">In C++, you have the option of using the [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) interface or performing access checks on security descriptors.</span></span> <span data-ttu-id="1c977-149">Per ulteriori informazioni, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="1c977-149">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="1c977-150">**Per configurare le notifiche degli eventi asincroni**</span><span class="sxs-lookup"><span data-stu-id="1c977-150">**To set up asynchronous event notifications**</span></span>

1.  <span data-ttu-id="1c977-151">Prima di inizializzare le notifiche asincrone, assicurarsi che i parametri di prevenzione della memoria esaurita siano impostati correttamente in [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting).</span><span class="sxs-lookup"><span data-stu-id="1c977-151">Before initializing any asynchronous notifications, ensure your out-of-memory avoidance parameters are set correctly in [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting).</span></span>

2.  <span data-ttu-id="1c977-152">Determinare il tipo di eventi che si desidera ricevere.</span><span class="sxs-lookup"><span data-stu-id="1c977-152">Determine what kind of events you want to receive.</span></span>

    <span data-ttu-id="1c977-153">WMI supporta eventi intrinseci ed estrinseci.</span><span class="sxs-lookup"><span data-stu-id="1c977-153">WMI supports intrinsic and extrinsic events.</span></span> <span data-ttu-id="1c977-154">Un evento intrinseco è un evento predefinito da WMI, mentre un evento estrinseco è un evento definito da un provider di terze parti.</span><span class="sxs-lookup"><span data-stu-id="1c977-154">An intrinsic event is an event predefined by WMI, whereas an extrinsic event is an event defined by a third party provider.</span></span> <span data-ttu-id="1c977-155">Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md).</span><span class="sxs-lookup"><span data-stu-id="1c977-155">For more information, see [Determining the Type of Event to Receive](determining-the-type-of-event-to-receive.md).</span></span>

<span data-ttu-id="1c977-156">Nella procedura seguente viene descritto come ricevere notifiche di eventi asincroni in C++.</span><span class="sxs-lookup"><span data-stu-id="1c977-156">The following procedure describes how to receive asynchronous event notifications in C++.</span></span>

<span data-ttu-id="1c977-157">**Per ricevere notifiche di eventi asincroni in C++**</span><span class="sxs-lookup"><span data-stu-id="1c977-157">**To receive asynchronous event notifications in C++**</span></span>

1.  <span data-ttu-id="1c977-158">Configurare l'applicazione con le chiamate alle funzioni [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="1c977-158">Set up your application with calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions.</span></span>

    <span data-ttu-id="1c977-159">La chiamata a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) Inizializza com, mentre [**COINITIALIZESECURITY**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) concede a WMI l'autorizzazione per chiamare il processo del consumer.</span><span class="sxs-lookup"><span data-stu-id="1c977-159">Calling [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) initializes COM, while [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) grants WMI the permission to call into the process of the consumer.</span></span> <span data-ttu-id="1c977-160">La funzione **CoInitializeEx** offre inoltre la possibilità di programmare un'applicazione multithread, necessaria per la notifica asincrona.</span><span class="sxs-lookup"><span data-stu-id="1c977-160">The **CoInitializeEx** function also grants you the ability to program a multithreaded application, which is necessary for asynchronous notification.</span></span> <span data-ttu-id="1c977-161">Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="1c977-161">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

    <span data-ttu-id="1c977-162">Il codice in questo argomento richiede i riferimenti seguenti e le \# istruzioni di inclusione per la compilazione corretta.</span><span class="sxs-lookup"><span data-stu-id="1c977-162">The code in this topic requires the following references and \#include statements to compile correctly.</span></span>

    ```C++
    #define _WIN32_DCOM
    #include <iostream>
    using namespace std;
    #include <wbemidl.h>
    ```

    

    <span data-ttu-id="1c977-163">Nell'esempio di codice seguente viene descritto come configurare il consumer di eventi temporanei con chiamate a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="1c977-163">The following code example describes how to set up the temporary event consumer with calls to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    ```C++
    void main(int argc, char **argv)
    {
        HRESULT hr = 0;
        hr = CoInitializeEx (0, COINIT_MULTITHREADED);
        hr = CoInitializeSecurity (NULL, 
           -1, 
           NULL, 
           NULL,   
           RPC_C_AUTHN_LEVEL_NONE, 
           RPC_C_IMP_LEVEL_IMPERSONATE, 
           NULL,
           EOAC_NONE,
           NULL); 

        if (FAILED(hr))
        {
           CoUninitialize();
           cout << "Failed to initialize security. Error code = 0x"
               << hex << hr << endl;
           return;
        }

    // ...
    }
    ```

    

2.  <span data-ttu-id="1c977-164">Creare un oggetto sink tramite l'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="1c977-164">Create a sink object through the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="1c977-165">WMI utilizza [**IWbemObjectSink**](iwbemobjectsink.md) per inviare notifiche degli eventi e per segnalare lo stato di un'operazione asincrona o di una notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="1c977-165">WMI uses [**IWbemObjectSink**](iwbemobjectsink.md) to send event notifications and to report status on an asynchronous operation or event notification.</span></span>

3.  <span data-ttu-id="1c977-166">Registrare il consumer di eventi con una chiamata al metodo [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) .</span><span class="sxs-lookup"><span data-stu-id="1c977-166">Register your event consumer with a call to the [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) method.</span></span>

    <span data-ttu-id="1c977-167">Verificare che il parametro *pResponseHandler* punti all'oggetto sink creato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="1c977-167">Make sure that the *pResponseHandler* parameter points to the sink object created in the preceding step.</span></span>

    <span data-ttu-id="1c977-168">Lo scopo della registrazione è quello di ricevere solo le notifiche richieste.</span><span class="sxs-lookup"><span data-stu-id="1c977-168">The purpose of registration is to receive only the required notifications.</span></span> <span data-ttu-id="1c977-169">La ricezione di notifiche superflue spreca l'elaborazione e il tempo di recapito; e non usa la capacità di filtraggio di WMI al massimo del potenziale.</span><span class="sxs-lookup"><span data-stu-id="1c977-169">Receiving superfluous notifications wastes processing and delivery time; and does not use the filtering ability of WMI to the fullest potential.</span></span>

    <span data-ttu-id="1c977-170">Un consumer temporaneo può tuttavia ricevere più di un tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="1c977-170">However, a temporary consumer can receive more than one type of event.</span></span> <span data-ttu-id="1c977-171">In questo caso, un consumer temporaneo deve effettuare chiamate separate a [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) per ogni tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="1c977-171">In this case, a temporary consumer must make separate calls to [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) for each event type.</span></span> <span data-ttu-id="1c977-172">Un consumer può, ad esempio, richiedere una notifica quando vengono creati nuovi processi (un evento di creazione dell'istanza o [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md)) e per le modifiche a determinate chiavi del registro di sistema (un evento del registro di sistema, ad esempio [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)).</span><span class="sxs-lookup"><span data-stu-id="1c977-172">For example, a consumer might require notification when new processes are created (an instance creation event or [**\_\_InstanceCreationEvent**](--instancecreationevent.md)) and for changes to certain registry keys (a registry event such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)).</span></span> <span data-ttu-id="1c977-173">Pertanto, il consumer effettua una chiamata a [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) per registrare gli eventi di creazione dell'istanza e un'altra chiamata a **ExecNotificationQueryAsync** per la registrazione degli eventi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1c977-173">Therefore, the consumer makes one call to [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) to register for instance creation events and another call to **ExecNotificationQueryAsync** to register for registry events.</span></span>

    <span data-ttu-id="1c977-174">Se si sceglie di creare un consumer di eventi che si registra per più eventi, è consigliabile evitare di registrare più classi con lo stesso sink.</span><span class="sxs-lookup"><span data-stu-id="1c977-174">If you choose to create an event consumer that registers for multiple events, you should avoid registering multiple classes with the same sink.</span></span> <span data-ttu-id="1c977-175">Usare invece un sink separato per ogni classe di evento registrato.</span><span class="sxs-lookup"><span data-stu-id="1c977-175">Instead, use a separate sink for each class of registered event.</span></span> <span data-ttu-id="1c977-176">Un sink dedicato semplifica l'elaborazione e favorisce la manutenzione, consentendo di annullare una registrazione senza influire sugli altri.</span><span class="sxs-lookup"><span data-stu-id="1c977-176">Having a dedicated sink simplifies processing and aids in maintenance, allowing you to cancel one registration without affecting the others.</span></span>

4.  <span data-ttu-id="1c977-177">Eseguire tutte le attività necessarie nel consumer di eventi.</span><span class="sxs-lookup"><span data-stu-id="1c977-177">Perform any necessary activities in your event consumer.</span></span>

    <span data-ttu-id="1c977-178">Questo passaggio deve contenere la maggior parte del codice e includere attività quali la visualizzazione di eventi in un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="1c977-178">This step should contain most of your code and include such activities as displaying events to a user interface.</span></span>

5.  <span data-ttu-id="1c977-179">Al termine, annullare la registrazione del consumer di eventi temporanei con una chiamata all'evento [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .</span><span class="sxs-lookup"><span data-stu-id="1c977-179">When finished, unregister the temporary event consumer with a call to the [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) event.</span></span>

    <span data-ttu-id="1c977-180">Indipendentemente dal fatto che la chiamata a [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) abbia esito positivo o negativo, non eliminare l'oggetto sink fino a quando il conteggio dei riferimenti all'oggetto non raggiunge lo zero.</span><span class="sxs-lookup"><span data-stu-id="1c977-180">Regardless of whether the call to [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) succeeds or fails, do not delete the sink object until the object reference count reaches zero.</span></span> <span data-ttu-id="1c977-181">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="1c977-181">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 
