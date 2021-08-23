---
description: Controllo di un dispositivo esterno
ms.assetid: 5347cd55-a27e-40b9-857c-09e3665a1817
title: Controllo di un dispositivo esterno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f530bb48f35a6e35a0ab75d0559cc3c6770c4d0d1dfb2948f871982f70eb0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652131"
---
# <a name="controlling-an-external-device"></a>Controllo di un dispositivo esterno

Per controllare un dispositivo VTR (Video Tape Recorder), usare il metodo [**IAMExtTransport::p ut \_ Mode.**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) Specificare il nuovo stato usando una delle costanti elencate in [Stato del trasporto del dispositivo](device-transport-state.md). Ad esempio, per arrestare il dispositivo, usare quanto segue:


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



Poiché la VTR è un dispositivo fisico, in genere si verifica un ritardo tra l'esecuzione del comando e il completamento del comando. L'applicazione deve creare un secondo thread di lavoro che attende il completamento del comando. Al termine del comando, il thread può aggiornare l'interfaccia utente. Usare una sezione critica per serializzare la modifica dello stato.

Alcuni VTR possono notificare all'applicazione quando lo stato di trasporto del dispositivo è cambiato. Se il dispositivo supporta questa funzionalità, il thread di lavoro può attendere la notifica. In base alla specifica "AV/C Tape Recorder/Player Subunit Specification" della 1394 Trade Association, tuttavia, il comando di notifica dello stato del trasporto è facoltativo, vale a dire che non è necessario che i dispositivi lo supportino. Se un dispositivo non supporta la notifica, è necessario eseguire il polling del dispositivo a intervalli periodici per lo stato corrente.

Questa sezione descrive innanzitutto il meccanismo di notifica e quindi il polling dei dispositivi.

Utilizzo della notifica dello stato del trasporto

La notifica dello stato del trasporto funziona facendo in modo che il driver segnali un evento quando il trasporto passa a un nuovo stato. Nell'applicazione dichiarare una sezione critica, un evento e un handle di thread. La sezione critica viene usata per sincronizzare lo stato del dispositivo. L'evento viene usato per arrestare il thread di lavoro quando l'applicazione viene chiusa:


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



Nel thread di lavoro iniziare chiamando il metodo [**IAMExtTransport::GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) con il valore ED \_ NOTIFY \_ HEVENT \_ GET. Questa chiamata restituisce un handle a un evento che verrà segnalato al completamento di un'operazione:


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



Chiamare quindi di nuovo **GetState** e passare il valore ED \_ MODE CHANGE \_ \_ NOTIFY:


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



Se il dispositivo supporta la notifica, il metodo restituisce il valore E \_ PENDING. In caso contrario, è necessario eseguire il polling del dispositivo, come descritto nella sezione successiva. Supponendo che il dispositivo supporti la notifica, l'evento verrà segnalato ogni volta che lo stato del trasporto VTR cambia. A questo punto, è possibile aggiornare l'interfaccia utente per riflettere il nuovo stato. Per ottenere la notifica successiva, reimpostare l'handle dell'evento e chiamare di nuovo **GetStatus** con ED \_ MODE CHANGE \_ \_ NOTIFY.

Prima della chiusura del thread di lavoro, rilasciare l'handle di evento chiamando **GetStatus** con il flag ED \_ NOTIFY \_ HEVENT \_ RELEASE e l'indirizzo dell'handle:


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



Nel codice seguente viene illustrata la procedura di thread completa. Si presuppone che la funzione UpdateTransportState sia una funzione dell'applicazione che aggiorna l'interfaccia utente. Si noti che il thread attende due eventi: l'evento di notifica (*hNotify*) e l'evento di terminazione del thread (*hThreadEnd*). Si noti anche dove viene usata la sezione critica per proteggere la variabile di stato del dispositivo.


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



Usare anche la sezione critica quando si emettere comandi per il dispositivo, come indicato di seguito:


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



Prima della chiusura dell'applicazione, arrestare il thread secondario impostando l'evento di fine thread:


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

Se si chiama **IAMExtTransport::GetStatus** con il flag ED MODE CHANGE NOTIFY e il valore restituito non è E PENDING, significa che il dispositivo non \_ supporta la \_ \_ \_ notifica. In tal caso, è necessario eseguire il polling del dispositivo per determinarne lo stato. *Il polling* significa semplicemente chiamare **get \_ Mode** a intervalli regolari per controllare lo stato del trasporto. È comunque consigliabile usare un thread secondario e una sezione critica, come descritto in precedenza. Il thread esegue una query sul dispositivo per il relativo stato a intervalli regolari. L'esempio seguente illustra un modo per implementare il thread:


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

[Controllo di un videocamere DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



