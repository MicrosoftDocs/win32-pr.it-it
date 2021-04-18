---
title: Masterizzazione di playlist contenenti file protetti
description: Masterizzazione di playlist contenenti file protetti
ms.assetid: 0d9415a1-a154-4fe4-af4c-cce4cb05ade5
keywords:
- Windows Media Format SDK, masterizzare playlist con file protetti
- Windows Media Format SDK, playlist con file protetti
- ASF (Advanced Systems Format), masterizzazione di playlist con file protetti
- ASF (Advanced Systems Format), masterizzazione di playlist con file protetti
- ASF (Advanced Systems Format), playlist con file protetti
- ASF (Advanced Systems Format), playlist con file protetti
- Digital Rights Management (DRM), masterizzare playlist con file protetti
- DRM (Digital Rights Management), masterizzare playlist con file protetti
- Digital Rights Management (DRM), playlist con file protetti
- DRM (Digital Rights Management), playlist con file protetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 214c1dbd4ee08f90b3e5e8aa6186508af5044f29
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "106299502"
---
# <a name="burning-playlists-that-contain-secure-files"></a><span data-ttu-id="19279-113">Masterizzazione di playlist contenenti file protetti</span><span class="sxs-lookup"><span data-stu-id="19279-113">Burning Playlists That Contain Secure Files</span></span>

<span data-ttu-id="19279-114">Le licenze create con gli oggetti di Windows Media Rights Manager 10 SDK possono specificare il diritto di copiare un file in Compact disk come parte di una playlist.</span><span class="sxs-lookup"><span data-stu-id="19279-114">Licenses created by using the objects of the Windows Media Rights Manager 10 SDK can specify the right to copy a file to compact disc as part of a playlist.</span></span> <span data-ttu-id="19279-115">Questa funzionalità, denominata playlist Burning, richiede la verifica delle licenze di tutti i file nella playlist prima di iniziare a copiare i dati.</span><span class="sxs-lookup"><span data-stu-id="19279-115">This feature, called playlist burning, requires that you verify the licenses of all of the files in the playlist before starting to copy data.</span></span> <span data-ttu-id="19279-116">Windows Media Format SDK fornisce l'interfaccia [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) per eseguire la verifica dei file.</span><span class="sxs-lookup"><span data-stu-id="19279-116">The Windows Media Format SDK provides the [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) interface to perform file verification for you.</span></span>

<span data-ttu-id="19279-117">Per implementare la masterizzazione della playlist, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="19279-117">To implement playlist burning, perform the following steps:</span></span>

1.  <span data-ttu-id="19279-118">Creare un'istanza dell'oggetto Reader o l'oggetto Reader sincrono.</span><span class="sxs-lookup"><span data-stu-id="19279-118">Create an instance of the reader object, or the synchronous reader object.</span></span> <span data-ttu-id="19279-119">Per ulteriori informazioni, vedere la pagina relativa alla [lettura di file ASF](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="19279-119">For more information, see [Reading ASF Files](reading-asf-files.md).</span></span>
2.  <span data-ttu-id="19279-120">Chiamare il metodo **QueryInterface** dell'interfaccia Reader ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) o [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) per ottenere un puntatore all'interfaccia [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) .</span><span class="sxs-lookup"><span data-stu-id="19279-120">Call the **QueryInterface** method of the reader interface ([**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader) or [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)) to obtain a pointer to the [**IWMReaderPlaylistBurn**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderplaylistburn) interface.</span></span>
3.  <span data-ttu-id="19279-121">Copiare i nomi dei file dalla playlist in una matrice di stringhe a caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="19279-121">Copy the file names from the playlist into an array of wide-character strings.</span></span> <span data-ttu-id="19279-122">I nomi di file nella matrice devono essere nello stesso ordine in cui compaiono nella playlist.</span><span class="sxs-lookup"><span data-stu-id="19279-122">The file names in the array must be in the same order as they appear in the playlist.</span></span>
4.  <span data-ttu-id="19279-123">Chiamare il metodo [**IWMReaderPlaylistBurn:: InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) , passando un puntatore alla matrice creata nel passaggio 3, per inizializzare la verifica della licenza per i file.</span><span class="sxs-lookup"><span data-stu-id="19279-123">Call the [**IWMReaderPlaylistBurn::InitPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-initplaylistburn) method, passing in a pointer to the array created in step 3, to initialize the license verification for the files.</span></span>
5.  <span data-ttu-id="19279-124">Al termine della verifica della licenza, l'oggetto Reader Invia un \_ \_ \_ messaggio di masterizzazione della playlist WMT init all'implementazione del metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback.</span><span class="sxs-lookup"><span data-stu-id="19279-124">When the license verification is completed, the reader object sends a WMT\_INIT\_PLAYLIST\_BURN message to your implementation of the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="19279-125">Quando il callback riceve questo messaggio, chiamare il metodo [**IWMReaderPlaylistBurn:: GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) per ottenere i risultati del controllo della licenza.</span><span class="sxs-lookup"><span data-stu-id="19279-125">When your callback receives this message, call the [**IWMReaderPlaylistBurn::GetInitResults**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-getinitresults) method to get the results of the license check.</span></span> <span data-ttu-id="19279-126">Questo metodo accetta una matrice di variabili **HRESULT** che corrispondono ai nomi di file nella matrice passata a **InitPlaylistBurn**.</span><span class="sxs-lookup"><span data-stu-id="19279-126">This method takes an array of **HRESULT** variables that correspond to the file names in the array passed to **InitPlaylistBurn**.</span></span> <span data-ttu-id="19279-127">Se tutti i valori nella matrice di risultati sono uguali a S \_ OK, è possibile continuare.</span><span class="sxs-lookup"><span data-stu-id="19279-127">If all of the values in the result array are equal to S\_OK, you can continue.</span></span> <span data-ttu-id="19279-128">Se il risultato è un codice di errore, la playlist non deve essere copiata.</span><span class="sxs-lookup"><span data-stu-id="19279-128">If any result is an error code, the playlist must not be copied.</span></span>
6.  <span data-ttu-id="19279-129">Utilizzando la stessa istanza del lettore, aprire e leggere ogni file.</span><span class="sxs-lookup"><span data-stu-id="19279-129">Using the same instance of the reader, open and read each file.</span></span> <span data-ttu-id="19279-130">È necessario aprire i file nell'ordine in cui sono stati visualizzati i nomi dei file nella matrice di nomi di file passata a **InitPlaylistBurn**.</span><span class="sxs-lookup"><span data-stu-id="19279-130">You must open the files in the order in which the file names appeared in the file name array passed to **InitPlaylistBurn**.</span></span>
7.  <span data-ttu-id="19279-131">Dopo aver copiato tutti i file nella playlist, chiamare [**IWMReaderPlaylistBurn:: EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) per completare il processo di masterizzazione della playlist e liberare le risorse usate dal reader.</span><span class="sxs-lookup"><span data-stu-id="19279-131">When you have copied all of the files in the playlist, call the [**IWMReaderPlaylistBurn::EndPlaylistBurn**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderplaylistburn-endplaylistburn) to complete the playlist burn process and free the resources used by the reader.</span></span>

> [!Note]  
> <span data-ttu-id="19279-132">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="19279-132">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="19279-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="19279-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19279-134">**Abilitazione del supporto DRM**</span><span class="sxs-lookup"><span data-stu-id="19279-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




