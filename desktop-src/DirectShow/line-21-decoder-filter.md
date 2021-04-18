---
description: Filtro decodificatore riga 21
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Filtro decodificatore riga 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839a6ff8e77f4815b74f5de65b8f0e2a565cdc2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303762"
---
# <a name="line-21-decoder-filter"></a><span data-ttu-id="ab803-103">Filtro decodificatore riga 21</span><span class="sxs-lookup"><span data-stu-id="ab803-103">Line 21 Decoder Filter</span></span>

<span data-ttu-id="ab803-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ab803-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ab803-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="ab803-105">It may be altered or unavailable in subsequent versions.</span></span>

<span data-ttu-id="ab803-106">Questo filtro decodificatore riga 21 decodifica i dati della riga 21 e disegna il testo della didascalia sulle bitmap.</span><span class="sxs-lookup"><span data-stu-id="ab803-106">This Line 21 Decoder filter decodes line 21 data and draws the caption text onto bitmaps.</span></span>

<span data-ttu-id="ab803-107">Il pin di input si connette a un provider di dati della riga 21, in genere un decodificatore video DVD o il filtro [decodificatore CC](cc-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="ab803-107">The input pin connects to any line 21 data provider, typically either a DVD video decoder or the [CC Decoder](cc-decoder-filter.md) filter.</span></span> <span data-ttu-id="ab803-108">Il decodificatore CC fornisce i dati della riga 21 dal VBI di un segnale televisivo analogo.</span><span class="sxs-lookup"><span data-stu-id="ab803-108">The CC Decoder provides line 21 data from the VBI of an analog television signal.</span></span> <span data-ttu-id="ab803-109">Il pin di output si connette a un pin secondario sul [mixer della sovrimpressione](overlay-mixer-filter.md) o a un altro renderer video, ad esempio VMR.</span><span class="sxs-lookup"><span data-stu-id="ab803-109">The output pin connects to a secondary pin on the [Overlay Mixer](overlay-mixer-filter.md) or to another video renderer, such as the VMR.</span></span>

<span data-ttu-id="ab803-110">Questo filtro accetta i dati della riga 21 nel formato standard della coppia di byte oppure, per DVD, come pacchetto per l'intero Group of Pictures (GOP).</span><span class="sxs-lookup"><span data-stu-id="ab803-110">This filter accepts line 21 data in the standard byte-pair format or, for DVD, as a packet for the whole group of pictures (GOP).</span></span> <span data-ttu-id="ab803-111">Per ogni GOP nel flusso video DVD, può essere presente un pacchetto di dati utente con le informazioni di intestazione e i dati della riga 21 specifici del GOP.</span><span class="sxs-lookup"><span data-stu-id="ab803-111">For every GOP in the DVD video stream, there can be a user data packet that has that particular GOP's header information and line 21 data.</span></span> <span data-ttu-id="ab803-112">Il formato delle coppie di byte è definito nello standard EIA/CEA-608-B; Per ulteriori informazioni, fare riferimento a tale standard.</span><span class="sxs-lookup"><span data-stu-id="ab803-112">The format of the byte pairs is defined in the EIA/CEA-608-B standard; please refer to that standard for more information.</span></span>

<span data-ttu-id="ab803-113">Sono disponibili due versioni di questo filtro:</span><span class="sxs-lookup"><span data-stu-id="ab803-113">Two versions of this filter are available:</span></span>



| <span data-ttu-id="ab803-114">Filtra</span><span class="sxs-lookup"><span data-stu-id="ab803-114">Filter</span></span>            | <span data-ttu-id="ab803-115">CLSID</span><span class="sxs-lookup"><span data-stu-id="ab803-115">CLSID</span></span>                 |
|-------------------|-----------------------|
| <span data-ttu-id="ab803-116">Decodificatore riga 21</span><span class="sxs-lookup"><span data-stu-id="ab803-116">Line 21 Decoder</span></span>   | <span data-ttu-id="ab803-117">\_LINE21DECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="ab803-117">CLSID\_Line21Decoder</span></span>  |
| <span data-ttu-id="ab803-118">Decodificatore riga 21 2</span><span class="sxs-lookup"><span data-stu-id="ab803-118">Line 21 Decoder 2</span></span> | <span data-ttu-id="ab803-119">\_LINE21DECODER2 CLSID</span><span class="sxs-lookup"><span data-stu-id="ab803-119">CLSID\_Line21Decoder2</span></span> |



 

<span data-ttu-id="ab803-120">Il filtro versione 1 viene usato nelle piattaforme Microsoft® Windows® 95/98/me e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ab803-120">The version 1 filter is used on Microsoft® Windows® 95/98/Me and Windows 2000 platforms.</span></span> <span data-ttu-id="ab803-121">Il filtro versione 2 è disponibile in Microsoft Windows XP e versioni successive e viene usato ogni volta che il renderer di missaggio video si trova nel grafico.</span><span class="sxs-lookup"><span data-stu-id="ab803-121">The version 2 filter is available in Microsoft Windows XP and later, and is used whenever the Video Mixing Renderer is in the graph.</span></span>

<span data-ttu-id="ab803-122">Le informazioni nella tabella seguente si applicano a entrambe le versioni del filtro:</span><span class="sxs-lookup"><span data-stu-id="ab803-122">The information in the following table applies to both versions of the filter:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ab803-123">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="ab803-123">Filter Interfaces</span></span></td>
<td><span data-ttu-id="ab803-124"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab803-124"><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab803-125">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="ab803-125">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="ab803-126">Tipo principale: MEDIATYPE_AUXLine21DataSubtype:</span><span class="sxs-lookup"><span data-stu-id="ab803-126">Major Type: MEDIATYPE_AUXLine21DataSubtype:</span></span><br/>
<ul>
<li><span data-ttu-id="ab803-127">MEDIASUBTYPE_Line21_BytePair (riga standard 21)</span><span class="sxs-lookup"><span data-stu-id="ab803-127">MEDIASUBTYPE_Line21_BytePair (standard line 21)</span></span></li>
<li><span data-ttu-id="ab803-128">MEDIASUBTYPE_Line21_GOPPacket (riga DVD 21)</span><span class="sxs-lookup"><span data-stu-id="ab803-128">MEDIASUBTYPE_Line21_GOPPacket (DVD line 21)</span></span></li>
</ul>
<span data-ttu-id="ab803-129">Tipo di formato: FORMAT_VideoInfo o GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="ab803-129">Format Type: FORMAT_VideoInfo or GUID_NULL</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab803-130">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="ab803-130">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="ab803-131"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab803-131"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab803-132">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="ab803-132">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="ab803-133">Tipo principale: MEDIATYPE_VideoSubtype:</span><span class="sxs-lookup"><span data-stu-id="ab803-133">Major type: MEDIATYPE_VideoSubtype:</span></span><br/>
<ul>
<li><span data-ttu-id="ab803-134">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="ab803-134">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="ab803-135">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="ab803-135">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="ab803-136">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="ab803-136">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="ab803-137">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="ab803-137">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="ab803-138">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="ab803-138">MEDIASUBTYPE_RGB32</span></span></li>
</ul>
<span data-ttu-id="ab803-139">Tipo formato: FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="ab803-139">Format Type: FORMAT_VideoInfo</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab803-140">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="ab803-140">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="ab803-141"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="ab803-141"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab803-142">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="ab803-142">Filter CLSID</span></span></td>
<td><span data-ttu-id="ab803-143">Vedere la tabella precedente</span><span class="sxs-lookup"><span data-stu-id="ab803-143">See previous table</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab803-144">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="ab803-144">Property Page CLSID</span></span></td>
<td><span data-ttu-id="ab803-145">nessuno</span><span class="sxs-lookup"><span data-stu-id="ab803-145">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab803-146">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="ab803-146">Executable</span></span></td>
<td><span data-ttu-id="ab803-147">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="ab803-147">qdvd.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ab803-148"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="ab803-148"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="ab803-149">Decodificatore riga 21: MERIT_NORMALLine 21 decodificatore 2: MERIT_NORMAL + 2</span><span class="sxs-lookup"><span data-stu-id="ab803-149">Line 21 Decoder: MERIT_NORMALLine 21 Decoder 2: MERIT_NORMAL + 2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ab803-150"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="ab803-150"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="ab803-151">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="ab803-151">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ab803-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ab803-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab803-153">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="ab803-153">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="ab803-154">Didascalie e televideo chiusi</span><span class="sxs-lookup"><span data-stu-id="ab803-154">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> <dt>

[<span data-ttu-id="ab803-155">Configurazione del grafico del filtro DVD</span><span class="sxs-lookup"><span data-stu-id="ab803-155">DVD Filter Graph Configuration</span></span>](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




