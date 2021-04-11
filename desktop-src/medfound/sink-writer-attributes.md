---
description: Attributi del writer di sink
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: Attributi del writer di sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23dbca06c3ff1a4ac80b8e68413fdd0816d71a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130470"
---
# <a name="sink-writer-attributes"></a><span data-ttu-id="59233-103">Attributi del writer di sink</span><span class="sxs-lookup"><span data-stu-id="59233-103">Sink Writer Attributes</span></span>

<span data-ttu-id="59233-104">Gli attributi seguenti possono essere utilizzati per inizializzare il writer del sink.</span><span class="sxs-lookup"><span data-stu-id="59233-104">The following attributes can be used to initialize the sink writer.</span></span>



| <span data-ttu-id="59233-105">Attributo</span><span class="sxs-lookup"><span data-stu-id="59233-105">Attribute</span></span>                                                                                  | <span data-ttu-id="59233-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59233-106">Description</span></span>                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="59233-107">MF \_ bassa \_ latenza</span><span class="sxs-lookup"><span data-stu-id="59233-107">MF\_LOW\_LATENCY</span></span>](mf-low-latency.md)                                                     | <span data-ttu-id="59233-108">Abilita l'elaborazione a bassa latenza.</span><span class="sxs-lookup"><span data-stu-id="59233-108">Enables low-latency processing.</span></span>                                                                                                                                                                                                    |
| [<span data-ttu-id="59233-109">MF \_ ReadWrite \_ Disabilita \_ convertitori</span><span class="sxs-lookup"><span data-stu-id="59233-109">MF\_READWRITE\_DISABLE\_CONVERTERS</span></span>](mf-readwrite-disable-converters.md)                  | <span data-ttu-id="59233-110">Abilita o Disabilita le conversioni di formato dal writer del sink.</span><span class="sxs-lookup"><span data-stu-id="59233-110">Enables or disables format conversions by the sink writer.</span></span>                                                                                                                                                                         |
| [<span data-ttu-id="59233-111">MF \_ ReadWrite \_ Abilita \_ le \_ trasformazioni hardware</span><span class="sxs-lookup"><span data-stu-id="59233-111">MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS</span></span>](mf-readwrite-enable-hardware-transforms.md) | <span data-ttu-id="59233-112">Consente al writer di sink di utilizzare le trasformazioni di Media Foundation basate su hardware (MFTs).</span><span class="sxs-lookup"><span data-stu-id="59233-112">Enables the sink writer to use hardware-based Media Foundation transforms (MFTs).</span></span>                                                                                                                                                  |
| [<span data-ttu-id="59233-113">\_ \_ callback asincrono del writer di sink MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="59233-113">MF\_SINK\_WRITER\_ASYNC\_CALLBACK</span></span>](mf-sink-writer-async-callback.md)                     | <span data-ttu-id="59233-114">Contiene un puntatore all'interfaccia di callback dell'applicazione per il writer del sink.</span><span class="sxs-lookup"><span data-stu-id="59233-114">Contains a pointer to the application's callback interface for the sink writer.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="59233-115">\_disabilitare la \_ limitazione del writer di sink MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="59233-115">MF\_SINK\_WRITER\_DISABLE\_THROTTLING</span></span>](mf-sink-writer-disable-throttling.md)             | <span data-ttu-id="59233-116">Specifica se il writer di sink limita la frequenza dei dati in arrivo.</span><span class="sxs-lookup"><span data-stu-id="59233-116">Specifies whether the sink writer limits the rate of incoming data.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="59233-117">MF \_ transcode \_ CONTAINERTYPE</span><span class="sxs-lookup"><span data-stu-id="59233-117">MF\_TRANSCODE\_CONTAINERTYPE</span></span>](mf-transcode-containertype.md)                             | <span data-ttu-id="59233-118">Specifica il tipo di contenitore del file di output.</span><span class="sxs-lookup"><span data-stu-id="59233-118">Specifies the container type of the output file.</span></span>                                                                                                                                                                                   |
| [<span data-ttu-id="59233-119">\_Attributo di \_ sblocco \_ FIELDOFUSE MFT</span><span class="sxs-lookup"><span data-stu-id="59233-119">MFT\_FIELDOFUSE\_UNLOCK\_Attribute</span></span>](mft-fieldofuse-unlock-attribute.md)                  | <span data-ttu-id="59233-120">Contiene un puntatore [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , che viene usato per sbloccare un MFT con restrizioni di campo di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="59233-120">Contains an [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer, which is used to unlock an MFT with field-of-use restrictions.</span></span> <span data-ttu-id="59233-121">Per ulteriori informazioni, vedere [restrizioni relative all'utilizzo dei campi](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="59233-121">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> |
| [<span data-ttu-id="59233-122">\_ \_ \_ Gestione D3D sink writer \_ MF</span><span class="sxs-lookup"><span data-stu-id="59233-122">MF\_SINK\_WRITER\_D3D\_MANAGER</span></span>](mf-sink-writer-d3d-manager.md)                           | <span data-ttu-id="59233-123">Usare questo attributo per fornire un dispositivo Direct3D per tutti i codificatori video o i sink di supporto caricati dal writer del sink.</span><span class="sxs-lookup"><span data-stu-id="59233-123">Use this attribute to provide a Direct3D device for any video encoders or media sinks loaded by the sink writer.</span></span>                                                                                                                   |



 

<span data-ttu-id="59233-124">Usare questi attributi con i metodi e le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="59233-124">Use these attributes with the following methods and functions:</span></span>

-   [<span data-ttu-id="59233-125">**IMFReadWriteClassFactory::CreateInstanceFromObject**</span><span class="sxs-lookup"><span data-stu-id="59233-125">**IMFReadWriteClassFactory::CreateInstanceFromObject**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [<span data-ttu-id="59233-126">**IMFReadWriteClassFactory::CreateInstanceFromURL**</span><span class="sxs-lookup"><span data-stu-id="59233-126">**IMFReadWriteClassFactory::CreateInstanceFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [<span data-ttu-id="59233-127">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="59233-127">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="59233-128">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="59233-128">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

<span data-ttu-id="59233-129">Per usare uno di questi attributi, chiamare prima [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un nuovo archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="59233-129">To use any of these attributes, first call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span> <span data-ttu-id="59233-130">Usare quindi l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per impostare gli attributi desiderati nell'archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="59233-130">Then use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface to set the desired attributes on the attribute store.</span></span> <span data-ttu-id="59233-131">Passare il puntatore **IMFAttributes** al parametro *pAttributes* di uno dei metodi o delle funzioni elencate in precedenza.</span><span class="sxs-lookup"><span data-stu-id="59233-131">Pass the **IMFAttributes** pointer to the *pAttributes* parameter of any of the methods or functions listed previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59233-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="59233-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59233-133">**IMFSinkWriter**</span><span class="sxs-lookup"><span data-stu-id="59233-133">**IMFSinkWriter**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[<span data-ttu-id="59233-134">Attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59233-134">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



