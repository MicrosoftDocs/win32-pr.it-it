---
title: Determinazione dello stato di sincronizzazione della playlist
description: Determinazione dello stato di sincronizzazione della playlist
ms.assetid: 634b659b-c3ae-4957-b17e-18fd92e915be
keywords:
- Media Player di Windows, playlist di sincronizzazione
- Modello a oggetti di Windows Media Player, playlist di sincronizzazione
- modello a oggetti, playlist di sincronizzazione
- Windows Media Player Mobile, playlist di sincronizzazione
- Controllo ActiveX di Windows Media Player, playlist di sincronizzazione
- Controllo ActiveX Windows Media Player Mobile, playlist di sincronizzazione
- Controllo ActiveX, playlist di sincronizzazione
- playlist, sincronizzazione
- playlist di metafile, sincronizzazione
- Playlist di Windows Media Metafile, sincronizzazione
- dispositivi portatili, determinazione dello stato della playlist di sincronizzazione
- playlist di sincronizzazione, stato di sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9758cfbb73c698a40d6d4f48e645e57750d8a332
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299377"
---
# <a name="determining-playlist-synchronization-state"></a><span data-ttu-id="02c05-115">Determinazione dello stato di sincronizzazione della playlist</span><span class="sxs-lookup"><span data-stu-id="02c05-115">Determining Playlist Synchronization State</span></span>

<span data-ttu-id="02c05-116">Windows Media Player 10 o versioni successive utilizza l'attributo **SyncState** per contenere informazioni sul fatto che un file multimediale digitale specifico sia stato copiato in un dispositivo portatile e, in caso di errore, se la copia non è riuscita perché la memoria del dispositivo non è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="02c05-116">Windows Media Player 10 or later uses the **SyncState** attribute to contain information about whether a particular digital media file has been copied to a portable device and, in the case of a failure, whether copying failed because the device did not have enough memory.</span></span>

<span data-ttu-id="02c05-117">Nell'esempio di codice seguente viene creata una funzione che recupera queste informazioni da un file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="02c05-117">The following example code creates a function that retrieves this information from a digital media file.</span></span> <span data-ttu-id="02c05-118">La funzione accetta i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="02c05-118">The function takes the following parameters:</span></span>

-   <span data-ttu-id="02c05-119">*pMedia*.</span><span class="sxs-lookup"><span data-stu-id="02c05-119">*pMedia*.</span></span> <span data-ttu-id="02c05-120">Puntatore a un'interfaccia **IWMPMedia** che rappresenta il file multimediale digitale da ispezionare.</span><span class="sxs-lookup"><span data-stu-id="02c05-120">Pointer to an **IWMPMedia** interface that represents the digital media file to inspect.</span></span>
-   <span data-ttu-id="02c05-121">*lPsIndex*.</span><span class="sxs-lookup"><span data-stu-id="02c05-121">*lPsIndex*.</span></span> <span data-ttu-id="02c05-122">Indice di partnership del dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="02c05-122">Partnership index of the current device.</span></span>
-   <span data-ttu-id="02c05-123">*pulOnDevice*.</span><span class="sxs-lookup"><span data-stu-id="02c05-123">*pulOnDevice*.</span></span> <span data-ttu-id="02c05-124">Puntatore a una variabile **Long** che riceve il valore che indica se il file multimediale digitale è stato copiato nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="02c05-124">Pointer to a **long** variable that receives the value indicating whether the digital media file has been copied to the device.</span></span>
-   <span data-ttu-id="02c05-125">*pulDidNotFit*.</span><span class="sxs-lookup"><span data-stu-id="02c05-125">*pulDidNotFit*.</span></span> <span data-ttu-id="02c05-126">Puntatore a una variabile **Long** che riceve il valore che indica se l'operazione di copia non è riuscita perché la memoria del dispositivo non è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="02c05-126">Pointer to a **long** variable that receives the value indicating whether the copy operation failed because the device did not have enough memory.</span></span>

<span data-ttu-id="02c05-127">Le informazioni contenute nell'attributo **SyncState** sono codificate in modo bit per bit.</span><span class="sxs-lookup"><span data-stu-id="02c05-127">The information contained in the **SyncState** attribute is encoded in a bitwise fashion.</span></span> <span data-ttu-id="02c05-128">È possibile osservare come questa funzione viene usata nel codice di esempio nell' [enumerazione degli elementi multimediali](enumerating-the-media-items.md).</span><span class="sxs-lookup"><span data-stu-id="02c05-128">You can see how this function is used in the example code in [Enumerating the Media Items](enumerating-the-media-items.md).</span></span>


```C++
STDMETHODIMP CSyncSettings::GetPartnershipSyncState(IWMPMedia* pMedia, long lPsIndex, ULONG *pulOnDevice, ULONG *pulDidNotFit)
{
    ATLASSERT(pMedia); 
    ATLASSERT(lPsIndex > 0 && 
              lPsIndex < 17);
    ATLASSERT(pulOnDevice);
    ATLASSERT(pulDidNotFit);
  
    CComVariant varSyncStateVal;   
    CComPtr<IWMPMedia> spMedia(pMedia); 
    CComPtr<IWMPMedia3> spMedia3;     
    HRESULT hr = spMedia.QueryInterface(&spMedia3); 
    ULONG ulSyncState = 0; // Stores the ulVal member of varSyncStateVal. 
    ULONG lLSB = 0; // Represents least significant bit: Did the media fail to copy because it would not fit?
    ULONG lMSB = 0; // Represents most significant bit: Is the media on the device?

    // Calculate the bit shift required to isolate the partnership bit 
    // pair from the SyncState attribute.
    const int iRshift = (lPsIndex - 1) * 2;

    if(SUCCEEDED(hr) && spMedia3)
    {       
        hr = spMedia3->getItemInfoByType(CComBSTR("SyncState"), CComBSTR(""), 0, &varSyncStateVal);
    }

    if(SUCCEEDED(hr) && varSyncStateVal.vt == VT_UI4)
    {   
        // Get the value.
        ulSyncState = varSyncStateVal.ulVal;

        // Shift the bit pair to the rightmost position.
        ulSyncState >>= iRshift; 

        // Mask the rightmost bit pair.
        ulSyncState &= 3;

        // Get the LSB         
        lLSB = ulSyncState & ~2; // Sets the 2E1 bit to zero. 

        // Get the MSB
        ulSyncState >>= 1;
        lMSB = ulSyncState;       
    }

    // Return the bits.
    *pulOnDevice = lMSB;
    *pulDidNotFit = lLSB;

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="02c05-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="02c05-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02c05-130">**Interfaccia IWMPMedia**</span><span class="sxs-lookup"><span data-stu-id="02c05-130">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="02c05-131">**IWMPMedia3::getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="02c05-131">**IWMPMedia3::getItemInfoByType**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype)
</dt> <dt>

[<span data-ttu-id="02c05-132">**Gestione delle playlist di sincronizzazione**</span><span class="sxs-lookup"><span data-stu-id="02c05-132">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="02c05-133">**Attributo SyncState**</span><span class="sxs-lookup"><span data-stu-id="02c05-133">**SyncState Attribute**</span></span>](syncstate-attribute.md)
</dt> </dl>

 

 




