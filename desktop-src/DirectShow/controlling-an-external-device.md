---
description: Controllo di un dispositivo esterno
ms.assetid: 5347cd55-a27e-40b9-857c-09e3665a1817
title: Controllo di un dispositivo esterno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84cb82de59877f2527c92da9123d8a9d5a59d41e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520722"
---
# <a name="controlling-an-external-device"></a><span data-ttu-id="0273b-103">Controllo di un dispositivo esterno</span><span class="sxs-lookup"><span data-stu-id="0273b-103">Controlling an External Device</span></span>

<span data-ttu-id="0273b-104">Per controllare un dispositivo VTR (video tape recorder), usare il metodo [**IAMExtTransport::p UT \_ mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) .</span><span class="sxs-lookup"><span data-stu-id="0273b-104">To control a video tape recorder (VTR) device, use the [**IAMExtTransport::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) method.</span></span> <span data-ttu-id="0273b-105">Specificare il nuovo stato usando una delle costanti elencate nello stato del trasporto del [dispositivo](device-transport-state.md).</span><span class="sxs-lookup"><span data-stu-id="0273b-105">Specify the new state by using one of the constants listed in the [Device Transport State](device-transport-state.md).</span></span> <span data-ttu-id="0273b-106">Per arrestare il dispositivo, ad esempio, usare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="0273b-106">For example, to stop the device, use the following:</span></span>


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



<span data-ttu-id="0273b-107">Poiché il VTR è un dispositivo fisico, in genere si verifica un ritardo tra l'invio del comando e il completamento del comando.</span><span class="sxs-lookup"><span data-stu-id="0273b-107">Because the VTR is a physical device, there is typically a lag between issuing the command and when the command completes.</span></span> <span data-ttu-id="0273b-108">L'applicazione deve creare un secondo thread di lavoro che attende il completamento del comando.</span><span class="sxs-lookup"><span data-stu-id="0273b-108">Your application should create a second worker thread that waits for the command to finish.</span></span> <span data-ttu-id="0273b-109">Al termine del comando, il thread può aggiornare l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0273b-109">When the command finishes, the thread can update the user interface.</span></span> <span data-ttu-id="0273b-110">Usare una sezione critica per serializzare la modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="0273b-110">Use a critical section to serialize the state change.</span></span>

<span data-ttu-id="0273b-111">Alcuni VTR possono notificare all'applicazione quando lo stato di trasporto del dispositivo è cambiato.</span><span class="sxs-lookup"><span data-stu-id="0273b-111">Some VTRs can notify the application when the device's transport state has changed.</span></span> <span data-ttu-id="0273b-112">Se il dispositivo supporta questa funzionalità, il thread di lavoro può attendere la notifica.</span><span class="sxs-lookup"><span data-stu-id="0273b-112">If the device supports this feature, the worker thread can wait for the notification.</span></span> <span data-ttu-id="0273b-113">Secondo la specifica "unità di registrazione/lettore nastri AV/C" dell'associazione commerciale 1394, tuttavia, il comando notifica stato trasporto è facoltativo, ovvero i dispositivi non sono necessari per supportarla.</span><span class="sxs-lookup"><span data-stu-id="0273b-113">According to the 1394 Trade Association's "AV/C Tape Recorder/Player Subunit Specification", however, the transport-state notification command is optional, meaning devices are not required to support it.</span></span> <span data-ttu-id="0273b-114">Se un dispositivo non supporta la notifica, è consigliabile eseguire il polling del dispositivo a intervalli periodici per lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="0273b-114">If a device does not support notification, you should poll the device at periodic intervals for its current state.</span></span>

<span data-ttu-id="0273b-115">In questa sezione viene innanzitutto descritto il meccanismo di notifica, quindi viene descritto il polling del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0273b-115">This section first describes the notification mechanism, and then describes device polling.</span></span>

<span data-ttu-id="0273b-116">Uso della notifica sullo stato del trasporto</span><span class="sxs-lookup"><span data-stu-id="0273b-116">Using Transport State Notification</span></span>

<span data-ttu-id="0273b-117">La notifica sullo stato del trasporto funziona facendo in modo che il driver segnali un evento quando il trasporto passa a un nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="0273b-117">Transport state notification works by having the driver signal an event when the transport switches to a new state.</span></span> <span data-ttu-id="0273b-118">Nell'applicazione dichiarare una sezione critica, un evento e un handle di thread.</span><span class="sxs-lookup"><span data-stu-id="0273b-118">In your application, declare a critical section, an event, and a thread handle.</span></span> <span data-ttu-id="0273b-119">La sezione critica viene usata per sincronizzare lo stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0273b-119">The critical section is used to synchronize the device state.</span></span> <span data-ttu-id="0273b-120">L'evento viene usato per arrestare il thread di lavoro quando l'applicazione viene chiusa:</span><span class="sxs-lookup"><span data-stu-id="0273b-120">The event is used to halt the worker thread when the application exits:</span></span>


```C++
HANDLE hThread = 0;
HANDLE hThreadEnd = CreateEvent(NULL, TRUE, FALSE, NULL); 
if (hThreadEnd == NULL)
{
    // Handle error.
}
CRITICAL_SECTION csIssueCmd;
InitializeCriticalSection(&cdIssueCmd);
```



<span data-ttu-id="0273b-121">Dopo aver creato un'istanza del filtro di acquisizione, creare il thread di lavoro:</span><span class="sxs-lookup"><span data-stu-id="0273b-121">After you create an instance of the capture filter, create the worker thread:</span></span>


```C++
DWORD ThreadId;
hThread = CreateThread(NULL, 0, ThreadProc, 0, 0, &ThreadId);
```



<span data-ttu-id="0273b-122">Nel thread di lavoro, iniziare chiamando il metodo [**IAMExtTransport:: GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) con il valore ed \_ inviare \_ HEVENT \_ Get.</span><span class="sxs-lookup"><span data-stu-id="0273b-122">In the worker thread, start by calling the [**IAMExtTransport::GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) method with the value ED\_NOTIFY\_HEVENT\_GET.</span></span> <span data-ttu-id="0273b-123">Questa chiamata restituisce un handle a un evento che verrà segnalato al completamento di un'operazione:</span><span class="sxs-lookup"><span data-stu-id="0273b-123">This call returns a handle to an event that will be signaled when an operation completes:</span></span>


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



<span data-ttu-id="0273b-124">Successivamente, chiamare di nuovo **GetState** e passare il valore \_ \_ Notify Change Mode \_ :</span><span class="sxs-lookup"><span data-stu-id="0273b-124">Next, call **GetState** again and pass the value ED\_MODE\_CHANGE\_NOTIFY:</span></span>


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



<span data-ttu-id="0273b-125">Se il dispositivo supporta la notifica, il metodo restituisce il valore E \_ in sospeso.</span><span class="sxs-lookup"><span data-stu-id="0273b-125">If the device supports notification, the method returns the value E\_PENDING.</span></span> <span data-ttu-id="0273b-126">In caso contrario, è necessario eseguire il polling del dispositivo, come descritto nella sezione successiva. Supponendo che il dispositivo supporti la notifica, l'evento viene segnalato ogni volta che viene modificato lo stato del trasporto VTR.</span><span class="sxs-lookup"><span data-stu-id="0273b-126">(Otherwise, you must poll device, as described in the next section.) Assuming the device supports notification, the event will be signaled whenever the state of the VTR transport changes.</span></span> <span data-ttu-id="0273b-127">A questo punto, è possibile aggiornare l'interfaccia utente in modo da riflettere il nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="0273b-127">At this point, you can update the user interface to reflect the new state.</span></span> <span data-ttu-id="0273b-128">Per ottenere la notifica successiva, reimpostare l'handle di evento e chiamare di nuovo **GetStatus** con la \_ modalità di notifica di \_ modifica \_ .</span><span class="sxs-lookup"><span data-stu-id="0273b-128">To get the next notification, reset the event handle and call **GetStatus** with ED\_MODE\_CHANGE\_NOTIFY again.</span></span>

<span data-ttu-id="0273b-129">Prima di uscire dal thread di lavoro, rilasciare l'handle di evento chiamando **GetStatus** con il flag ed \_ inviare Notify \_ HEVENT \_ e l'indirizzo dell'handle:</span><span class="sxs-lookup"><span data-stu-id="0273b-129">Before the worker thread exits, release the event handle by calling **GetStatus** with the flag ED\_NOTIFY\_HEVENT\_RELEASE and the address of the handle:</span></span>


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



<span data-ttu-id="0273b-130">Nel codice seguente viene illustrata la procedura completa del thread.</span><span class="sxs-lookup"><span data-stu-id="0273b-130">The following code shows the complete thread procedure.</span></span> <span data-ttu-id="0273b-131">Si presuppone che la funzione UpdateTransportState sia una funzione dell'applicazione che aggiorna l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="0273b-131">The function UpdateTransportState is assumed to be an application function that updates the user interface.</span></span> <span data-ttu-id="0273b-132">Si noti che il thread è in attesa di due eventi: l'evento di notifica (*hNotify*) e l'evento di terminazione del thread (*hThreadEnd*).</span><span class="sxs-lookup"><span data-stu-id="0273b-132">Note that the thread waits for two events: the notification event (*hNotify*) and the thread-termination event (*hThreadEnd*).</span></span> <span data-ttu-id="0273b-133">Si noti anche che la sezione critica viene usata per proteggere la variabile di stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0273b-133">Also note where the critical section is used to protect the device state variable.</span></span>


```C++
DWORD WINAPI ThreadProc(void *pParam)
{
    HRESULT hr;
    HANDLE  EventHandles[2];
    HANDLE  hNotify = NULL;
    DWORD   WaitStatus;
    LONG    State;

    // Get the notification event handle. This event will be signaled when
    // the next state-change operation completes.   
    hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);

    while (hThread && hNotify && hThreadEnd) 
    {
        EnterCriticalSection(&csIssueCmd);
        // Ask the device to notify us when the state changes.
        hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
        LeaveCriticalSection(&csIssueCmd); 

        if(hr == E_PENDING)  // The device supports notification.
        {
            // Wait for the notification.
            EventHandles[0] = hNotify;
            EventHandles[1] = hThreadEnd;
            WaitStatus = WaitForMultipleObjects(2, EventHandles, FALSE, INFINITE);
            if(WAIT_OBJECT_0 == WaitStatus) 
            {
                // We got notified. Query for the new state.
                EnterCriticalSection(&csIssueCmd);  
                hr = m_pTransport->get_Mode(State);
                UpdateTransportState(State);  // Update the UI.
                LeaveCriticalSection(&m_csIssueCmd);
                ResetEvent(hNotify);
            } 
            else {
                break;  // End this thread.
            }
        } 
        else {          
            // The device does not support notification.
            PollDevice();        
        } 
    } // while

    // Cancel notification. 
    hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify);
    return 1; 
}
```



<span data-ttu-id="0273b-134">Usare anche la sezione Critical quando si inviano comandi al dispositivo, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="0273b-134">Also use the critical section when you issue commands to the device, as follows:</span></span>


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



<span data-ttu-id="0273b-135">Prima di uscire dall'applicazione, arrestare il thread secondario impostando l'evento thread-end:</span><span class="sxs-lookup"><span data-stu-id="0273b-135">Before the application exits, halt the secondary thread by setting the thread-end event:</span></span>


```C++
if (hThread) 
{
    // Signaling this event will cause the thread to end.    
    if (SetEvent(hThreadEnd))
    {
        // Wait for it to end.
        WaitForSingleObjectEx(hThread, INFINITE, FALSE);
    }
}
CloseHandle(hThreadEnd);
CloseHandle(hThread);
```



<span data-ttu-id="0273b-136">Polling dello stato del trasporto</span><span class="sxs-lookup"><span data-stu-id="0273b-136">Polling the Transport State</span></span>

<span data-ttu-id="0273b-137">Se si chiama **IAMExtTransport:: GetStatus** con il \_ flag di notifica della modifica della modalità ed \_ \_ , il valore restituito non è e \_ in sospeso, significa che il dispositivo non supporta la notifica.</span><span class="sxs-lookup"><span data-stu-id="0273b-137">If you call **IAMExtTransport::GetStatus** with the ED\_MODE\_CHANGE\_NOTIFY flag and the return value is not E\_PENDING, it means the device does not support notification.</span></span> <span data-ttu-id="0273b-138">In tal caso, è necessario eseguire il polling del dispositivo per determinarne lo stato.</span><span class="sxs-lookup"><span data-stu-id="0273b-138">In that case, you must poll the device to determine its state.</span></span> <span data-ttu-id="0273b-139">Il *polling* indica semplicemente la chiamata della **\_ modalità Get** a intervalli regolari per verificare lo stato del trasporto.</span><span class="sxs-lookup"><span data-stu-id="0273b-139">*Polling* simply means calling **get\_Mode** at regular intervals to check the transport state.</span></span> <span data-ttu-id="0273b-140">È comunque necessario usare un thread secondario e una sezione critica, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="0273b-140">You should still use a secondary thread and a critical section, as described earlier.</span></span> <span data-ttu-id="0273b-141">Il thread esegue una query sul dispositivo per lo stato a intervalli regolari.</span><span class="sxs-lookup"><span data-stu-id="0273b-141">The thread queries the device for its state at a regular interval.</span></span> <span data-ttu-id="0273b-142">Nell'esempio seguente viene illustrato un modo per implementare il thread:</span><span class="sxs-lookup"><span data-stu-id="0273b-142">The following example shows one way to implement the thread:</span></span>


```C++
DWORD WINAPI ThreadProc(void *pParam)
{
    HRESULT hr;
    LONG State;
    DWORD WaitStatus;

    while (hThread && hThreadEnd) 
    {
        EnterCriticalSection(&csIssueCmd);  
        State = 0;
        hr = pTransport->get_Mode(&State);
        LeaveCriticalSection(&csIssueCmd); 
        UpdateTransportState(State);

        // Wait for a while, or until the thread ends. 
        WaitStatus = WaitForSingleObjectEx(hThreadEnd, 200, FALSE); 
        if (WaitStatus == WAIT_OBJECT_0)
        {
            break; // Exit thread now. 
        }
        // Otherwise, the wait timed out. Time to poll again.
    }
    return 1;
}
```



## <a name="related-topics"></a><span data-ttu-id="0273b-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0273b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0273b-144">Controllo di una videocamera DV</span><span class="sxs-lookup"><span data-stu-id="0273b-144">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



