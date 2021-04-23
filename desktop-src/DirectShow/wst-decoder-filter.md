---
description: Filtro decodificatore WST
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Filtro decodificatore WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb6804f82e5d15aa324feb163261544969e3c45
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908479"
---
# <a name="wst-decoder-filter"></a><span data-ttu-id="cf8b8-103">Filtro decodificatore WST</span><span class="sxs-lookup"><span data-stu-id="cf8b8-103">WST Decoder Filter</span></span>

<span data-ttu-id="cf8b8-104">Questo componente è stato rimosso da Windows Vista e dai sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="cf8b8-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="cf8b8-105">È disponibile per l'uso nei sistemi operativi Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="cf8b8-105">It is available for use in the Windows XP and Windows Server 2003 operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="cf8b8-106">A partire da Windows Vista, DirectShow non fornisce un filtro per decodificare WST (World Standard Teletext).</span><span class="sxs-lookup"><span data-stu-id="cf8b8-106">Starting in Windows Vista, DirectShow does not provide a filter to decode World Standard Teletext (WST).</span></span>

 

<span data-ttu-id="cf8b8-107">Il decodificatore WST è un filtro in modalità kernel che accetta dati teletext World Standard decodificati dal [codec WST](wst-codec-filter.md) e recapita le bitmap al Pin 2 nel [mixer](overlay-mixer-filter.md) di sovrapposizione usando i tipi di carattere forniti da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cf8b8-107">The WST Decoder is a kernel-mode filter that accepts decoded World Standard Teletext data from the [WST Codec](wst-codec-filter.md) and delivers the bitmaps to Pin 2 on the [Overlay Mixer](overlay-mixer-filter.md) using fonts supplied by Microsoft.</span></span> <span data-ttu-id="cf8b8-108">Al momento sono supportate solo le lingue dell'Europa occidentale. Non sono attualmente disponibili tipi di carattere Unicode.</span><span class="sxs-lookup"><span data-stu-id="cf8b8-108">Only Western European languages are supported at this time; no Unicode fonts are currently provided.</span></span>

<span data-ttu-id="cf8b8-109">Questo filtro può essere aggiunto automaticamente al grafico chiamando [**ICaptureGraphBuilder2::RenderStream,**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)usando il pin di output del codec WST.</span><span class="sxs-lookup"><span data-stu-id="cf8b8-109">This filter can be added to the graph automatically by calling [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), using the output pin of the WST Codec.</span></span>



| <span data-ttu-id="cf8b8-110">Label</span><span class="sxs-lookup"><span data-stu-id="cf8b8-110">Label</span></span> | <span data-ttu-id="cf8b8-111">Valore</span><span class="sxs-lookup"><span data-stu-id="cf8b8-111">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="cf8b8-112">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="cf8b8-112">Filter Interfaces</span></span>                        | <span data-ttu-id="cf8b8-113">ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span><span class="sxs-lookup"><span data-stu-id="cf8b8-113">ISpecifyPropertyPages, [**IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span></span> |
| <span data-ttu-id="cf8b8-114">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="cf8b8-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="cf8b8-115">MEDIATYPE \_ VBI, MEDIASUBTYPE \_ TELETEXT</span><span class="sxs-lookup"><span data-stu-id="cf8b8-115">MEDIATYPE\_VBI, MEDIASUBTYPE\_TELETEXT</span></span>                        |
| <span data-ttu-id="cf8b8-116">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="cf8b8-116">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="cf8b8-117">**IPin**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="cf8b8-118">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="cf8b8-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="cf8b8-119">MEDIATYPE \_ Video</span><span class="sxs-lookup"><span data-stu-id="cf8b8-119">MEDIATYPE\_Video</span></span>                                              |
| <span data-ttu-id="cf8b8-120">Interfacce pin di output</span><span class="sxs-lookup"><span data-stu-id="cf8b8-120">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="cf8b8-121">**IPin**</span><span class="sxs-lookup"><span data-stu-id="cf8b8-121">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="cf8b8-122">CLSID del filtro</span><span class="sxs-lookup"><span data-stu-id="cf8b8-122">Filter CLSID</span></span>                             | <span data-ttu-id="cf8b8-123">CLSID \_ WSTDecoder</span><span class="sxs-lookup"><span data-stu-id="cf8b8-123">CLSID\_WSTDecoder</span></span>                                             |
| <span data-ttu-id="cf8b8-124">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="cf8b8-124">Property Page CLSID</span></span>                      | <span data-ttu-id="cf8b8-125">CLSID \_ WstDecoderPropertyPage</span><span class="sxs-lookup"><span data-stu-id="cf8b8-125">CLSID\_WstDecoderPropertyPage</span></span>                                 |
| <span data-ttu-id="cf8b8-126">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="cf8b8-126">Executable</span></span>                               | <span data-ttu-id="cf8b8-127">Wstdecod.DLL</span><span class="sxs-lookup"><span data-stu-id="cf8b8-127">Wstdecod.DLL</span></span>                                                  |
| [<span data-ttu-id="cf8b8-128">Merito</span><span class="sxs-lookup"><span data-stu-id="cf8b8-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="cf8b8-129">MERITO \_ NORMALE</span><span class="sxs-lookup"><span data-stu-id="cf8b8-129">MERIT\_NORMAL</span></span>                                                 |
| [<span data-ttu-id="cf8b8-130">Categoria filtro</span><span class="sxs-lookup"><span data-stu-id="cf8b8-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="cf8b8-131">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="cf8b8-131">CLSID\_LegacyAmFilterCategory</span></span>                                 |



 

## <a name="related-topics"></a><span data-ttu-id="cf8b8-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cf8b8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf8b8-133">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="cf8b8-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="cf8b8-134">Visualizzazione del teletesto standard del mondo</span><span class="sxs-lookup"><span data-stu-id="cf8b8-134">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



