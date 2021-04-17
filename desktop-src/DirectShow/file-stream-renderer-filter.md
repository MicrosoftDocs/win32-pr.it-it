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
# <a name="file-stream-renderer-filter"></a>Filtro del renderer del flusso di file

Il filtro renderer del flusso di file esegue il rendering dei nomi di file analizzati dal filtro del parser per più [file](multi-file-parser-filter.md) . Per ulteriori informazioni, vedere la documentazione relativa a tale filtro.

L'uso di questo filtro è deprecato. Per eseguire il rendering di più file all'interno dello stesso grafico di filtro, l'applicazione deve semplicemente chiamare **RenderFile** o **AddSourceFilter** più volte.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td><ul>
<li>Tipo principale: MEDIATYPE_File</li>
<li>Sottotipo: GUID_NULL</li>
<li>Tipo formato: MEDIATYPE_File</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td>nessuno</td>
</tr>
<tr class="odd">
<td>Interfacce del PIN di output</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></td>
</tr>
<tr class="even">
<td>CLSID filtro</td>
<td>CLSID_FileRend</td>
</tr>
<tr class="odd">
<td>File eseguibile</td>
<td>Quartz.dll</td>
</tr>
<tr class="even">
<td><a href="merit.md">Merito</a></td>
<td>MERIT_UNLIKELY</td>
</tr>
<tr class="odd">
<td><a href="filter-categories.md">Categoria filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Il CLSID del filtro non è definito in UUIDs. h. Usare questa macro nel proprio file di intestazione:


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



