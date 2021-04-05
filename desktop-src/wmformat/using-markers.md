---
title: Uso dei marcatori
description: Uso dei marcatori
ms.assetid: b801c985-4ec7-441e-9f8a-40c69b1299a9
keywords:
- Windows Media Format SDK, marcatori
- Advanced Systems Format (ASF), marcatori
- ASF (formato avanzato dei sistemi), marcatori
- Formato di sistemi avanzati (ASF), ricerca di marcatori
- ASF (formato avanzato dei sistemi), ricerca di marcatori
- marcatori, informazioni
- marcatori, aggiunta
- marcatori, rimozione
- marcatori, recupero
- marcatori, ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cc585b8c71e3bfbae85953650809ad031d36a2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724116"
---
# <a name="using-markers"></a><span data-ttu-id="be984-113">Uso dei marcatori</span><span class="sxs-lookup"><span data-stu-id="be984-113">Using Markers</span></span>

<span data-ttu-id="be984-114">Un *marcatore* è un punto denominato all'interno di un file ASF.</span><span class="sxs-lookup"><span data-stu-id="be984-114">A *marker* is a named point within an ASF file.</span></span> <span data-ttu-id="be984-115">Ogni marcatore è costituito da un nome e da un orario associato, misurato come offset dall'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="be984-115">Each marker consists of a name and an associated time, measured as an offset from the start of the file.</span></span> <span data-ttu-id="be984-116">Un'applicazione può usare i marcatori per assegnare nomi a diversi punti all'interno del contenuto, visualizzare i nomi dell'utente e quindi cercare le posizioni del marcatore.</span><span class="sxs-lookup"><span data-stu-id="be984-116">An application can use markers to assign names to various points within the content, display those names to the user, and then seek to the marker positions.</span></span> <span data-ttu-id="be984-117">Un'applicazione può aggiungere o rimuovere marcatori da un file ASF esistente.</span><span class="sxs-lookup"><span data-stu-id="be984-117">An application can add or remove markers from an existing ASF file.</span></span>

<span data-ttu-id="be984-118">L'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) contiene i metodi per lavorare con i marcatori.</span><span class="sxs-lookup"><span data-stu-id="be984-118">The [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface contains methods for working with markers.</span></span> <span data-ttu-id="be984-119">L'oggetto dell'editor di metadati supporta l'aggiunta e la rimozione di marcatori.</span><span class="sxs-lookup"><span data-stu-id="be984-119">The metadata editor object supports adding and removing markers.</span></span> <span data-ttu-id="be984-120">Gli oggetti writer e Reader possono recuperare i marcatori ma non possono aggiungere o rimuovere marcatori.</span><span class="sxs-lookup"><span data-stu-id="be984-120">The writer and reader objects can retrieve markers but cannot add or remove markers.</span></span>

## <a name="adding-markers"></a><span data-ttu-id="be984-121">Aggiunta di marcatori</span><span class="sxs-lookup"><span data-stu-id="be984-121">Adding Markers</span></span>

<span data-ttu-id="be984-122">Per aggiungere un marcatore, eseguire una query sull'editor dei metadati per l'interfaccia **IWMHeaderInfo** .</span><span class="sxs-lookup"><span data-stu-id="be984-122">To add a marker, query the metadata editor for the **IWMHeaderInfo** interface.</span></span> <span data-ttu-id="be984-123">Chiamare quindi il metodo [**IWMHeaderInfo:: AddMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) , specificando il nome del marcatore come stringa di caratteri wide e l'ora in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="be984-123">Then call the [**IWMHeaderInfo::AddMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) method, specifying the marker name as a wide-character string and the time in 100-nanosecond units.</span></span> <span data-ttu-id="be984-124">Il tempo non deve superare la durata del file.</span><span class="sxs-lookup"><span data-stu-id="be984-124">The time must not exceed the file duration.</span></span> <span data-ttu-id="be984-125">Due marcatori possono avere la stessa ora.</span><span class="sxs-lookup"><span data-stu-id="be984-125">Two markers can have the same time.</span></span>

<span data-ttu-id="be984-126">Nell'esempio seguente vengono aggiunti diversi marcatori a un file:</span><span class="sxs-lookup"><span data-stu-id="be984-126">The following example adds several markers to a file:</span></span>


```C++
IWMMetadataEditor *pEdit = 0;
IWMHeaderInfo     *pInfo = 0;

// Create the metadata editor object.

WMCreateEditor(&pEdit);
pEdit->Open(L"C:\\example.wmv");
pEdit->QueryInterface(IID_IWMHeaderInfo, (void**)&pInfo);

// Add the markers. Note that we add the last ones first. Do this when possible
// for improved performance when writing the markers to the file.
hr = pInfo->AddMarker(L"End",  520000000);   // 52 sec.
hr = pInfo->AddMarker(L"Segue",  350000000); // 35 sec.
hr = pInfo->AddMarker(L"Intro",  15000000);  // 1.5 sec.

// Commit changes and clean up.

pEdit->Flush();
pEdit->Close(); 
pInfo->Release();
pEdit->Release();

```



## <a name="removing-markers"></a><span data-ttu-id="be984-127">Rimozione di marcatori</span><span class="sxs-lookup"><span data-stu-id="be984-127">Removing Markers</span></span>

<span data-ttu-id="be984-128">Per rimuovere un marcatore, chiamare [**IWMHeaderInfo:: RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker), specificando l'indice del marcatore da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="be984-128">To remove a marker, call [**IWMHeaderInfo::RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker), specifying the index of the marker to remove.</span></span> <span data-ttu-id="be984-129">I marcatori vengono ordinati automaticamente in ordine di tempo crescente, pertanto l'indice 0 è sempre il primo marcatore.</span><span class="sxs-lookup"><span data-stu-id="be984-129">Markers are automatically sorted in increasing time order, so index 0 is always the first marker.</span></span> <span data-ttu-id="be984-130">Si noti che la chiamata a **RemoveMarker** modifica i numeri di indice di tutti i marcatori che seguono.</span><span class="sxs-lookup"><span data-stu-id="be984-130">Note that calling **RemoveMarker** changes the index numbers of any markers that follow.</span></span> <span data-ttu-id="be984-131">Il codice seguente, in cui *pInfo* è un puntatore a un'interfaccia **IWMHeaderInfo** , rimuove tutti i marcatori da un file:</span><span class="sxs-lookup"><span data-stu-id="be984-131">The following code, where *pInfo* is a pointer to an **IWMHeaderInfo** interface, removes all the markers from a file:</span></span>


```C++
WORD count = 0;
pInfo->GetMarkerCount(&count);
while (count--)
{
    pInfo->RemoveMarker(0);
}

```



## <a name="retrieving-markers"></a><span data-ttu-id="be984-132">Recupero di marcatori</span><span class="sxs-lookup"><span data-stu-id="be984-132">Retrieving Markers</span></span>

<span data-ttu-id="be984-133">Per recuperare il nome e l'ora di un marcatore, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="be984-133">To retrieve the name and time of a marker, perform the following steps:</span></span>

1.  <span data-ttu-id="be984-134">Chiamare il metodo [**IWMHeaderInfo:: GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) per determinare il numero di marcatori contenuti nel file.</span><span class="sxs-lookup"><span data-stu-id="be984-134">Call the [**IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) method to determine how many markers the file contains.</span></span>
2.  <span data-ttu-id="be984-135">Recuperare le dimensioni della stringa necessaria per contenere il nome del marcatore.</span><span class="sxs-lookup"><span data-stu-id="be984-135">Retrieve the size of the string needed to contain the marker name.</span></span> <span data-ttu-id="be984-136">A tale scopo, chiamare il metodo [**IWMHeaderInfo:: Getmarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) .</span><span class="sxs-lookup"><span data-stu-id="be984-136">To do so, call the [**IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) method.</span></span> <span data-ttu-id="be984-137">Specificare l'indice del marcatore da recuperare e **null** per il buffer di stringa (il parametro *pwszMarkerName* ).</span><span class="sxs-lookup"><span data-stu-id="be984-137">Specify the index of the marker to retrieve, and **NULL** for the string buffer (the *pwszMarkerName* parameter).</span></span> <span data-ttu-id="be984-138">Il metodo restituisce la lunghezza della stringa, incluso il carattere di terminazione ' \\ 0', nel parametro *pcchMarkerNameLen* .</span><span class="sxs-lookup"><span data-stu-id="be984-138">The method returns the length of the string, including the terminating '\\0' character, in the *pcchMarkerNameLen* parameter.</span></span>
3.  <span data-ttu-id="be984-139">Allocare una stringa di caratteri wide per ricevere il nome.</span><span class="sxs-lookup"><span data-stu-id="be984-139">Allocate a wide-character string to receive the name.</span></span>
4.  <span data-ttu-id="be984-140">Chiamare nuovamente **Getmarker** , ma questa volta passare l'indirizzo della stringa nel parametro *pwszMarkerName* .</span><span class="sxs-lookup"><span data-stu-id="be984-140">Call **GetMarker** again, but this time pass the address of the string in the *pwszMarkerName* parameter.</span></span> <span data-ttu-id="be984-141">Il metodo scrive il nome del marcatore nella stringa e restituisce l'ora del marcatore nel parametro *pcnsMarkerTime* .</span><span class="sxs-lookup"><span data-stu-id="be984-141">The method writes the marker name into the string, and returns the marker time in the *pcnsMarkerTime* parameter.</span></span>

<span data-ttu-id="be984-142">Il codice seguente esegue il ciclo di ogni marcatore in ordine e recupera il nome e l'ora:</span><span class="sxs-lookup"><span data-stu-id="be984-142">The following code loops through every marker in order and retrieves the name and time:</span></span>


```C++
WORD cMarkers = 0;
HRESULT hr = pInfo->GetMarkerCount(&cMarkers);

WCHAR *wszName = 0;
WORD  len = 0;
for (WORD iMarker = 0; iMarker < cMarkers; ++iMarker)
{
    QWORD rtTime = 0;
    WORD req_len = 0;
    hr = pInfo->GetMarker(iMarker, 0, &req_len, &rtTime);
    
    // Reallocate if necessary.
    if (len < req_len)
    {
        delete[] wszName;
        wszName = new WCHAR[req_len];
        len = req_len;
    }
    hr = pInfo->GetMarker(iMarker, wszName, &req_len, &rtTime);
    // Display the name...
}
delete[] wszName;

```



## <a name="seeking-to-a-marker"></a><span data-ttu-id="be984-143">Ricerca di un marcatore</span><span class="sxs-lookup"><span data-stu-id="be984-143">Seeking to a Marker</span></span>

<span data-ttu-id="be984-144">Per avviare la riproduzione da una posizione del marcatore, chiamare il metodo [**IWMReaderAdvanced2:: StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) dell'oggetto Reader, specificando l'indice del marcatore.</span><span class="sxs-lookup"><span data-stu-id="be984-144">To start playback from a marker location, call the reader object's [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) method, specifying the index of the marker.</span></span> <span data-ttu-id="be984-145">I parametri rimanenti sono identici a quelli per il metodo [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) .</span><span class="sxs-lookup"><span data-stu-id="be984-145">The remaining parameters are identical to those for the [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) method.</span></span> <span data-ttu-id="be984-146">Nell'esempio seguente viene eseguita una query sul Reader per l'interfaccia [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) e viene eseguita la ricerca del primo marcatore.</span><span class="sxs-lookup"><span data-stu-id="be984-146">The following example queries the reader for the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface and seeks to the first marker.</span></span>


```C++
IWMReaderAdvanced2 *pReader2 = 0
WORD iMarkerIndex = 0;
hr = pReader->QueryInterface(IID_IWMReaderAdvanced2, (void**)&pReader2);
if (SUCCEEDED(hr))
{
    hr = pPlayer2->StartAtMarker(iMarkerIndex, 0, 1.0, 0);
    pPlayer2->Release();
}

```



## <a name="related-topics"></a><span data-ttu-id="be984-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="be984-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be984-148">**Interfaccia IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="be984-148">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="be984-149">**IWMReaderAdvanced2::StartAtMarker**</span><span class="sxs-lookup"><span data-stu-id="be984-149">**IWMReaderAdvanced2::StartAtMarker**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)
</dt> <dt>

[<span data-ttu-id="be984-150">**Utilizzo dei metadati**</span><span class="sxs-lookup"><span data-stu-id="be984-150">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




