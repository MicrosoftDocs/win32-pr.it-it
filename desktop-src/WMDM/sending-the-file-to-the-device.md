---
title: Invio del file al dispositivo
description: Invio del file al dispositivo
ms.assetid: 202185b8-f10e-4108-a950-60658c006cec
keywords:
- Windows Media Gestione dispositivi, invio di file ai dispositivi
- Gestione dispositivi, invio di file ai dispositivi
- Guida per programmatori, invio di file ai dispositivi
- applicazioni desktop, invio di file ai dispositivi
- creazione di applicazioni Windows Media Gestione dispositivi, invio di file ai dispositivi
- scrittura di file nei dispositivi, invio di file ai dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65be0c18a6022538dc5573d936f63392234e9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515805"
---
# <a name="sending-the-file-to-the-device"></a><span data-ttu-id="ab155-109">Invio del file al dispositivo</span><span class="sxs-lookup"><span data-stu-id="ab155-109">Sending the File to the Device</span></span>

<span data-ttu-id="ab155-110">Dopo che il file è stato transcodificato, se necessario, e sono stati impostati tutti i metadati che includono il formato, l'applicazione può inviare il file al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab155-110">After the file has been transcoded if necessary, and all metadata including the format has been set, your application can send the file to the device.</span></span> <span data-ttu-id="ab155-111">A tale scopo, è necessario prima di tutto ottenere un'interfaccia **IWMDMStorageControl** (o una versione successiva) per un percorso di destinazione nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab155-111">In order to do so, you must first get an **IWMDMStorageControl** interface (or a later version) for a target location on the device.</span></span> <span data-ttu-id="ab155-112">I flag di **inserimento** specificano se la nuova risorsa di archiviazione deve essere di pari livello o figlio della destinazione.</span><span class="sxs-lookup"><span data-stu-id="ab155-112">The **Insert** flags specify whether the new storage should be a sibling or child of the target.</span></span> <span data-ttu-id="ab155-113">Una volta ottenuta la destinazione, è possibile chiamare [**IWMDMStorageControl:: Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2:: Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)o [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) per trasferire il file.</span><span class="sxs-lookup"><span data-stu-id="ab155-113">Once you have gotten the target, you can call [**IWMDMStorageControl::Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2), or [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) to transfer the file.</span></span> <span data-ttu-id="ab155-114">L'applicazione può gestire la lettura dei dati dei file implementando [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)o può consentire al metodo **Insert** di leggere e trasferire automaticamente il file non fornendo un puntatore a una **IWMDMOperation** implementata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ab155-114">The application can handle reading the file data itself by implementing [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation), or it can allow the **Insert** method to read and transfer the file automatically by not providing a pointer to an application-implemented **IWMDMOperation**.</span></span>

<span data-ttu-id="ab155-115">Nel codice C++ riportato di seguito viene illustrata la chiamata a **Insert3** per scrivere un file in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab155-115">The following C++ code demonstrates calling **Insert3** to write a file to a device.</span></span> <span data-ttu-id="ab155-116">Se il puntatore *pOperation* passato a **Insert3** è **null**, il file verrà inviato in un unico passaggio. Se questo puntatore è un puntatore a interfaccia valido, Windows Media Gestione dispositivi chiamerà il metodo di callback per ottenere i dati in blocchi.</span><span class="sxs-lookup"><span data-stu-id="ab155-116">If the *pOperation* pointer passed to **Insert3** is **NULL**, the file will be sent in one step; if this pointer is a valid interface pointer, Windows Media Device Manager will call your callback method to get data in blocks.</span></span> <span data-ttu-id="ab155-117">Per informazioni dettagliate su come implementare **IWMDMOperation**, vedere [gestione manuale dei trasferimenti di file](handling-file-transfers-manually.md).</span><span class="sxs-lookup"><span data-stu-id="ab155-117">For details on how to implement **IWMDMOperation**, see [Handling File Transfers Manually](handling-file-transfers-manually.md).</span></span>


```C++
// Set the flags for the operation
UINT flags = WMDM_MODE_BLOCK | // Synchronous call. 
    WMDM_STORAGECONTROL_INSERTINTO | // Insert it into the destination folder.
    WMDM_CONTENT_FILE | // We're inserting a file.
    WMDM_FILE_CREATE_OVERWRITE; // Overwrite existing files.
if (pOperation != NULL)
    flags |= WMDM_CONTENT_OPERATIONINTERFACE;

// Send the file and metadata.
hr = pStgCtl3->Insert3(
    flags,
    WMDM_FILE_ATTR_FOLDER, // The current storage is a folder.
    const_cast<WCHAR*>(pwszFileName), // Source file.
    L"My New File.wma",//NULL, // Destination file name.
    pOperation, // NULL to allow the SDK to read the file; 
                // non-NULL to present raw data bytes to the SDK.
    pProgress, // Interface to send simple progress notifications.
    pMetadata, // IWMDMMetaData interface previously created and filled.
    NULL, 
    &pNewStorage); // Out: handle to the new storage, if the method succeeds.
```



## <a name="related-topics"></a><span data-ttu-id="ab155-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ab155-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab155-119">**Scrittura di file nel dispositivo**</span><span class="sxs-lookup"><span data-stu-id="ab155-119">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




