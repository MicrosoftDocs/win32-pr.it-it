---
description: Interfacce di codifica e decodifica di file
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Interfacce di codifica e decodifica di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73de2304f2b473a634127755ca900b99592ed63
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125595"
---
# <a name="file-encoding-and-decoding-interfaces"></a><span data-ttu-id="f834e-103">Interfacce di codifica e decodifica di file</span><span class="sxs-lookup"><span data-stu-id="f834e-103">File Encoding and Decoding Interfaces</span></span>

<span data-ttu-id="f834e-104">Queste interfacce supportano la codifica e la decodifica dei file.</span><span class="sxs-lookup"><span data-stu-id="f834e-104">These interfaces support file encoding and decoding.</span></span>



| <span data-ttu-id="f834e-105">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="f834e-105">Interface</span></span>                                                    | <span data-ttu-id="f834e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f834e-106">Description</span></span>                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f834e-107">**IAMMediaContent**</span><span class="sxs-lookup"><span data-stu-id="f834e-107">**IAMMediaContent**</span></span>](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | <span data-ttu-id="f834e-108">Recuperare i metadati da un flusso, ad esempio l'autore e il titolo.</span><span class="sxs-lookup"><span data-stu-id="f834e-108">Retrieve meta-data from a stream, such as the author and title.</span></span>                                              |
| [<span data-ttu-id="f834e-109">**IAMOpenProgress**</span><span class="sxs-lookup"><span data-stu-id="f834e-109">**IAMOpenProgress**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | <span data-ttu-id="f834e-110">Determinare lo stato di avanzamento di un'operazione di apertura file.</span><span class="sxs-lookup"><span data-stu-id="f834e-110">Determine the progress of a file-open operation.</span></span>                                                             |
| [<span data-ttu-id="f834e-111">**IAMParse**</span><span class="sxs-lookup"><span data-stu-id="f834e-111">**IAMParse**</span></span>](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | <span data-ttu-id="f834e-112">Eseguire una query e impostare il tempo di analisi per la posizione corrente in un flusso MPEG.</span><span class="sxs-lookup"><span data-stu-id="f834e-112">Query and set the parse time for the current position in an MPEG stream.</span></span>                                     |
| [<span data-ttu-id="f834e-113">**IAMStreamSelect**</span><span class="sxs-lookup"><span data-stu-id="f834e-113">**IAMStreamSelect**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | <span data-ttu-id="f834e-114">Controllare quali flussi logici vengono riprodotti e recuperare le relative informazioni.</span><span class="sxs-lookup"><span data-stu-id="f834e-114">Control which logical streams are played, and retrieve information about them.</span></span>                               |
| [<span data-ttu-id="f834e-115">**IAMVfwCompressDialogs**</span><span class="sxs-lookup"><span data-stu-id="f834e-115">**IAMVfwCompressDialogs**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | <span data-ttu-id="f834e-116">Visualizzare le finestre di dialogo fornite dai codec VFW.</span><span class="sxs-lookup"><span data-stu-id="f834e-116">Display dialog boxes provided by VFW codecs.</span></span>                                                                 |
| [<span data-ttu-id="f834e-117">**IAMVideoCompression**</span><span class="sxs-lookup"><span data-stu-id="f834e-117">**IAMVideoCompression**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | <span data-ttu-id="f834e-118">Imposta i parametri di compressione video.</span><span class="sxs-lookup"><span data-stu-id="f834e-118">Set video compression parameters.</span></span>                                                                            |
| [<span data-ttu-id="f834e-119">**IConfigAsfWriter**</span><span class="sxs-lookup"><span data-stu-id="f834e-119">**IConfigAsfWriter**</span></span>](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | <span data-ttu-id="f834e-120">Controllare il modo in cui il filtro del [writer WM ASF](wm-asf-writer-filter.md) scrive i file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="f834e-120">Control how the [WM ASF Writer](wm-asf-writer-filter.md) filter writes Advanced Systems Format (ASF) files.</span></span> |
| [<span data-ttu-id="f834e-121">**IConfigAviMux**</span><span class="sxs-lookup"><span data-stu-id="f834e-121">**IConfigAviMux**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | <span data-ttu-id="f834e-122">Controllare il modo in cui il filtro [Mux AVI](avi-mux-filter.md) scrive i file AVI.</span><span class="sxs-lookup"><span data-stu-id="f834e-122">Control how the [AVI Mux](avi-mux-filter.md) filter writes AVI files.</span></span>                                       |
| [<span data-ttu-id="f834e-123">**IConfigInterleaving**</span><span class="sxs-lookup"><span data-stu-id="f834e-123">**IConfigInterleaving**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | <span data-ttu-id="f834e-124">Configurare l'interfoliazione quando il filtro Mux AVI scrive file AVI.</span><span class="sxs-lookup"><span data-stu-id="f834e-124">Configure interleaving when the AVI Mux filter writes AVI files.</span></span>                                             |
| [<span data-ttu-id="f834e-125">**IDVEnc**</span><span class="sxs-lookup"><span data-stu-id="f834e-125">**IDVEnc**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | <span data-ttu-id="f834e-126">Impostare la risoluzione della codifica sul filtro del [codificatore video DV](dv-video-encoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="f834e-126">Set the encoding resolution on the [DV Video Encoder](dv-video-encoder-filter.md) filter.</span></span>                   |
| [<span data-ttu-id="f834e-127">**IDVSplitter**</span><span class="sxs-lookup"><span data-stu-id="f834e-127">**IDVSplitter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | <span data-ttu-id="f834e-128">Effettuare il downgrade della frequenza dei fotogrammi in un flusso video digitale (DV)</span><span class="sxs-lookup"><span data-stu-id="f834e-128">Downgrade the frame rate on a digital video (DV) stream</span></span>                                                      |
| [<span data-ttu-id="f834e-129">**IIPDVDec**</span><span class="sxs-lookup"><span data-stu-id="f834e-129">**IIPDVDec**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | <span data-ttu-id="f834e-130">Impostare la risoluzione della decodifica sul filtro del decodificatore [video DV](dv-video-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="f834e-130">Set the decoding resolution on the [DV Video Decoder](dv-video-decoder-filter.md) filter.</span></span>                   |
| [<span data-ttu-id="f834e-131">**IPersistMediaPropertyBag**</span><span class="sxs-lookup"><span data-stu-id="f834e-131">**IPersistMediaPropertyBag**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | <span data-ttu-id="f834e-132">Impostare e recuperare i blocchi INFO e DISP nei flussi AVI.</span><span class="sxs-lookup"><span data-stu-id="f834e-132">Set and retrieve INFO and DISP chunks in AVI streams.</span></span>                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="f834e-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f834e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f834e-134">Interfacce</span><span class="sxs-lookup"><span data-stu-id="f834e-134">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 



