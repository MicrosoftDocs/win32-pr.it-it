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
# <a name="multi-file-parser-filter"></a>Filtro parser per più file

Il filtro parser per più file analizza un formato di file semplice che consente di specificare più nomi di file come se fossero un unico file. Questi file hanno il formato illustrato nell'esempio seguente:


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



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
<li>Tipo principale: MEDIATYPE_Stream</li>
<li>Sottotipo: CLSID_MultFile</li>
<li>Tipo formato: GUID_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td><ul>
<li>Tipo principale: MEDIATYPE_File</li>
<li>Sottotipo: GUID_NULL</li>
<li>Tipo formato: MEDIATYPE_File</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce del PIN di output</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID filtro</td>
<td>CLSID_MultFile</td>
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

Il filtro crea un pin di output per ogni file elencato nel file di origine. Il tipo di output è il \_ file MEDIATYPE e il blocco di formato per il tipo di output è una stringa di caratteri wide che contiene il nome del file. Ogni pin si connette a un'istanza del filtro [renderer del flusso di file](file-stream-renderer-filter.md) . Il filtro di rendering del flusso di file crea un pin di output, che espone l'interfaccia [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) . Il pin di output esegue il rendering del file specificato. Non vengono trasmessi dati multimediali tra il parser per più file e il renderer del flusso di file.

Il CLSID del filtro non è definito in UUIDs. h. Usare questa macro nel proprio file di intestazione:


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



