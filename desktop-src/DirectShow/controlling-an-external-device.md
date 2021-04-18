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
# <a name="controlling-an-external-device"></a>Controllo di un dispositivo esterno

Per controllare un dispositivo VTR (video tape recorder), usare il metodo [**IAMExtTransport::p UT \_ mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) . Specificare il nuovo stato usando una delle costanti elencate nello stato del trasporto del [dispositivo](device-transport-state.md). Per arrestare il dispositivo, ad esempio, usare quanto segue:


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



Poiché il VTR è un dispositivo fisico, in genere si verifica un ritardo tra l'invio del comando e il completamento del comando. L'applicazione deve creare un secondo thread di lavoro che attende il completamento del comando. Al termine del comando, il thread può aggiornare l'interfaccia utente. Usare una sezione critica per serializzare la modifica dello stato.

Alcuni VTR possono notificare all'applicazione quando lo stato di trasporto del dispositivo è cambiato. Se il dispositivo supporta questa funzionalità, il thread di lavoro può attendere la notifica. Secondo la specifica "unità di registrazione/lettore nastri AV/C" dell'associazione commerciale 1394, tuttavia, il comando notifica stato trasporto è facoltativo, ovvero i dispositivi non sono necessari per supportarla. Se un dispositivo non supporta la notifica, è consigliabile eseguire il polling del dispositivo a intervalli periodici per lo stato corrente.

In questa sezione viene innanzitutto descritto il meccanismo di notifica, quindi viene descritto il polling del dispositivo.

Uso della notifica sullo stato del trasporto

La notifica sullo stato del trasporto funziona facendo in modo che il driver segnali un evento quando il trasporto passa a un nuovo stato. Nell'applicazione dichiarare una sezione critica, un evento e un handle di thread. La sezione critica viene usata per sincronizzare lo stato del dispositivo. L'evento viene usato per arrestare il thread di lavoro quando l'applicazione viene chiusa:


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



Dopo aver creato un'istanza del filtro di acquisizione, creare il thread di lavoro:


```C++
DWORD ThreadId;
hThread = CreateThread(NULL, 0, ThreadProc, 0, 0, &ThreadId);
```



Nel thread di lavoro, iniziare chiamando il metodo [**IAMExtTransport:: GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) con il valore ed \_ inviare \_ HEVENT \_ Get. Questa chiamata restituisce un handle a un evento che verrà segnalato al completamento di un'operazione:


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



Successivamente, chiamare di nuovo **GetState** e passare il valore \_ \_ Notify Change Mode \_ :


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



Se il dispositivo supporta la notifica, il metodo restituisce il valore E \_ in sospeso. In caso contrario, è necessario eseguire il polling del dispositivo, come descritto nella sezione successiva. Supponendo che il dispositivo supporti la notifica, l'evento viene segnalato ogni volta che viene modificato lo stato del trasporto VTR. A questo punto, è possibile aggiornare l'interfaccia utente in modo da riflettere il nuovo stato. Per ottenere la notifica successiva, reimpostare l'handle di evento e chiamare di nuovo **GetStatus** con la \_ modalità di notifica di \_ modifica \_ .

Prima di uscire dal thread di lavoro, rilasciare l'handle di evento chiamando **GetStatus** con il flag ed \_ inviare Notify \_ HEVENT \_ e l'indirizzo dell'handle:


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



Nel codice seguente viene illustrata la procedura completa del thread. Si presuppone che la funzione UpdateTransportState sia una funzione dell'applicazione che aggiorna l'interfaccia utente. Si noti che il thread è in attesa di due eventi: l'evento di notifica (*hNotify*) e l'evento di terminazione del thread (*hThreadEnd*). Si noti anche che la sezione critica viene usata per proteggere la variabile di stato del dispositivo.


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



Usare anche la sezione Critical quando si inviano comandi al dispositivo, come indicato di seguito:


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



Prima di uscire dall'applicazione, arrestare il thread secondario impostando l'evento thread-end:


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



Polling dello stato del trasporto

Se si chiama **IAMExtTransport:: GetStatus** con il \_ flag di notifica della modifica della modalità ed \_ \_ , il valore restituito non è e \_ in sospeso, significa che il dispositivo non supporta la notifica. In tal caso, è necessario eseguire il polling del dispositivo per determinarne lo stato. Il *polling* indica semplicemente la chiamata della **\_ modalità Get** a intervalli regolari per verificare lo stato del trasporto. È comunque necessario usare un thread secondario e una sezione critica, come descritto in precedenza. Il thread esegue una query sul dispositivo per lo stato a intervalli regolari. Nell'esempio seguente viene illustrato un modo per implementare il thread:


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di una videocamera DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



