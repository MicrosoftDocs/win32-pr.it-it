---
description: Filtro renderer interno comando script
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Filtro renderer interno comando script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b241643d991e9348015dc51ea5b2f1c4875f079d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521594"
---
# <a name="internal-script-command-renderer-filter"></a><span data-ttu-id="68a98-103">Filtro renderer interno comando script</span><span class="sxs-lookup"><span data-stu-id="68a98-103">Internal Script Command Renderer Filter</span></span>

<span data-ttu-id="68a98-104">Riceve i comandi di script e li invia all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="68a98-104">Receives script commands and dispatches them to the application.</span></span>

<span data-ttu-id="68a98-105">Questo filtro accetta i comandi script in uno dei due formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="68a98-105">This filter accepts script commands in one of two formats:</span></span>

-   <span data-ttu-id="68a98-106">\_Testo MEDIATYPE: ogni esempio multimediale contiene una stringa di testo ANSI.</span><span class="sxs-lookup"><span data-stu-id="68a98-106">MEDIATYPE\_Text: Each media sample contains an ANSI text string.</span></span>
-   <span data-ttu-id="68a98-107">MEDIATYPE \_ ScriptCommand: ogni esempio di supporto contiene due stringhe Unicode con terminazione null, concatenate insieme.</span><span class="sxs-lookup"><span data-stu-id="68a98-107">MEDIATYPE\_ScriptCommand: Each media sample contains two NULL-terminated Unicode strings, concatenated together.</span></span> <span data-ttu-id="68a98-108">La prima stringa descrive il tipo di comando e la seconda stringa è il comando script.</span><span class="sxs-lookup"><span data-stu-id="68a98-108">The first string describes the command type and the second string is the script command.</span></span>

    <span data-ttu-id="68a98-109">Quando il filtro riceve un esempio, invia una notifica degli eventi dell' [**\_ \_ evento OLE EC**](ec-ole-event.md) .</span><span class="sxs-lookup"><span data-stu-id="68a98-109">When the filter receives a sample, it sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="68a98-110">Il primo parametro dell'evento è un **BSTR** con il tipo di comando o `Text` se il formato è MEDIATYPE \_ testo.</span><span class="sxs-lookup"><span data-stu-id="68a98-110">The first event parameter is a **BSTR** with the command type, or `Text` if the format is MEDIATYPE\_Text.</span></span> <span data-ttu-id="68a98-111">Il secondo parametro dell'evento è un **BSTR** con il comando script.</span><span class="sxs-lookup"><span data-stu-id="68a98-111">The second event parameter is a **BSTR** with the script command.</span></span> <span data-ttu-id="68a98-112">L'applicazione può recuperare l'evento e rispondere al comando script.</span><span class="sxs-lookup"><span data-stu-id="68a98-112">The application can retrieve the event and respond to the script command.</span></span>

<span data-ttu-id="68a98-113">Per un esempio di come usare questo filtro, vedere [parser Sami (CC)](sami--cc--parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="68a98-113">For an example of how to use this filter, see [SAMI (CC) Parser](sami--cc--parser-filter.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="68a98-114">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="68a98-114">Filter Interfaces</span></span></td>
<td><span data-ttu-id="68a98-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="68a98-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68a98-116">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="68a98-116">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="68a98-117">MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="68a98-117">MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</span></span></li>
<li><span data-ttu-id="68a98-118">MEDIATYPE_Text, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="68a98-118">MEDIATYPE_Text, MEDIASUBTYPE_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68a98-119">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="68a98-119">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="68a98-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="68a98-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68a98-121">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="68a98-121">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="68a98-122">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="68a98-122">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68a98-123">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="68a98-123">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="68a98-124">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="68a98-124">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68a98-125">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="68a98-125">Filter CLSID</span></span></td>
<td><span data-ttu-id="68a98-126">{48025243-2D39-11CE-875D-00608CB78066}</span><span class="sxs-lookup"><span data-stu-id="68a98-126">{48025243-2D39-11CE-875D-00608CB78066}</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68a98-127">CLSID della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="68a98-127">Property Page CLSID</span></span></td>
<td><span data-ttu-id="68a98-128">Nessuna pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="68a98-128">No property page</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68a98-129">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="68a98-129">Executable</span></span></td>
<td><span data-ttu-id="68a98-130">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="68a98-130">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68a98-131"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="68a98-131"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="68a98-132">MERIT_PREFERRED + 1</span><span class="sxs-lookup"><span data-stu-id="68a98-132">MERIT_PREFERRED + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68a98-133"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="68a98-133"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="68a98-134">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="68a98-134">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="68a98-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="68a98-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68a98-136">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="68a98-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



