---
title: Copia da CD con IWMPPlayerServices::setTaskPane
description: Copia da CD con IWMPPlayerServices::setTaskPane
ms.assetid: 0d3efb0e-e8f5-40e3-abb5-6ad22009a4eb
keywords:
- Windows Media Player, copia di CD
- Modello a oggetti di Windows Media Player, copia di CD
- modello a oggetti, copia di CD
- Controllo ActiveX di Windows Media Player, copia di CD
- Controllo ActiveX, copia di CD
- Controllo ActiveX Windows Media Player Mobile, copia di CD
- Windows Media Player Mobile, copia di CD
- Ripping del CD, interfaccia setTaskPane di IWMPPlayerServices
- ripping di CDs, interfaccia setTaskPane di IWMPPlayerServices
- Interfaccia setTaskPane di IWMPPlayerServices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfb1a09d67f310266ae4818bc0b594fe3b74d128
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104472382"
---
# <a name="ripping-by-using-iwmpplayerservicessettaskpane"></a><span data-ttu-id="d7e58-113">Estrazione tramite IWMPPlayerServices:: setTaskPane</span><span class="sxs-lookup"><span data-stu-id="d7e58-113">Ripping by Using IWMPPlayerServices::setTaskPane</span></span>

> [!Note]  
> <span data-ttu-id="d7e58-114">Questa sezione documenta una funzionalità dei controlli ActiveX Windows Media Player 9 e Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="d7e58-114">This section documents a feature of the Windows Media Player 9 Series and Windows Media Player 10 ActiveX controls.</span></span> <span data-ttu-id="d7e58-115">Si consiglia di usare l'interfaccia **IWMPCdromRip** con versioni successive.</span><span class="sxs-lookup"><span data-stu-id="d7e58-115">It is recommended that you use the **IWMPCdromRip** interface with later versions.</span></span> <span data-ttu-id="d7e58-116">Vedere [interfaccia IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).</span><span class="sxs-lookup"><span data-stu-id="d7e58-116">See [IWMPCdromRip Interface](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip).</span></span>

 

<span data-ttu-id="d7e58-117">È possibile utilizzare il controllo Windows Media Player 9 Series o versione successiva per copiare tracce di CD nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d7e58-117">You can use the Windows Media Player 9 Series or later control to copy CD tracks to the user's computer.</span></span> <span data-ttu-id="d7e58-118">Questo processo è denominato *estrazione*.</span><span class="sxs-lookup"><span data-stu-id="d7e58-118">This process is called *ripping*.</span></span> <span data-ttu-id="d7e58-119">A tale scopo, è necessario incorporare il controllo Media Player Windows in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="d7e58-119">To do this, you must embed the Windows Media Player control in remote mode.</span></span> <span data-ttu-id="d7e58-120">Per ulteriori informazioni sulla modalità remota, vedere [la pagina relativa alla comunicazione remota del controllo Media Player di Windows](remoting-the-windows-media-player-control.md).</span><span class="sxs-lookup"><span data-stu-id="d7e58-120">For more information about remote mode, see [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).</span></span>

<span data-ttu-id="d7e58-121">Per avviare il processo di strappo, chiamare [IWMPPlayerServices:: setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), passando il CopyFromCD? AutoCopy: valore *ID* per il parametro *bstrTaskPane* , dove *ID* è l'indice dell'unità CD da cui eseguire la copia.</span><span class="sxs-lookup"><span data-stu-id="d7e58-121">To start the ripping process, call [IWMPPlayerServices::setTaskPane](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerservices-settaskpane), passing the CopyFromCD?AutoCopy:*id* value for the *bstrTaskPane* parameter, where *id* is the index of the CD drive from which to copy.</span></span> <span data-ttu-id="d7e58-122">Questo indice corrisponde all'indice di un oggetto **CDROM** nell'interfaccia **IWMPCdromCollection** o dell'evento **CdromMediaChange** .</span><span class="sxs-lookup"><span data-stu-id="d7e58-122">This index corresponds to the index of a **Cdrom** object in the **IWMPCdromCollection** interface or the **CdromMediaChange** event.</span></span>

<span data-ttu-id="d7e58-123">Il codice di esempio seguente è una funzione che avvia il processo di estrazione di un CD dall'unità CD identificata dall'indice zero.</span><span class="sxs-lookup"><span data-stu-id="d7e58-123">The following example code is a function that starts the process of ripping a CD from the CD drive identified by index zero.</span></span> <span data-ttu-id="d7e58-124">La funzione usa la variabile membro seguente:</span><span class="sxs-lookup"><span data-stu-id="d7e58-124">The function uses the following member variable:</span></span>


```C++
CComPtr<IWMPPlayer4>  m_spPlayer;  // Smart pointer to IWMPPlayer4.

```



<span data-ttu-id="d7e58-125">Il codice seguente illustra il corpo della funzione:</span><span class="sxs-lookup"><span data-stu-id="d7e58-125">The following code shows the body of the function:</span></span>


```C++
HRESULT CMyApp::StartRip()
{
    CComPtr<IWMPPlayerApplication>  spPlayerApp;
    CComPtr<IWMPPlayerServices>     spPlayerServices;
    CComBSTR bstrParam;  // Contains the parameter string.

    ATLASSERT(m_spPlayer.p);

    HRESULT hr = m_spPlayer->QueryInterface(&spPlayerServices);

    if(SUCCEEDED(hr))
    {
        // Create the parameter string.
        hr = bstrParam.Append(_T("CopyFromCD?AutoCopy:0"));
    }

    if(SUCCEEDED(hr))
    {
        // Rip the CD in drive 0.
        hr = spPlayerServices->setTaskPane(bstrParam);
    }

    return hr;
}

```



<span data-ttu-id="d7e58-126">Visualizzazione dello stato dell'utente</span><span class="sxs-lookup"><span data-stu-id="d7e58-126">Displaying Status to the User</span></span>

<span data-ttu-id="d7e58-127">Quando si esegue la copia da un CD, è possibile recuperare una stringa contenente informazioni sullo stato relative all'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="d7e58-127">When copying from a CD, you can retrieve a string containing status information about the copy operation.</span></span> <span data-ttu-id="d7e58-128">A tale scopo, è necessario innanzitutto recuperare una playlist contenente elementi multimediali che rappresentano le tracce CD chiamando [IWMPCdrom:: Get \_ playlist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist).</span><span class="sxs-lookup"><span data-stu-id="d7e58-128">To do this, you must first retrieve a playlist containing media items that represent the CD tracks by calling [IWMPCdrom::get\_playlist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdrom-get_playlist).</span></span> <span data-ttu-id="d7e58-129">Come nell'esempio precedente, il codice di esempio seguente funziona con l'indice di unità CD zero.</span><span class="sxs-lookup"><span data-stu-id="d7e58-129">Like the previous example, the following example code works with CD drive index zero.</span></span> <span data-ttu-id="d7e58-130">Archivia la playlist recuperata nella variabile membro seguente:</span><span class="sxs-lookup"><span data-stu-id="d7e58-130">It stores the retrieved playlist in the following member variable:</span></span>


```C++
CComPtr<IWMPPlaylist>  m_spCDPlaylist;

```



<span data-ttu-id="d7e58-131">Il codice seguente illustra il corpo della funzione:</span><span class="sxs-lookup"><span data-stu-id="d7e58-131">The following code shows the body of the function:</span></span>


```C++
HRESULT CMyApp::GetCDPlaylist()
{
    HRESULT hr = S_OK;

    // Release any existing playlist instance.
    m_spCDPlaylist.Release();

    CComPtr<IWMPCdromCollection> spCDDrives;
    CComPtr<IWMPCdrom>  spDrive;
    long lCount = 0;  // Count of CD drives.

    ATLASSERT(m_spPlayer);

    hr = m_spPlayer->get_cdromCollection(&spCDDrives);

    // Test to make sure there is at least one drive.
    if(SUCCEEDED(hr))
    {
        hr = spCDDrives->get_count(&lCount);
    }

    if(SUCCEEDED(hr) && lCount < 1)
    {
        MessageBox(_T("No CD drive detected"), 
                   _T("CD Rip Error"), MB_OK);
        hr = NS_E_CD_READ_ERROR;
    }

    if(SUCCEEDED(hr))
    {
        // Retrieve the first drive.
        hr = spCDDrives->item(0, &spDrive);
    }
    
    if(SUCCEEDED(hr))
    {
        // Get the playlist.
        hr = spDrive->get_playlist(&m_spCDPlaylist);
    }
   
    return hr;
}

```



<span data-ttu-id="d7e58-132">Quindi, gestire l'evento [IWMPEvents:: MediaChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) .</span><span class="sxs-lookup"><span data-stu-id="d7e58-132">Next, handle the [IWMPEvents::MediaChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-mediachange) event.</span></span> <span data-ttu-id="d7e58-133">Questo evento si verifica quando viene rilevata una traccia del CD.</span><span class="sxs-lookup"><span data-stu-id="d7e58-133">This event occurs when a CD track is being ripped.</span></span> <span data-ttu-id="d7e58-134">Il puntatore **IDispatch** passato al gestore eventi punta all'interfaccia **IWMPMedia** per la traccia del CD. Chiamare **QueryInterface** tramite **IDispatch** per recuperare il puntatore a **IWMPMedia**.</span><span class="sxs-lookup"><span data-stu-id="d7e58-134">The **IDispatch** pointer passed to the event handler points to the **IWMPMedia** interface for the CD track. Call **QueryInterface** through **IDispatch** to retrieve the pointer to **IWMPMedia**.</span></span>

<span data-ttu-id="d7e58-135">Per individuare la traccia del CD da estrarre, confrontare il puntatore **IWMPMedia** dall'evento con gli elementi multimediali nella playlist CD chiamando [IWMPMedia:: Get \_ identico](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).</span><span class="sxs-lookup"><span data-stu-id="d7e58-135">To detect which CD track is being ripped, compare the **IWMPMedia** pointer from the event to the media items in the CD playlist by calling [IWMPMedia::get\_isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-get_isidentical).</span></span>

<span data-ttu-id="d7e58-136">Chiamare [IWMPMedia:: GetItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), passando la stringa "status" come nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="d7e58-136">Call [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo), passing the string "Status" as the item name.</span></span> <span data-ttu-id="d7e58-137">**Lo stato** è un attributo temporaneo impostato da Windows Media Player su elementi multimediali mentre vengono ricopiati dal CD; non è disponibile dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="d7e58-137">**Status** is a temporary attribute set by Windows Media Player on media items while they are being ripped from CD; it is not available from the library.</span></span>

<span data-ttu-id="d7e58-138">Il codice di esempio seguente mostra un gestore dell'evento **MediaChange** .</span><span class="sxs-lookup"><span data-stu-id="d7e58-138">The following example code shows a **MediaChange** event handler.</span></span>


```C++
void CMyApp::MediaChange(IDispatch * Item)
{
    // Test whether the CD playlist exists.
    if(!m_spCDPlaylist)
    {
        return;
    }

    // Declare and initialize variables.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = S_OK;
    VARIANT_BOOL vbIdentical = VARIANT_FALSE;
    CComBSTR bstrVal;
    CComBSTR bstrName;
    long lCount = 0;  

    // Create the attribute value string.
    hr = bstrName.Append(_T("Status"));

    if(SUCCEEDED(hr))
    { 
        // Retrieve the IWMPMedia pointer from IDispatch.
        hr = Item->QueryInterface(__uuidof(IWMPMedia),(void**)&spMedia);
    }

    if(SUCCEEDED(hr))
    {
        // Get the value of the Status attribute.
        hr = spMedia->getItemInfo(bstrName, &bstrVal);
    }

    if(SUCCEEDED(hr))
    {
        // If the attribute is empty, set a failure code
        // to simply exit the function.
        if(bstrVal.Length() == 0)
        {
            hr = E_PENDING;
        }
    }
      
    if(SUCCEEDED(hr))
    {
        // Retrieve the count of items in the CD playlist.
        hr = m_spCDPlaylist->get_count(&lCount);
    }

    if(lCount < 1)
    {
        // Exit if the playlist is empty.
        hr = E_PENDING;
    }    

    if(SUCCEEDED(hr) && spMedia)
    {
        // Iterate through the playlist.
        // Compare the media item that raised the event
        // to each CD track. This detects which track
        // has a new status.
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spTrack;

            // Retrieve the CD track as a media object.
            hr = m_spCDPlaylist->get_item(i, &spTrack);

            if(SUCCEEDED(hr))
            {
                // Do the comparison.
                hr = spMedia->get_isIdentical(spTrack, &vbIdentical);
            }

            if(SUCCEEDED(hr) && VARIANT_TRUE == vbIdentical)
            {
                 // spTrack represents a track with changed status.
                 // bstrVal contains a status string. For example:
                 // "Ripping (10%)"
                 //
                 // TODO: Retrieve metadata about the track, and then
                 // display the status to the user.
            }
        }
    }

    return;
}

```



## <a name="related-topics"></a><span data-ttu-id="d7e58-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7e58-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7e58-140">**Interfaccia IWMPCdrom**</span><span class="sxs-lookup"><span data-stu-id="d7e58-140">**IWMPCdrom Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[<span data-ttu-id="d7e58-141">**Interfaccia IWMPCdromCollection**</span><span class="sxs-lookup"><span data-stu-id="d7e58-141">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[<span data-ttu-id="d7e58-142">**Interfaccia IWMPEvents**</span><span class="sxs-lookup"><span data-stu-id="d7e58-142">**IWMPEvents Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> <dt>

[<span data-ttu-id="d7e58-143">**Interfaccia IWMPMedia**</span><span class="sxs-lookup"><span data-stu-id="d7e58-143">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="d7e58-144">**Interfaccia IWMPPlayerServices**</span><span class="sxs-lookup"><span data-stu-id="d7e58-144">**IWMPPlayerServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
</dt> <dt>

[<span data-ttu-id="d7e58-145">**Interfaccia IWMPPlaylist**</span><span class="sxs-lookup"><span data-stu-id="d7e58-145">**IWMPPlaylist Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[<span data-ttu-id="d7e58-146">**Guida al controllo del lettore**</span><span class="sxs-lookup"><span data-stu-id="d7e58-146">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> <dt>

[<span data-ttu-id="d7e58-147">**Ripping mediante l'interfaccia IWMPCdromRip**</span><span class="sxs-lookup"><span data-stu-id="d7e58-147">**Ripping by Using the IWMPCdromRip Interface**</span></span>](ripping-by-using-the-iwmpcdromrip-interface.md)
</dt> </dl>

 

 




