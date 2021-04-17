---
description: Filtro del renderer del flusso di file
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Filtro del renderer del flusso di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64c8d8a0c87dab3aa811c8246be24ded8ee04dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522314"
---
# <a name="file-stream-renderer-filter"></a><span data-ttu-id="1fd9a-103">Filtro del renderer del flusso di file</span><span class="sxs-lookup"><span data-stu-id="1fd9a-103">File Stream Renderer Filter</span></span>

<span data-ttu-id="1fd9a-104">Il filtro renderer del flusso di file esegue il rendering dei nomi di file analizzati dal filtro del parser per più [file](multi-file-parser-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="1fd9a-104">The File Stream Renderer filter renders file names that are parsed by the [Multi-File Parser](multi-file-parser-filter.md) filter.</span></span> <span data-ttu-id="1fd9a-105">Per ulteriori informazioni, vedere la documentazione relativa a tale filtro.</span><span class="sxs-lookup"><span data-stu-id="1fd9a-105">For more information, see the documentation for that filter.</span></span>

<span data-ttu-id="1fd9a-106">L'uso di questo filtro è deprecato.</span><span class="sxs-lookup"><span data-stu-id="1fd9a-106">The use of this filter is deprecated.</span></span> <span data-ttu-id="1fd9a-107">Per eseguire il rendering di più file all'interno dello stesso grafico di filtro, l'applicazione deve semplicemente chiamare **RenderFile** o **AddSourceFilter** più volte.</span><span class="sxs-lookup"><span data-stu-id="1fd9a-107">To render multiple files within the same filter graph, the application should simply call **RenderFile** or **AddSourceFilter** multiple times.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1fd9a-108">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="1fd9a-108">Filter interfaces</span></span></td>
<td><span data-ttu-id="1fd9a-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd9a-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd9a-110">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="1fd9a-110">Input pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="1fd9a-111">Tipo principale: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="1fd9a-111">Major type: MEDIATYPE_File</span></span></li>
<li><span data-ttu-id="1fd9a-112">Sottotipo: GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="1fd9a-112">Subtype: GUID_NULL</span></span></li>
<li><span data-ttu-id="1fd9a-113">Tipo formato: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="1fd9a-113">Format type: MEDIATYPE_File</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd9a-114">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="1fd9a-114">Input pin interfaces</span></span></td>
<td><span data-ttu-id="1fd9a-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd9a-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd9a-116">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="1fd9a-116">Output pin media types</span></span></td>
<td><span data-ttu-id="1fd9a-117">nessuno</span><span class="sxs-lookup"><span data-stu-id="1fd9a-117">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd9a-118">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="1fd9a-118">Output pin interfaces</span></span></td>
<td><span data-ttu-id="1fd9a-119"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></span><span class="sxs-lookup"><span data-stu-id="1fd9a-119"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd9a-120">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="1fd9a-120">Filter CLSID</span></span></td>
<td><span data-ttu-id="1fd9a-121">CLSID_FileRend</span><span class="sxs-lookup"><span data-stu-id="1fd9a-121">CLSID_FileRend</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd9a-122">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="1fd9a-122">Executable</span></span></td>
<td><span data-ttu-id="1fd9a-123">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="1fd9a-123">Quartz.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fd9a-124"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="1fd9a-124"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="1fd9a-125">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="1fd9a-125">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fd9a-126"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="1fd9a-126"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="1fd9a-127">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="1fd9a-127">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="1fd9a-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="1fd9a-128">Remarks</span></span>

<span data-ttu-id="1fd9a-129">Il CLSID del filtro non è definito in UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="1fd9a-129">The filter's CLSID is not defined in Uuids.h.</span></span> <span data-ttu-id="1fd9a-130">Usare questa macro nel proprio file di intestazione:</span><span class="sxs-lookup"><span data-stu-id="1fd9a-130">Use this macro in your own header file:</span></span>


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a><span data-ttu-id="1fd9a-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1fd9a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fd9a-132">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="1fd9a-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



