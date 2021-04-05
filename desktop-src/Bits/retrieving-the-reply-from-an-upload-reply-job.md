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
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a><span data-ttu-id="da76b-103">Recupero della risposta da un processo di Upload-Reply</span><span class="sxs-lookup"><span data-stu-id="da76b-103">Retrieving the Reply from an Upload-Reply Job</span></span>

<span data-ttu-id="da76b-104">Un bit Upload-Reply processo, oltre a caricare un file in un server, esaminerà anche un URL di risposta inviato come parte della risposta del server e quindi seguirà automaticamente l'URL di risposta e scaricherà una risposta.</span><span class="sxs-lookup"><span data-stu-id="da76b-104">A BITS Upload-Reply job, in addition to uploading a file to a server, will also examine a reply URL sent as part of the server reply and then automatically follow the reply URL and download a response from it.</span></span> <span data-ttu-id="da76b-105">Per ulteriori informazioni sul valore dell'intestazione BITS-Reply-URL, vedere la documentazione relativa al [ACK per il frammento](/windows/desktop/Bits/ack-for-fragment) .</span><span class="sxs-lookup"><span data-stu-id="da76b-105">See the [Ack for Fragment](/windows/desktop/Bits/ack-for-fragment) documentation for more details about the BITS-Reply-URL header value.</span></span>

<span data-ttu-id="da76b-106">\_ \_ \_ \_ Per creare un processo di tipo Upload-Reply, impostare il tipo di processo come tipo di processo BG Reply.</span><span class="sxs-lookup"><span data-stu-id="da76b-106">Set the job type as BG\_JOB\_TYPE\_UPLOAD\_REPLY to create an Upload-Reply type job.</span></span> <span data-ttu-id="da76b-107">I dati di risposta sono disponibili per il client dopo che il processo entra \_ nello \_ stato di trasferimento dello stato del processo BG \_ .</span><span class="sxs-lookup"><span data-stu-id="da76b-107">The reply data is available to the client after the job enters the BG\_JOB\_STATE\_TRANSFERRED state.</span></span> <span data-ttu-id="da76b-108">Per recuperare la risposta, chiamare uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="da76b-108">To retrieve the reply, call one of the following methods:</span></span>

-   [<span data-ttu-id="da76b-109">**IBackgroundCopyJob2::GetReplyData**</span><span class="sxs-lookup"><span data-stu-id="da76b-109">**IBackgroundCopyJob2::GetReplyData**</span></span>](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    <span data-ttu-id="da76b-110">Fornisce una copia in memoria dei dati di risposta.</span><span class="sxs-lookup"><span data-stu-id="da76b-110">Provides an in-memory copy of the reply data.</span></span> <span data-ttu-id="da76b-111">Utilizzare questo metodo per leggere i dati di risposta prima o dopo la chiamata al metodo [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="da76b-111">Use this method to read the reply data before or after calling the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="da76b-112">Se i dati di risposta superano 1 MB, l'applicazione deve chiamare il metodo [**IBackgroundCopyJob2:: GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) per recuperare il nome del file di risposta e leggerne direttamente il contenuto.</span><span class="sxs-lookup"><span data-stu-id="da76b-112">If the reply data exceeds 1 MB, the application must call the [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) method to retrieve the name of the reply file and read its contents directly.</span></span>

-   [<span data-ttu-id="da76b-113">**IBackgroundCopyJob2::GetReplyFileName**</span><span class="sxs-lookup"><span data-stu-id="da76b-113">**IBackgroundCopyJob2::GetReplyFileName**</span></span>](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    <span data-ttu-id="da76b-114">Fornisce il nome del file che contiene la risposta.</span><span class="sxs-lookup"><span data-stu-id="da76b-114">Provides the name of the file that contains the reply.</span></span> <span data-ttu-id="da76b-115">È necessario chiamare il metodo **Metodo ibackgroundcopyjob:: complete** prima di aprire e leggere il file di risposta. il file di risposta non è disponibile per il client fino a quando non viene chiamato il metodo **completo** .</span><span class="sxs-lookup"><span data-stu-id="da76b-115">You must call the **IBackgroundCopyJob::Complete** method before opening and reading the reply file; the reply file is not available to the client until you call the **Complete** method.</span></span>

<span data-ttu-id="da76b-116">Chiamare questi metodi nel metodo [**IBackgroundCopyCallback:: JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) solo se la risposta è di dimensioni ridotte e può essere elaborata rapidamente in modo da non bloccare il thread di callback.</span><span class="sxs-lookup"><span data-stu-id="da76b-116">Call these methods in your [**IBackgroundCopyCallback::JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) method only if the reply is small and can be processed quickly so as to not block the callback thread.</span></span> <span data-ttu-id="da76b-117">Se invece del callback si utilizza la [**notifica della riga di comando**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) , passare l'identificatore del processo al file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="da76b-117">If you use [**command line notification**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) instead of the callback, pass the job identifier to the executable file.</span></span> <span data-ttu-id="da76b-118">Il file eseguibile usa l'identificatore del processo per chiamare il metodo **completo** per rendere disponibile il file di risposta.</span><span class="sxs-lookup"><span data-stu-id="da76b-118">The executable file uses the job identifier to call the **Complete** method to make the reply file available.</span></span>

<span data-ttu-id="da76b-119">Gli esempi seguenti illustrano come usare ogni metodo per recuperare i dati di risposta.</span><span class="sxs-lookup"><span data-stu-id="da76b-119">The following examples show how to use each method to retrieve the reply data.</span></span>

-   [<span data-ttu-id="da76b-120">Uso di GetReplyData</span><span class="sxs-lookup"><span data-stu-id="da76b-120">Using GetReplyData</span></span>](#using-getreplydata)
-   [<span data-ttu-id="da76b-121">Uso di GetReplyFileName</span><span class="sxs-lookup"><span data-stu-id="da76b-121">Using GetReplyFileName</span></span>](#using-getreplyfilename)

## <a name="using-getreplydata"></a><span data-ttu-id="da76b-122">Uso di GetReplyData</span><span class="sxs-lookup"><span data-stu-id="da76b-122">Using GetReplyData</span></span>

<span data-ttu-id="da76b-123">Nell'esempio seguente viene illustrato come recuperare i dati di risposta utilizzando il metodo [**IBackgroundCopyJob2:: GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) .</span><span class="sxs-lookup"><span data-stu-id="da76b-123">The following example shows how to retrieve the reply data using the [**IBackgroundCopyJob2::GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) method.</span></span> <span data-ttu-id="da76b-124">Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido, che il tipo di processo sia upload-Reply e che lo stato del processo sia BG \_ processo \_ stato \_ trasferito.</span><span class="sxs-lookup"><span data-stu-id="da76b-124">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid, the type of the job is upload-reply, and the state of the job is BG\_JOB\_STATE\_TRANSFERRED.</span></span>


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



## <a name="using-getreplyfilename"></a><span data-ttu-id="da76b-125">Uso di GetReplyFileName</span><span class="sxs-lookup"><span data-stu-id="da76b-125">Using GetReplyFileName</span></span>

<span data-ttu-id="da76b-126">Nell'esempio seguente viene illustrato come recuperare i dati di risposta utilizzando il metodo [**IBackgroundCopyJob2:: GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) .</span><span class="sxs-lookup"><span data-stu-id="da76b-126">The following example shows how to retrieve the reply data using the [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) method.</span></span> <span data-ttu-id="da76b-127">Nell'esempio si presuppone che il puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) sia valido, che il tipo di processo sia upload-Reply e che lo stato del processo sia lo \_ stato del processo BG \_ \_ trasferito.</span><span class="sxs-lookup"><span data-stu-id="da76b-127">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid, the type of job is upload-reply, and the state of the job is BG\_JOB\_STATE\_TRANSFERRED.</span></span>


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



 

 




