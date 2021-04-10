---
title: Mapping di feed RSS a Windows Media Gestione dispositivi proprietà
description: Mapping di feed RSS a Windows Media Gestione dispositivi proprietà
ms.assetid: 354c98ab-1392-476f-a650-75b948dc971a
keywords:
- Windows Media Gestione dispositivi, feed RSS
- Gestione dispositivi, feed RSS
- Guida per programmatori, feed RSS
- applicazioni desktop, feed RSS
- creazione di applicazioni Windows Media Gestione dispositivi, feed RSS
- Feed RSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3a81d52b4099d77542963d2e87ae5b7dc26b034
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855573"
---
# <a name="mapping-rss-feeds-to-windows-media-device-manager-properties"></a><span data-ttu-id="47ee9-109">Mapping di feed RSS a Windows Media Gestione dispositivi proprietà</span><span class="sxs-lookup"><span data-stu-id="47ee9-109">Mapping RSS Feeds to Windows Media Device Manager Properties</span></span>

<span data-ttu-id="47ee9-110">Windows Media Player 11 fornisce una funzionalità di aggregatore RSS che consente agli utenti di archiviare contenuti ottenuti da podcast nei propri computer.</span><span class="sxs-lookup"><span data-stu-id="47ee9-110">Windows Media Player 11 provides an RSS aggregator feature that enables users to store content obtained from podcasts on their computers.</span></span> <span data-ttu-id="47ee9-111">In questo argomento vengono descritti gli elementi XML disponibili in un feed RSS.</span><span class="sxs-lookup"><span data-stu-id="47ee9-111">This topic describes the XML elements found in an RSS feed.</span></span> <span data-ttu-id="47ee9-112">Inoltre, esegue il mapping di questi elementi RSS a Windows Media Gestione dispositivi proprietà.</span><span class="sxs-lookup"><span data-stu-id="47ee9-112">In addition, it maps these RSS elements to Windows Media Device Manager properties.</span></span>

<span data-ttu-id="47ee9-113">Gli elementi in un feed RSS hanno la gerarchia e gli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="47ee9-113">The elements in an RSS feed have the following hierarchy and attributes:</span></span>


```C++
<channel>
    <title />
    <link />
    <description />
    <language />
    <copyright />
    <managingEditor />
    <webMaster />
    <pubDate />
    <lastBuildDate />
    <category />
    <generator />
    <docs />
    <cloud />
    <ttl />

    <image>
        <url />
        <title />
        <link />
        <width />
        <height />
        <description />
    </image>

    <rating />

    <textInput>
        <title />
        <description />
        <name />
        <link />
    </textInput>

    <skipHours />
    <skipDays />

    <item>
        <title />
        <link />
        <description />
        <author />
        <category domain = " "/>
        <comments />
        <enclousure url = " " length = " " type = " "/>
        <guid isPermaLink = " "/>
        <pubDate />
        <source url = " " />
    </item>
</channel>
```



<span data-ttu-id="47ee9-114">La tabella seguente elenca gli elementi del canale in un feed RSS e le proprietà Windows Media Gestione dispositivi corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="47ee9-114">The following table lists the channel elements in an RSS feed and the corresponding Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="47ee9-115">Elemento Channel</span><span class="sxs-lookup"><span data-stu-id="47ee9-115">Channel element</span></span> | <span data-ttu-id="47ee9-116">Stato</span><span class="sxs-lookup"><span data-stu-id="47ee9-116">Status</span></span>         | <span data-ttu-id="47ee9-117">Proprietà Gestione dispositivi Windows Media corrispondente</span><span class="sxs-lookup"><span data-stu-id="47ee9-117">Corresponding Windows Media Device Manager property</span></span>   |
|-----------------|----------------|-------------------------------------------------------|
| <span data-ttu-id="47ee9-118">category</span><span class="sxs-lookup"><span data-stu-id="47ee9-118">category</span></span>        | <span data-ttu-id="47ee9-119">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-119">Optional</span></span>       | [<span data-ttu-id="47ee9-120">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="47ee9-120">g\_wszWMDMGenre</span></span>](metadata-constants.md)             |
| <span data-ttu-id="47ee9-121">cloud</span><span class="sxs-lookup"><span data-stu-id="47ee9-121">cloud</span></span>           | <span data-ttu-id="47ee9-122">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-122">Not applicable</span></span> | <span data-ttu-id="47ee9-123">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-123">Not applicable</span></span>                                        |
| <span data-ttu-id="47ee9-124">copyright</span><span class="sxs-lookup"><span data-stu-id="47ee9-124">copyright</span></span>       | <span data-ttu-id="47ee9-125">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-125">Optional</span></span>       | [<span data-ttu-id="47ee9-126">g \_ wszWMDMProviderCopyright</span><span class="sxs-lookup"><span data-stu-id="47ee9-126">g\_wszWMDMProviderCopyright</span></span>](metadata-constants.md) |
| <span data-ttu-id="47ee9-127">description</span><span class="sxs-lookup"><span data-stu-id="47ee9-127">description</span></span>     | <span data-ttu-id="47ee9-128">Necessario</span><span class="sxs-lookup"><span data-stu-id="47ee9-128">Required</span></span>       | [<span data-ttu-id="47ee9-129">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="47ee9-129">g\_wszWMDMDescription</span></span>](metadata-constants.md)       |
| <span data-ttu-id="47ee9-130">docs</span><span class="sxs-lookup"><span data-stu-id="47ee9-130">docs</span></span>            | <span data-ttu-id="47ee9-131">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-131">Not applicable</span></span> | <span data-ttu-id="47ee9-132">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-132">Not applicable</span></span>                                        |
| <span data-ttu-id="47ee9-133">generatore</span><span class="sxs-lookup"><span data-stu-id="47ee9-133">generator</span></span>       | <span data-ttu-id="47ee9-134">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-134">Not applicable</span></span> | <span data-ttu-id="47ee9-135">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-135">Not applicable</span></span>                                        |
| <span data-ttu-id="47ee9-136">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="47ee9-136">language</span></span>        | <span data-ttu-id="47ee9-137">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-137">Not applicable</span></span> | <span data-ttu-id="47ee9-138">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-138">Not applicable</span></span>                                        |
| <span data-ttu-id="47ee9-139">lastBuildDate</span><span class="sxs-lookup"><span data-stu-id="47ee9-139">lastBuildDate</span></span>   | <span data-ttu-id="47ee9-140">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-140">Optional</span></span>       | [<span data-ttu-id="47ee9-141">g \_ wszWMDMLastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="47ee9-141">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md)  |
| <span data-ttu-id="47ee9-142">link</span><span class="sxs-lookup"><span data-stu-id="47ee9-142">link</span></span>            | <span data-ttu-id="47ee9-143">Necessario</span><span class="sxs-lookup"><span data-stu-id="47ee9-143">Required</span></span>       | [<span data-ttu-id="47ee9-144">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="47ee9-144">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)    |
| <span data-ttu-id="47ee9-145">managingEditor</span><span class="sxs-lookup"><span data-stu-id="47ee9-145">managingEditor</span></span>  | <span data-ttu-id="47ee9-146">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-146">Optional</span></span>       | [<span data-ttu-id="47ee9-147">g \_ wszWMDMEditor</span><span class="sxs-lookup"><span data-stu-id="47ee9-147">g\_wszWMDMEditor</span></span>](metadata-constants.md)            |
| <span data-ttu-id="47ee9-148">pubDate</span><span class="sxs-lookup"><span data-stu-id="47ee9-148">pubDate</span></span>         | <span data-ttu-id="47ee9-149">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-149">Optional</span></span>       | [<span data-ttu-id="47ee9-150">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="47ee9-150">g\_wszWMDMYear</span></span>](metadata-constants.md)              |
| <span data-ttu-id="47ee9-151">rating</span><span class="sxs-lookup"><span data-stu-id="47ee9-151">rating</span></span>          | <span data-ttu-id="47ee9-152">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-152">Not applicable</span></span> | <span data-ttu-id="47ee9-153">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-153">Not applicable</span></span>                                        |
| <span data-ttu-id="47ee9-154">skipDays</span><span class="sxs-lookup"><span data-stu-id="47ee9-154">skipDays</span></span>        | <span data-ttu-id="47ee9-155">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-155">Not applicable</span></span> | <span data-ttu-id="47ee9-156">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-156">Not applicable</span></span>                                        |
| <span data-ttu-id="47ee9-157">skipHours</span><span class="sxs-lookup"><span data-stu-id="47ee9-157">skipHours</span></span>       | <span data-ttu-id="47ee9-158">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-158">Not applicable</span></span> | <span data-ttu-id="47ee9-159">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-159">Not applicable</span></span>                                        |
| <span data-ttu-id="47ee9-160">textInput</span><span class="sxs-lookup"><span data-stu-id="47ee9-160">textInput</span></span>       | <span data-ttu-id="47ee9-161">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-161">Not applicable</span></span> | <span data-ttu-id="47ee9-162">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-162">Not applicable</span></span>                                        |
| <span data-ttu-id="47ee9-163">title</span><span class="sxs-lookup"><span data-stu-id="47ee9-163">title</span></span>           | <span data-ttu-id="47ee9-164">Necessario</span><span class="sxs-lookup"><span data-stu-id="47ee9-164">Required</span></span>       | [<span data-ttu-id="47ee9-165">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="47ee9-165">g\_wszWMDMTitle</span></span>](metadata-constants.md)             |
| <span data-ttu-id="47ee9-166">ttl</span><span class="sxs-lookup"><span data-stu-id="47ee9-166">ttl</span></span>             | <span data-ttu-id="47ee9-167">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-167">Optional</span></span>       | [<span data-ttu-id="47ee9-168">g \_ wszWMDMTimeToLive</span><span class="sxs-lookup"><span data-stu-id="47ee9-168">g\_wszWMDMTimeToLive</span></span>](metadata-constants.md)        |
| <span data-ttu-id="47ee9-169">webMaster</span><span class="sxs-lookup"><span data-stu-id="47ee9-169">webMaster</span></span>       | <span data-ttu-id="47ee9-170">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-170">Optional</span></span>       | [<span data-ttu-id="47ee9-171">g \_ wszWMDMWebMaster</span><span class="sxs-lookup"><span data-stu-id="47ee9-171">g\_wszWMDMWebMaster</span></span>](metadata-constants.md)         |



 

<span data-ttu-id="47ee9-172">La tabella seguente elenca gli elementi immagine in un feed RSS e le proprietà WMDM corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="47ee9-172">The following table lists the image elements in an RSS feed and the corresponding WMDM properties.</span></span>



| <span data-ttu-id="47ee9-173">Elemento Image</span><span class="sxs-lookup"><span data-stu-id="47ee9-173">Image element</span></span> | <span data-ttu-id="47ee9-174">Stato</span><span class="sxs-lookup"><span data-stu-id="47ee9-174">Status</span></span>   | <span data-ttu-id="47ee9-175">Proprietà Gestione dispositivi Windows Media corrispondente</span><span class="sxs-lookup"><span data-stu-id="47ee9-175">Corresponding Windows Media Device Manager property</span></span> |
|---------------|----------|-----------------------------------------------------|
| <span data-ttu-id="47ee9-176">description</span><span class="sxs-lookup"><span data-stu-id="47ee9-176">description</span></span>   | <span data-ttu-id="47ee9-177">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-177">Optional</span></span> | [<span data-ttu-id="47ee9-178">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="47ee9-178">g\_wszWMDMDescription</span></span>](metadata-constants.md)     |
| <span data-ttu-id="47ee9-179">altezza</span><span class="sxs-lookup"><span data-stu-id="47ee9-179">height</span></span>        | <span data-ttu-id="47ee9-180">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-180">Optional</span></span> | [<span data-ttu-id="47ee9-181">g \_ wszWMDMHeight</span><span class="sxs-lookup"><span data-stu-id="47ee9-181">g\_wszWMDMHeight</span></span>](metadata-constants.md)          |
| <span data-ttu-id="47ee9-182">link</span><span class="sxs-lookup"><span data-stu-id="47ee9-182">link</span></span>          | <span data-ttu-id="47ee9-183">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-183">Optional</span></span> | [<span data-ttu-id="47ee9-184">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="47ee9-184">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)  |
| <span data-ttu-id="47ee9-185">title</span><span class="sxs-lookup"><span data-stu-id="47ee9-185">title</span></span>         | <span data-ttu-id="47ee9-186">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-186">Optional</span></span> | [<span data-ttu-id="47ee9-187">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="47ee9-187">g\_wszWMDMTitle</span></span>](metadata-constants.md)           |
| <span data-ttu-id="47ee9-188">url</span><span class="sxs-lookup"><span data-stu-id="47ee9-188">url</span></span>           | <span data-ttu-id="47ee9-189">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-189">Optional</span></span> | [<span data-ttu-id="47ee9-190">g \_ wszWMDMSourceURL</span><span class="sxs-lookup"><span data-stu-id="47ee9-190">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)       |
| <span data-ttu-id="47ee9-191">width</span><span class="sxs-lookup"><span data-stu-id="47ee9-191">width</span></span>         | <span data-ttu-id="47ee9-192">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-192">Optional</span></span> | [<span data-ttu-id="47ee9-193">g \_ wszWMDMWidth</span><span class="sxs-lookup"><span data-stu-id="47ee9-193">g\_wszWMDMWidth</span></span>](metadata-constants.md)           |



 

<span data-ttu-id="47ee9-194">Nella tabella seguente sono elencati gli elementi elemento in un feed RSS e le proprietà corrispondenti di Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="47ee9-194">The following table lists the item elements in an RSS feed and the corresponding Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="47ee9-195">Elemento Item</span><span class="sxs-lookup"><span data-stu-id="47ee9-195">Item element</span></span> | <span data-ttu-id="47ee9-196">Attributo</span><span class="sxs-lookup"><span data-stu-id="47ee9-196">Attribute</span></span>   | <span data-ttu-id="47ee9-197">Stato</span><span class="sxs-lookup"><span data-stu-id="47ee9-197">Status</span></span>         | <span data-ttu-id="47ee9-198">Proprietà Gestione dispositivi Windows Media corrispondente</span><span class="sxs-lookup"><span data-stu-id="47ee9-198">Corresponding Windows Media Device Manager property</span></span>            |
|--------------|-------------|----------------|----------------------------------------------------------------|
| <span data-ttu-id="47ee9-199">author</span><span class="sxs-lookup"><span data-stu-id="47ee9-199">author</span></span>       |             | <span data-ttu-id="47ee9-200">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-200">Optional</span></span>       | [<span data-ttu-id="47ee9-201">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="47ee9-201">g\_wszWMDMAuthor</span></span>](metadata-constants.md)                     |
| <span data-ttu-id="47ee9-202">category</span><span class="sxs-lookup"><span data-stu-id="47ee9-202">category</span></span>     |             | <span data-ttu-id="47ee9-203">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-203">Optional</span></span>       | [<span data-ttu-id="47ee9-204">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="47ee9-204">g\_wszWMDMGenre</span></span>](metadata-constants.md)                      |
|              | <span data-ttu-id="47ee9-205">dominio</span><span class="sxs-lookup"><span data-stu-id="47ee9-205">domain</span></span>      | <span data-ttu-id="47ee9-206">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-206">Not applicable</span></span> | <span data-ttu-id="47ee9-207">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-207">Not applicable</span></span>                                                 |
| <span data-ttu-id="47ee9-208">description</span><span class="sxs-lookup"><span data-stu-id="47ee9-208">description</span></span>  |             | <span data-ttu-id="47ee9-209">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-209">Optional</span></span>       | [<span data-ttu-id="47ee9-210">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="47ee9-210">g\_wszWMDMDescription</span></span>](metadata-constants.md)                |
| <span data-ttu-id="47ee9-211">recinto</span><span class="sxs-lookup"><span data-stu-id="47ee9-211">enclosure</span></span>    |             | <span data-ttu-id="47ee9-212">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-212">Optional</span></span>       | <span data-ttu-id="47ee9-213">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-213">Not applicable</span></span>                                                 |
|              | <span data-ttu-id="47ee9-214">length</span><span class="sxs-lookup"><span data-stu-id="47ee9-214">length</span></span>      | <span data-ttu-id="47ee9-215">Necessario</span><span class="sxs-lookup"><span data-stu-id="47ee9-215">Required</span></span>       | [<span data-ttu-id="47ee9-216">g \_ wszWMDMFileSize</span><span class="sxs-lookup"><span data-stu-id="47ee9-216">g\_wszWMDMFileSize</span></span>](metadata-constants.md)                   |
|              | <span data-ttu-id="47ee9-217">type</span><span class="sxs-lookup"><span data-stu-id="47ee9-217">type</span></span>        | <span data-ttu-id="47ee9-218">Obbligatoria</span><span class="sxs-lookup"><span data-stu-id="47ee9-218">Required</span></span>       | <span data-ttu-id="47ee9-219">(Il tipo MIME deve essere mappato al tipo di contenuto della proprietà).</span><span class="sxs-lookup"><span data-stu-id="47ee9-219">(The MIME type should be mapped to the property content type.)</span></span> |
|              | <span data-ttu-id="47ee9-220">url</span><span class="sxs-lookup"><span data-stu-id="47ee9-220">url</span></span>         | <span data-ttu-id="47ee9-221">Necessario</span><span class="sxs-lookup"><span data-stu-id="47ee9-221">Required</span></span>       | [<span data-ttu-id="47ee9-222">g \_ wszWMDMSourceURL</span><span class="sxs-lookup"><span data-stu-id="47ee9-222">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)                  |
| <span data-ttu-id="47ee9-223">guid</span><span class="sxs-lookup"><span data-stu-id="47ee9-223">guid</span></span>         |             | <span data-ttu-id="47ee9-224">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-224">Optional</span></span>       | [<span data-ttu-id="47ee9-225">g \_ wszWMDMediaGuid</span><span class="sxs-lookup"><span data-stu-id="47ee9-225">g\_wszWMDMediaGuid</span></span>](metadata-constants.md)                   |
|              | <span data-ttu-id="47ee9-226">PermaLink</span><span class="sxs-lookup"><span data-stu-id="47ee9-226">isPermaLink</span></span> | <span data-ttu-id="47ee9-227">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-227">Not applicable</span></span> | <span data-ttu-id="47ee9-228">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-228">Not applicable</span></span>                                                 |
| <span data-ttu-id="47ee9-229">link</span><span class="sxs-lookup"><span data-stu-id="47ee9-229">link</span></span>         |             | <span data-ttu-id="47ee9-230">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-230">Optional</span></span>       | [<span data-ttu-id="47ee9-231">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="47ee9-231">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)             |
| <span data-ttu-id="47ee9-232">pubDate</span><span class="sxs-lookup"><span data-stu-id="47ee9-232">pubDate</span></span>      |             | <span data-ttu-id="47ee9-233">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-233">Optional</span></span>       | [<span data-ttu-id="47ee9-234">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="47ee9-234">g\_wszWMDMYear</span></span>](metadata-constants.md)                       |
| <span data-ttu-id="47ee9-235">source</span><span class="sxs-lookup"><span data-stu-id="47ee9-235">source</span></span>       |             | <span data-ttu-id="47ee9-236">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-236">Not applicable</span></span> | <span data-ttu-id="47ee9-237">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="47ee9-237">Not applicable</span></span>                                                 |
| <span data-ttu-id="47ee9-238">title</span><span class="sxs-lookup"><span data-stu-id="47ee9-238">title</span></span>        |             | <span data-ttu-id="47ee9-239">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="47ee9-239">Optional</span></span>       | [<span data-ttu-id="47ee9-240">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="47ee9-240">g\_wszWMDMTitle</span></span>](metadata-constants.md)                      |



 

<span data-ttu-id="47ee9-241">Esempio</span><span class="sxs-lookup"><span data-stu-id="47ee9-241">Example</span></span>

<span data-ttu-id="47ee9-242">Nell'esempio seguente viene illustrato un feed RSS completo per un podcast fittizio fornito dal CEO di una società di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="47ee9-242">The following example shows a complete RSS feed for a fictitious podcast supplied by the CEO of a publishing company.</span></span>


```C++
<channel>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing.com/podcasting</link>
    <description>Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</description>
    <language>en-us</language>
    <copyright>2006 Lucerne Publishing LP, LLLP. All Rights Reserved.</copyright>
    <managingEditor>someone@example.com</managingEditor>
    <webMaster>someone@example.com</webMaster>
    <pubDate>Fri, 9 June 2006 14:00:28 EDT</pubDate>
    <lastBuildDate Fri, 9 June 2006 14:00:28 EDT />
    <category>News</category>
    <generator>Podcaster version 1.0</generator>
    <docs>https://www.lucernepublishing.com/tech/rss</docs>
    <cloud />
    <ttl>240</ttl>
    <rating />
    <textInput />
    <skipHours />
    <skipDays />

<image>
     <url>https://www.lucernepublishing.com/images/logo.gif</url>
     <title>Lucerne Publishing</title>
     <link>https://www.lucernepublishing.com/community/podcasts</link>
     <width>300</width>
     <height>300</height>
     <description>Lucerne Logo</description>
</image>

<item>
    <title>The Digital Publication</title>
    <link>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</link>
    <description>Online publications are rapidly changing. A publishing house CEO examines the trends of the past five years and their implications.</description>
    <author>Lucerne</author>
    <category>News</category>
    <comments />
    <enclosure url="https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3" length="10329011" type="audio/mpeg" />
    <guid>https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3</guid>
    <pubDate>Thur, 1 June 2006 14:00:28 EDT</pubDate>
    <source />
</item>

</channel>
```



<span data-ttu-id="47ee9-243">Mapping di elementi del canale RSS a Windows Media Gestione dispositivi valori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="47ee9-243">Mapping of RSS Channel Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="47ee9-244">Nella tabella seguente viene descritto in che modo i valori negli elementi del canale RSS nell'esempio precedente vengono mappati a specifiche proprietà di Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="47ee9-244">The following table describes how the values in the RSS Channel elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="47ee9-245">Windows Media Gestione dispositivi proprietà</span><span class="sxs-lookup"><span data-stu-id="47ee9-245">Windows Media Device Manager property</span></span>                    | <span data-ttu-id="47ee9-246">Valore</span><span class="sxs-lookup"><span data-stu-id="47ee9-246">Value</span></span>                                                                                         |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47ee9-247">g \_ wszWMDMAuthorDate</span><span class="sxs-lookup"><span data-stu-id="47ee9-247">g\_wszWMDMAuthorDate</span></span>](metadata-constants.md)           | <span data-ttu-id="47ee9-248">Venerdì, 9 giugno 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="47ee9-248">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="47ee9-249">g \_ wszWMDMDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="47ee9-249">g\_wszWMDMDESCRIPTION</span></span>](metadata-constants.md)          | <span data-ttu-id="47ee9-250">Il CEO della pubblicazione di Lucerne Peter Bankov esamina le tendenze più recenti nelle pubblicazioni online.</span><span class="sxs-lookup"><span data-stu-id="47ee9-250">Lucerne Publishing CEO Peter Bankov takes a look at the latest trends in online publications.</span></span> |
| [<span data-ttu-id="47ee9-251">\_URL wszWMDMDESTINATION \_ g</span><span class="sxs-lookup"><span data-stu-id="47ee9-251">g\_wszWMDMDESTINATION\_URL</span></span>](metadata-constants.md)     | https://www.lucernepublishing/services/podcasting                                              |
| [<span data-ttu-id="47ee9-252">g \_ wszWMDMEDITOR</span><span class="sxs-lookup"><span data-stu-id="47ee9-252">g\_wszWMDMEDITOR</span></span>](metadata-constants.md)               | someone@example.com                                                                           |
| [<span data-ttu-id="47ee9-253">g \_ wszWMDMFileCreationDate</span><span class="sxs-lookup"><span data-stu-id="47ee9-253">g\_wszWMDMFileCreationDate</span></span>](metadata-constants.md)     | <span data-ttu-id="47ee9-254">Venerdì, 9 giugno 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="47ee9-254">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="47ee9-255">g \_ wszWMDMFileName</span><span class="sxs-lookup"><span data-stu-id="47ee9-255">g\_wszWMDMFileName</span></span>](metadata-constants.md)             | <span data-ttu-id="47ee9-256">Pubblicazione digitale</span><span class="sxs-lookup"><span data-stu-id="47ee9-256">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="47ee9-257">g \_ wszWMDMFileSize</span><span class="sxs-lookup"><span data-stu-id="47ee9-257">g\_wszWMDMFileSize</span></span>](metadata-constants.md)             | <span data-ttu-id="47ee9-258">13.790</span><span class="sxs-lookup"><span data-stu-id="47ee9-258">13,790</span></span>                                                                                        |
| [<span data-ttu-id="47ee9-259">g \_ wszWMDMFormatCode</span><span class="sxs-lookup"><span data-stu-id="47ee9-259">g\_wszWMDMFormatCode</span></span>](metadata-constants.md)           | <span data-ttu-id="47ee9-260">\_ \_ cast multimediale WMDM \_ FORMATCODE</span><span class="sxs-lookup"><span data-stu-id="47ee9-260">WMDM\_FORMATCODE\_MEDIA\_CAST</span></span>                                                                 |
| [<span data-ttu-id="47ee9-261">g \_ wszWMDMGENRE</span><span class="sxs-lookup"><span data-stu-id="47ee9-261">g\_wszWMDMGENRE</span></span>](metadata-constants.md)                | <span data-ttu-id="47ee9-262">Notizie</span><span class="sxs-lookup"><span data-stu-id="47ee9-262">News</span></span>                                                                                          |
| [<span data-ttu-id="47ee9-263">g \_ wszWMDMLAST \_ Data di modifica \_</span><span class="sxs-lookup"><span data-stu-id="47ee9-263">g\_wszWMDMLAST\_MODIFIED\_DATE</span></span>](metadata-constants.md) | <span data-ttu-id="47ee9-264">Venerdì, 9 giugno 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="47ee9-264">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="47ee9-265">g \_ wszWMDMLastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="47ee9-265">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md)     | <span data-ttu-id="47ee9-266">Venerdì, 9 giugno 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="47ee9-266">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |
| [<span data-ttu-id="47ee9-267">g \_ wszWMDMProviderCopyright</span><span class="sxs-lookup"><span data-stu-id="47ee9-267">g\_wszWMDMProviderCopyright</span></span>](metadata-constants.md)    | <span data-ttu-id="47ee9-268">2006 Lucerne Publishing LP, LLLP.</span><span class="sxs-lookup"><span data-stu-id="47ee9-268">2006 Lucerne Publishing LP, LLLP.</span></span> <span data-ttu-id="47ee9-269">All Rights Reserved.</span><span class="sxs-lookup"><span data-stu-id="47ee9-269">All Rights Reserved.</span></span>                                        |
| [<span data-ttu-id="47ee9-270">g \_ wszWMDMTimeToLive</span><span class="sxs-lookup"><span data-stu-id="47ee9-270">g\_wszWMDMTimeToLive</span></span>](metadata-constants.md)           | <span data-ttu-id="47ee9-271">240</span><span class="sxs-lookup"><span data-stu-id="47ee9-271">240</span></span>                                                                                           |
| [<span data-ttu-id="47ee9-272">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="47ee9-272">g\_wszWMDMTitle</span></span>](metadata-constants.md)                | <span data-ttu-id="47ee9-273">Pubblicazione digitale</span><span class="sxs-lookup"><span data-stu-id="47ee9-273">The Digital Publication</span></span>                                                                       |
| [<span data-ttu-id="47ee9-274">g \_ wszWMDMWEBMASTER</span><span class="sxs-lookup"><span data-stu-id="47ee9-274">g\_wszWMDMWEBMASTER</span></span>](metadata-constants.md)            | someone@example.com                                                                           |
| [<span data-ttu-id="47ee9-275">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="47ee9-275">g\_wszWMDMYear</span></span>](metadata-constants.md)                 | <span data-ttu-id="47ee9-276">Venerdì, 9 giugno 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="47ee9-276">Fri, 9 June 2006 14:00:28 EDT</span></span>                                                                 |



 

<span data-ttu-id="47ee9-277">Mapping di elementi immagine RSS a Windows Media Gestione dispositivi valori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="47ee9-277">Mapping of RSS Image Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="47ee9-278">Nella tabella seguente viene descritto in che modo i valori negli elementi immagine RSS nell'esempio precedente vengono mappati a specifiche proprietà di Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="47ee9-278">The following table describes how the values in the RSS Image elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="47ee9-279">Windows Media Gestione dispositivi proprietà</span><span class="sxs-lookup"><span data-stu-id="47ee9-279">Windows Media Device Manager property</span></span>                | <span data-ttu-id="47ee9-280">Valore</span><span class="sxs-lookup"><span data-stu-id="47ee9-280">Value</span></span>                                            |
|------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="47ee9-281">g \_ wszWMDMAlbumCoverFormat</span><span class="sxs-lookup"><span data-stu-id="47ee9-281">g\_wszWMDMAlbumCoverFormat</span></span>](metadata-constants.md) | <span data-ttu-id="47ee9-282">\_ \_ GIF formato oggetto \_ WPD</span><span class="sxs-lookup"><span data-stu-id="47ee9-282">WPD\_OBJECT\_FORMAT\_GIF</span></span>                         |
| [<span data-ttu-id="47ee9-283">g \_ wszWMDMAlbumCoverSize</span><span class="sxs-lookup"><span data-stu-id="47ee9-283">g\_wszWMDMAlbumCoverSize</span></span>](metadata-constants.md)   | <span data-ttu-id="47ee9-284">512</span><span class="sxs-lookup"><span data-stu-id="47ee9-284">512</span></span>                                              |
| [<span data-ttu-id="47ee9-285">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="47ee9-285">g\_wszWMDMDescription</span></span>](metadata-constants.md)      | <span data-ttu-id="47ee9-286">Logo Lucerne</span><span class="sxs-lookup"><span data-stu-id="47ee9-286">Lucerne Logo</span></span>                                     |
| [<span data-ttu-id="47ee9-287">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="47ee9-287">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)   | <span data-ttu-id="47ee9-288">www.lucernepublishing.com/community/podcasts</span><span class="sxs-lookup"><span data-stu-id="47ee9-288">//www.lucernepublishing.com/community/podcasts</span></span>   |
| [<span data-ttu-id="47ee9-289">g \_ wszWMDMHeight</span><span class="sxs-lookup"><span data-stu-id="47ee9-289">g\_wszWMDMHeight</span></span>](metadata-constants.md)           | <span data-ttu-id="47ee9-290">300</span><span class="sxs-lookup"><span data-stu-id="47ee9-290">300</span></span>                                              |
| [<span data-ttu-id="47ee9-291">g \_ wszWMDMSourceURL</span><span class="sxs-lookup"><span data-stu-id="47ee9-291">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)        | https://www.lucernepublishing.com/images/logo.gif |
| [<span data-ttu-id="47ee9-292">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="47ee9-292">g\_wszWMDMTitle</span></span>](metadata-constants.md)            | <span data-ttu-id="47ee9-293">Pubblicazione di Lucerne</span><span class="sxs-lookup"><span data-stu-id="47ee9-293">Lucerne Publishing</span></span>                               |
| [<span data-ttu-id="47ee9-294">g \_ wszWMDMWidth</span><span class="sxs-lookup"><span data-stu-id="47ee9-294">g\_wszWMDMWidth</span></span>](metadata-constants.md)            | <span data-ttu-id="47ee9-295">300</span><span class="sxs-lookup"><span data-stu-id="47ee9-295">300</span></span>                                              |



 

<span data-ttu-id="47ee9-296">Mapping di elementi elemento RSS a Windows Media Gestione dispositivi valori delle proprietà</span><span class="sxs-lookup"><span data-stu-id="47ee9-296">Mapping of RSS Item Elements to Windows Media Device Manager Property Values</span></span>

<span data-ttu-id="47ee9-297">Nella tabella seguente viene descritto in che modo i valori negli elementi RSS dell'esempio precedente vengono mappati a specifiche proprietà di Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="47ee9-297">The following table describes how the values in the RSS Item elements in the previous example map to particular Windows Media Device Manager properties.</span></span>



| <span data-ttu-id="47ee9-298">Windows Media Gestione dispositivi proprietà</span><span class="sxs-lookup"><span data-stu-id="47ee9-298">Windows Media Device Manager property</span></span>                | <span data-ttu-id="47ee9-299">Valore</span><span class="sxs-lookup"><span data-stu-id="47ee9-299">Value</span></span>                                                                                                                               |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47ee9-300">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="47ee9-300">g\_wszWMDMAuthor</span></span>](metadata-constants.md)           | <span data-ttu-id="47ee9-301">Lucerna</span><span class="sxs-lookup"><span data-stu-id="47ee9-301">Lucerne</span></span>                                                                                                                             |
| [<span data-ttu-id="47ee9-302">g \_ wszWMDMAuthorDate</span><span class="sxs-lookup"><span data-stu-id="47ee9-302">g\_wszWMDMAuthorDate</span></span>](metadata-constants.md)       | <span data-ttu-id="47ee9-303">Gio, 1 giugno 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="47ee9-303">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="47ee9-304">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="47ee9-304">g\_wszWMDMDescription</span></span>](metadata-constants.md)      | <span data-ttu-id="47ee9-305">Le pubblicazioni online sono in rapida evoluzione.</span><span class="sxs-lookup"><span data-stu-id="47ee9-305">Online publications are rapidly changing.</span></span> <span data-ttu-id="47ee9-306">Un CEO della casa di pubblicazione esamina le tendenze degli ultimi cinque anni e le loro implicazioni.</span><span class="sxs-lookup"><span data-stu-id="47ee9-306">A publishing house CEO examines the trends of the past five years and their implications.</span></span> |
| [<span data-ttu-id="47ee9-307">g \_ wszWMDMDestinationURL</span><span class="sxs-lookup"><span data-stu-id="47ee9-307">g\_wszWMDMDestinationURL</span></span>](metadata-constants.md)   | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="47ee9-308">g \_ wszWMDMDuration</span><span class="sxs-lookup"><span data-stu-id="47ee9-308">g\_wszWMDMDuration</span></span>](metadata-constants.md)         | <span data-ttu-id="47ee9-309">120325445</span><span class="sxs-lookup"><span data-stu-id="47ee9-309">120325445</span></span>                                                                                                                           |
| [<span data-ttu-id="47ee9-310">g \_ wszWMDMFileCreationDate</span><span class="sxs-lookup"><span data-stu-id="47ee9-310">g\_wszWMDMFileCreationDate</span></span>](metadata-constants.md) | <span data-ttu-id="47ee9-311">Gio, 1 giugno 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="47ee9-311">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="47ee9-312">g \_ wszWMDMFileSize</span><span class="sxs-lookup"><span data-stu-id="47ee9-312">g\_wszWMDMFileSize</span></span>](metadata-constants.md)         | <span data-ttu-id="47ee9-313">10329011</span><span class="sxs-lookup"><span data-stu-id="47ee9-313">10329011</span></span>                                                                                                                            |
| [<span data-ttu-id="47ee9-314">g \_ wszWMDMFormatCode</span><span class="sxs-lookup"><span data-stu-id="47ee9-314">g\_wszWMDMFormatCode</span></span>](metadata-constants.md)       | <span data-ttu-id="47ee9-315">WMDM \_ FORMATCODE \_ MP3</span><span class="sxs-lookup"><span data-stu-id="47ee9-315">WMDM\_FORMATCODE\_MP3</span></span>                                                                                                               |
| [<span data-ttu-id="47ee9-316">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="47ee9-316">g\_wszWMDMGenre</span></span>](metadata-constants.md)            | <span data-ttu-id="47ee9-317">Notizie</span><span class="sxs-lookup"><span data-stu-id="47ee9-317">News</span></span>                                                                                                                                |
| [<span data-ttu-id="47ee9-318">g \_ wszWMDMLastModifiedDate</span><span class="sxs-lookup"><span data-stu-id="47ee9-318">g\_wszWMDMLastModifiedDate</span></span>](metadata-constants.md) | <span data-ttu-id="47ee9-319">Gio, 1 giugno 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="47ee9-319">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |
| [<span data-ttu-id="47ee9-320">g \_ wszWMDMMediaGuid</span><span class="sxs-lookup"><span data-stu-id="47ee9-320">g\_wszWMDMMediaGuid</span></span>](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="47ee9-321">g \_ wszWMDMSourceURL</span><span class="sxs-lookup"><span data-stu-id="47ee9-321">g\_wszWMDMSourceURL</span></span>](metadata-constants.md)        | https://www.lucernepublishing/services/podcasting/digital.publishing/audio/2006/06/digital0601.mp3                                   |
| [<span data-ttu-id="47ee9-322">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="47ee9-322">g\_wszWMDMTitle</span></span>](metadata-constants.md)            | <span data-ttu-id="47ee9-323">Pubblicazione digitale</span><span class="sxs-lookup"><span data-stu-id="47ee9-323">The Digital Publication</span></span>                                                                                                             |
| [<span data-ttu-id="47ee9-324">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="47ee9-324">g\_wszWMDMYear</span></span>](metadata-constants.md)             | <span data-ttu-id="47ee9-325">Gio, 1 giugno 2006 14:00:28 EDT</span><span class="sxs-lookup"><span data-stu-id="47ee9-325">Thur, 1 June 2006 14:00:28 EDT</span></span>                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="47ee9-326">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="47ee9-326">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47ee9-327">**Costanti dei metadati**</span><span class="sxs-lookup"><span data-stu-id="47ee9-327">**Metadata Constants**</span></span>](metadata-constants.md)
</dt> </dl>

 

 




