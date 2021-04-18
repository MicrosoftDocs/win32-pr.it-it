---
description: Trasferimento di un'immagine o di un file musicale al dispositivo
ms.assetid: bace274c-512a-46da-80a7-84734ee880b7
title: Trasferimento di un'immagine o di un file musicale al dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3308212825f6c67ea79a40873fc466164d62f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316370"
---
# <a name="transferring-an-image-or-music-file-to-the-device"></a><span data-ttu-id="13ebe-103">Trasferimento di un'immagine o di un file musicale al dispositivo</span><span class="sxs-lookup"><span data-stu-id="13ebe-103">Transferring an Image or Music File to the Device</span></span>

<span data-ttu-id="13ebe-104">Una delle operazioni più comuni eseguite da un'applicazione è il trasferimento di contenuto a un dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="13ebe-104">One of the most common operations accomplished by an application is the transfer of content to a connected device.</span></span>

<span data-ttu-id="13ebe-105">I trasferimenti di contenuto vengono eseguiti usando le interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="13ebe-105">Content transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="13ebe-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="13ebe-106">Interface</span></span>                                                                | <span data-ttu-id="13ebe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="13ebe-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="13ebe-108">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="13ebe-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | <span data-ttu-id="13ebe-109">Fornisce l'accesso ai metodi specifici del contenuto.</span><span class="sxs-lookup"><span data-stu-id="13ebe-109">Provides access to the content-specific methods.</span></span>               |
| [<span data-ttu-id="13ebe-110">**Interfaccia IPortableDeviceDataStream**</span><span class="sxs-lookup"><span data-stu-id="13ebe-110">**IPortableDeviceDataStream Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) | <span data-ttu-id="13ebe-111">Usato durante la scrittura del contenuto nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13ebe-111">Used when writing the content to the device.</span></span>                   |
| [<span data-ttu-id="13ebe-112">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="13ebe-112">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)         | <span data-ttu-id="13ebe-113">Utilizzato per recuperare le proprietà che descrivono il contenuto.</span><span class="sxs-lookup"><span data-stu-id="13ebe-113">Used to retrieve properties that describe the content.</span></span>         |
| <span data-ttu-id="13ebe-114">Interfaccia IStream</span><span class="sxs-lookup"><span data-stu-id="13ebe-114">IStream Interface</span></span>                                                        | <span data-ttu-id="13ebe-115">Usato per semplificare la lettura del contenuto e la scrittura nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13ebe-115">Used to simplify reading of content and writing to the device.</span></span> |



 

<span data-ttu-id="13ebe-116">La `TransferContentToDevice` funzione nel modulo ContentTransfer. cpp dell'applicazione di esempio illustra come un'applicazione può trasferire il contenuto da un PC a un dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="13ebe-116">The `TransferContentToDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer content from a PC to a connected device.</span></span> <span data-ttu-id="13ebe-117">In questo particolare esempio, il contenuto trasferito può essere un file contenente un'immagine, una musica o informazioni di contatto.</span><span class="sxs-lookup"><span data-stu-id="13ebe-117">In this particular sample, the transferred content can be a file containing an image, music, or contact information.</span></span>

<span data-ttu-id="13ebe-118">La prima attività eseguita dalla `TransferContentToDevice` funzione consiste nel richiedere all'utente di immettere un identificatore di oggetto, che identifica l'oggetto da trasferire.</span><span class="sxs-lookup"><span data-stu-id="13ebe-118">The first task accomplished by the `TransferContentToDevice` function is to prompt the user to enter an object identifier, which identifies the object to be transferred.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
WCHAR                               szFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IPortableDeviceDataStream>  pFinalObjectDataStream;
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IStream>                    pTempStream;  // Temporary IStream which we use to QI for IPortableDeviceDataStream

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the file will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



<span data-ttu-id="13ebe-119">La seconda attività eseguita dalla `TransferContentToDevice` funzione consiste nel creare un oggetto [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) chiamando il metodo [**IPortableDevice:: content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .</span><span class="sxs-lookup"><span data-stu-id="13ebe-119">The second task accomplished by the `TransferContentToDevice` function is to create an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object by calling the [**IPortableDevice::Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) method.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="13ebe-120">L'attività successiva eseguita dalla `TransferContentToDevice` funzione è la creazione di una finestra di dialogo **FileOpen** con la quale l'utente può specificare il percorso e il nome del file da trasferire.</span><span class="sxs-lookup"><span data-stu-id="13ebe-120">The next task accomplished by the `TransferContentToDevice` function is the creation of a **FileOpen** dialog with which the user can specify the location and name of the file to be transferred.</span></span>


```C++
if (SUCCEEDED(hr))
{
    OPENFILENAME OpenFileNameInfo   = {0};

    OpenFileNameInfo.lStructSize    = sizeof(OPENFILENAME);
    OpenFileNameInfo.hwndOwner      = NULL;
    OpenFileNameInfo.lpstrFile      = szFilePath;
    OpenFileNameInfo.nMaxFile       = ARRAYSIZE(szFilePath);
    OpenFileNameInfo.lpstrFilter    = pszFileTypeFilter;
    OpenFileNameInfo.nFilterIndex   = 1;
    OpenFileNameInfo.Flags          = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;
    OpenFileNameInfo.lpstrDefExt    = pszDefaultFileExtension;

    if (GetOpenFileName(&OpenFileNameInfo) == FALSE)
    {
        printf("The transfer operation was canceled.\n");
        hr = E_ABORT;
    }
}
```



<span data-ttu-id="13ebe-121">La `TransferContentToDevice` funzione passa una stringa di filtro ( `wszFileTypeFilter` ) al metodo GetOpenFilename, che determina il tipo di file che l'utente può scegliere.</span><span class="sxs-lookup"><span data-stu-id="13ebe-121">The `TransferContentToDevice` function passes a filter string (`wszFileTypeFilter`) to the GetOpenFileName method, which determines the type of files that the user can choose.</span></span> <span data-ttu-id="13ebe-122">`DoMenu`Per esempi dei tre diversi filtri consentiti dall'esempio, vedere la funzione nel modulo WpdApiSample. cpp.</span><span class="sxs-lookup"><span data-stu-id="13ebe-122">Refer to the `DoMenu` function in the WpdApiSample.cpp module for examples of the three different filters allowed by the sample.</span></span>

<span data-ttu-id="13ebe-123">Dopo che l'utente ha identificato un determinato file per il trasferimento al dispositivo, la `TransferContentToDevice` funzione apre il file come oggetto IStream e recupera le proprietà necessarie per completare il trasferimento.</span><span class="sxs-lookup"><span data-stu-id="13ebe-123">After the user identifies a particular file for transfer to the device, the `TransferContentToDevice` function opens that file as an IStream object and retrieves properties that are required to complete the transfer.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Open the selected file as an IStream.  This will simplify reading the
    // data and writing to the device.
    hr = SHCreateStreamOnFile(szFilePath, STGM_READ, &pFileStream);
    if (SUCCEEDED(hr))
    {
        // Get the required properties needed to properly describe the data being
        // transferred to the device.
        hr = GetRequiredPropertiesForContentType(guidContentType,           // Content type of the data
                                                 szSelection,              // Parent to transfer the data under
                                                 szFilePath,               // Full file path to the data file
                                                 pFileStream,               // Open IStream that contains the data
                                                 &pFinalObjectProperties);  // Returned properties describing the data
        if (FAILED(hr))
        {
            printf("! Failed to get required properties needed to transfer a file to the device, hr = 0x%lx\n", hr);
        }
    }

    if (FAILED(hr))
    {
        printf("! Failed to open file named (%ws) to transfer to device, hr = 0x%lx\n",szFilePath, hr);
    }
}
```



<span data-ttu-id="13ebe-124">Le proprietà obbligatorie vengono recuperate chiamando la `GetRequiredPropertiesForContentType` funzione helper, che agisce sull'oggetto IStream.</span><span class="sxs-lookup"><span data-stu-id="13ebe-124">The required properties are retrieved by calling the`GetRequiredPropertiesForContentType` helper-function, which operates on the IStream object.</span></span> <span data-ttu-id="13ebe-125">La `GetRequiredPropertiesForContentType` funzione helper crea un oggetto [**IPortableDeviceValues**](iportabledevicevalues.md) , recupera le proprietà nell'elenco seguente e le aggiunge all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="13ebe-125">The `GetRequiredPropertiesForContentType` helper-function creates an [**IPortableDeviceValues**](iportabledevicevalues.md) object, retrieves the properties in the following list, and adds them to this object.</span></span>

-   <span data-ttu-id="13ebe-126">Identificatore oggetto padre</span><span class="sxs-lookup"><span data-stu-id="13ebe-126">Parent-object identifier</span></span>
-   <span data-ttu-id="13ebe-127">Dimensioni del flusso in byte</span><span class="sxs-lookup"><span data-stu-id="13ebe-127">Stream size in bytes</span></span>
-   <span data-ttu-id="13ebe-128">Nome file di contenuto</span><span class="sxs-lookup"><span data-stu-id="13ebe-128">Content file name</span></span>
-   <span data-ttu-id="13ebe-129">Nome del contenuto (il nome del file senza estensione)</span><span class="sxs-lookup"><span data-stu-id="13ebe-129">Content name (the file name without the extension)</span></span>
-   <span data-ttu-id="13ebe-130">Tipo di contenuto (immagine, audio o contatto)</span><span class="sxs-lookup"><span data-stu-id="13ebe-130">Content type (image, audio, or contact)</span></span>
-   <span data-ttu-id="13ebe-131">Formato del contenuto (JFIF, WMA o vCard2)</span><span class="sxs-lookup"><span data-stu-id="13ebe-131">Content format (JFIF, WMA, or vCard2)</span></span>

<span data-ttu-id="13ebe-132">L'applicazione di esempio usa le proprietà recuperate per creare il nuovo contenuto nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13ebe-132">The sample application uses the retrieved properties to create the new content on the device.</span></span> <span data-ttu-id="13ebe-133">Questa operazione viene eseguita in tre fasi:</span><span class="sxs-lookup"><span data-stu-id="13ebe-133">This is done in three phases:</span></span>

1.  <span data-ttu-id="13ebe-134">L'applicazione chiama il metodo [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) per creare un nuovo oggetto IStream sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="13ebe-134">The application calls [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) method to create a new IStream object on the device.</span></span>
2.  <span data-ttu-id="13ebe-135">L'applicazione usa questo oggetto per ottenere un oggetto [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) dal driver WPD.</span><span class="sxs-lookup"><span data-stu-id="13ebe-135">The application uses this object to obtain an [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) object from the WPD driver.</span></span>
3.  <span data-ttu-id="13ebe-136">L'applicazione usa il nuovo oggetto **IPortableDeviceDataStream** per scrivere il contenuto nel dispositivo (tramite la funzione helper StreamCopy).</span><span class="sxs-lookup"><span data-stu-id="13ebe-136">The application uses the new **IPortableDeviceDataStream** object to write the content to the device (via the StreamCopy helper function).</span></span> <span data-ttu-id="13ebe-137">La funzione helper scrive i dati dal file di origine nel flusso restituito da [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="13ebe-137">The helper function writes the data from the source file to the stream returned by [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span>
4.  <span data-ttu-id="13ebe-138">L'applicazione completa l'operazione chiamando il metodo commit nel flusso di destinazione.</span><span class="sxs-lookup"><span data-stu-id="13ebe-138">The application completes the operation by calling the Commit method on the destination stream.</span></span>


```C++
// 4) Transfer for the content to the device
if (SUCCEEDED(hr))
{
    hr = pContent->CreateObjectWithPropertiesAndData(pFinalObjectProperties,    // Properties describing the object data
                                                     &pTempStream,              // Returned object data stream (to transfer the data to)
                                                     &cbOptimalTransferSize,    // Returned optimal buffer size to use during transfer
                                                     NULL);

    // Once we have a the IStream returned from CreateObjectWithPropertiesAndData,
    // QI for IPortableDeviceDataStream so we can use the additional methods
    // to get more information about the object (i.e. The newly created object
    // identifier on the device)
    if (SUCCEEDED(hr))
    {
        hr = pTempStream->QueryInterface(IID_PPV_ARGS(&pFinalObjectDataStream));
        if (FAILED(hr))
        {
            printf("! Failed to QueryInterface for IPortableDeviceDataStream, hr = 0x%lx\n",hr);
        }
    }

    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    if (SUCCEEDED(hr))
    {
        DWORD cbTotalBytesWritten = 0;

        hr = StreamCopy(pFinalObjectDataStream, // Destination (The Object to transfer to)
                        pFileStream,            // Source (The File data to transfer from)
                        cbOptimalTransferSize,  // The driver specified optimal transfer buffer size
                        &cbTotalBytesWritten);  // The total number of bytes transferred from file to the device
        if (FAILED(hr))
        {
            printf("! Failed to transfer object to device, hr = 0x%lx\n",hr);
        }
    }
    else
    {
        printf("! Failed to get IStream (representing destination object data on the device) from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // After transferring content to the device, the client is responsible for letting the
    // driver know that the transfer is complete by calling the Commit() method
    // on the IPortableDeviceDataStream interface.
    if (SUCCEEDED(hr))
    {
        hr = pFinalObjectDataStream->Commit(0);
        if (FAILED(hr))
        {
            printf("! Failed to commit object to device, hr = 0x%lx\n",hr);
        }
    }

    // Some clients may want to know the object identifier of the newly created
    // object.  This is done by calling GetObjectID() method on the
    // IPortableDeviceDataStream interface.
    if (SUCCEEDED(hr))
    {
        PWSTR pszNewlyCreatedObject = NULL;
        hr = pFinalObjectDataStream->GetObjectID(&pszNewlyCreatedObject);
        if (SUCCEEDED(hr))
        {
            printf("The file '%ws' was transferred to the device.\nThe newly created object's ID is '%ws'\n",szFilePath ,pszNewlyCreatedObject);
        }

        if (FAILED(hr))
        {
            printf("! Failed to get the newly transferred object's identifier from the device, hr = 0x%lx\n",hr);
        }

        // Free the object identifier string returned from the GetObjectID() method.
        CoTaskMemFree(pszNewlyCreatedObject);
        pszNewlyCreatedObject = NULL;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="13ebe-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="13ebe-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13ebe-140">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="13ebe-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="13ebe-141">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="13ebe-141">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="13ebe-142">**Interfaccia IPortableDeviceDataStream**</span><span class="sxs-lookup"><span data-stu-id="13ebe-142">**IPortableDeviceDataStream Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)
</dt> <dt>

[<span data-ttu-id="13ebe-143">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="13ebe-143">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="13ebe-144">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="13ebe-144">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



