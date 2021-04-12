---
title: Lettura di file dal dispositivo
description: Lettura di file dal dispositivo
ms.assetid: adb87b53-39e2-4f83-ab6d-7e2f7c0bd5d3
keywords:
- Windows Media Gestione dispositivi, lettura di file dai dispositivi
- Gestione dispositivi, lettura di file dai dispositivi
- Guida per programmatori, lettura di file dai dispositivi
- applicazioni desktop, lettura di file dai dispositivi
- creazione di applicazioni Windows Media Gestione dispositivi, lettura di file dai dispositivi
- lettura di file dai dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b80cf820e889b29e612206f90b07e1cb02c4c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221072"
---
# <a name="reading-files-from-the-device"></a><span data-ttu-id="4f438-109">Lettura di file dal dispositivo</span><span class="sxs-lookup"><span data-stu-id="4f438-109">Reading Files from the Device</span></span>

<span data-ttu-id="4f438-110">Quando è stato trovato un file che si vuole copiare dal dispositivo, è possibile copiare il file dal dispositivo al computer in un'unica chiamata oppure usare un callback per fare in modo che i byte del file vengano letti direttamente nell'applicazione, che può quindi elaborare o archiviare i dati nel modo più appropriato.</span><span class="sxs-lookup"><span data-stu-id="4f438-110">When you have found a file you would like to copy from the device, you can then copy the file from the device to the computer in a single call, or use a callback to have the file bytes read directly to your application, which can then process or store the data as it sees fits.</span></span>

<span data-ttu-id="4f438-111">I passaggi seguenti illustrano il modo più semplice per copiare un file da un dispositivo in una singola chiamata:</span><span class="sxs-lookup"><span data-stu-id="4f438-111">The following steps show the basic way to copy a file from a device in a single call:</span></span>

1.  <span data-ttu-id="4f438-112">Ottenere un handle per il file nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f438-112">Get a handle to the file on the device.</span></span> <span data-ttu-id="4f438-113">È possibile ottenere l'handle usando una ricerca ricorsiva di file o, se si conosce l'ID persistente dell'archiviazione, chiamando [**IWMDMDevice3:: FindStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage).</span><span class="sxs-lookup"><span data-stu-id="4f438-113">You might obtain the handle by using a recursive file search or, if you know the persistent ID of the storage, by calling [**IWMDMDevice3::FindStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage).</span></span> <span data-ttu-id="4f438-114">In entrambi i casi, è necessaria l'interfaccia [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4f438-114">In either case, you need the [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) interface of the object.</span></span>
2.  <span data-ttu-id="4f438-115">Determinare se l'archiviazione è un file o una cartella.</span><span class="sxs-lookup"><span data-stu-id="4f438-115">Determine whether the storage is a file or a folder.</span></span> <span data-ttu-id="4f438-116">Solo i file possono essere copiati dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f438-116">Only files can be copied from the device.</span></span> <span data-ttu-id="4f438-117">Chiamare [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) per ottenere gli attributi di archiviazione, in modo da indicare se l'archiviazione è un file o una cartella.</span><span class="sxs-lookup"><span data-stu-id="4f438-117">Call [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) to get storage attributes, which will tell you whether the storage is a file or a folder.</span></span>
3.  <span data-ttu-id="4f438-118">Eseguire una query su **IWMDMStorage** per [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)e chiamare [**IWMDMStorageControl:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) per leggere il file dal dispositivo e salvarlo nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="4f438-118">Query **IWMDMStorage** for [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol), and call [**IWMDMStorageControl::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) to read the file from the device and save it to a specified location.</span></span>

<span data-ttu-id="4f438-119">Se invece si vuole leggere il blocco di file per blocco dal dispositivo, è necessario implementare l'interfaccia di callback [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) .</span><span class="sxs-lookup"><span data-stu-id="4f438-119">If, instead, you want to read the file block by block from the device, you must implement the [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) callback interface.</span></span> <span data-ttu-id="4f438-120">Passare questa interfaccia alla chiamata **IWMDMStorageControl:: Read** e Windows Media Gestione dispositivi invierà i blocchi di dati dei file in sequenza al callback.</span><span class="sxs-lookup"><span data-stu-id="4f438-120">Pass this interface into the **IWMDMStorageControl::Read** call, and Windows Media Device Manager will send chunks of file data sequentially to your callback.</span></span> <span data-ttu-id="4f438-121">I passaggi seguenti illustrano come leggere un blocco di file del dispositivo per blocco:</span><span class="sxs-lookup"><span data-stu-id="4f438-121">The following steps show how to read a device file block by block:</span></span>

1.  <span data-ttu-id="4f438-122">Ottenere l'interfaccia **IWMDMStorage** per l'archiviazione e determinare se si tratta di un file, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="4f438-122">Get the **IWMDMStorage** interface for the storage and determine whether it is a file, as described previously.</span></span>
2.  <span data-ttu-id="4f438-123">Preparare gli handle di file o altri handle necessari per conservare i dati ricevuti.</span><span class="sxs-lookup"><span data-stu-id="4f438-123">Prepare any file handles or other handles you need to hold the received data.</span></span>
3.  <span data-ttu-id="4f438-124">Eseguire una query per l'interfaccia **IWMDMStorageControl** dell'archiviazione</span><span class="sxs-lookup"><span data-stu-id="4f438-124">Query for the storage's **IWMDMStorageControl** interface</span></span>
4.  <span data-ttu-id="4f438-125">Chiamare **IWMDMStorageControl:: Read** per iniziare l'operazione di lettura, passando l'interfaccia **IWMDMOperation** implementata.</span><span class="sxs-lookup"><span data-stu-id="4f438-125">Call **IWMDMStorageControl::Read** to begin the read operation, passing in the **IWMDMOperation** interface you have implemented.</span></span>
5.  <span data-ttu-id="4f438-126">Windows Media Gestione dispositivi invierà il blocco di dati per blocco al dispositivo, come descritto in [gestione manuale dei trasferimenti di file](handling-file-transfers-manually.md).</span><span class="sxs-lookup"><span data-stu-id="4f438-126">Windows Media Device Manager will send the data block by block to your device as described in [Handling File Transfers Manually](handling-file-transfers-manually.md).</span></span>

<span data-ttu-id="4f438-127">La funzione di esempio C++ seguente legge un oggetto di archiviazione da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f438-127">The following C++ example function reads a storage object from a device.</span></span> <span data-ttu-id="4f438-128">La funzione accetta un puntatore all'interfaccia **IWMDMOperation** facoltativo; Se l'invio viene inviato, la funzione creerà un file in modo esplicito e gestirà la scrittura dei dati nel file durante l'implementazione di **IWMDMOperation:: TransferObjectData**; in caso contrario, il file verrà letto e salvato nella destinazione specificata da *pwszDestName*.</span><span class="sxs-lookup"><span data-stu-id="4f438-128">The function accepts an optional **IWMDMOperation** interface pointer; if submitted, the function will create a file explicitly and handle writing the data to file on its implementation of **IWMDMOperation::TransferObjectData**; if not, it will read the file and save to the destination specified by *pwszDestName*.</span></span>


```C++
HANDLE m_File = NULL;

HRESULT myFileRead(IWMDMStorage pStorage, LPWSTR pwszDestName, IWMDMOperation* pOperation)
{
    HRESULT hr = S_OK;
    if ((pStorage == NULL) || (pwszDestName == NULL)) 
    {
        return E_INVALIDPARAM;
    }

    // Check that the storage is readable.
    DWORD attributes = 0;
    UINT flags = 0;
    hr = pStorage->GetAttributes(&attributes, NULL); 
    if (FAILED(hr))
    {
        return hr;
    }

    // Check that content is readable.
    if ((attributes & WMDM_FILE_ATTR_CANREAD) == 0)
    {
        return E_FAIL;
    }
    // Check that it is not abstract (such as an abstract playlist).
    else if (attributes & WMDM_STORAGE_ATTR_VIRTUAL)
    {
        return E_FAIL;
    }

    // Set some flag values for the read operation.
    flags |= WMDM_MODE_BLOCK;
    if (attributes & WMDM_FILE_ATTR_FOLDER)
    {
        flags |= WMDM_CONTENT_FOLDER;
    }
    if (attributes & WMDM_FILE_ATTR_FILE)
    {
        flags |= WMDM_CONTENT_FILE;
    }

    // Get the IWMDMStorageControl interface.
    CComQIPtr<IWMDMStorageControl> pStgControl(pStorage);
    
    // Extra steps if we want to read the file ourselves using IWMDMOperation3.
    if (pOperation != NULL)
    {
        // Create a new file and get the handle. m_File is a global variable
        // that we will use in IWMDMOperation::TransferObjectData.
        // This can also be done when IWMDMOperation::BeginRead is called.
        m_File = CreateFile(
            pwszDestName,   // Destination file name.
            GENERIC_WRITE,  // Write and append writes
            NULL,           // File can't be shared while using, and must be closed.
            NULL,           // Handle can't be inherited.
            CREATE_ALWAYS,  // Overwrite existing files.
            FILE_ATTRIBUTE_NORMAL, // No special attributes.
            NULL            // No template file supplied.
           );
        if (m_File == INVALID_HANDLE_VALUE) return E_FAIL;
        // Modify the Read() method flag. WMDM_CONTENT_FILE and WMDM_CONTENT_FOLDER 
        // are not valid flags when pOperation != NULL.
        flags |= WMDM_CONTENT_OPERATIONINTERFACE;
    }

    // Read the file.
    hr = pStgControl->Read(
             flags,        // Synchronous call specified.
             pwszDestName, // Ignored if pOperation is not NULL.
             NULL,         // No progress callback sent.
             pOperation);  // IWMDMOperation interface, if provided.
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="4f438-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f438-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f438-130">**Creazione di un'applicazione Windows Media Gestione dispositivi**</span><span class="sxs-lookup"><span data-stu-id="4f438-130">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




