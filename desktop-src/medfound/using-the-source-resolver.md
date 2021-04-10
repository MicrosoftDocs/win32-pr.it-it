---
description: Uso del resolver di origine
ms.assetid: 94e2a411-96b8-4506-8491-78f4f5f286ce
title: Uso del resolver di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e992199b097ff3f3337f92216b684d68e46bca13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226901"
---
# <a name="using-the-source-resolver"></a><span data-ttu-id="25cca-103">Uso del resolver di origine</span><span class="sxs-lookup"><span data-stu-id="25cca-103">Using the Source Resolver</span></span>

<span data-ttu-id="25cca-104">Il resolver dell'origine accetta un URL o un flusso di byte e crea l'origine multimediale appropriata per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="25cca-104">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span> <span data-ttu-id="25cca-105">Per creare il resolver di origine, chiamare [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver).</span><span class="sxs-lookup"><span data-stu-id="25cca-105">To create the source resolver, call [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver).</span></span> <span data-ttu-id="25cca-106">Questa funzione restituisce un puntatore di interfaccia [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) .</span><span class="sxs-lookup"><span data-stu-id="25cca-106">This function returns an [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface pointer.</span></span>

<span data-ttu-id="25cca-107">Il resolver di origine include metodi sincroni e asincroni.</span><span class="sxs-lookup"><span data-stu-id="25cca-107">The source resolver has both synchronous and asynchronous methods.</span></span> <span data-ttu-id="25cca-108">Se si usa il resolver di origine dal thread dell'applicazione principale, i metodi asincroni rendono più reattiva l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="25cca-108">If you are using the source resolver from your main application thread, the asynchronous methods will make your user interface more responsive.</span></span> <span data-ttu-id="25cca-109">I metodi sincroni possono bloccarsi per un periodo di tempo significativo, in particolare se il resolver di origine deve aprire una risorsa di rete.</span><span class="sxs-lookup"><span data-stu-id="25cca-109">The synchronous methods can block for a noticeable amount of time, particularly if the source resolver must open a network resource.</span></span>

<span data-ttu-id="25cca-110">I metodi sincroni sono:</span><span class="sxs-lookup"><span data-stu-id="25cca-110">The synchronous methods are:</span></span>

-   [<span data-ttu-id="25cca-111">**IMFSourceResolver::CreateObjectFromURL**</span><span class="sxs-lookup"><span data-stu-id="25cca-111">**IMFSourceResolver::CreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)
-   [<span data-ttu-id="25cca-112">**IMFSourceResolver::CreateObjectFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="25cca-112">**IMFSourceResolver::CreateObjectFromByteStream**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream)

<span data-ttu-id="25cca-113">I metodi asincroni sono:</span><span class="sxs-lookup"><span data-stu-id="25cca-113">The asynchronous methods are:</span></span>

-   [<span data-ttu-id="25cca-114">**IMFSourceResolver::BeginCreateObjectFromURL**</span><span class="sxs-lookup"><span data-stu-id="25cca-114">**IMFSourceResolver::BeginCreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)
-   [<span data-ttu-id="25cca-115">**IMFSourceResolver::BeginCreateObjectFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="25cca-115">**IMFSourceResolver::BeginCreateObjectFromByteStream**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)

<span data-ttu-id="25cca-116">Per i metodi asincroni, ogni metodo dispone di un metodo **end..** . corrispondente per completare la richiesta asincrona e un metodo **Cancel...** per annullare una richiesta in sospeso.</span><span class="sxs-lookup"><span data-stu-id="25cca-116">For the asynchronous methods, each method has a corresponding **End...** method to complete the asynchronous request, and a **Cancel...** method to cancel a pending request.</span></span> <span data-ttu-id="25cca-117">Per ulteriori informazioni sui metodi asincroni in Media Foundation, vedere [metodi di callback asincroni](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="25cca-117">For more information about asynchronous methods in Media Foundation, see [Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>

<span data-ttu-id="25cca-118">Nell'esempio di codice seguente viene creata un'origine multimediale da un URL.</span><span class="sxs-lookup"><span data-stu-id="25cca-118">The following code example creates a media source from a URL.</span></span> <span data-ttu-id="25cca-119">In questo esempio viene usato il metodo sincrono.</span><span class="sxs-lookup"><span data-stu-id="25cca-119">This example uses the synchronous method.</span></span>


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="25cca-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="25cca-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25cca-121">Resolver di origine</span><span class="sxs-lookup"><span data-stu-id="25cca-121">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



