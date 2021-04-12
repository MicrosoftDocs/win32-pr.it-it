---
title: Creazione di una playlist nel dispositivo
description: Creazione di una playlist nel dispositivo
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Windows Media Gestione dispositivi, playlist
- Gestione dispositivi, playlist
- Guida per programmatori, playlist
- applicazioni desktop, playlist
- creazione di applicazioni Windows Media Gestione dispositivi, playlist
- playlist astratte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287cc406b795db07fde3f10103822dea32185a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329463"
---
# <a name="creating-a-playlist-on-the-device"></a><span data-ttu-id="16b9b-109">Creazione di una playlist nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="16b9b-109">Creating a Playlist on the Device</span></span>

<span data-ttu-id="16b9b-110">Windows Media Gestione dispositivi SDK fornisce i mezzi per un'applicazione MTP per la creazione di una playlist in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="16b9b-110">The Windows Media Device Manager SDK provides the means for an MTP application to create a playlist on a device.</span></span> <span data-ttu-id="16b9b-111">Questo tipo di playlist è denominato playlist *astratta* , perché il file creato nel dispositivo non contiene dati multimediali, ma solo i metadati, che contengono i collegamenti ai file multimediali nella playlist.</span><span class="sxs-lookup"><span data-stu-id="16b9b-111">This type of playlist is called an *abstract* playlist, because the file created on the device contains no media data, but only metadata, which holds the links to media files in the playlist.</span></span>

<span data-ttu-id="16b9b-112">Altri elementi astratti che possono essere creati nel dispositivo includono album (essenzialmente playlist con proprietà aggiuntive, ad esempio copertina), contatti e messaggi.</span><span class="sxs-lookup"><span data-stu-id="16b9b-112">Other abstract items that can be created on the device include albums (essentially playlists with extra properties such as cover art), contacts, and messages.</span></span>

<span data-ttu-id="16b9b-113">**Per creare una playlist**</span><span class="sxs-lookup"><span data-stu-id="16b9b-113">**To create a playlist**</span></span>

1.  <span data-ttu-id="16b9b-114">Acquisire un'interfaccia [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) al dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="16b9b-114">Acquire an [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) interface to the target device.</span></span>
2.  <span data-ttu-id="16b9b-115">Chiamare [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) per ottenere la \_ Proprietà g wszWMDMFormatsSupported.</span><span class="sxs-lookup"><span data-stu-id="16b9b-115">Call [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) to obtain the g\_wszWMDMFormatsSupported property.</span></span>
3.  <span data-ttu-id="16b9b-116">Se non sono supportati formati della playlist, non consentire l'invio di playlist al dispositivo e ignorare i passaggi seguenti.</span><span class="sxs-lookup"><span data-stu-id="16b9b-116">If no playlist formats are supported, disallow sending playlists to the device, and skip the following steps.</span></span> <span data-ttu-id="16b9b-117">In caso contrario, scegliere il codice del formato supportato dal dispositivo che corrisponde maggiormente al tipo di oggetto previsto.</span><span class="sxs-lookup"><span data-stu-id="16b9b-117">Otherwise, choose the device-supported format code that matches most closely the intended object type.</span></span> <span data-ttu-id="16b9b-118">I codici di \_ formato WMDM FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST e WMDM \_ FORMATCODE \_ ABSTRACTAUDIOLAYLIST sono i più comunemente supportati.</span><span class="sxs-lookup"><span data-stu-id="16b9b-118">The generic WMDM\_FORMATCODE\_ABSTRACTAUDIOVIDEOPLAYLIST and WMDM\_FORMATCODE\_ABSTRACTAUDIOLAYLIST format codes are the most commonly supported.</span></span>
4.  <span data-ttu-id="16b9b-119">Ottenere un'interfaccia [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) per l'archiviazione (la radice o una cartella) in cui si desidera creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="16b9b-119">Obtain an [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) interface for the storage (the root or a folder) where you want to create the object.</span></span> <span data-ttu-id="16b9b-120">Alcuni dispositivi funzionano meglio se l'oggetto playlist viene inserito in una cartella di livello superiore denominata "playlists".</span><span class="sxs-lookup"><span data-stu-id="16b9b-120">Some devices work best if the playlist object is placed in a top level folder named "Playlists".</span></span>
5.  <span data-ttu-id="16b9b-121">Creare un oggetto di metadati vuoto usando [**IWMDMStorage3:: CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).</span><span class="sxs-lookup"><span data-stu-id="16b9b-121">Create an empty metadata object by using [**IWMDMStorage3::CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).</span></span>
6.  <span data-ttu-id="16b9b-122">Utilizzando l'interfaccia **IWMDMMetaData** ottenuta nel passaggio precedente, chiamare [**IWMDMMetaData:: AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) per aggiungere il codice di formato scelto (dal passaggio 3) alle proprietà dei metadati di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="16b9b-122">Using the **IWMDMMetaData** interface obtained in the previous step, call [**IWMDMMetaData::AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) to add your chosen format code (from step 3) to the storage metadata properties.</span></span>
7.  <span data-ttu-id="16b9b-123">Ottenere l'interfaccia [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) dall'interfaccia **IWMDMStorage3** .</span><span class="sxs-lookup"><span data-stu-id="16b9b-123">Obtain the [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) interface from the **IWMDMStorage3** interface.</span></span>
8.  <span data-ttu-id="16b9b-124">Chiamare [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) per inserire un nuovo file della playlist nello spazio di archiviazione selezionato.</span><span class="sxs-lookup"><span data-stu-id="16b9b-124">Call [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) to insert a new playlist file in the selected storage.</span></span> <span data-ttu-id="16b9b-125">Questo file contiene i metadati rappresentati dall'interfaccia **IWMDMMetaData** creata nel passaggio 5 e passati a **Insert3**.</span><span class="sxs-lookup"><span data-stu-id="16b9b-125">This file contains the metadata represented by the **IWMDMMetaData** interface you created in step 5 and passed to **Insert3**.</span></span> <span data-ttu-id="16b9b-126">Il metodo restituisce un'interfaccia **IWMDMStorage** per il file della playlist; è possibile eseguire una query per l'interfaccia [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) .</span><span class="sxs-lookup"><span data-stu-id="16b9b-126">The method returns an **IWMDMStorage** interface for the playlist file; you can query for the [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) interface.</span></span>
9.  <span data-ttu-id="16b9b-127">Chiamare [**IWMDMStorage4:: Sereferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) per creare riferimenti alle interfacce **IWMDMStorage** dei file multimediali nella playlist.</span><span class="sxs-lookup"><span data-stu-id="16b9b-127">Call [**IWMDMStorage4::SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) to create references to the **IWMDMStorage** interfaces of the media files in the playlist.</span></span>

<span data-ttu-id="16b9b-128">Per un esempio di codice, vedere la \_ funzione OnCreatePlaylist nell' [applicazione desktop di esempio](sample-desktop-application.md).</span><span class="sxs-lookup"><span data-stu-id="16b9b-128">For example code, see the \_OnCreatePlaylist function in the [Sample Desktop Application](sample-desktop-application.md).</span></span>

> [!Note]  
> <span data-ttu-id="16b9b-129">Il provider di servizi MTP fornito da Microsoft consente a un'applicazione di impostare riferimenti nei metadati.</span><span class="sxs-lookup"><span data-stu-id="16b9b-129">The Microsoft-provided MTP service provider enables an application to set references in metadata.</span></span> <span data-ttu-id="16b9b-130">Per implementare le playlist, l'applicazione deve comunicare con un dispositivo MTP o usare un provider di servizi personalizzato in grado di gestire gli oggetti astratti.</span><span class="sxs-lookup"><span data-stu-id="16b9b-130">To implement playlists, your application must be communicating with an MTP device or using a custom service provider that can handle abstract objects.</span></span> <span data-ttu-id="16b9b-131">Il provider di servizi CE gestisce gli oggetti playlist e album.</span><span class="sxs-lookup"><span data-stu-id="16b9b-131">The CE service provider handles playlist and album objects.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="16b9b-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16b9b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16b9b-133">**Scrittura di file nel dispositivo**</span><span class="sxs-lookup"><span data-stu-id="16b9b-133">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




