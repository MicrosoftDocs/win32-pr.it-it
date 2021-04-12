---
title: Recupero delle informazioni di configurazione dei flussi dai codec
description: Recupero delle informazioni di configurazione dei flussi dai codec
ms.assetid: 76c734a1-6fe4-4958-8773-a65f5ced80c6
keywords:
- flussi, configurazioni da codec
- codec, recupero di configurazioni di flusso
- flussi, formati di codec
- codec, formati
- flussi, interfaccia IWMCodecInfo
- IWMCodecInfo, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8657e03af97f9e4f1cae953d541c0e4369da193
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "104398746"
---
# <a name="getting-stream-configuration-information-from-codecs"></a><span data-ttu-id="d300e-109">Recupero delle informazioni di configurazione dei flussi dai codec</span><span class="sxs-lookup"><span data-stu-id="d300e-109">Getting Stream Configuration Information from Codecs</span></span>

<span data-ttu-id="d300e-110">Per i flussi audio e video che usano i codec Windows Media Audio e video, è necessario ottenere i valori per le strutture di configurazione del flusso dal codec che si vuole usare.</span><span class="sxs-lookup"><span data-stu-id="d300e-110">For audio and video streams that use the Windows Media Audio and Video codecs, you should get the values for the stream configuration structures from the codec you want to use.</span></span> <span data-ttu-id="d300e-111">Sebbene sia possibile impostare questi valori manualmente, l'uso dei codec garantisce che i valori siano accurati.</span><span class="sxs-lookup"><span data-stu-id="d300e-111">While it is possible to set these values yourself, using the codecs ensures that the values are accurate.</span></span> <span data-ttu-id="d300e-112">Non modificare i valori in queste strutture, a meno che nella documentazione non venga consigliata una modifica specifica.</span><span class="sxs-lookup"><span data-stu-id="d300e-112">You should not alter the values in these structures unless the documentation specifically recommends a particular change.</span></span>

<span data-ttu-id="d300e-113">Le informazioni dei codec sono costituite da formati di codec.</span><span class="sxs-lookup"><span data-stu-id="d300e-113">Information from the codecs comes in the form of codec formats.</span></span> <span data-ttu-id="d300e-114">Ogni formato di codec è un formato di flusso singolo supportato dal codec.</span><span class="sxs-lookup"><span data-stu-id="d300e-114">Each codec format is a single stream format supported by the codec.</span></span> <span data-ttu-id="d300e-115">Per ulteriori informazioni sui formati di flusso, vedere [formati](formats.md).</span><span class="sxs-lookup"><span data-stu-id="d300e-115">For more information about stream formats, see [Formats](formats.md).</span></span>

<span data-ttu-id="d300e-116">È possibile richiedere informazioni dai codec Windows Media usando le interfacce [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)e [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) dell'oggetto Profile Manager.</span><span class="sxs-lookup"><span data-stu-id="d300e-116">You can request information from the Windows Media codecs using the [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo), [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2), and [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) interfaces of the profile manager object.</span></span> <span data-ttu-id="d300e-117">Per ottenere l'interfaccia [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) di un oggetto di gestione profilo, chiamare la funzione [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="d300e-117">To get the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface of a profile manager object, call the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span> <span data-ttu-id="d300e-118">Chiamare **QueryInterface** su **IWMProfileManager** per ottenere **IWMCodecInfo3**.</span><span class="sxs-lookup"><span data-stu-id="d300e-118">Call **QueryInterface** on **IWMProfileManager** to get **IWMCodecInfo3**.</span></span>

<span data-ttu-id="d300e-119">Le sezioni seguenti descrivono come ottenere le informazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="d300e-119">The following sections describe how to get the information you need.</span></span>



| <span data-ttu-id="d300e-120">Sezione</span><span class="sxs-lookup"><span data-stu-id="d300e-120">Section</span></span>                                                                                                | <span data-ttu-id="d300e-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d300e-121">Description</span></span>                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d300e-122">Per enumerare tutti i codec Windows Media installati</span><span class="sxs-lookup"><span data-stu-id="d300e-122">To Enumerate All Installed Windows Media Codecs</span></span>](to-enumerate-all-installed-windows-media-codecs.md) | <span data-ttu-id="d300e-123">Viene descritto come utilizzare i metodi delle interfacce **IWMCodecInfo** e **IWMCodecInfo2** per recuperare il nome e l'indice di codec di ciascun codec Windows Media installato.</span><span class="sxs-lookup"><span data-stu-id="d300e-123">Describes how to use the methods of the **IWMCodecInfo** and **IWMCodecInfo2** interfaces to retrieve the name and codec index of each Windows Media codec installed.</span></span> |
| [<span data-ttu-id="d300e-124">Per enumerare i formati di codec</span><span class="sxs-lookup"><span data-stu-id="d300e-124">To Enumerate Codec Formats</span></span>](to-enumerate-codec-formats.md)                                           | <span data-ttu-id="d300e-125">Viene descritto come ottenere oggetti di configurazione del flusso dai codec da usare nei profili.</span><span class="sxs-lookup"><span data-stu-id="d300e-125">Describes how to get stream configuration objects from codecs for use in your profiles.</span></span>                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="d300e-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d300e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d300e-127">**Configurazione di flussi**</span><span class="sxs-lookup"><span data-stu-id="d300e-127">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




