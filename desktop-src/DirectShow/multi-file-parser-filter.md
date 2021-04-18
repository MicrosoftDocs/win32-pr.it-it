---
description: Filtro parser per più file
ms.assetid: 8ef06f49-fda4-49e2-9b07-70453a2e897c
title: Filtro parser per più file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fc83a56bb12c307b85be875a3a2e7e73b744d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304133"
---
# <a name="multi-file-parser-filter"></a><span data-ttu-id="9da19-103">Filtro parser per più file</span><span class="sxs-lookup"><span data-stu-id="9da19-103">Multi-File Parser Filter</span></span>

<span data-ttu-id="9da19-104">Il filtro parser per più file analizza un formato di file semplice che consente di specificare più nomi di file come se fossero un unico file.</span><span class="sxs-lookup"><span data-stu-id="9da19-104">The Multi-File Parser filter parses a simple file format that enables multiple file names to be specified as though they were one file.</span></span> <span data-ttu-id="9da19-105">Questi file hanno il formato illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="9da19-105">These files have the format shown in the following example:</span></span>


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



<span data-ttu-id="9da19-106">L'uso di questo filtro è deprecato.</span><span class="sxs-lookup"><span data-stu-id="9da19-106">The use of this filter is deprecated.</span></span> <span data-ttu-id="9da19-107">Per eseguire il rendering di più file all'interno dello stesso grafico di filtro, l'applicazione deve semplicemente chiamare **RenderFile** o **AddSourceFilter** più volte.</span><span class="sxs-lookup"><span data-stu-id="9da19-107">To render multiple files within the same filter graph, the application should simply call **RenderFile** or **AddSourceFilter** multiple times.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9da19-108">Interfacce di filtro</span><span class="sxs-lookup"><span data-stu-id="9da19-108">Filter interfaces</span></span></td>
<td><span data-ttu-id="9da19-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="9da19-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9da19-110">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="9da19-110">Input pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="9da19-111">Tipo principale: MEDIATYPE_Stream</span><span class="sxs-lookup"><span data-stu-id="9da19-111">Major type: MEDIATYPE_Stream</span></span></li>
<li><span data-ttu-id="9da19-112">Sottotipo: CLSID_MultFile</span><span class="sxs-lookup"><span data-stu-id="9da19-112">Subtype: CLSID_MultFile</span></span></li>
<li><span data-ttu-id="9da19-113">Tipo formato: GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="9da19-113">Format type: GUID_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9da19-114">Interfacce pin di input</span><span class="sxs-lookup"><span data-stu-id="9da19-114">Input pin interfaces</span></span></td>
<td><span data-ttu-id="9da19-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="9da19-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9da19-116">Tipi di supporti pin di output</span><span class="sxs-lookup"><span data-stu-id="9da19-116">Output pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="9da19-117">Tipo principale: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="9da19-117">Major type: MEDIATYPE_File</span></span></li>
<li><span data-ttu-id="9da19-118">Sottotipo: GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="9da19-118">Subtype: GUID_NULL</span></span></li>
<li><span data-ttu-id="9da19-119">Tipo formato: MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="9da19-119">Format type: MEDIATYPE_File</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9da19-120">Interfacce del PIN di output</span><span class="sxs-lookup"><span data-stu-id="9da19-120">Output pin interfaces</span></span></td>
<td><span data-ttu-id="9da19-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="9da19-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9da19-122">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="9da19-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="9da19-123">CLSID_MultFile</span><span class="sxs-lookup"><span data-stu-id="9da19-123">CLSID_MultFile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9da19-124">File eseguibile</span><span class="sxs-lookup"><span data-stu-id="9da19-124">Executable</span></span></td>
<td><span data-ttu-id="9da19-125">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="9da19-125">Quartz.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9da19-126"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="9da19-126"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="9da19-127">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="9da19-127">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9da19-128"><a href="filter-categories.md">Categoria filtro</a></span><span class="sxs-lookup"><span data-stu-id="9da19-128"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="9da19-129">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="9da19-129">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="9da19-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="9da19-130">Remarks</span></span>

<span data-ttu-id="9da19-131">Il filtro crea un pin di output per ogni file elencato nel file di origine.</span><span class="sxs-lookup"><span data-stu-id="9da19-131">The filter creates one output pin for each file listed in the source file.</span></span> <span data-ttu-id="9da19-132">Il tipo di output è il \_ file MEDIATYPE e il blocco di formato per il tipo di output è una stringa di caratteri wide che contiene il nome del file.</span><span class="sxs-lookup"><span data-stu-id="9da19-132">The output type is MEDIATYPE\_File, and the format block for the output type is a wide-character string that contains the file name.</span></span> <span data-ttu-id="9da19-133">Ogni pin si connette a un'istanza del filtro [renderer del flusso di file](file-stream-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="9da19-133">Each pin connects to an instance of the [File Stream Renderer](file-stream-renderer-filter.md) filter.</span></span> <span data-ttu-id="9da19-134">Il filtro di rendering del flusso di file crea un pin di output, che espone l'interfaccia [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) .</span><span class="sxs-lookup"><span data-stu-id="9da19-134">The File Stream Renderer filter creates one output pin, which exposes the [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) interface.</span></span> <span data-ttu-id="9da19-135">Il pin di output esegue il rendering del file specificato.</span><span class="sxs-lookup"><span data-stu-id="9da19-135">The output pin renders the specified file.</span></span> <span data-ttu-id="9da19-136">Non vengono trasmessi dati multimediali tra il parser per più file e il renderer del flusso di file.</span><span class="sxs-lookup"><span data-stu-id="9da19-136">No media data travels between the Multi-File Parser and the File Stream Renderer.</span></span>

<span data-ttu-id="9da19-137">Il CLSID del filtro non è definito in UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="9da19-137">The filter's CLSID is not defined in Uuids.h.</span></span> <span data-ttu-id="9da19-138">Usare questa macro nel proprio file di intestazione:</span><span class="sxs-lookup"><span data-stu-id="9da19-138">Use this macro in your own header file:</span></span>


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a><span data-ttu-id="9da19-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9da19-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9da19-140">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="9da19-140">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



