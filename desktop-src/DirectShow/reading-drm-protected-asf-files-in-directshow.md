---
description: Questo argomento descrive come usare DirectShow per riprodurre file multimediali protetti con Windows Media Digital Rights Management (DRM).
ms.assetid: a014942a-01e5-49d4-8a25-4604cd40f374
title: Lettura di DRM-Protected file ASF in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3a90b61982d6c7c444ddcf53948c225b6fc685
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320843"
---
# <a name="reading-drm-protected-asf-files-in-directshow"></a><span data-ttu-id="b0b46-103">Lettura di DRM-Protected file ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b0b46-103">Reading DRM-Protected ASF Files in DirectShow</span></span>

<span data-ttu-id="b0b46-104">Questo argomento descrive come usare DirectShow per riprodurre file multimediali protetti con Windows Media Digital Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="b0b46-104">This topic describes how to use DirectShow to play media files that are protected with Windows Media Digital Rights Management (DRM).</span></span>

## <a name="drm-concepts"></a><span data-ttu-id="b0b46-105">Concetti relativi a DRM</span><span class="sxs-lookup"><span data-stu-id="b0b46-105">DRM Concepts</span></span>

<span data-ttu-id="b0b46-106">La protezione di un file multimediale con Windows Media DRM prevede due passaggi distinti:</span><span class="sxs-lookup"><span data-stu-id="b0b46-106">Protecting a media file with Windows Media DRM involves two distinct steps:</span></span>

-   <span data-ttu-id="b0b46-107">Il provider di contenuti esegue il pacchetto del file, ovvero crittografa il file e connette le informazioni sulle licenze all'intestazione del file ASF.</span><span class="sxs-lookup"><span data-stu-id="b0b46-107">The content provider packages the file—that is, encrypts the file and attaches licensing information to the ASF file header.</span></span> <span data-ttu-id="b0b46-108">Le informazioni sulle licenze includono un URL in cui il client può ottenere la licenza.</span><span class="sxs-lookup"><span data-stu-id="b0b46-108">The licensing information includes a URL where the client can obtain the license.</span></span>
-   <span data-ttu-id="b0b46-109">L'applicazione client acquisisce una licenza per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="b0b46-109">The client application acquires a license for the content.</span></span>

<span data-ttu-id="b0b46-110">Il pacchetto si verifica prima della distribuzione del file.</span><span class="sxs-lookup"><span data-stu-id="b0b46-110">Packaging happens before the file is distributed.</span></span> <span data-ttu-id="b0b46-111">L'acquisizione della licenza si verifica quando l'utente tenta di riprodurre o copiare il file.</span><span class="sxs-lookup"><span data-stu-id="b0b46-111">License acquisition occurs when the user tries to play or copy the file.</span></span> <span data-ttu-id="b0b46-112">L'acquisizione della licenza può essere *invisibile* all'utente o *non invisibile all'utente*.</span><span class="sxs-lookup"><span data-stu-id="b0b46-112">License acquisition may be either *silent* or *non-silent*.</span></span> <span data-ttu-id="b0b46-113">L'acquisizione invisibile all'utente non richiede alcuna interazione con l'utente.</span><span class="sxs-lookup"><span data-stu-id="b0b46-113">Silent acquisition does not require any interaction with the user.</span></span> <span data-ttu-id="b0b46-114">Per l'acquisizione non invisibile all'utente è necessario che l'applicazione apra una finestra del browser e visualizzi una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="b0b46-114">Non-silent acquisition requires the application to open a browser window and display a web page to the user.</span></span> <span data-ttu-id="b0b46-115">A questo punto, l'utente potrebbe dover fornire un tipo di informazioni al provider di contenuti.</span><span class="sxs-lookup"><span data-stu-id="b0b46-115">At that point, the user might need to provide some kind of information to the content provider.</span></span> <span data-ttu-id="b0b46-116">Tuttavia, entrambi i tipi di acquisizione della licenza richiedono che il client invii una richiesta HTTP a un server licenze.</span><span class="sxs-lookup"><span data-stu-id="b0b46-116">However, both types of license acquisition require the client to submit an HTTP request to a license server.</span></span>

### <a name="drm-versions"></a><span data-ttu-id="b0b46-117">Versioni DRM</span><span class="sxs-lookup"><span data-stu-id="b0b46-117">DRM Versions</span></span>

<span data-ttu-id="b0b46-118">Sono presenti diverse versioni di Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="b0b46-118">Several versions of Windows Media DRM exist.</span></span> <span data-ttu-id="b0b46-119">Dal punto di vista di un'applicazione client, possono essere raggruppate in due categorie: DRM versione 1 e DRM versione 7 o successiva.</span><span class="sxs-lookup"><span data-stu-id="b0b46-119">From the perspective of a client application, they can be grouped into two categories: DRM version 1, and DRM version 7 or later.</span></span> <span data-ttu-id="b0b46-120">La seconda categoria include le versioni 9 e 10 di DRM, nonché la versione 7. Il motivo per la categorizzazione delle versioni DRM in questo modo è che le licenze della versione 1 sono gestite in modo diverso rispetto alle licenze della versione 7 o successive.</span><span class="sxs-lookup"><span data-stu-id="b0b46-120">(The second category includes DRM versions 9 and 10, as well as version 7.) The reason for categorizing DRM versions this way is that version 1 licenses are handled somewhat differently than version 7 or later licenses.</span></span> <span data-ttu-id="b0b46-121">In questa documentazione, il termine *licenza versione 7* indica la versione 7 o successiva.</span><span class="sxs-lookup"><span data-stu-id="b0b46-121">In this documentation, the term *version 7 license* means version 7 or later.</span></span>

<span data-ttu-id="b0b46-122">È anche importante distinguere la creazione di pacchetti DRM dalla licenza DRM.</span><span class="sxs-lookup"><span data-stu-id="b0b46-122">It is also important to distinguish the DRM packaging from the DRM license.</span></span> <span data-ttu-id="b0b46-123">Se il file è incluso in un pacchetto con Windows Media Rights Manager versione 7 o successiva, l'intestazione DRM può contenere un URL di licenza della versione 1 oltre all'URL della licenza della versione 7.</span><span class="sxs-lookup"><span data-stu-id="b0b46-123">If the file is packaged using Windows Media Rights Manager version 7 or later, the DRM header can contain a version 1 license URL in addition to the version 7 license URL.</span></span> <span data-ttu-id="b0b46-124">L'URL di licenza della versione 1 consente ai lettori meno recenti che non supportano la versione 7 di ottenere una licenza per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="b0b46-124">The version 1 license URL enables older players that do not support version 7 to obtain a license for the content.</span></span> <span data-ttu-id="b0b46-125">Tuttavia, il contrario non è vero, quindi un file con la confezione della versione 1 non può avere un URL di licenza della versione 7.</span><span class="sxs-lookup"><span data-stu-id="b0b46-125">However, the converse is not true, so a file with version 1 packaging cannot have a version 7 license URL.</span></span>

### <a name="application-security-level"></a><span data-ttu-id="b0b46-126">Livello di sicurezza dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="b0b46-126">Application Security Level</span></span>

<span data-ttu-id="b0b46-127">Per riprodurre file protetti da DRM, l'applicazione client deve essere collegata a una libreria statica fornita in formato binario da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b0b46-127">To play DRM-protected files, the client application must be linked to a static library that is provided in binary form by Microsoft.</span></span> <span data-ttu-id="b0b46-128">Questa libreria, che identifica in modo univoco l'applicazione, viene talvolta chiamata libreria stub.</span><span class="sxs-lookup"><span data-stu-id="b0b46-128">This library, which uniquely identifies the application, is sometimes called the stub library.</span></span> <span data-ttu-id="b0b46-129">Alla libreria stub è assegnato un livello di sicurezza, il cui valore è determinato dal contratto di licenza firmato quando si è ottenuta la libreria stub.</span><span class="sxs-lookup"><span data-stu-id="b0b46-129">The stub library has an assigned security level, the value of which is determined by the license agreement that you signed when you obtained the stub library.</span></span>

<span data-ttu-id="b0b46-130">Il provider di contenuti imposta un livello di sicurezza minimo necessario per acquisire la licenza.</span><span class="sxs-lookup"><span data-stu-id="b0b46-130">The content provider sets a minimum security level needed to acquire the license.</span></span> <span data-ttu-id="b0b46-131">Se il livello di sicurezza della libreria stub è inferiore al livello di sicurezza minimo richiesto dal server licenze, l'applicazione non è in grado di ottenere la licenza.</span><span class="sxs-lookup"><span data-stu-id="b0b46-131">If the security level of your stub library is less than the minimum security level required by the license server, the application cannot obtain the license.</span></span>

### <a name="individualization"></a><span data-ttu-id="b0b46-132">Individualizzazione</span><span class="sxs-lookup"><span data-stu-id="b0b46-132">Individualization</span></span>

<span data-ttu-id="b0b46-133">Per aumentare la sicurezza, un'applicazione può aggiornare i componenti DRM nel computer del client.</span><span class="sxs-lookup"><span data-stu-id="b0b46-133">To increase security, an application may update the DRM components on the client's computer.</span></span> <span data-ttu-id="b0b46-134">Questo aggiornamento, denominato individualizzazione, distingue la copia dell'applicazione dell'utente da tutte le altre copie della stessa applicazione.</span><span class="sxs-lookup"><span data-stu-id="b0b46-134">This update, called individualization, differentiates the user's copy of the application from all other copies of the same application.</span></span> <span data-ttu-id="b0b46-135">È possibile che l'intestazione DRM di un file protetto specifichi un livello di individualizzazione minimo.</span><span class="sxs-lookup"><span data-stu-id="b0b46-135">The DRM header of a protected file may specify may specify a minimum individualization level.</span></span> <span data-ttu-id="b0b46-136">Per ulteriori informazioni, vedere la documentazione relativa a WMRMHeader. IndividualizedVersion in Windows Media Rights Manager SDK.</span><span class="sxs-lookup"><span data-stu-id="b0b46-136">(For more information, see the documentation for WMRMHeader.IndividualizedVersion in the Windows Media Rights Manager SDK.)</span></span>

<span data-ttu-id="b0b46-137">Poiché il servizio di individualizzazione Microsoft gestisce le informazioni dell'utente, è necessario visualizzare l'informativa sulla privacy di Microsoft o fornire un collegamento a tale pagina nel sito Web Microsoft prima dell'applicazione individua: <https://go.microsoft.com/fwlink/p/?linkid=10240> .</span><span class="sxs-lookup"><span data-stu-id="b0b46-137">Because the Microsoft Individualization Service handles information from the user, you must display the Microsoft privacy policy or provide a link to that page at the Microsoft website before your application individualizes: <https://go.microsoft.com/fwlink/p/?linkid=10240>.</span></span>

## <a name="provide-the-software-certificate"></a><span data-ttu-id="b0b46-138">Fornire il certificato software</span><span class="sxs-lookup"><span data-stu-id="b0b46-138">Provide the Software Certificate</span></span>

<span data-ttu-id="b0b46-139">Per consentire all'applicazione di utilizzare la licenza DRM, è necessario che l'applicazione fornisca una *chiave* o un certificato software al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="b0b46-139">To enable the application to use the DRM license, the application must provide a software certificate or *key* to the Filter Graph Manager.</span></span> <span data-ttu-id="b0b46-140">Questa chiave è contenuta in una libreria statica che viene personalizzata per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b0b46-140">This key is contained in a static library that is individualized for the application.</span></span> <span data-ttu-id="b0b46-141">Per informazioni su come ottenere la libreria personalizzata, vedere [ottenere la libreria DRM necessaria](../wmformat/obtaining-the-required-drm-library.md) nella documentazione di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="b0b46-141">For information about obtaining the individualized library, see [Obtaining the Required DRM Library](../wmformat/obtaining-the-required-drm-library.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="b0b46-142">Per fornire la chiave software, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="b0b46-142">To provide the software key, perform the following steps:</span></span>

1.  <span data-ttu-id="b0b46-143">Collegamento alla libreria statica.</span><span class="sxs-lookup"><span data-stu-id="b0b46-143">Link to the static library.</span></span>
2.  <span data-ttu-id="b0b46-144">Implementare l'interfaccia **IServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="b0b46-144">Implement the **IServiceProvider** interface.</span></span>
3.  <span data-ttu-id="b0b46-145">Eseguire una query su Filter Graph Manager per l'interfaccia [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) .</span><span class="sxs-lookup"><span data-stu-id="b0b46-145">Query the Filter Graph Manager for the [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite) interface.</span></span>
4.  <span data-ttu-id="b0b46-146">Chiamare [**IObjectWithSite:: SESITE**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) con un puntatore all'implementazione di **IServiceProvider**.</span><span class="sxs-lookup"><span data-stu-id="b0b46-146">Call [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) with a pointer to your implementation of **IServiceProvider**.</span></span>
5.  <span data-ttu-id="b0b46-147">Il gestore del grafico del filtro chiamerà **IServiceProvider:: QueryService**, specificando **IID \_ IWMReader** per l'identificatore del servizio.</span><span class="sxs-lookup"><span data-stu-id="b0b46-147">The Filter Graph Manager will call **IServiceProvider::QueryService**, specifying **IID\_IWMReader** for the service identifier.</span></span>
6.  <span data-ttu-id="b0b46-148">Nell'implementazione di **QueryService**, chiamare [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) per creare la chiave software.</span><span class="sxs-lookup"><span data-stu-id="b0b46-148">In your implementation of **QueryService**, call [**WMCreateCertificate**](/previous-versions/windows/desktop/legacy/dd757745(v=vs.85)) to create the software key.</span></span>

<span data-ttu-id="b0b46-149">Nel codice seguente viene illustrato come implementare il metodo **QueryService** :</span><span class="sxs-lookup"><span data-stu-id="b0b46-149">The following code shows how to implement the **QueryService** method:</span></span>


```C++
STDMETHODIMP Player::QueryService(REFIID siid, REFIID riid, void **ppv)
{
    if (ppv == NULL ) 
    { 
        return E_POINTER; 
    }

    if (siid == __uuidof(IWMReader) && riid == __uuidof(IUnknown))
    {
        IUnknown *punkCert;

        HRESULT hr = WMCreateCertificate(&punkCert);

        if (SUCCEEDED(hr))
        {
            *ppv = (void *) punkCert;
        }

        return hr;
    }
    return E_NOINTERFACE;
}
```



<span data-ttu-id="b0b46-150">Nel codice riportato di seguito viene illustrato [**come chiamare il**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) metodo in gestione grafico dei filtri:</span><span class="sxs-lookup"><span data-stu-id="b0b46-150">The following code shows how to call [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) on the Filter Graph Manager:</span></span>


```C++
HRESULT Player::CreateFilterGraph()
{
    CComPtr<IObjectWithSite> pSite;

    HRESULT hr = pGraph.CoCreateInstance(CLSID_FilterGraph);

    if (FAILED(hr))
    {
        goto done;
    }

    // Register the application as a site (service).
    hr = pGraph->QueryInterface(&pSite);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSite->SetSite(this);


done:
    return hr;
}
```





## <a name="building-the-playback-graph"></a><span data-ttu-id="b0b46-151">Creazione del grafico di riproduzione</span><span class="sxs-lookup"><span data-stu-id="b0b46-151">Building the Playback Graph</span></span>

<span data-ttu-id="b0b46-152">Per riprodurre un file ASF protetto da DRM, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="b0b46-152">To play a DRM-protected ASF file, perform the following steps:</span></span>

1.  <span data-ttu-id="b0b46-153">Creare il [gestore del grafo del filtro](filter-graph-manager.md) e usare l'interfaccia [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) per registrare eventi Graph.</span><span class="sxs-lookup"><span data-stu-id="b0b46-153">Create the [Filter Graph Manager](filter-graph-manager.md) and use the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface to register for graph events.</span></span>
2.  <span data-ttu-id="b0b46-154">Chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare una nuova istanza del filtro [WM ASF Reader](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="b0b46-154">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a new instance of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>
3.  <span data-ttu-id="b0b46-155">Chiamare [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) per aggiungere il filtro al grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="b0b46-155">Call [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) to add the filter to the filter graph.</span></span>
4.  <span data-ttu-id="b0b46-156">Eseguire una query sul filtro per l'interfaccia [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) .</span><span class="sxs-lookup"><span data-stu-id="b0b46-156">Query the filter for the [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interface.</span></span>
5.  <span data-ttu-id="b0b46-157">Chiamare [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) con l'URL del file.</span><span class="sxs-lookup"><span data-stu-id="b0b46-157">Call [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) with the URL of the file.</span></span>
6.  <span data-ttu-id="b0b46-158">Gestisce gli eventi di [**\_ \_ evento WMT EC**](ec-wmt-event.md) .</span><span class="sxs-lookup"><span data-stu-id="b0b46-158">Handle [**EC\_WMT\_EVENT**](ec-wmt-event.md) events.</span></span>
7.  <span data-ttu-id="b0b46-159">Nel primo evento [**EC \_ WMT \_ evento**](ec-wmt-event.md) , eseguire una query sul filtro [WM ASF Reader](wm-asf-reader-filter.md) per l'interfaccia **IServiceProvider** .</span><span class="sxs-lookup"><span data-stu-id="b0b46-159">On the first [**EC\_WMT\_EVENT**](ec-wmt-event.md) event, query the [WM ASF Reader](wm-asf-reader-filter.md) filter for the **IServiceProvider** interface.</span></span>
8.  <span data-ttu-id="b0b46-160">Chiamare **IServiceProvider:: QueryService** per ottenere un puntatore all'interfaccia [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .</span><span class="sxs-lookup"><span data-stu-id="b0b46-160">Call **IServiceProvider::QueryService** to get a pointer to the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface.</span></span>
9.  <span data-ttu-id="b0b46-161">Chiamare [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) per eseguire il rendering dei pin di output del filtro [WM ASF Reader](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="b0b46-161">Call [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) to render the output pins of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>

> [!Note]  
> <span data-ttu-id="b0b46-162">Quando si apre un file protetto da DRM, non chiamare [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) per creare il grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="b0b46-162">When opening a DRM-protected file, do not call [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) to create the filter graph.</span></span> <span data-ttu-id="b0b46-163">Il filtro WM ASF Reader non è in grado di connettersi ad altri filtri fino a quando non viene acquistata la licenza DRM.</span><span class="sxs-lookup"><span data-stu-id="b0b46-163">The WM ASF Reader filter cannot connect to any other filters until the DRM license is acquired.</span></span> <span data-ttu-id="b0b46-164">Per questo passaggio è necessario che l'applicazione usi l'interfaccia [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) , che deve essere ottenuta dal filtro, come descritto nei passaggi 7-8.</span><span class="sxs-lookup"><span data-stu-id="b0b46-164">This step requires the application to use the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface, which must be obtained from the filter, as described in steps 7–8.</span></span> <span data-ttu-id="b0b46-165">Pertanto, è necessario creare il filtro e aggiungerlo al grafo</span><span class="sxs-lookup"><span data-stu-id="b0b46-165">Therefore, you must create the filter and add it to the graph</span></span>

 

> [!Note]  
> <span data-ttu-id="b0b46-166">È importante registrarsi per gli eventi Graph (passaggio 1) prima di aggiungere il filtro [WM ASF Reader](wm-asf-reader-filter.md) al grafo (passaggio 3), perché l'applicazione deve gestire gli eventi dell' [**\_ \_ evento EC WMT**](ec-wmt-event.md) .</span><span class="sxs-lookup"><span data-stu-id="b0b46-166">It is important to register for graph events (step 1) before adding the [WM ASF Reader](wm-asf-reader-filter.md) filter to the graph (step 3), because the application must handle the [**EC\_WMT\_EVENT**](ec-wmt-event.md) events.</span></span> <span data-ttu-id="b0b46-167">Gli eventi vengono inviati quando viene chiamato il metodo [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) (passaggio 5).</span><span class="sxs-lookup"><span data-stu-id="b0b46-167">The events are sent when [**Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) is called (step 5).</span></span>

 

<span data-ttu-id="b0b46-168">Nel codice seguente viene illustrato come compilare il grafico:</span><span class="sxs-lookup"><span data-stu-id="b0b46-168">The following code shows how to build the graph:</span></span>


```C++
HRESULT Player::LoadMediaFile(PCWSTR pwszFile)
{


    BOOL bIsWindowsMediaFile = IsWindowsMediaFile(pwszFile);

    HRESULT hr = S_OK;

    // If this is the first time opening the file, create the
    // filter graph and add the WM ASF Reader filter.

    if (m_DRM.State() == DRM_INITIAL)
    {
        hr = CreateFilterGraph();
        if (FAILED(hr))
        {
            goto done;
        }

        // Use special handling for Windows Media files.
        if (bIsWindowsMediaFile)
        {
            // Add the ASF Reader filter to the graph.
            hr = m_pReader.CoCreateInstance(CLSID_WMAsfReader);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pGraph->AddFilter(m_pReader, NULL);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = m_pReader->QueryInterface(&m_pFileSource);
            if (FAILED(hr))
            {
                goto done;
            }
        }
    }

    if (bIsWindowsMediaFile)
    {
            hr = m_pFileSource->Load(pwszFile, NULL);
```

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b0b46-169">C++</span><span class="sxs-lookup"><span data-stu-id="b0b46-169">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            if (FAILED(hr))
            {
                goto done;
            }
            hr = RenderOutputPins(pGraph, m_pReader);
    }
    else
    {
        // Not a Windows Media file, so just render the standard way.
        hr = pGraph->RenderFile(pwszFile, NULL);
    }

done:
    return hr;
}</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="b0b46-170">Nel codice precedente, la `RenderOutputPins` funzione enumera i pin di output sul filtro [WM ASF Reader](wm-asf-reader-filter.md) e chiama [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) per ogni pin.</span><span class="sxs-lookup"><span data-stu-id="b0b46-170">In the previous code, the `RenderOutputPins` function enumerates the output pins on the [WM ASF Reader](wm-asf-reader-filter.md) filter and calls [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) for each pin.</span></span>


```C++
HRESULT RenderOutputPins(IGraphBuilder *pGraph, IBaseFilter *pFilter)
{
    CComPtr<IEnumPins>  pEnumPin = NULL;
    CComPtr<IPin>       pConnectedPin;
    CComPtr<IPin>       pPin;

    // Enumerate all pins on the filter
    HRESULT hr = pFilter->EnumPins(&pEnumPin);
    if (FAILED(hr))
    {
        goto done;
    }

    // Step through every pin, looking for the output pins.
    while (S_OK == (hr = pEnumPin->Next(1, &pPin, NULL)))
    {
        // Skip connected pins.
        hr = pPin->ConnectedTo(&pConnectedPin);
        if (hr == VFW_E_NOT_CONNECTED)
        {
            PIN_DIRECTION PinDirection;
            hr = pPin->QueryDirection(&PinDirection);

            if ((S_OK == hr) && (PinDirection == PINDIR_OUTPUT))
            {
                hr = pGraph->Render(pPin);
            }
        }

        pConnectedPin.Release();
        pPin.Release();

        // If there was an error, stop enumerating.
        if (FAILED(hr))
        {
            break;
        }
    }

done:
    return hr;
}
```



<span data-ttu-id="b0b46-171">Il codice seguente illustra come ottenere un puntatore all'interfaccia [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) dal [lettore di WM ASF](wm-asf-reader-filter.md):</span><span class="sxs-lookup"><span data-stu-id="b0b46-171">The following code shows how to get a pointer to the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface from the [WM ASF Reader](wm-asf-reader-filter.md):</span></span>


```C++
HRESULT DrmManager::Initialize(IBaseFilter *pFilter)
{


    CComPtr<IServiceProvider> pService;
    CComPtr<IWMDRMReader> pDrmReader;

    HRESULT hr = pFilter->QueryInterface(&pService);
    if (SUCCEEDED(hr))
    {
        hr = pService->QueryService(
            __uuidof(IWMDRMReader), IID_PPV_ARGS(&m_pDrmReader));
    }
    return hr;
}
```





## <a name="related-topics"></a><span data-ttu-id="b0b46-172">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0b46-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0b46-173">Lettura di file ASF in DirectShow</span><span class="sxs-lookup"><span data-stu-id="b0b46-173">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
