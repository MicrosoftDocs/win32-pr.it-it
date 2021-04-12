---
title: Esplorazione di un dispositivo
description: Esplorazione di un dispositivo
ms.assetid: 8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0
keywords:
- Windows Media Gestione dispositivi, esplorazione di dispositivi
- Gestione dispositivi, esplorazione dei dispositivi
- Guida per programmatori, esplorazione di dispositivi
- applicazioni desktop, esplorazione di dispositivi
- creazione di applicazioni Windows Media Gestione dispositivi, esplorazione di dispositivi
- esplorazione dei dispositivi
- depositi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc154960a4c95efbdf2626271ba90000df99ae8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396062"
---
# <a name="exploring-a-device"></a><span data-ttu-id="f9976-110">Esplorazione di un dispositivo</span><span class="sxs-lookup"><span data-stu-id="f9976-110">Exploring a Device</span></span>

<span data-ttu-id="f9976-111">L'esplorazione di un dispositivo è simile all'esplorazione di un'unità disco.</span><span class="sxs-lookup"><span data-stu-id="f9976-111">Exploring a device is similar to exploring a disk drive.</span></span> <span data-ttu-id="f9976-112">Tutti gli oggetti in un dispositivo sono detti *archiviazione*.</span><span class="sxs-lookup"><span data-stu-id="f9976-112">All objects on a device are called *storages*.</span></span> <span data-ttu-id="f9976-113">Una risorsa di archiviazione può essere un file, una cartella o un oggetto astratto (ad esempio una playlist) nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9976-113">A storage can be a file, folder, or abstract object (such as a playlist) on the device.</span></span> <span data-ttu-id="f9976-114">Per comprendere il tipo di archiviazione, è necessario esaminare gli attributi e i metadati di archiviazione (se supportati).</span><span class="sxs-lookup"><span data-stu-id="f9976-114">You must examine a storage's attributes and metadata (if supported) to understand what kind of storage it is.</span></span> <span data-ttu-id="f9976-115">Le archiviazioni sono organizzate gerarchicamente sul dispositivo. ogni risorsa di archiviazione ha esattamente un elemento padre e tutte le archiviazioni derivano da una singola risorsa di archiviazione del dispositivo radice, in genere denominata " \\ ".</span><span class="sxs-lookup"><span data-stu-id="f9976-115">Storages are organized hierarchically on the device; every storage has exactly one parent, and all storages ultimately descend from a single root device storage, typically named "\\".</span></span>

<span data-ttu-id="f9976-116">I passaggi seguenti descrivono come esplorare un dispositivo:</span><span class="sxs-lookup"><span data-stu-id="f9976-116">The following steps describe how to explore a device:</span></span>

1.  <span data-ttu-id="f9976-117">Ottenere l'interfaccia [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) di un dispositivo come descritto in [enumerazione dei dispositivi](enumerating-devices.md).</span><span class="sxs-lookup"><span data-stu-id="f9976-117">Get the [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface of a device as described in [Enumerating Devices](enumerating-devices.md).</span></span>
2.  <span data-ttu-id="f9976-118">Chiamare [**IWMDMDevice:: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) per recuperare un'interfaccia [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) .</span><span class="sxs-lookup"><span data-stu-id="f9976-118">Call [**IWMDMDevice::EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-enumstorage) to retrieve an [**IWMDMEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmenumstorage) interface.</span></span> <span data-ttu-id="f9976-119">Questa interfaccia viene usata per ottenere tutti gli oggetti figlio dell'archiviazione che restituisce questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="f9976-119">This interface is used to get all child objects of the storage that returns this interface.</span></span> <span data-ttu-id="f9976-120">Quando si recupera questa interfaccia dal dispositivo, come in questo caso, verrà mantenuta solo una risorsa di archiviazione: l'archiviazione del dispositivo radice.</span><span class="sxs-lookup"><span data-stu-id="f9976-120">When getting this interface from the device, as we are here, it will hold only one storage: the root device storage.</span></span>
3.  <span data-ttu-id="f9976-121">Chiamare [**IWMDMEnumStorage:: Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) con il conteggio 1 per recuperare l'interfaccia [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) per l'archiviazione del dispositivo radice.</span><span class="sxs-lookup"><span data-stu-id="f9976-121">Call [**IWMDMEnumStorage::Next**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmenumstorage-next) with a count of 1 to retrieve the [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) interface for the root device storage.</span></span> <span data-ttu-id="f9976-122">Non è possibile richiedere più di un elemento figlio dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9976-122">(You cannot request more than one child from the device.)</span></span>
4.  <span data-ttu-id="f9976-123">Esaminare tutte le archiviazioni sul dispositivo richiamando in modo ricorsivo [**IWMDMStorage:: EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) e quindi **IWMDMEnumStorage:: Next** per ottenere gli elementi figlio di una risorsa di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f9976-123">Examine all storages on the device by recursively calling [**IWMDMStorage::EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) and then **IWMDMEnumStorage::Next** to get children of a storage.</span></span> <span data-ttu-id="f9976-124">Per verificare se una risorsa di archiviazione dispone di elementi figlio per evitare le chiamate a **EnumStorage** e **Next**, è possibile chiamare [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) per verificare se i flag WMDM \_ storage \_ attr \_ contiene \_ files o WMDM \_ storage \_ attr \_ has \_ Folders.</span><span class="sxs-lookup"><span data-stu-id="f9976-124">To see if a storage has children to avoid the calls to **EnumStorage** and **Next**, you can call [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) to check for the flags WMDM\_STORAGE\_ATTR\_HAS\_FILES or WMDM\_STORAGE\_ATTR\_HAS\_FOLDERS.</span></span> <span data-ttu-id="f9976-125">Per ulteriori informazioni su come ottenere le proprietà di una risorsa di archiviazione, vedere [ottenere e impostare metadati e attributi](getting-and-setting-metadata-and-attributes.md) e [ottenere e impostare metadati e attributi nell'applicazione](getting-and-setting-metadata-and-attributes-in-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="f9976-125">For more information about how to get the properties of a storage, see [Getting and Setting Metadata and Attributes](getting-and-setting-metadata-and-attributes.md) and [Getting and Setting Metadata and Attributes in the Application](getting-and-setting-metadata-and-attributes-in-the-application.md).</span></span>

<span data-ttu-id="f9976-126">Windows Media Gestione dispositivi non espone un set di cartelle standard per contenere supporti di un tipo specifico, ad esempio una cartella "playlist personali" per le playlist.</span><span class="sxs-lookup"><span data-stu-id="f9976-126">Windows Media Device Manager does not expose a standard set of folders to hold media of a specific type (for example, a "My Playlists" folder for playlists).</span></span> <span data-ttu-id="f9976-127">Ogni dispositivo ha un file system univoco ed è necessario decidere in quale posizione è opportuno cercare o inviare un file specifico.</span><span class="sxs-lookup"><span data-stu-id="f9976-127">Every device has a unique file system, and you will have to decide on an appropriate place to look for, or to send, a specific file.</span></span>

> [!Note]  
> <span data-ttu-id="f9976-128">Esplora risorse consente di visualizzare le cartelle virtuali che non esistono effettivamente nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9976-128">Windows Explorer can show virtual folders that do not actually exist on the device.</span></span> <span data-ttu-id="f9976-129">Le cartelle virtuali di esempio sono le cartelle "supporti" e "dati" visualizzate per i dispositivi MTP.</span><span class="sxs-lookup"><span data-stu-id="f9976-129">Example virtual folders are the "Media" and "Data" folders displayed for MTP devices.</span></span> <span data-ttu-id="f9976-130">Queste cartelle vengono create da Windows per rendere più semplici i download per gli utenti finali; non esistono effettivamente nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9976-130">These folders are created by Windows to make downloads simpler for end users; they do not actually exist on the device.</span></span> <span data-ttu-id="f9976-131">L'applicazione non deve dipendere dalla ricerca di questi tipi di cartelle generali.</span><span class="sxs-lookup"><span data-stu-id="f9976-131">Your application should not depend on finding these types of general folders.</span></span> <span data-ttu-id="f9976-132">Viceversa, Esplora risorse potrebbe non visualizzare alcune cartelle o oggetti che esistono nel dispositivo (ad esempio, playlist).</span><span class="sxs-lookup"><span data-stu-id="f9976-132">Conversely, Windows Explorer might not show some folders or objects that do exist on the device (for example, playlists).</span></span>

 

<span data-ttu-id="f9976-133">Nell'esempio di codice C++ riportato di seguito viene illustrata l'esplorazione ricorsiva di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9976-133">The following C++ example code demonstrates the recursive exploration of a device.</span></span> <span data-ttu-id="f9976-134">USA due funzioni:</span><span class="sxs-lookup"><span data-stu-id="f9976-134">It uses two functions:</span></span>

-   <span data-ttu-id="f9976-135">ExploreDevice, una funzione iniziale che riceve un puntatore di dispositivo e ottiene un puntatore all'enumeratore radice per quel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9976-135">ExploreDevice, a starting function that receives a device pointer and obtains a pointer to the root enumerator for that device.</span></span>
-   <span data-ttu-id="f9976-136">RecursiveExploreStorage, che viene chiamato per esplorare un dispositivo in modo ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="f9976-136">RecursiveExploreStorage, which is called to explore a device recursively.</span></span>


```C++
// Get the root enumerator and start the recursive function.
HRESULT ExploreDevice(IWMDMDevice* pDevice)
{
    HRESULT hr = S_OK;

    // Get a root enumerator.
    CComPtr<IWMDMEnumStorage> pEnumStorage;
    hr = pDevice->EnumStorage(&pEnumStorage);
    if (SUCCEEDED(hr))
    {
        RecursiveExploreStorage(pEnumStorage);
    }
    return hr;
}

// Recursively explore a storage.
void RecursiveExploreStorage(IWMDMEnumStorage* pEnumStorage)
{
    HRESULT hr = S_OK;
    CComPtr<IWMDMStorage> pStorage;

    ULONG numRetrieved = 0;
    // Loop through all storages in the current storage.
    while((pEnumStorage->Next(1, &pStorage, &numRetrieved) == S_OK) && (numRetrieved == 1))
    {
        // Get the name of the object.
        const UINT MAX_LEN = 255;
        WCHAR name[MAX_LEN];
        hr = pStorage->GetName((LPWSTR)&name, MAX_LEN);
        // TODO: Display the retrieved storage name

        // If this is a folder, recurse into it.
        if (attributes & WMDM_FILE_ATTR_FOLDER)
        {
            CComPtr<IWMDMEnumStorage> pEnumSubStorage;
            hr = pStorage->EnumStorage(&pEnumSubStorage);
            if (SUCCEEDED(hr)
            {
                RecursiveExploreStorage(pEnumSubStorage);
            }
        }
        pStorage.Release();
    } // Get the next storage pointer.
    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="f9976-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f9976-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9976-138">**Creazione di un'applicazione Windows Media Gestione dispositivi**</span><span class="sxs-lookup"><span data-stu-id="f9976-138">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




