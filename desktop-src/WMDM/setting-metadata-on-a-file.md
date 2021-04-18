---
title: Impostazione dei metadati in un file
description: Impostazione dei metadati in un file
ms.assetid: 478a5412-e8b4-41c8-802f-9c2748dbaeae
keywords:
- Windows Media Gestione dispositivi, metadati
- Gestione dispositivi, metadati
- Guida per programmatori, metadati
- applicazioni desktop, metadati
- creazione di applicazioni Windows Media Gestione dispositivi, metadati
- scrittura di file in dispositivi, metadati
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a6fa7002d4fafffe0793ef91b00dd3f1f0e20c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298271"
---
# <a name="setting-metadata-on-a-file"></a><span data-ttu-id="6085d-110">Impostazione dei metadati in un file</span><span class="sxs-lookup"><span data-stu-id="6085d-110">Setting Metadata on a File</span></span>

<span data-ttu-id="6085d-111">È possibile impostare i metadati in un file prima di scriverli nel dispositivo (quando si usa [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)) o in una risorsa di archiviazione esistente (chiamando [**IWMDMStorage3:: FileMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)).</span><span class="sxs-lookup"><span data-stu-id="6085d-111">You can set metadata on a file before writing it to the device (when using [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)) or on an existing storage (by calling [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)).</span></span> <span data-ttu-id="6085d-112">È possibile impostare gli attributi solo in una risorsa di archiviazione esistente (chiamando [**IWMDMStorage:: SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes) o [**IWMDMStorage2:: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)).</span><span class="sxs-lookup"><span data-stu-id="6085d-112">You can set attributes only on an existing storage (by calling [**IWMDMStorage::SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes) or [**IWMDMStorage2::SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)).</span></span>

<span data-ttu-id="6085d-113">L'impostazione dei metadati viene eseguita creando e riempiendo un'interfaccia [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) che viene passata in [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span><span class="sxs-lookup"><span data-stu-id="6085d-113">Setting metadata is done by creating and filling an [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) interface that is passed into [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span></span> <span data-ttu-id="6085d-114">Questo metodo, tuttavia, può cancellare tutti i metadati esistenti nel file, ad eccezione dei metadati hardcoded archiviati nel file system stesso, ad esempio il nome o la dimensione del file.</span><span class="sxs-lookup"><span data-stu-id="6085d-114">However, this method can clear all existing metadata on the file, other than hard-coded metadata stored in the file system itself, such as file name or size.</span></span> <span data-ttu-id="6085d-115">Pertanto, è necessario copiare tutti i metadati esistenti che si desidera mantenere nell'interfaccia IWMDMMetaData inviata.</span><span class="sxs-lookup"><span data-stu-id="6085d-115">Therefore, you must copy all existing metadata that you wish to retain into the IWMDMMetaData interface you submit.</span></span> <span data-ttu-id="6085d-116">Poiché non è possibile utilizzare Windows Media Gestione dispositivi per recuperare i metadati dai file locali, è necessario utilizzare Windows Media Format SDK (o un altro strumento) per recuperare tali metadati.</span><span class="sxs-lookup"><span data-stu-id="6085d-116">Because Windows Media Device Manager cannot be used to retrieve metadata from local files, you must use the Windows Media Format SDK (or some other tool) to retrieve such metadata.</span></span>

<span data-ttu-id="6085d-117">Per utilizzare Windows Media Format SDK per recuperare le proprietà del file ASF, attenersi alla seguente procedura:</span><span class="sxs-lookup"><span data-stu-id="6085d-117">To use the Windows Media Format SDK to retrieve ASF file properties, follow these steps:</span></span>

1.  <span data-ttu-id="6085d-118">Creare un oggetto dell'editor di metadati chiamando **WMCreateEditor** e richiedendo un'interfaccia **IWMMetadataEditor** .</span><span class="sxs-lookup"><span data-stu-id="6085d-118">Create a metadata editor object by calling **WMCreateEditor** and requesting an **IWMMetadataEditor** interface.</span></span>
2.  <span data-ttu-id="6085d-119">Aprire il file per la lettura dei metadati chiamando **IWMMetadataEditor:: Open**.</span><span class="sxs-lookup"><span data-stu-id="6085d-119">Open the file for metadata reading by calling **IWMMetadataEditor::Open**.</span></span>
3.  <span data-ttu-id="6085d-120">Se il file è un file ASF valido e può essere aperto, eseguire una query sull'editor per l'interfaccia **IWMHeaderInfo** .</span><span class="sxs-lookup"><span data-stu-id="6085d-120">If the file is a valid ASF file and can be opened, query the editor for the **IWMHeaderInfo** interface.</span></span>
4.  <span data-ttu-id="6085d-121">Recuperare le proprietà del file chiamando **IWMHeaderInfo:: GetAttributeByName**, passando la costante della proprietà SDK di formato Windows Media desiderata.</span><span class="sxs-lookup"><span data-stu-id="6085d-121">Retrieve file properties by calling **IWMHeaderInfo::GetAttributeByName**, passing in the desired Windows Media Format SDK property constant.</span></span> <span data-ttu-id="6085d-122">Nella tabella seguente è riportato un elenco di costanti SDK di formato con costanti Windows Media Gestione dispositivi SDK equivalenti.</span><span class="sxs-lookup"><span data-stu-id="6085d-122">A list of Format SDK constants with equivalent Windows Media Device Manager SDK constants is given in the following table.</span></span>



| <span data-ttu-id="6085d-123">Costante Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="6085d-123">Windows Media Format SDK Constant</span></span>    | <span data-ttu-id="6085d-124">Costante Windows Media Gestione dispositivi SDK</span><span class="sxs-lookup"><span data-stu-id="6085d-124">Windows Media Device Manager SDK Constant</span></span>      |
|--------------------------------------|------------------------------------------------|
| <span data-ttu-id="6085d-125">g \_ wszWMTitle</span><span class="sxs-lookup"><span data-stu-id="6085d-125">g\_wszWMTitle</span></span>                        | <span data-ttu-id="6085d-126">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="6085d-126">g\_wszWMDMTitle</span></span>                                |
| <span data-ttu-id="6085d-127">g \_ wszWMAuthor</span><span class="sxs-lookup"><span data-stu-id="6085d-127">g\_wszWMAuthor</span></span>                       | <span data-ttu-id="6085d-128">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="6085d-128">g\_wszWMDMAuthor</span></span>                               |
| <span data-ttu-id="6085d-129">g \_ wszWMAlbumTitle</span><span class="sxs-lookup"><span data-stu-id="6085d-129">g\_wszWMAlbumTitle</span></span>                   | <span data-ttu-id="6085d-130">g \_ wszWMDMAlbumTitle</span><span class="sxs-lookup"><span data-stu-id="6085d-130">g\_wszWMDMAlbumTitle</span></span>                           |
| <span data-ttu-id="6085d-131">g \_ wszWMGenre</span><span class="sxs-lookup"><span data-stu-id="6085d-131">g\_wszWMGenre</span></span>                        | <span data-ttu-id="6085d-132">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="6085d-132">g\_wszWMDMGenre</span></span>                                |
| <span data-ttu-id="6085d-133">g \_ wszWMYear</span><span class="sxs-lookup"><span data-stu-id="6085d-133">g\_wszWMYear</span></span>                         | <span data-ttu-id="6085d-134">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="6085d-134">g\_wszWMDMYear</span></span>                                 |
| <span data-ttu-id="6085d-135">g \_ wszWMTrackNumber o g \_ wszWMTrack</span><span class="sxs-lookup"><span data-stu-id="6085d-135">g\_wszWMTrackNumber or g\_wszWMTrack</span></span> | <span data-ttu-id="6085d-136">g \_ wszWMDMTrack</span><span class="sxs-lookup"><span data-stu-id="6085d-136">g\_wszWMDMTrack</span></span>                                |
| <span data-ttu-id="6085d-137">g \_ wszWMComposer</span><span class="sxs-lookup"><span data-stu-id="6085d-137">g\_wszWMComposer</span></span>                     | <span data-ttu-id="6085d-138">g \_ wszWMDMComposer</span><span class="sxs-lookup"><span data-stu-id="6085d-138">g\_wszWMDMComposer</span></span>                             |
| <span data-ttu-id="6085d-139">g \_ wszWMDuration</span><span class="sxs-lookup"><span data-stu-id="6085d-139">g\_wszWMDuration</span></span>                     | <span data-ttu-id="6085d-140">g \_ wszWMDMDuration</span><span class="sxs-lookup"><span data-stu-id="6085d-140">g\_wszWMDMDuration</span></span>                             |
| <span data-ttu-id="6085d-141">g \_ wszWMCopyright</span><span class="sxs-lookup"><span data-stu-id="6085d-141">g\_wszWMCopyright</span></span>                    | <span data-ttu-id="6085d-142">g \_ wszWMDMProviderCopyright</span><span class="sxs-lookup"><span data-stu-id="6085d-142">g\_wszWMDMProviderCopyright</span></span>                    |
| <span data-ttu-id="6085d-143">g \_ wszWMDescription</span><span class="sxs-lookup"><span data-stu-id="6085d-143">g\_wszWMDescription</span></span>                  | <span data-ttu-id="6085d-144">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="6085d-144">g\_wszWMDMDescription</span></span>                          |
| <span data-ttu-id="6085d-145">g \_ wszWMBitrate</span><span class="sxs-lookup"><span data-stu-id="6085d-145">g\_wszWMBitrate</span></span>                      | <span data-ttu-id="6085d-146">g \_ wszWMDMBitrate</span><span class="sxs-lookup"><span data-stu-id="6085d-146">g\_wszWMDMBitrate</span></span>                              |
| <span data-ttu-id="6085d-147">g \_ wszWMRating</span><span class="sxs-lookup"><span data-stu-id="6085d-147">g\_wszWMRating</span></span>                       | <span data-ttu-id="6085d-148">g \_ wszWMDMUserRating</span><span class="sxs-lookup"><span data-stu-id="6085d-148">g\_wszWMDMUserRating</span></span>                           |
| <span data-ttu-id="6085d-149">g \_ wszWMAlbumArtist</span><span class="sxs-lookup"><span data-stu-id="6085d-149">g\_wszWMAlbumArtist</span></span>                  | <span data-ttu-id="6085d-150">g \_ wszWMDMAlbumArtist</span><span class="sxs-lookup"><span data-stu-id="6085d-150">g\_wszWMDMAlbumArtist</span></span>                          |
| <span data-ttu-id="6085d-151">g \_ wszWMParentalRating</span><span class="sxs-lookup"><span data-stu-id="6085d-151">g\_wszWMParentalRating</span></span>               | <span data-ttu-id="6085d-152">g \_ wszWMDMParentalRating</span><span class="sxs-lookup"><span data-stu-id="6085d-152">g\_wszWMDMParentalRating</span></span>                       |
| <span data-ttu-id="6085d-153">g \_ wszWMRadioStationName</span><span class="sxs-lookup"><span data-stu-id="6085d-153">g\_wszWMRadioStationName</span></span>             | <span data-ttu-id="6085d-154">g \_ wszWMDMMediaStationName</span><span class="sxs-lookup"><span data-stu-id="6085d-154">g\_wszWMDMMediaStationName</span></span>                     |
| <span data-ttu-id="6085d-155">g \_ wszWMSubTitle</span><span class="sxs-lookup"><span data-stu-id="6085d-155">g\_wszWMSubTitle</span></span>                     | <span data-ttu-id="6085d-156">g \_ wszWMDMSubTitle</span><span class="sxs-lookup"><span data-stu-id="6085d-156">g\_wszWMDMSubTitle</span></span>                             |
| <span data-ttu-id="6085d-157">g \_ wszWMVideoWidth</span><span class="sxs-lookup"><span data-stu-id="6085d-157">g\_wszWMVideoWidth</span></span>                   | <span data-ttu-id="6085d-158">g \_ wszWMDMWidth</span><span class="sxs-lookup"><span data-stu-id="6085d-158">g\_wszWMDMWidth</span></span>                                |
| <span data-ttu-id="6085d-159">g \_ wszWMVideoHeight</span><span class="sxs-lookup"><span data-stu-id="6085d-159">g\_wszWMVideoHeight</span></span>                  | <span data-ttu-id="6085d-160">g \_ wszWMDMHeight</span><span class="sxs-lookup"><span data-stu-id="6085d-160">g\_wszWMDMHeight</span></span>                               |
| <span data-ttu-id="6085d-161">g \_ wszWMMood</span><span class="sxs-lookup"><span data-stu-id="6085d-161">g\_wszWMMood</span></span>                         | <span data-ttu-id="6085d-162">g \_ wszWMDMTrackMood</span><span class="sxs-lookup"><span data-stu-id="6085d-162">g\_wszWMDMTrackMood</span></span>                            |
| <span data-ttu-id="6085d-163">g \_ wszWMCodec</span><span class="sxs-lookup"><span data-stu-id="6085d-163">g\_wszWMCodec</span></span>                        | <span data-ttu-id="6085d-164">g \_ wszAudioWAVECodec o g \_ wszVideoFourCCCodec</span><span class="sxs-lookup"><span data-stu-id="6085d-164">g\_wszAudioWAVECodec or g\_wszVideoFourCCCodec</span></span> |



 

<span data-ttu-id="6085d-165">Nell'esempio di codice C++ riportato di seguito viene illustrato il recupero di una serie di proprietà di metadati da un file ASF utilizzando Windows Media Format SDK e la relativa conversione ai valori equivalenti di Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="6085d-165">The following C++ example code demonstrates retrieving a number of metadata properties from an ASF file using the Windows Media Format SDK and converting them to the equivalent Windows Media Device Manager values.</span></span>


```C++
// Structure and array to hold equivalent Windows Media Format SDK 
// and Windows Media Device Manager SDK metadata property names.
struct EquivalentProperty
{
    LPCWSTR FormatSDKConst;
    LPCWSTR WMDMSDKConst;
};
EquivalentProperty EquivalentProperties []= 
{
    {g_wszWMTitle,        g_wszWMDMTitle},
    {g_wszWMAuthor,      g_wszWMDMAuthor},
    {g_wszWMAlbumTitle,  g_wszWMDMAlbumTitle},
    {g_wszWMGenre,       g_wszWMDMGenre},
    {g_wszWMYear,        g_wszWMDMYear},
    {g_wszWMTrackNumber, g_wszWMDMTrack},
    {g_wszWMTrack,       g_wszWMDMTrack},
    {g_wszWMComposer,    g_wszWMDMComposer},
    {g_wszWMBitrate,     g_wszWMDMBitrate},
    {g_wszWMDuration,    g_wszWMDMDuration},
    {g_wszWMCopyright,   g_wszWMDMProviderCopyright},
    {g_wszWMDescription, g_wszWMDMDescription},
    {g_wszWMRating,      g_wszWMDMUserRating},
    {g_wszWMAlbumArtist, g_wszWMDMAlbumArtist},
    {g_wszWMParentalRating,    g_wszWMDMParentalRating},
    {g_wszWMRadioStationName,  g_wszWMDMMediaStationName},
    {g_wszWMSubTitle,    g_wszWMDMSubTitle},
    {g_wszWMVideoWidth,  g_wszWMDMWidth},
    {g_wszWMVideoHeight, g_wszWMDMHeight},
    {g_wszWMMood,        g_wszWMDMTrackMood},
    {g_wszWMCodec,       g_wszAudioWAVECodec},
    {g_wszWMCodec,       g_wszVideoFourCCCodec}
};
// Function that tries to get metadata by using the Format SDK. 
// If it cannot open the file, it returns E_FAIL.
HRESULT GetFileMetadataFromFormatSDK(IWMDMMetaData* pMetadata, LPCWSTR file)
{
    if ((pMetaData == NULL) || (file == NULL)) return E_INVALIDPARAM;
    HRESULT hr = S_OK;
    CComPtr<IWMMetadataEditor> pEditor;

    // Do loop to allow easy error trapping. Even if there are no errors, 
    // the loop executes only once.
    do {
        hr = WMCreateEditor(&pEditor);
        if (FAILED(hr)) 
            break;

        // Open the file.
        hr = pEditor->Open(file);
        if (FAILED(hr)) 
            break;

        CComPtr<IWMHeaderInfo>pHeaderInfo;
        hr = pEditor->QueryInterface(__uuidof(IWMHeaderInfo), (void**)&pHeaderInfo);
        if (FAILED(hr))
            break;

        // Copy values from Format SDK to equivalent WMDM SDK metadata values.

        // Loop through all known values
        WORD stream = 0;
        WMT_ATTR_DATATYPE wmfType;
        WORD len = 0;
        BYTE* value = NULL;
        WMDM_TAG_DATATYPE wmdmType;
        for (int i = 0; i < sizeof(EquivalentProperties) / sizeof(EquivalentProperties[0]); i++)
        {
            // Request each value from our equivalency list by name.
            // The function is called twice: once to get the buffer size,
            // and once to get the value in the allocated buffer.
            if (FAILED(pHeaderInfo->GetAttributeByName(
                &stream, EquivalentProperties[i].FormatSDKConst, &wmfType, NULL, &len)))
            {
                continue;
            }

            value = new BYTE[len];
            if (value == NULL) continue;

            if (FAILED(pHeaderInfo->GetAttributeByName(&stream, EquivalentProperties[i].FormatSDKConst, &wmfType, value, &len)))
            {
                delete[] value;
                continue;
            }

            // Send the data to the equivalent WMDM metadata value.
            // First, find the equivalent WMDM type for the WMF type.
            switch(wmfType)
            {
            case WMT_TYPE_BINARY:
                wmdmType = WMDM_TYPE_BINARY;
                break;
            case WMT_TYPE_DWORD:
                wmdmType = WMDM_TYPE_DWORD;
                break;
            case WMT_TYPE_STRING:
                wmdmType = WMDM_TYPE_STRING;
                break;
            case WMT_TYPE_BOOL:
                wmdmType = WMDM_TYPE_BOOL;
                break;
            case WMT_TYPE_QWORD:
                wmdmType = WMDM_TYPE_QWORD;
                break;
            case WMT_TYPE_WORD:
                wmdmType = WMDM_TYPE_WORD;
                break;
            case WMT_TYPE_GUID:
                wmdmType = WMDM_TYPE_GUID;
                break;
            default:
                wmdmType = WMDM_TYPE_BINARY;
                break;
            }

            // Don't worry about trapping errors, because there's nothing 
            // we can do about it.
            pMetadata->AddItem(wmdmType, 
                EquivalentProperties[i].WMDMSDKConst, value, len);
            delete[] value;
        } // Add next value.
    } while (FALSE); // End Do loop error trap.

    // Close the file opened with IWMMetadataEditor.
    pEditor->Close();
    return hr;
}
```



<span data-ttu-id="6085d-166">La funzione di esempio C++ seguente mostra come usare DirectShow per ottenere informazioni su file e aggiungerlo ai metadati.</span><span class="sxs-lookup"><span data-stu-id="6085d-166">The following C++ example function shows how to use DirectShow to get some file information and add it to the metadata.</span></span>


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
HRESULT GetFileMetadataFromDShow(IWMDMMetaData* pMetadata, LPCWSTR file)
{
    HRESULT hr = S_OK;

    // Add file metadata properties from DirectShow. 
    // This is good for non-ASF files, or to add any information
    // that the Format SDK didn't get.

    // Do loop to allow easy error trapping. Even if there are no errors, 
    // the loop executes only once.
    do
    {
        // Create the Media Detector object.
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (FAILED(hr)) 
            break;

        // Open the file.
        hr = pIMediaDet->put_Filename(BSTR(file));
        if (FAILED(hr))
            break;

        // Get the media type for the default stream.
        AM_MEDIA_TYPE mediaType;
        hr = pIMediaDet->get_StreamMediaType(&mediaType);
        if (FAILED(hr))
            break;

        // We have the file open, so start requesting information from the 
        // Media Detector and adding it to the metadata. When adding 
        // individual metadata values, ignore the HRESULT, because failure 
        // to add these metadata values is not a breaking issue.

        // Get major and minor types.
        WCHAR strMediaType[64];
        ZeroMemory(strMediaType, 64);

        //Change the major type to a string, then add to IWMDMMetaData.
        StringFromGUID2(reinterpret_cast<GUID&>(mediaType.majortype),
            (LPOLESTR)strMediaType, 64);
        hr = pMetadata->AddItem(WMDM_TYPE_STRING, 
             g_wszWMDMediaClassPrimaryID, 
            (BYTE*) strMediaType, 
             sizeof(strMediaType) / sizeof(strMediaType[0]));

        // Clear local string, then retrieve subtype the same way.
        ZeroMemory(strMediaType, 64);
        StringFromGUID2(reinterpret_cast<GUID&>(mediaType.subtype),
            (LPOLESTR)strMediaType, 64);
        hr = pMetadata->AddItem(WMDM_TYPE_STRING, 
            g_wszWMDMMediaClassSecondaryID, (BYTE*) strMediaType,
            sizeof(strMediaType) / sizeof(strMediaType[0]));

        // Get the duration. Duration is retrieved in seconds, but set 
        // in 100-nanosecond units.
        double duration = 0;
        hr = pIMediaDet->get_StreamLength(&duration);
        if (duration > 0)
        {
            duration *= 10E7;
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMDuration, (BYTE*) &duration, sizeof(duration));
        }

        // Get the frame rate.
        double frameRate = 0;
        hr = pIMediaDet->get_FrameRate(&frameRate);
        if (frameRate > 0)
        {
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMFrameRate, 
                (BYTE*) &frameRate,
                sizeof(frameRate));
        }

        // Get the structure for the default stream's major type and 
        // fill in additional information.

        if (IsEqualGUID(mediaType.formattype, FORMAT_VideoInfo))
        {
            VIDEOINFOHEADER* data = (VIDEOINFOHEADER*) mediaType.pbFormat;
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMVideoBitrate, 
               (BYTE*) &data->dwBitRate, sizeof(DWORD));
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMHeight, 
               (BYTE*) &data->bmiHeader.biHeight, sizeof(LONG));
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMWidth, 
               (BYTE*) &data->bmiHeader.biWidth, sizeof(LONG));
        }

        if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
        {
            WAVEFORMATEX* data = (WAVEFORMATEX*) mediaType.pbFormat;
            hr = pMetadata->AddItem(WMDM_TYPE_WORD, g_wszWMDMBlockAlignment, 
                (BYTE*) &data->nBlockAlign, sizeof(WORD));
            hr = pMetadata->AddItem(WMDM_TYPE_WORD, g_wszWMDMNumChannels, 
               (BYTE*) &data->nChannels, sizeof(WORD));
        }
    } while (FALSE); // End of error loop.
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="6085d-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6085d-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6085d-168">**Scrittura di file nel dispositivo**</span><span class="sxs-lookup"><span data-stu-id="6085d-168">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




