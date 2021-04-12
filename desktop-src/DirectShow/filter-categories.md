---
description: Nelle tabelle seguenti sono elencati i CLSID per le categorie di filtro DirectShow.
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: Filtra categorie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4ccb9443c405abcbd0b9afbd406d6faf2558a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401079"
---
# <a name="filter-categories"></a><span data-ttu-id="03efb-103">Filtra categorie</span><span class="sxs-lookup"><span data-stu-id="03efb-103">Filter Categories</span></span>

<span data-ttu-id="03efb-104">Nelle tabelle seguenti sono elencati i CLSID per le categorie di filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="03efb-104">The following tables list the CLSIDs for the DirectShow filter categories.</span></span>

-   [<span data-ttu-id="03efb-105">Categorie filtro DirectShow</span><span class="sxs-lookup"><span data-stu-id="03efb-105">DirectShow Filter Categories</span></span>](#directshow-filter-categories)
-   [<span data-ttu-id="03efb-106">Altre categorie di filtro</span><span class="sxs-lookup"><span data-stu-id="03efb-106">Other Filter Categories</span></span>](#other-filter-categories)
-   [<span data-ttu-id="03efb-107">Meta-categoria del filtro DirectShow</span><span class="sxs-lookup"><span data-stu-id="03efb-107">DirectShow Filter Meta-Category</span></span>](#directshow-filter-meta-category)
-   [<span data-ttu-id="03efb-108">Categorie DMO</span><span class="sxs-lookup"><span data-stu-id="03efb-108">DMO Categories</span></span>](#dmo-categories)
-   [<span data-ttu-id="03efb-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03efb-109">Related topics</span></span>](#related-topics)

## <a name="directshow-filter-categories"></a><span data-ttu-id="03efb-110">Categorie filtro DirectShow</span><span class="sxs-lookup"><span data-stu-id="03efb-110">DirectShow Filter Categories</span></span>

<span data-ttu-id="03efb-111">Le categorie elencate di seguito vengono enumerate dal [mapper dei filtri](filter-mapper.md).</span><span class="sxs-lookup"><span data-stu-id="03efb-111">The categories listed here are enumerated by the [Filter Mapper](filter-mapper.md).</span></span> <span data-ttu-id="03efb-112">Per impostazione predefinita, tuttavia, il mapper dei filtri ignora le categorie con meriti di \_ merito \_ non \_ usare o meno.</span><span class="sxs-lookup"><span data-stu-id="03efb-112">By default, however, the Filter Mapper ignores categories with merits of MERIT\_DO\_NOT\_USE or less.</span></span> <span data-ttu-id="03efb-113">Per ulteriori informazioni, vedere [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters).</span><span class="sxs-lookup"><span data-stu-id="03efb-113">For more information, see [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters).</span></span> <span data-ttu-id="03efb-114">Tutte le categorie elencate di seguito possono essere enumerate anche con l' [enumeratore di dispositivo di sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="03efb-114">All of the categories listed here can also be enumerated with the [System Device Enumerator](system-device-enumerator.md).</span></span>

<span data-ttu-id="03efb-115">Le categorie seguenti sono dichiarate in UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="03efb-115">The following categories are declared in Uuids.h.</span></span> <span data-ttu-id="03efb-116">Includere il file di intestazione dshow. h.</span><span class="sxs-lookup"><span data-stu-id="03efb-116">Include the header file Dshow.h.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03efb-117">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="03efb-117">Friendly Name</span></span></th>
<th><span data-ttu-id="03efb-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="03efb-118">CLSID</span></span></th>
<th><span data-ttu-id="03efb-119">Merito</span><span class="sxs-lookup"><span data-stu-id="03efb-119">Merit</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03efb-120">Origini di acquisizione audio</span><span class="sxs-lookup"><span data-stu-id="03efb-120">Audio Capture Sources</span></span></td>
<td><span data-ttu-id="03efb-121"><strong>CLSID_AudioInputDeviceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-121"><strong>CLSID_AudioInputDeviceCategory</strong></span></span></td>
<td><span data-ttu-id="03efb-122"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-122"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03efb-123">Commediatori audio</span><span class="sxs-lookup"><span data-stu-id="03efb-123">Audio Compressors</span></span></td>
<td><span data-ttu-id="03efb-124"><strong>CLSID_AudioCompressorCategory</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-124"><strong>CLSID_AudioCompressorCategory</strong></span></span></td>
<td><span data-ttu-id="03efb-125"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-125"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03efb-126">Renderer audio</span><span class="sxs-lookup"><span data-stu-id="03efb-126">Audio Renderers</span></span></td>
<td><span data-ttu-id="03efb-127"><strong>CLSID_AudioRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-127"><strong>CLSID_AudioRendererCategory</strong></span></span></td>
<td><span data-ttu-id="03efb-128"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-128"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03efb-129">Filtri di controllo del dispositivo</span><span class="sxs-lookup"><span data-stu-id="03efb-129">Device Control Filters</span></span></td>
<td><span data-ttu-id="03efb-130"><strong>CLSID_DeviceControlCategory</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-130"><strong>CLSID_DeviceControlCategory</strong></span></span></td>
<td><span data-ttu-id="03efb-131"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-131"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03efb-132">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="03efb-132">DirectShow Filters</span></span></td>
<td><span data-ttu-id="03efb-133"><strong>CLSID_LegacyAmFilterCategory</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-133"><strong>CLSID_LegacyAmFilterCategory</strong></span></span></td>
<td><span data-ttu-id="03efb-134"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-134"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03efb-135">Renderer esterni</span><span class="sxs-lookup"><span data-stu-id="03efb-135">External Renderers</span></span></td>
<td><span data-ttu-id="03efb-136"><strong>CLSID_TransmitCategory</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-136"><strong>CLSID_TransmitCategory</strong></span></span></td>
<td><span data-ttu-id="03efb-137"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-137"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03efb-138">Renderer MIDI</span><span class="sxs-lookup"><span data-stu-id="03efb-138">Midi Renderers</span></span></td>
<td><span data-ttu-id="03efb-139"><strong>CLSID_MidiRendererCategory</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-139"><strong>CLSID_MidiRendererCategory</strong></span></span></td>
<td><span data-ttu-id="03efb-140"><strong>MERIT_NORMAL</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-140"><strong>MERIT_NORMAL</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03efb-141">Origini acquisizione video</span><span class="sxs-lookup"><span data-stu-id="03efb-141">Video Capture Sources</span></span></td>
<td><span data-ttu-id="03efb-142"><strong>CLSID_VideoInputDeviceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-142"><strong>CLSID_VideoInputDeviceCategory</strong></span></span></td>
<td><span data-ttu-id="03efb-143"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-143"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03efb-144">Compressione video</span><span class="sxs-lookup"><span data-stu-id="03efb-144">Video Compressors</span></span></td>
<td><span data-ttu-id="03efb-145"><strong>CLSID_VideoCompressorCategory</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-145"><strong>CLSID_VideoCompressorCategory</strong></span></span></td>
<td><span data-ttu-id="03efb-146"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-146"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03efb-147">Dispositivi di decompressione dei flussi WDM</span><span class="sxs-lookup"><span data-stu-id="03efb-147">WDM Stream Decompression Devices</span></span></td>
<td><span data-ttu-id="03efb-148"><strong>CLSID_DVDHWDecodersCategory</strong>
</span><span class="sxs-lookup"><span data-stu-id="03efb-148"><strong>CLSID_DVDHWDecodersCategory</strong>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="03efb-149">Questa categoria contiene decodificatori DVD hardware.</span><span class="sxs-lookup"><span data-stu-id="03efb-149">This category contains hardware DVD decoders.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="03efb-150"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-150"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03efb-151">Dispositivi di acquisizione di streaming WDM</span><span class="sxs-lookup"><span data-stu-id="03efb-151">WDM Streaming Capture Devices</span></span></td>
<td><span data-ttu-id="03efb-152"><strong>AM_KSCATEGORY_CAPTURE</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-152"><strong>AM_KSCATEGORY_CAPTURE</strong></span></span></td>
<td><span data-ttu-id="03efb-153"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-153"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03efb-154">Dispositivi traversa di streaming WDM</span><span class="sxs-lookup"><span data-stu-id="03efb-154">WDM Streaming Crossbar Devices</span></span></td>
<td><span data-ttu-id="03efb-155"><strong>AM_KSCATEGORY_CROSSBAR</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-155"><strong>AM_KSCATEGORY_CROSSBAR</strong></span></span></td>
<td><span data-ttu-id="03efb-156"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-156"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03efb-157">Dispositivi di rendering di streaming WDM</span><span class="sxs-lookup"><span data-stu-id="03efb-157">WDM Streaming Rendering Devices</span></span></td>
<td><span data-ttu-id="03efb-158"><strong>AM_KSCATEGORY_RENDER</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-158"><strong>AM_KSCATEGORY_RENDER</strong></span></span></td>
<td><span data-ttu-id="03efb-159"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-159"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03efb-160">Dispositivi t/Splitter streaming WDM</span><span class="sxs-lookup"><span data-stu-id="03efb-160">WDM Streaming Tee/Splitter Devices</span></span></td>
<td><span data-ttu-id="03efb-161"><strong>AM_KSCATEGORY_SPLITTER</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-161"><strong>AM_KSCATEGORY_SPLITTER</strong></span></span></td>
<td><span data-ttu-id="03efb-162"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-162"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03efb-163">Dispositivi audio WDM Streaming TV</span><span class="sxs-lookup"><span data-stu-id="03efb-163">WDM Streaming TV Audio Devices</span></span></td>
<td><span data-ttu-id="03efb-164"><strong>AM_KSCATEGORY_TVAUDIO</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-164"><strong>AM_KSCATEGORY_TVAUDIO</strong></span></span></td>
<td><span data-ttu-id="03efb-165"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-165"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03efb-166">Dispositivi sintonizzatore streaming TV WDM</span><span class="sxs-lookup"><span data-stu-id="03efb-166">WDM Streaming TV Tuner Devices</span></span></td>
<td><span data-ttu-id="03efb-167"><strong>AM_KSCATEGORY_TVTUNER</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-167"><strong>AM_KSCATEGORY_TVTUNER</strong></span></span></td>
<td><span data-ttu-id="03efb-168"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-168"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03efb-169">Codec VBI per flussi WDM</span><span class="sxs-lookup"><span data-stu-id="03efb-169">WDM Streaming VBI Codecs</span></span></td>
<td><span data-ttu-id="03efb-170"><strong>AM_KSCATEGORY_VBICODEC</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-170"><strong>AM_KSCATEGORY_VBICODEC</strong></span></span></td>
<td><span data-ttu-id="03efb-171"><strong>MERIT_DO_NOT_USE</strong></span><span class="sxs-lookup"><span data-stu-id="03efb-171"><strong>MERIT_DO_NOT_USE</strong></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="03efb-172">Le seguenti categorie sono dichiarate nel file di intestazione KS. h.</span><span class="sxs-lookup"><span data-stu-id="03efb-172">The following categories are declared in the header file Ks.h.</span></span>



| <span data-ttu-id="03efb-173">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="03efb-173">Friendly Name</span></span>                          | <span data-ttu-id="03efb-174">CLSID</span><span class="sxs-lookup"><span data-stu-id="03efb-174">CLSID</span></span>                                   | <span data-ttu-id="03efb-175">Merito</span><span class="sxs-lookup"><span data-stu-id="03efb-175">Merit</span></span>                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| <span data-ttu-id="03efb-176">Trasformazioni di comunicazione WDM Streaming</span><span class="sxs-lookup"><span data-stu-id="03efb-176">WDM Streaming Communication Transforms</span></span> | <span data-ttu-id="03efb-177">**\_COMMUNICATIONSTRANSFORM KSCATEGORY**</span><span class="sxs-lookup"><span data-stu-id="03efb-177">**KSCATEGORY\_COMMUNICATIONSTRANSFORM**</span></span> | <span data-ttu-id="03efb-178">**il merito non viene \_ \_ \_ utilizzato**</span><span class="sxs-lookup"><span data-stu-id="03efb-178">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="03efb-179">Trasformazioni di dati di streaming WDM</span><span class="sxs-lookup"><span data-stu-id="03efb-179">WDM Streaming Data Transforms</span></span>          | <span data-ttu-id="03efb-180">**KSCATEGORY \_ DATAtransform**</span><span class="sxs-lookup"><span data-stu-id="03efb-180">**KSCATEGORY\_DATATRANSFORM**</span></span>           | <span data-ttu-id="03efb-181">**il merito non viene \_ \_ \_ utilizzato**</span><span class="sxs-lookup"><span data-stu-id="03efb-181">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="03efb-182">Trasformazioni dell'interfaccia di streaming WDM</span><span class="sxs-lookup"><span data-stu-id="03efb-182">WDM Streaming Interface Transforms</span></span>     | <span data-ttu-id="03efb-183">**\_INTERFACETRANSFORM KSCATEGORY**</span><span class="sxs-lookup"><span data-stu-id="03efb-183">**KSCATEGORY\_INTERFACETRANSFORM**</span></span>      | <span data-ttu-id="03efb-184">**il merito non viene \_ \_ \_ utilizzato**</span><span class="sxs-lookup"><span data-stu-id="03efb-184">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="03efb-185">Dispositivi mixer di streaming WDM</span><span class="sxs-lookup"><span data-stu-id="03efb-185">WDM Streaming Mixer Devices</span></span>            | <span data-ttu-id="03efb-186">**\_mixer KSCATEGORY**</span><span class="sxs-lookup"><span data-stu-id="03efb-186">**KSCATEGORY\_MIXER**</span></span>                   | <span data-ttu-id="03efb-187">**il merito non viene \_ \_ \_ utilizzato**</span><span class="sxs-lookup"><span data-stu-id="03efb-187">**MERIT\_DO\_NOT\_USE**</span></span> |



 

<span data-ttu-id="03efb-188">Le seguenti categorie sono dichiarate nel file di intestazione Bdamedia. h.</span><span class="sxs-lookup"><span data-stu-id="03efb-188">The following categories are declared in the header file Bdamedia.h.</span></span> <span data-ttu-id="03efb-189">Includere i file di intestazione seguenti: KS. h, ksmedia. h e bdamedia. h.</span><span class="sxs-lookup"><span data-stu-id="03efb-189">Include the following header files: ks.h, ksmedia.h, and bdamedia.h.</span></span>



| <span data-ttu-id="03efb-190">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="03efb-190">Friendly Name</span></span>                       | <span data-ttu-id="03efb-191">CLSID</span><span class="sxs-lookup"><span data-stu-id="03efb-191">CLSID</span></span>                                       | <span data-ttu-id="03efb-192">Merito</span><span class="sxs-lookup"><span data-stu-id="03efb-192">Merit</span></span>                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| <span data-ttu-id="03efb-193">Provider di rete BDA</span><span class="sxs-lookup"><span data-stu-id="03efb-193">BDA Network Providers</span></span>               | <span data-ttu-id="03efb-194">**\_provider di \_ rete \_ BDA KSCATEGORY**</span><span class="sxs-lookup"><span data-stu-id="03efb-194">**KSCATEGORY\_BDA\_NETWORK\_PROVIDER**</span></span>      | <span data-ttu-id="03efb-195">**VALORE \_ normale**</span><span class="sxs-lookup"><span data-stu-id="03efb-195">**MERIT\_NORMAL**</span></span>       |
| <span data-ttu-id="03efb-196">Componenti ricevitore BDA</span><span class="sxs-lookup"><span data-stu-id="03efb-196">BDA Receiver Components</span></span>             | <span data-ttu-id="03efb-197">**\_ \_ componente ricevitore BDA \_ KSCATEGORY**</span><span class="sxs-lookup"><span data-stu-id="03efb-197">**KSCATEGORY\_BDA\_RECEIVER\_COMPONENT**</span></span>    | <span data-ttu-id="03efb-198">**il merito non viene \_ \_ \_ utilizzato**</span><span class="sxs-lookup"><span data-stu-id="03efb-198">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="03efb-199">Filtri per il rendering BDA</span><span class="sxs-lookup"><span data-stu-id="03efb-199">BDA Rendering Filters</span></span>               | <span data-ttu-id="03efb-200">**\_sink IP \_ KSCATEGORY**</span><span class="sxs-lookup"><span data-stu-id="03efb-200">**KSCATEGORY\_IP\_SINK**</span></span>                    | <span data-ttu-id="03efb-201">**il merito non viene \_ \_ \_ utilizzato**</span><span class="sxs-lookup"><span data-stu-id="03efb-201">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="03efb-202">Filtri origine BDA</span><span class="sxs-lookup"><span data-stu-id="03efb-202">BDA Source Filters</span></span>                  | <span data-ttu-id="03efb-203">**\_Tuner di \_ rete \_ BDA KSCATEGORY**</span><span class="sxs-lookup"><span data-stu-id="03efb-203">**KSCATEGORY\_BDA\_NETWORK\_TUNER**</span></span>         | <span data-ttu-id="03efb-204">**il merito non viene \_ \_ \_ utilizzato**</span><span class="sxs-lookup"><span data-stu-id="03efb-204">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="03efb-205">Renderer delle informazioni di trasporto BDA</span><span class="sxs-lookup"><span data-stu-id="03efb-205">BDA Transport Information Renderers</span></span> | <span data-ttu-id="03efb-206">**\_ \_ informazioni sul trasporto BDA KSCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="03efb-206">**KSCATEGORY\_BDA\_TRANSPORT\_INFORMATION**</span></span> | <span data-ttu-id="03efb-207">**VALORE \_ normale**</span><span class="sxs-lookup"><span data-stu-id="03efb-207">**MERIT\_NORMAL**</span></span>       |



 

> [!Note]  
> <span data-ttu-id="03efb-208">I decodificatori sono registrati nella categoria "filtri DirectShow" (CLSID \_ LegacyAmFilterCategory).</span><span class="sxs-lookup"><span data-stu-id="03efb-208">Decoders are registered under the "DirectShow Filters" category (CLSID\_LegacyAmFilterCategory).</span></span>

 

## <a name="other-filter-categories"></a><span data-ttu-id="03efb-209">Altre categorie di filtro</span><span class="sxs-lookup"><span data-stu-id="03efb-209">Other Filter Categories</span></span>

<span data-ttu-id="03efb-210">Le categorie elencate di seguito possono essere enumerate con l'enumeratore del dispositivo di sistema, ma non sono visibili al mapper dei filtri e non vengono usate da [Intelligent Connect](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="03efb-210">The categories listed here can be enumerated with the System Device Enumerator, but are not visible to the Filter Mapper and are not used by [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="03efb-211">Le seguenti categorie sono dichiarate nel file di intestazione qedit. h.</span><span class="sxs-lookup"><span data-stu-id="03efb-211">The following categories are declared in the header file Qedit.h.</span></span>



| <span data-ttu-id="03efb-212">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="03efb-212">Friendly Name</span></span>            | <span data-ttu-id="03efb-213">CLID</span><span class="sxs-lookup"><span data-stu-id="03efb-213">CLID</span></span>                             | <span data-ttu-id="03efb-214">Merito</span><span class="sxs-lookup"><span data-stu-id="03efb-214">Merit</span></span>                   |
|--------------------------|----------------------------------|-------------------------|
| <span data-ttu-id="03efb-215">Effetti video (1 input)</span><span class="sxs-lookup"><span data-stu-id="03efb-215">Video Effects (1 input)</span></span>  | <span data-ttu-id="03efb-216">**\_VIDEOEFFECTS1CATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="03efb-216">**CLSID\_VideoEffects1Category**</span></span> | <span data-ttu-id="03efb-217">**il merito non viene \_ \_ \_ utilizzato**</span><span class="sxs-lookup"><span data-stu-id="03efb-217">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="03efb-218">Effetti video (2 input)</span><span class="sxs-lookup"><span data-stu-id="03efb-218">Video Effects (2 inputs)</span></span> | <span data-ttu-id="03efb-219">**\_VIDEOEFFECTS2CATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="03efb-219">**CLSID\_VideoEffects2Category**</span></span> | <span data-ttu-id="03efb-220">**il merito non viene \_ \_ \_ utilizzato**</span><span class="sxs-lookup"><span data-stu-id="03efb-220">**MERIT\_DO\_NOT\_USE**</span></span> |



 

<span data-ttu-id="03efb-221">Queste categorie contengono effetti video e transizioni per i [servizi di modifica DirectShow](directshow-editing-services.md):</span><span class="sxs-lookup"><span data-stu-id="03efb-221">These categories contain video effects and transitions for [DirectShow Editing Services](directshow-editing-services.md):</span></span>

-   <span data-ttu-id="03efb-222">"Effetti video (1 input)" contiene effetti video.</span><span class="sxs-lookup"><span data-stu-id="03efb-222">"Video Effects (1 input)" contains video effects.</span></span>
-   <span data-ttu-id="03efb-223">"Video Effects (2 input)" contiene transizioni video.</span><span class="sxs-lookup"><span data-stu-id="03efb-223">"Video Effects (2 input)" contains video transitions.</span></span>

<span data-ttu-id="03efb-224">Per ulteriori informazioni, vedere [enumerazione degli effetti e delle transizioni](enumerating-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="03efb-224">For more information, see [Enumerating Effects and Transitions](enumerating-effects-and-transitions.md).</span></span>

<span data-ttu-id="03efb-225">Le seguenti categorie sono dichiarate nel file di intestazione UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="03efb-225">The following categories are declared in the header file Uuids.h.</span></span> <span data-ttu-id="03efb-226">Includere il file di intestazione dshow. h.</span><span class="sxs-lookup"><span data-stu-id="03efb-226">Include the header file Dshow.h.</span></span>



| <span data-ttu-id="03efb-227">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="03efb-227">Friendly Name</span></span>       | <span data-ttu-id="03efb-228">CLID</span><span class="sxs-lookup"><span data-stu-id="03efb-228">CLID</span></span>                                | <span data-ttu-id="03efb-229">Merito</span><span class="sxs-lookup"><span data-stu-id="03efb-229">Merit</span></span>                   |
|---------------------|-------------------------------------|-------------------------|
| <span data-ttu-id="03efb-230">Codificatori</span><span class="sxs-lookup"><span data-stu-id="03efb-230">EncAPI Encoders</span></span>     | <span data-ttu-id="03efb-231">**\_MEDIAENCODERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="03efb-231">**CLSID\_MediaEncoderCategory**</span></span>     | <span data-ttu-id="03efb-232">**il merito non viene \_ \_ \_ utilizzato**</span><span class="sxs-lookup"><span data-stu-id="03efb-232">**MERIT\_DO\_NOT\_USE**</span></span> |
| <span data-ttu-id="03efb-233">Multiplexer</span><span class="sxs-lookup"><span data-stu-id="03efb-233">EncAPI Multiplexers</span></span> | <span data-ttu-id="03efb-234">**\_MEDIAMULTIPLEXERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="03efb-234">**CLSID\_MediaMultiplexerCategory**</span></span> | <span data-ttu-id="03efb-235">**il merito non viene \_ \_ \_ utilizzato**</span><span class="sxs-lookup"><span data-stu-id="03efb-235">**MERIT\_DO\_NOT\_USE**</span></span> |



 

## <a name="directshow-filter-meta-category"></a><span data-ttu-id="03efb-236">Meta-Category filtro DirectShow</span><span class="sxs-lookup"><span data-stu-id="03efb-236">DirectShow Filter Meta-Category</span></span>



| <span data-ttu-id="03efb-237">Nome descrittivo</span><span class="sxs-lookup"><span data-stu-id="03efb-237">Friendly Name</span></span>                 | <span data-ttu-id="03efb-238">CLSID</span><span class="sxs-lookup"><span data-stu-id="03efb-238">CLSID</span></span>                            | <span data-ttu-id="03efb-239">Merito</span><span class="sxs-lookup"><span data-stu-id="03efb-239">Merit</span></span>          |
|-------------------------------|----------------------------------|----------------|
| <span data-ttu-id="03efb-240">Categorie filtro ActiveMovie</span><span class="sxs-lookup"><span data-stu-id="03efb-240">ActiveMovie Filter Categories</span></span> | <span data-ttu-id="03efb-241">**\_ACTIVEMOVIECATEGORIES CLSID**</span><span class="sxs-lookup"><span data-stu-id="03efb-241">**CLSID\_ActiveMovieCategories**</span></span> | <span data-ttu-id="03efb-242">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="03efb-242">Not applicable</span></span> |



 

<span data-ttu-id="03efb-243">Questa meta-categoria contiene un elenco di categorie di filtro.</span><span class="sxs-lookup"><span data-stu-id="03efb-243">This meta-category contains a list of filter categories.</span></span> <span data-ttu-id="03efb-244">Se una categoria di filtri non viene visualizzata in questo elenco, il [mapper dei filtri](filter-mapper.md) ignora la categoria, il che significa che il filtro non è disponibile per la [connessione intelligente](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="03efb-244">If a filter category does not appear within this list, the [Filter Mapper](filter-mapper.md) ignores the category, which means the filter is not available for [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="03efb-245">Per enumerare l'elenco di categorie di filtro, chiamare [**ICreateDevEnum:: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) con il valore CLSID \_ ActiveMovieCategories.</span><span class="sxs-lookup"><span data-stu-id="03efb-245">To enumerate the list of filter categories, call [**ICreateDevEnum::CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) with the value CLSID\_ActiveMovieCategories.</span></span> <span data-ttu-id="03efb-246">I moniker restituiti da questo metodo supportano le seguenti proprietà.</span><span class="sxs-lookup"><span data-stu-id="03efb-246">The monikers returned by this method support the following properties.</span></span>



| <span data-ttu-id="03efb-247">Nome proprietà</span><span class="sxs-lookup"><span data-stu-id="03efb-247">Property Name</span></span>  | <span data-ttu-id="03efb-248">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03efb-248">Description</span></span>                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03efb-249">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="03efb-249">"FriendlyName"</span></span> | <span data-ttu-id="03efb-250">Nome della categoria (VT \_ BSTR).</span><span class="sxs-lookup"><span data-stu-id="03efb-250">Category name (VT\_BSTR).</span></span>                                                              |
| <span data-ttu-id="03efb-251">Merito</span><span class="sxs-lookup"><span data-stu-id="03efb-251">"Merit"</span></span>        | <span data-ttu-id="03efb-252">Merit categoria (VT \_ I4).</span><span class="sxs-lookup"><span data-stu-id="03efb-252">Category merit (VT\_I4).</span></span> <span data-ttu-id="03efb-253">Se questa proprietà è assente, considerare come **Merit non \_ \_ \_ usare**.</span><span class="sxs-lookup"><span data-stu-id="03efb-253">If this property is absent, treat as **MERIT\_DO\_NOT\_USE**.</span></span> |
| <span data-ttu-id="03efb-254">CLSID</span><span class="sxs-lookup"><span data-stu-id="03efb-254">"CLSID"</span></span>        | <span data-ttu-id="03efb-255">Categoria CLSID (VT \_ BSTR).</span><span class="sxs-lookup"><span data-stu-id="03efb-255">Category CLSID (VT\_BSTR).</span></span>                                                             |



 

<span data-ttu-id="03efb-256">Per aggiungere una nuova categoria di filtri all'elenco, chiamare [**IFilterMapper2:: CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).</span><span class="sxs-lookup"><span data-stu-id="03efb-256">To add a new filter category to this list, call [**IFilterMapper2::CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory).</span></span>

## <a name="dmo-categories"></a><span data-ttu-id="03efb-257">Categorie DMO</span><span class="sxs-lookup"><span data-stu-id="03efb-257">DMO Categories</span></span>

<span data-ttu-id="03efb-258">Gli oggetti multimediali DirectX (DMOs) utilizzano un meccanismo di enumerazione diverso dai filtri DirectShow.</span><span class="sxs-lookup"><span data-stu-id="03efb-258">DirectX Media Objects (DMOs) use a different enumeration mechanism from DirectShow filters.</span></span> <span data-ttu-id="03efb-259">Per ulteriori informazioni, vedere la pagina relativa alla [registrazione di un DMO](registering-a-dmo.md).</span><span class="sxs-lookup"><span data-stu-id="03efb-259">For more information, see [Registering a DMO](registering-a-dmo.md).</span></span> <span data-ttu-id="03efb-260">Tuttavia, è possibile usare l'enumeratore System Device per enumerare le categorie DMO.</span><span class="sxs-lookup"><span data-stu-id="03efb-260">However, you can use the System Device Enumerator to enumerate DMO categories.</span></span> <span data-ttu-id="03efb-261">I moniker vengono associati al [filtro del wrapper DMO](dmo-wrapper-filter.md) e inizializzano automaticamente il filtro con DMO.</span><span class="sxs-lookup"><span data-stu-id="03efb-261">The monikers bind to the [DMO Wrapper Filter](dmo-wrapper-filter.md) and automatically initialize the filter with the DMO.</span></span>

<span data-ttu-id="03efb-262">Inoltre, alcune categorie DMO sono mappate alle categorie di filtri DirectShow ai fini della connessione intelligente:</span><span class="sxs-lookup"><span data-stu-id="03efb-262">In addition, some of the DMO categories are mapped to DirectShow filter categories for the purposes of intelligent connect:</span></span>



| <span data-ttu-id="03efb-263">Categoria DMO</span><span class="sxs-lookup"><span data-stu-id="03efb-263">DMO Category</span></span>                    | <span data-ttu-id="03efb-264">Equivalente DirectShow</span><span class="sxs-lookup"><span data-stu-id="03efb-264">DirectShow Equivalent</span></span>              |
|---------------------------------|------------------------------------|
| <span data-ttu-id="03efb-265">**\_ \_ codificatore audio DMOCATEGORY**</span><span class="sxs-lookup"><span data-stu-id="03efb-265">**DMOCATEGORY\_AUDIO\_ENCODER**</span></span> | <span data-ttu-id="03efb-266">**\_AUDIOCOMPRESSORCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="03efb-266">**CLSID\_AudioCompressorCategory**</span></span> |
| <span data-ttu-id="03efb-267">**\_decodificatore audio DMOCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="03efb-267">**DMOCATEGORY\_AUDIO\_DECODER**</span></span> | <span data-ttu-id="03efb-268">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="03efb-268">**CLSID\_LegacyAmFilterCategory**</span></span>  |
| <span data-ttu-id="03efb-269">**\_ \_ codificatore video DMOCATEGORY**</span><span class="sxs-lookup"><span data-stu-id="03efb-269">**DMOCATEGORY\_VIDEO\_ENCODER**</span></span> | <span data-ttu-id="03efb-270">**\_VIDEOCOMPRESSORCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="03efb-270">**CLSID\_VideoCompressorCategory**</span></span> |
| <span data-ttu-id="03efb-271">**\_decodificatore video DMOCATEGORY \_**</span><span class="sxs-lookup"><span data-stu-id="03efb-271">**DMOCATEGORY\_VIDEO\_DECODER**</span></span> | <span data-ttu-id="03efb-272">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="03efb-272">**CLSID\_LegacyAmFilterCategory**</span></span>  |



 

<span data-ttu-id="03efb-273">Si noti che le categorie effetto video e effetto audio non sono mappate ad alcuna categoria DirectShow.</span><span class="sxs-lookup"><span data-stu-id="03efb-273">Note that the video effect and audio effect categories are not mapped to any DirectShow categories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03efb-274">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="03efb-274">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03efb-275">Costanti e GUID</span><span class="sxs-lookup"><span data-stu-id="03efb-275">Constants and GUIDs</span></span>](constants-and-guids.md)
</dt> <dt>

[<span data-ttu-id="03efb-276">Enumerazione dei dispositivi e dei filtri</span><span class="sxs-lookup"><span data-stu-id="03efb-276">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="03efb-277">Connessione intelligente</span><span class="sxs-lookup"><span data-stu-id="03efb-277">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> <dt>

[<span data-ttu-id="03efb-278">Layout delle chiavi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="03efb-278">Layout of the Registry Keys</span></span>](layout-of-the-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="03efb-279">Uso del mapper dei filtri</span><span class="sxs-lookup"><span data-stu-id="03efb-279">Using the Filter Mapper</span></span>](using-the-filter-mapper.md)
</dt> <dt>

[<span data-ttu-id="03efb-280">Uso di System Device Enumerator</span><span class="sxs-lookup"><span data-stu-id="03efb-280">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




