---
title: Registrazione di un callback COM
description: Anziché eseguire il polling delle modifiche allo stato di un processo, è possibile registrarsi per ricevere una notifica quando lo stato del processo cambia.
ms.assetid: 29350ea4-f7a9-4a42-a531-2cf623fe247b
keywords:
- trasferimento di bit di processo, notifica degli eventi
- registrazione per i bit di notifica degli eventi
- BIT di notifica degli eventi
- BIT di notifica degli eventi, callback
- BIT degli eventi di notifica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdcc52c772656c2168af9c10724ee43fac25aa80
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338222"
---
# <a name="registering-a-com-callback"></a><span data-ttu-id="f0e01-108">Registrazione di un callback COM</span><span class="sxs-lookup"><span data-stu-id="f0e01-108">Registering a COM Callback</span></span>

<span data-ttu-id="f0e01-109">Anziché eseguire il [polling](polling-for-the-status-of-the-job.md) delle modifiche allo stato di un processo, è possibile registrarsi per ricevere una notifica quando lo stato del processo cambia.</span><span class="sxs-lookup"><span data-stu-id="f0e01-109">Instead of [polling](polling-for-the-status-of-the-job.md) for changes in the status of a job, you can register to receive notification when the job's status changes.</span></span> <span data-ttu-id="f0e01-110">Per ricevere la notifica, è necessario implementare l'interfaccia [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) .</span><span class="sxs-lookup"><span data-stu-id="f0e01-110">To receive notification, you must implement the [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface.</span></span> <span data-ttu-id="f0e01-111">L'interfaccia contiene i metodi seguenti chiamati da BITS, a seconda della registrazione:</span><span class="sxs-lookup"><span data-stu-id="f0e01-111">The interface contains the following methods that BITS calls, depending on your registration:</span></span>

-   [<span data-ttu-id="f0e01-112">**JobTransferred**</span><span class="sxs-lookup"><span data-stu-id="f0e01-112">**JobTransferred**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)
-   [<span data-ttu-id="f0e01-113">**JobError**</span><span class="sxs-lookup"><span data-stu-id="f0e01-113">**JobError**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)
-   [<span data-ttu-id="f0e01-114">**JobModification**</span><span class="sxs-lookup"><span data-stu-id="f0e01-114">**JobModification**</span></span>](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)
-   [<span data-ttu-id="f0e01-115">**Filetransfer**</span><span class="sxs-lookup"><span data-stu-id="f0e01-115">**FileTransferred**</span></span>](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred)

<span data-ttu-id="f0e01-116">Per un esempio che implementa l'interfaccia [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) , vedere il codice di esempio nell'argomento dell'interfaccia [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="f0e01-116">For an example that implements the [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface, see the example code in the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface topic.</span></span>

<span data-ttu-id="f0e01-117">L'interfaccia [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) fornisce una notifica quando un file viene trasferito.</span><span class="sxs-lookup"><span data-stu-id="f0e01-117">The [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) interface provides notification when a file is transferred.</span></span> <span data-ttu-id="f0e01-118">In genere, si usa questo metodo per convalidare il file, in modo che il file sia disponibile per il download dei peer. in caso contrario, il file non è disponibile per i peer fino a quando non viene chiamato il metodo [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="f0e01-118">Typically, you use this method to validate the file, so that the file is available for peers to download; otherwise, the file is not available to peers until you call the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="f0e01-119">Per convalidare il file, chiamare il metodo [**IBackgroundCopyFile3:: SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) .</span><span class="sxs-lookup"><span data-stu-id="f0e01-119">To validate the file, call the [**IBackgroundCopyFile3::SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) method.</span></span>

<span data-ttu-id="f0e01-120">Esistono due metodi per la registrazione di un callback COM: la registrazione di un oggetto callback o la registrazione di un ID di classe di callback.</span><span class="sxs-lookup"><span data-stu-id="f0e01-120">There are two methods for registering a COM callback: registering a callback object, or registering a callback class ID.</span></span> <span data-ttu-id="f0e01-121">L'utilizzo di un oggetto di callback è un sovraccarico più semplice e inferiore; l'utilizzo di un CLSID di callback è più affidabile, ma più complesso.</span><span class="sxs-lookup"><span data-stu-id="f0e01-121">Using a callback object is simpler and lower overhead; using a callback CLSID is more reliable, but more complicated.</span></span> <span data-ttu-id="f0e01-122">È possibile registrare, entrambi o nessuno dei due-BITS utilizzerà un oggetto callback se ne esiste uno e può comunque essere chiamato e verrà eseguito il fallback alla creazione di un'istanza di un nuovo oggetto in base a un ID di classe fornito in caso di esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f0e01-122">You can register either, both, or neither – BITS will use a callback object if one exists and can still be called, and will fall back to instantiating a new object based on a provided class ID if that fails.</span></span>

### <a name="registering-a-callback-object"></a><span data-ttu-id="f0e01-123">Registrazione di un oggetto callback</span><span class="sxs-lookup"><span data-stu-id="f0e01-123">Registering a Callback Object</span></span>

<span data-ttu-id="f0e01-124">Per registrare l'implementazione con BITS, chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) .</span><span class="sxs-lookup"><span data-stu-id="f0e01-124">To register your implementation with BITS, call the [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method.</span></span> <span data-ttu-id="f0e01-125">Per specificare i metodi chiamati da BITS, chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags).</span><span class="sxs-lookup"><span data-stu-id="f0e01-125">To specify which methods BITS calls, call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)method.</span></span>

<span data-ttu-id="f0e01-126">L'interfaccia di notifica diventa non valida al termine dell'applicazione; BITS non rende persistente l'interfaccia Notify.</span><span class="sxs-lookup"><span data-stu-id="f0e01-126">The notification interface becomes invalid when your application terminates; BITS does not persist the notify interface.</span></span> <span data-ttu-id="f0e01-127">Di conseguenza, il processo di inizializzazione dell'applicazione dovrebbe registrare i processi esistenti per i quali si desidera ricevere la notifica.</span><span class="sxs-lookup"><span data-stu-id="f0e01-127">As a result, your application's initialization process should register existing jobs for which you want to receive notification.</span></span> <span data-ttu-id="f0e01-128">Se è necessario acquisire informazioni sullo stato e sullo stato di avanzamento dopo l'ultima esecuzione dell'applicazione, eseguire il polling delle informazioni sullo stato e sullo stato durante l'inizializzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f0e01-128">If you need to capture state and progress information that occurred since the last time your application was run, poll for state and progress information during application initialization.</span></span>

<span data-ttu-id="f0e01-129">Prima di uscire, l'applicazione deve cancellare il puntatore all'interfaccia di callback (**SetNotifyInterface (null)**).</span><span class="sxs-lookup"><span data-stu-id="f0e01-129">Before exiting, your application should clear the callback interface pointer (**SetNotifyInterface(NULL)**).</span></span> <span data-ttu-id="f0e01-130">È più efficiente cancellare il puntatore di callback rispetto a consentire a BITS di rilevare che non è più valido.</span><span class="sxs-lookup"><span data-stu-id="f0e01-130">It is more efficient to clear the callback pointer than to let BITS discover that it is no longer valid.</span></span>

<span data-ttu-id="f0e01-131">Si noti che se più di un'applicazione chiama il metodo [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) per impostare l'interfaccia di notifica per il processo, l'ultima applicazione a chiamare il metodo **SetNotifyInterface** è quella che riceverà le notifiche, mentre le altre applicazioni non riceveranno le notifiche.</span><span class="sxs-lookup"><span data-stu-id="f0e01-131">Note that if more than one application calls the [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) method to set the notification interface for the job, the last application to call the **SetNotifyInterface** method is the one that will receive notifications—the other applications will not receive notifications.</span></span>

<span data-ttu-id="f0e01-132">Nell'esempio seguente viene illustrato come eseguire la registrazione per le notifiche.</span><span class="sxs-lookup"><span data-stu-id="f0e01-132">The following example shows how to register for notifications.</span></span> <span data-ttu-id="f0e01-133">Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido.</span><span class="sxs-lookup"><span data-stu-id="f0e01-133">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid.</span></span> <span data-ttu-id="f0e01-134">Per informazioni dettagliate sulla classe di esempio CNotifyInterface usata nell'esempio seguente, vedere l'interfaccia [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="f0e01-134">For details on the CNotifyInterface example class used in the following example, see the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
CNotifyInterface *pNotify = new CNotifyInterface();

if (pNotify)
{
    hr = pJob->SetNotifyInterface(pNotify);
    if (SUCCEEDED(hr))
    {
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
                                  BG_NOTIFY_JOB_ERROR );
    }
    pNotify->Release();
    pNotify = NULL;

    if (FAILED(hr))
    {
        //Handle error - unable to register callbacks.
    }
}
```



### <a name="registering-a-callback-clsid"></a><span data-ttu-id="f0e01-135">Registrazione di un CLSID di callback</span><span class="sxs-lookup"><span data-stu-id="f0e01-135">Registering a Callback CLSID</span></span>

<span data-ttu-id="f0e01-136">Per registrare un CLSID di callback con BITS, chiamare il metodo [**IBackgroundCopyJob5:: SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) con la **\_ notifica della \_ proprietà \_ \_ del processo BITS** PropertyId.</span><span class="sxs-lookup"><span data-stu-id="f0e01-136">To register a callback CLSID with BITS, call the [**IBackgroundCopyJob5::SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) method with the **BITS\_JOB\_PROPERTY\_NOTIFICATION\_CLSID** PropertyId.</span></span> <span data-ttu-id="f0e01-137">Per specificare i metodi chiamati da BITS, chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) .</span><span class="sxs-lookup"><span data-stu-id="f0e01-137">To specify which methods BITS calls, call the [**IBackgroundCopyJob::SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) method.</span></span>

<span data-ttu-id="f0e01-138">Prima di registrare il CLSID con un processo BITS, è necessario assicurarsi che il CLSID di notifica sia registrato in un server COM out-of-process.</span><span class="sxs-lookup"><span data-stu-id="f0e01-138">You must ensure that the notification CLSID is registered to an out-of-process COM server prior to registering the CLSID with a BITS job.</span></span> <span data-ttu-id="f0e01-139">L'implementazione di un [Server com](/windows/desktop/com/com-server-responsibilities) è significativamente più complessa rispetto alla definizione e al passaggio di un oggetto callback, ma offre diversi vantaggi importanti.</span><span class="sxs-lookup"><span data-stu-id="f0e01-139">Implementing a [COM server](/windows/desktop/com/com-server-responsibilities) is significantly more complicated than defining and passing a callback object, but offers several important advantages.</span></span> <span data-ttu-id="f0e01-140">Un server COM consente ai bit di mantenere l'associazione tra un processo BITS e il codice dell'applicazione tra i riavvii del sistema e per i processi di grandi dimensioni o di lunga durata.</span><span class="sxs-lookup"><span data-stu-id="f0e01-140">A COM server allows BITS to maintain the association between a BITS job and your application’s code across system reboots, and for large or long-lived jobs.</span></span> <span data-ttu-id="f0e01-141">Un server COM consente inoltre all'applicazione di arrestarsi completamente mentre BITS continua l'esecuzione di trasferimenti in background, che può migliorare l'utilizzo della batteria, della CPU e della memoria del sistema.</span><span class="sxs-lookup"><span data-stu-id="f0e01-141">A COM server also allows your application to shut down completely while BITS continues executing transfers in the background, which can improve battery, CPU, and memory usage of the system.</span></span>

<span data-ttu-id="f0e01-142">Per fornire una notifica che è stata registrata per la ricezione, BITS tenta innanzitutto di chiamare il metodo corrispondente di qualsiasi oggetto callback esistente collegato.</span><span class="sxs-lookup"><span data-stu-id="f0e01-142">To provide a notification you have registered to receive, BITS first attempts to call the corresponding method of any existing callback object you may have attached.</span></span> <span data-ttu-id="f0e01-143">Se non è presente alcun oggetto o se l'oggetto esistente è stato disconnesso (in genere in seguito all'interruzione dell'applicazione), BITS chiamerà CoCreateInstance utilizzando il CLSID di notifica per creare un'istanza di un nuovo oggetto callback e utilizzerà tale oggetto per eventuali ulteriori callback fino a quando non viene disconnesso o viene sostituito da una nuova chiamata a [**Metodo ibackgroundcopyjob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface).</span><span class="sxs-lookup"><span data-stu-id="f0e01-143">If there is no existing object, or if that existing object has become disconnected (typically as a result of your application terminating), BITS will call CoCreateInstance using the notification CLSID to instantiate a new callback object, and will use that object for any further callbacks until it becomes disconnected or it is replaced by a new call to [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface).</span></span>

<span data-ttu-id="f0e01-144">Diversamente dagli oggetti di callback, il CLSID di callback viene reso permanente insieme ai processi BITS corrispondenti se il servizio BITS o il sistema vengono arrestati e riavviati.</span><span class="sxs-lookup"><span data-stu-id="f0e01-144">Unlike callback objects, callback CLSID are persisted alongside their corresponding BITS job(s) if the BITS service or the system are shut down and restarted.</span></span> <span data-ttu-id="f0e01-145">L'applicazione può cancellare qualsiasi CLSID di notifica precedentemente impostato prima di uscire (o in qualsiasi altro momento) passando un nuovo CLSID di notifica del GUID \_ null, ma è possibile che l'applicazione preferisca lasciare la notifica CLSID registrata se l'applicazione è stata registrata in modo che com lo avvii in risposta alle richieste CoCreateInstance per il CLSID.</span><span class="sxs-lookup"><span data-stu-id="f0e01-145">Your application may clear any previously-set notification CLSID before exiting (or at any other time) by passing a new notification CLSID of GUID\_NULL, but your application may prefer to leave the notification CLSID registered if your application has registered to have COM start it in response to CoCreateInstance requests for your CLSID.</span></span> <span data-ttu-id="f0e01-146">Si noti che se più di un'applicazione imposta la proprietà **\_ \_ \_ \_ CLSID della proprietà del processo BITS** , l'ultimo CLSID da impostare è quello che verrà utilizzato da BITS per creare un'istanza degli oggetti di callback. non verrà creata un'istanza degli altri CLSID.</span><span class="sxs-lookup"><span data-stu-id="f0e01-146">Note that if more than one application sets the calls the **BITS\_JOB\_PROPERTY\_NOTIFICATION\_CLSID** property, the last CLSID to be set is the one that BITS will use to instantiate callback objects – the other CLSIDs will not be instantiated.</span></span> <span data-ttu-id="f0e01-147">Analogamente, se un'applicazione registra un CLSID e un altro registra un oggetto callback, le normali regole per l'oggetto callback che hanno la precedenza si applicano e il CLSID non verrà usato a meno che l'oggetto callback non venga cancellato o non venga disconnesso.</span><span class="sxs-lookup"><span data-stu-id="f0e01-147">Similarly, if one application registers a CLSID and another registers a callback object, the usual rules for the callback object taking precedence apply, and the CLSID will not be used unless the callback object is cleared or becomes disconnected.</span></span>

<span data-ttu-id="f0e01-148">Nell'esempio seguente viene illustrato come eseguire la registrazione per le notifiche CLSID.</span><span class="sxs-lookup"><span data-stu-id="f0e01-148">The following example shows how to register for CLSID notifications.</span></span> <span data-ttu-id="f0e01-149">Nell'esempio si presuppone che il puntatore all'interfaccia [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) sia valido e che l'applicazione sia già stata registrata come un server COM out-of-process che implementa la classe CNotifyInterface.</span><span class="sxs-lookup"><span data-stu-id="f0e01-149">The example assumes the [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) interface pointer is valid, and that your application has already registered as an out-of-process COM Server which implements the CNotifyInterface class.</span></span> <span data-ttu-id="f0e01-150">Per informazioni dettagliate sulla classe di esempio CNotifyInterface usata nell'esempio seguente, vedere l'interfaccia [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .</span><span class="sxs-lookup"><span data-stu-id="f0e01-150">For details on the CNotifyInterface example class used in the following example, see the [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) interface.</span></span>


```C++
HRESULT hr; 
IBackgroundCopyJob5* job; 
BITS_JOB_PROPERTY_VALUE propertyValue; 
propertyValue.ClsID = __uuidof(CNotifyInterface); 

hr = job->SetProperty(BITS_JOB_PROPERTY_NOTIFICATION_CLSID, propertyValue); 
if (SUCCEEDED(hr)) 
{ 
    hr = job->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED |  
                             BG_NOTIFY_JOB_ERROR); 
} 

if (FAILED(hr)) 
{ 
    // Handle error - unable to register callbacks. 
} 
```



 

 