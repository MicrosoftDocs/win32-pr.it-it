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
# <a name="registering-a-com-callback"></a>Registrazione di un callback COM

Anziché eseguire il [polling](polling-for-the-status-of-the-job.md) delle modifiche allo stato di un processo, è possibile registrarsi per ricevere una notifica quando lo stato del processo cambia. Per ricevere la notifica, è necessario implementare l'interfaccia [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) . L'interfaccia contiene i metodi seguenti chiamati da BITS, a seconda della registrazione:

-   [**JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)
-   [**JobError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)
-   [**JobModification**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)
-   [**Filetransfer**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred)

Per un esempio che implementa l'interfaccia [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) , vedere il codice di esempio nell'argomento dell'interfaccia [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .

L'interfaccia [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) fornisce una notifica quando un file viene trasferito. In genere, si usa questo metodo per convalidare il file, in modo che il file sia disponibile per il download dei peer. in caso contrario, il file non è disponibile per i peer fino a quando non viene chiamato il metodo [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . Per convalidare il file, chiamare il metodo [**IBackgroundCopyFile3:: SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) .

Esistono due metodi per la registrazione di un callback COM: la registrazione di un oggetto callback o la registrazione di un ID di classe di callback. L'utilizzo di un oggetto di callback è un sovraccarico più semplice e inferiore; l'utilizzo di un CLSID di callback è più affidabile, ma più complesso. È possibile registrare, entrambi o nessuno dei due-BITS utilizzerà un oggetto callback se ne esiste uno e può comunque essere chiamato e verrà eseguito il fallback alla creazione di un'istanza di un nuovo oggetto in base a un ID di classe fornito in caso di esito negativo.

### <a name="registering-a-callback-object"></a>Registrazione di un oggetto callback

Per registrare l'implementazione con BITS, chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) . Per specificare i metodi chiamati da BITS, chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags).

L'interfaccia di notifica diventa non valida al termine dell'applicazione; BITS non rende persistente l'interfaccia Notify. Di conseguenza, il processo di inizializzazione dell'applicazione dovrebbe registrare i processi esistenti per i quali si desidera ricevere la notifica. Se è necessario acquisire informazioni sullo stato e sullo stato di avanzamento dopo l'ultima esecuzione dell'applicazione, eseguire il polling delle informazioni sullo stato e sullo stato durante l'inizializzazione dell'applicazione.

Prima di uscire, l'applicazione deve cancellare il puntatore all'interfaccia di callback (**SetNotifyInterface (null)**). È più efficiente cancellare il puntatore di callback rispetto a consentire a BITS di rilevare che non è più valido.

Si noti che se più di un'applicazione chiama il metodo [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) per impostare l'interfaccia di notifica per il processo, l'ultima applicazione a chiamare il metodo **SetNotifyInterface** è quella che riceverà le notifiche, mentre le altre applicazioni non riceveranno le notifiche.

Nell'esempio seguente viene illustrato come eseguire la registrazione per le notifiche. Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido. Per informazioni dettagliate sulla classe di esempio CNotifyInterface usata nell'esempio seguente, vedere l'interfaccia [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .


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

Per registrare un CLSID di callback con BITS, chiamare il metodo [**IBackgroundCopyJob5:: SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) con la **\_ notifica della \_ proprietà \_ \_ del processo BITS** PropertyId. Per specificare i metodi chiamati da BITS, chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) .

Prima di registrare il CLSID con un processo BITS, è necessario assicurarsi che il CLSID di notifica sia registrato in un server COM out-of-process. L'implementazione di un [Server com](/windows/desktop/com/com-server-responsibilities) è significativamente più complessa rispetto alla definizione e al passaggio di un oggetto callback, ma offre diversi vantaggi importanti. Un server COM consente ai bit di mantenere l'associazione tra un processo BITS e il codice dell'applicazione tra i riavvii del sistema e per i processi di grandi dimensioni o di lunga durata. Un server COM consente inoltre all'applicazione di arrestarsi completamente mentre BITS continua l'esecuzione di trasferimenti in background, che può migliorare l'utilizzo della batteria, della CPU e della memoria del sistema.

Per fornire una notifica che è stata registrata per la ricezione, BITS tenta innanzitutto di chiamare il metodo corrispondente di qualsiasi oggetto callback esistente collegato. Se non è presente alcun oggetto o se l'oggetto esistente è stato disconnesso (in genere in seguito all'interruzione dell'applicazione), BITS chiamerà CoCreateInstance utilizzando il CLSID di notifica per creare un'istanza di un nuovo oggetto callback e utilizzerà tale oggetto per eventuali ulteriori callback fino a quando non viene disconnesso o viene sostituito da una nuova chiamata a [**Metodo ibackgroundcopyjob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface).

Diversamente dagli oggetti di callback, il CLSID di callback viene reso permanente insieme ai processi BITS corrispondenti se il servizio BITS o il sistema vengono arrestati e riavviati. L'applicazione può cancellare qualsiasi CLSID di notifica precedentemente impostato prima di uscire (o in qualsiasi altro momento) passando un nuovo CLSID di notifica del GUID \_ null, ma è possibile che l'applicazione preferisca lasciare la notifica CLSID registrata se l'applicazione è stata registrata in modo che com lo avvii in risposta alle richieste CoCreateInstance per il CLSID. Si noti che se più di un'applicazione imposta la proprietà **\_ \_ \_ \_ CLSID della proprietà del processo BITS** , l'ultimo CLSID da impostare è quello che verrà utilizzato da BITS per creare un'istanza degli oggetti di callback. non verrà creata un'istanza degli altri CLSID. Analogamente, se un'applicazione registra un CLSID e un altro registra un oggetto callback, le normali regole per l'oggetto callback che hanno la precedenza si applicano e il CLSID non verrà usato a meno che l'oggetto callback non venga cancellato o non venga disconnesso.

Nell'esempio seguente viene illustrato come eseguire la registrazione per le notifiche CLSID. Nell'esempio si presuppone che il puntatore all'interfaccia [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) sia valido e che l'applicazione sia già stata registrata come un server COM out-of-process che implementa la classe CNotifyInterface. Per informazioni dettagliate sulla classe di esempio CNotifyInterface usata nell'esempio seguente, vedere l'interfaccia [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .


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



 

 