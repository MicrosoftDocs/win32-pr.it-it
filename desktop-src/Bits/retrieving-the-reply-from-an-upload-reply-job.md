---
title: Recupero della risposta da un processo Upload-Reply lavoro
description: Per caricare i dati in un'applicazione server e fare in modo che restituiti i dati al client, specificare il processo come processo BG \_ JOB \_ TYPE UPLOAD \_ \_ REPLY.
ms.assetid: bab28a2c-1e2f-4b76-9dc6-57df26f7efec
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 79ca145a3ed243209fc0059b20823e32da3cf3974850a6bc3e872f43dbd40aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004881"
---
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a>Recupero della risposta da un processo Upload-Reply lavoro

Un processo di Upload-Reply BITS, oltre a caricare un file in un server, esaminerà anche un URL di risposta inviato come parte della risposta del server e quindi seguirà automaticamente l'URL di risposta e scarizzerà una risposta. Per altri dettagli sul valore dell'intestazione BITS-Reply-URL, vedere la documentazione di [Ack for Fragment.](/windows/desktop/Bits/ack-for-fragment)

Impostare il tipo di processo su BG \_ JOB TYPE UPLOAD REPLY per creare un Upload-Reply tipo di \_ \_ \_ processo. I dati di risposta sono disponibili per il client dopo che il processo passa allo stato BG \_ JOB \_ STATE \_ TRANSFERRED. Per recuperare la risposta, chiamare uno dei metodi seguenti:

-   [**IBackgroundCopyJob2::GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    Fornisce una copia in memoria dei dati di risposta. Usare questo metodo per leggere i dati di risposta prima o dopo la chiamata al [**metodo IBackgroundCopyJob::Complete.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) Se i dati di risposta superano 1 MB, l'applicazione deve chiamare il metodo [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) per recuperare il nome del file di risposta e leggerne direttamente il contenuto.

-   [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    Fornisce il nome del file che contiene la risposta. È necessario chiamare il **metodo IBackgroundCopyJob::Complete** prima di aprire e leggere il file di risposta. Il file di risposta non è disponibile per il client fino a quando non si chiama il **metodo** Complete.

Chiamare questi metodi nel metodo [**IBackgroundCopyCallback::JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) solo se la risposta è di piccole dimensioni e può essere elaborata rapidamente in modo da non bloccare il thread di callback. Se si usa [**la notifica della riga di**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) comando anziché il callback, passare l'identificatore del processo al file eseguibile. Il file eseguibile usa l'identificatore del processo per chiamare il **metodo Complete** per rendere disponibile il file di risposta.

Negli esempi seguenti viene illustrato come utilizzare ogni metodo per recuperare i dati di risposta.

-   [Uso di GetReplyData](#using-getreplydata)
-   [Uso di GetReplyFileName](#using-getreplyfilename)

## <a name="using-getreplydata"></a>Uso di GetReplyData

L'esempio seguente illustra come recuperare i dati di risposta usando il [**metodo IBackgroundCopyJob2::GetReplyData.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) Nell'esempio si presuppone che il puntatore a interfaccia [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido, che il tipo del processo sia upload-reply e che lo stato del processo sia BG \_ JOB STATE \_ \_ TRANSFERRED.


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

L'esempio seguente illustra come recuperare i dati di risposta usando il [**metodo IBackgroundCopyJob2::GetReplyFileName.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) Nell'esempio si presuppone che il puntatore a interfaccia [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido, che il tipo di processo sia upload-reply e che lo stato del processo sia BG \_ JOB STATE \_ \_ TRANSFERRED.


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



 

 




