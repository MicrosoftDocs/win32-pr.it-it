---
title: Registrazione di un callback COM
description: Anziché eseguire il polling delle modifiche nello stato di un processo, è possibile registrarsi per ricevere una notifica quando lo stato del processo cambia.
ms.assetid: 29350ea4-f7a9-4a42-a531-2cf623fe247b
keywords:
- transfer job BITS , notifica degli eventi
- registrazione per BITS di notifica degli eventi
- bits di notifica degli eventi
- bits di notifica degli eventi, callback
- eventi di notifica BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753feb481a578c30322d18def07418c2dcb611d601fcb438b0e85e843697790b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118680005"
---
# <a name="registering-a-com-callback"></a>Registrazione di un callback COM

Anziché eseguire [il polling](polling-for-the-status-of-the-job.md) delle modifiche nello stato di un processo, è possibile registrarsi per ricevere una notifica quando lo stato del processo cambia. Per ricevere la notifica, è necessario implementare [**l'interfaccia IBackgroundCopyCallback2.**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) L'interfaccia contiene i metodi seguenti che BITS chiama, a seconda della registrazione:

-   [**JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)
-   [**Errore di processo**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)
-   [**JobModification**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)
-   [**FileTransferred**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred)

Per un esempio che implementa [**l'interfaccia IBackgroundCopyCallback2,**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) vedere il codice di esempio [**nell'argomento Interfaccia IBackgroundCopyCallback.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)

[**L'interfaccia IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) fornisce una notifica quando viene trasferito un file. In genere, questo metodo viene usato per convalidare il file, in modo che il file sia disponibile per il download da parte dei peer. In caso contrario, il file non è disponibile per i peer fino a quando non si chiama il [**metodo IBackgroundCopyJob::Complete.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) Per convalidare il file, chiamare [**il metodo IBackgroundCopyFile3::SetValidationState.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate)

Esistono due metodi per registrare un callback COM: la registrazione di un oggetto callback o la registrazione di un ID di classe di callback. L'uso di un oggetto callback è più semplice e riduce il sovraccarico; L'uso di un CLSID di callback è più affidabile, ma più complicato. È possibile eseguire la registrazione, entrambe o nessuna delle due. BITS userà un oggetto callback, se esistente e può comunque essere chiamato, ed eseguire il fall back per creare un'istanza di un nuovo oggetto in base a un ID di classe specificato se l'operazione ha esito negativo.

### <a name="registering-a-callback-object"></a>Registrazione di un oggetto callback

Per registrare l'implementazione con BITS, chiamare [**il metodo IBackgroundCopyJob::SetNotifyInterface.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) Per specificare i metodi che BITS chiama, chiamare [**il metodo IBackgroundCopyJob::SetNotifyFlags.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)

L'interfaccia di notifica non è più valida al termine dell'applicazione. BITS non rende persistente l'interfaccia di notifica. Di conseguenza, il processo di inizializzazione dell'applicazione deve registrare i processi esistenti per i quali si vuole ricevere la notifica. Se è necessario acquisire informazioni sullo stato e sull'avanzamento dell'esecuzione dall'ultima esecuzione dell'applicazione, eseguire il polling delle informazioni sullo stato e sullo stato durante l'inizializzazione dell'applicazione.

Prima di uscire, l'applicazione deve cancellare il puntatore all'interfaccia di callback (**SetNotifyInterface(NULL)**). È più efficiente cancellare il puntatore di callback piuttosto che consentire a BITS di rilevare che non è più valido.

Si noti che se più applicazioni chiamano il metodo [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) per impostare l'interfaccia di notifica per il processo, l'ultima applicazione che chiama il metodo **SetNotifyInterface** è quella che riceverà le notifiche. Le altre applicazioni non riceveranno notifiche.

Nell'esempio seguente viene illustrato come eseguire la registrazione per le notifiche. Nell'esempio si presuppone che il [**puntatore a interfaccia IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido. Per informazioni dettagliate sulla classe di esempio CNotifyInterface usata nell'esempio seguente, vedere [**l'interfaccia IBackgroundCopyCallback.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)


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



### <a name="registering-a-callback-clsid"></a>Registrazione di un CLSID di callback

Per registrare un CLSID di callback con BITS, chiamare il metodo [**IBackgroundCopyJob5::SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) con IL VALORE PROPERTY **NOTIFICATION DI BITS \_ PROPERTY \_ \_ \_ CLSID** PropertyId. Per specificare i metodi che BITS chiama, chiamare [**il metodo IBackgroundCopyJob::SetNotifyFlags.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)

È necessario assicurarsi che il CLSID di notifica sia registrato in un server COM out-of-process prima di registrare il CLSID con un processo BITS. L'implementazione [di un server COM](/windows/desktop/com/com-server-responsibilities) è molto più complessa rispetto alla definizione e al passaggio di un oggetto callback, ma offre diversi vantaggi importanti. Un server COM consente a BITS di mantenere l'associazione tra un processo BITS e il codice dell'applicazione tra i riavvii del sistema e per i processi di grandi dimensioni o di lunga durata. Un server COM consente anche l'arresto completo dell'applicazione mentre BITS continua l'esecuzione dei trasferimenti in background, migliorando l'utilizzo di batteria, CPU e memoria del sistema.

Per fornire una notifica registrata per la ricezione, BITS tenta prima di tutto di chiamare il metodo corrispondente di qualsiasi oggetto callback esistente che è stato collegato. Se non è presente alcun oggetto esistente o se l'oggetto esistente è stato disconnesso (in genere in seguito alla chiusura dell'applicazione), BITS chiamerà CoCreateInstance usando il CLSID di notifica per creare un'istanza di un nuovo oggetto callback e userà tale oggetto per eventuali altri callback fino a quando non viene disconnesso o viene sostituito da una nuova chiamata a [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface).

A differenza degli oggetti callback, il CLSID di callback viene mantenuto insieme ai processi BITS corrispondenti se il servizio BITS o il sistema vengono arrestati e riavviati. L'applicazione può cancellare qualsiasi CLSID di notifica impostato in precedenza prima di uscire (o in qualsiasi altro momento) passando un nuovo CLSID di notifica null, ma l'applicazione potrebbe preferire lasciare registrato il CLSID di notifica se l'applicazione ha registrato per l'avvio COM in risposta alle richieste \_ CoCreateInstance per il CLSID. Si noti che se più applicazioni impostano il chiama la proprietà CLSID BITS JOB PROPERTY NOTIFICATION, l'ultimo CLSID da impostare è quello che VERRÀ utilizzato da BITS per creare un'istanza degli oggetti callback. Non verrà creata un'istanza degli altri **\_ \_ \_ \_ CLSID.** Analogamente, se un'applicazione registra un CLSID e un'altra registra un oggetto callback, vengono applicate le regole consuete per l'oggetto callback che ha la precedenza e il CLSID non verrà usato a meno che l'oggetto callback non venga cancellato o disconnesso.

Nell'esempio seguente viene illustrato come eseguire la registrazione per le notifiche CLSID. Nell'esempio si presuppone che il puntatore a interfaccia [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) sia valido e che l'applicazione sia già registrata come server COM out-of-process che implementa la classe CNotifyInterface. Per informazioni dettagliate sulla classe di esempio CNotifyInterface usata nell'esempio seguente, vedere [**l'interfaccia IBackgroundCopyCallback.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)


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



 

 