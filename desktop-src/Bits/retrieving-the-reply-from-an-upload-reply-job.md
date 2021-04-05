---
title: Recupero della risposta da un processo di Upload-Reply
description: Per caricare i dati in un'applicazione server e fare in modo che restituiscano dati al client, specificare il processo come \_ processo di risposta di caricamento del tipo di processo BG \_ \_ \_ .
ms.assetid: bab28a2c-1e2f-4b76-9dc6-57df26f7efec
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 582a37a31c13c5cc3e0b44c51a767cfbe465c64c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955211"
---
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a>Recupero della risposta da un processo di Upload-Reply

Un bit Upload-Reply processo, oltre a caricare un file in un server, esaminerà anche un URL di risposta inviato come parte della risposta del server e quindi seguirà automaticamente l'URL di risposta e scaricherà una risposta. Per ulteriori informazioni sul valore dell'intestazione BITS-Reply-URL, vedere la documentazione relativa al [ACK per il frammento](/windows/desktop/Bits/ack-for-fragment) .

\_ \_ \_ \_ Per creare un processo di tipo Upload-Reply, impostare il tipo di processo come tipo di processo BG Reply. I dati di risposta sono disponibili per il client dopo che il processo entra \_ nello \_ stato di trasferimento dello stato del processo BG \_ . Per recuperare la risposta, chiamare uno dei metodi seguenti:

-   [**IBackgroundCopyJob2::GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    Fornisce una copia in memoria dei dati di risposta. Utilizzare questo metodo per leggere i dati di risposta prima o dopo la chiamata al metodo [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . Se i dati di risposta superano 1 MB, l'applicazione deve chiamare il metodo [**IBackgroundCopyJob2:: GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) per recuperare il nome del file di risposta e leggerne direttamente il contenuto.

-   [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    Fornisce il nome del file che contiene la risposta. È necessario chiamare il metodo **Metodo ibackgroundcopyjob:: complete** prima di aprire e leggere il file di risposta. il file di risposta non è disponibile per il client fino a quando non viene chiamato il metodo **completo** .

Chiamare questi metodi nel metodo [**IBackgroundCopyCallback:: JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) solo se la risposta è di dimensioni ridotte e può essere elaborata rapidamente in modo da non bloccare il thread di callback. Se invece del callback si utilizza la [**notifica della riga di comando**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) , passare l'identificatore del processo al file eseguibile. Il file eseguibile usa l'identificatore del processo per chiamare il metodo **completo** per rendere disponibile il file di risposta.

Gli esempi seguenti illustrano come usare ogni metodo per recuperare i dati di risposta.

-   [Uso di GetReplyData](#using-getreplydata)
-   [Uso di GetReplyFileName](#using-getreplyfilename)

## <a name="using-getreplydata"></a>Uso di GetReplyData

Nell'esempio seguente viene illustrato come recuperare i dati di risposta utilizzando il metodo [**IBackgroundCopyJob2:: GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) . Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido, che il tipo di processo sia upload-Reply e che lo stato del processo sia BG \_ processo \_ stato \_ trasferito.


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
BYTE* pReply = NULL;
UINT64 ReplySize;

//Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob2
//interface pointer. The IBackgroundCopyJob2 interface contains the GetReplyData method.
hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
if (SUCCEEDED(hr))
{
    hr = pJob2->GetReplyData(&pReply, &ReplySize);
    if (S_OK == hr))
    {
        if (pReply)
        {
            //Do something with the data.
            CoTaskMemFree(pReply);
        }
        else
        {
            //The server application did not return a reply.
        }
    }
    else if (BG_E_TOO_LARGE == hr)
    {
        //The reply exceeds 1 MB. To retrieve the reply, get the reply file name,
        //complete the job, open the reply file, and read the reply.
    }
    else
    {
        //Handle the error
    }

    pJob2->Release(); //When done, release the interface.
}
else
{
    //Handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
    //running on the computer is less than BITS 1.5.
}
```



## <a name="using-getreplyfilename"></a>Uso di GetReplyFileName

Nell'esempio seguente viene illustrato come recuperare i dati di risposta utilizzando il metodo [**IBackgroundCopyJob2:: GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) . Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido, che il tipo di processo sia upload-Reply e che lo stato del processo sia lo \_ stato del processo BG \_ \_ trasferito.


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR* pszFileName = NULL;

//Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob2
//interface pointer. The IBackgroundCopyJob2 interface contains the GetReplyFileName method.
hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
if (SUCCEEDED(hr))
{
    hr = pJob2->GetReplyFileName(&pszFileName);
    if (SUCCEEDED(hr))
    {
        //Calling the Complete method removes the job from the queue, 
        //so make sure you maintain an interface pointer to this job 
        //or retrieve any job related information that you require 
        //when processing the reply.
        hr = pJob->Complete();

        //Open, read the file, and do something with the data.
        CoTaskMemFree(pszFileName);
    }

    pJob2->Release(); //When done, release the interface.
}
else
{
    //Handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
    //running on the computer is less than BITS 1.5.
}
```



 

 




