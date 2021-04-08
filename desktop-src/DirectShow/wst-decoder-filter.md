---
description: Filtro decodificatore WST
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Filtro decodificatore WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f2d20873ff9a5e7c009c4a84f7a23c273d6590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880026"
---
# <a name="wst-decoder-filter"></a><span data-ttu-id="9f784-103">Filtro decodificatore WST</span><span class="sxs-lookup"><span data-stu-id="9f784-103">WST Decoder Filter</span></span>

<span data-ttu-id="9f784-104">Questo componente è stato rimosso da Windows Vista e dai sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="9f784-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="9f784-105">È disponibile per l'uso nei sistemi operativi Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9f784-105">It is available for use in the Windows XP and Windows Server 2003 operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="9f784-106">A partire da Windows Vista, DirectShow non fornisce un filtro per decodificare il televideo standard del mondo (WST).</span><span class="sxs-lookup"><span data-stu-id="9f784-106">Starting in Windows Vista, DirectShow does not provide a filter to decode World Standard Teletext (WST).</span></span>

 

<span data-ttu-id="9f784-107">Il decodificatore WST è un filtro in modalità kernel che accetta dati del televideo standard del mondo decodificati dal [codec WST](wst-codec-filter.md) e recapita le bitmap al pin 2 sul [mixer sovrapposto](overlay-mixer-filter.md) usando i tipi di carattere forniti da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9f784-107">The WST Decoder is a kernel-mode filter that accepts decoded World Standard Teletext data from the [WST Codec](wst-codec-filter.md) and delivers the bitmaps to Pin 2 on the [Overlay Mixer](overlay-mixer-filter.md) using fonts supplied by Microsoft.</span></span> <span data-ttu-id="9f784-108">Al momento sono supportate solo le lingue europee occidentali; non sono attualmente disponibili tipi di carattere Unicode.</span><span class="sxs-lookup"><span data-stu-id="9f784-108">Only Western European languages are supported at this time; no Unicode fonts are currently provided.</span></span>

<span data-ttu-id="9f784-109">Questo filtro può essere aggiunto automaticamente al grafico chiamando [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), usando il pin di output del codec WST.</span><span class="sxs-lookup"><span data-stu-id="9f784-109">This filter can be added to the graph automatically by calling [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), using the output pin of the WST Codec.</span></span>



|                                          |                                                               |
|------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9f784-110">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="9f784-110">Filter Interfaces</span></span>                        | <span data-ttu-id="9f784-111">ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span><span class="sxs-lookup"><span data-stu-id="9f784-111">ISpecifyPropertyPages, [**IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span></span> |
| <span data-ttu-id="9f784-112">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="9f784-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="9f784-113">MEDIATYPE \_ VBI, MEDIASUBTYPE \_ Teletext</span><span class="sxs-lookup"><span data-stu-id="9f784-113">MEDIATYPE\_VBI, MEDIASUBTYPE\_TELETEXT</span></span>                        |
| <span data-ttu-id="9f784-114">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="9f784-114">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="9f784-115">**IPin**</span><span class="sxs-lookup"><span data-stu-id="9f784-115">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="9f784-116">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="9f784-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="9f784-117">Video di MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="9f784-117">MEDIATYPE\_Video</span></span>                                              |
| <span data-ttu-id="9f784-118">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="9f784-118">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="9f784-119">**IPin**</span><span class="sxs-lookup"><span data-stu-id="9f784-119">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="9f784-120">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="9f784-120">Filter CLSID</span></span>                             | <span data-ttu-id="9f784-121">\_WSTDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="9f784-121">CLSID\_WSTDecoder</span></span>                                             |
| <span data-ttu-id="9f784-122">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="9f784-122">Property Page CLSID</span></span>                      | <span data-ttu-id="9f784-123">\_WSTDECODERPROPERTYPAGE CLSID</span><span class="sxs-lookup"><span data-stu-id="9f784-123">CLSID\_WstDecoderPropertyPage</span></span>                                 |
| <span data-ttu-id="9f784-124">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="9f784-124">Executable</span></span>                               | <span data-ttu-id="9f784-125">Wstdecod.DLL</span><span class="sxs-lookup"><span data-stu-id="9f784-125">Wstdecod.DLL</span></span>                                                  |
| [<span data-ttu-id="9f784-126">Merito</span><span class="sxs-lookup"><span data-stu-id="9f784-126">Merit</span></span>](merit.md)                       | <span data-ttu-id="9f784-127">VALORE \_ normale</span><span class="sxs-lookup"><span data-stu-id="9f784-127">MERIT\_NORMAL</span></span>                                                 |
| [<span data-ttu-id="9f784-128">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="9f784-128">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="9f784-129">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="9f784-129">CLSID\_LegacyAmFilterCategory</span></span>                                 |



 

## <a name="related-topics"></a><span data-ttu-id="9f784-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9f784-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f784-131">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="9f784-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="9f784-132">Visualizzazione del televideo standard internazionale</span><span class="sxs-lookup"><span data-stu-id="9f784-132">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



