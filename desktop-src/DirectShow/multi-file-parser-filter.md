---
description: Filtro del parser multi-file
ms.assetid: 8ef06f49-fda4-49e2-9b07-70453a2e897c
title: Filtro del parser multi-file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d86663412400a4c1b116b6f831c80f72d66f88e648cf8f245be6581240d986bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152985"
---
# <a name="multi-file-parser-filter"></a>Filtro del parser multi-file

Il filtro Multi-File Parser analizza un formato di file semplice che consente di impostare più nomi di file come se fossero un unico file. Questi file hanno il formato illustrato nell'esempio seguente:


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



L'uso di questo filtro è deprecato. Per eseguire il rendering di più file all'interno dello stesso grafo di filtro, l'applicazione deve semplicemente chiamare **RenderFile** o **AddSourceFilter** più volte.



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
<li>Tipo di formato: GUID_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td><ul>
<li>Tipo principale: MEDIATYPE_File</li>
<li>Sottotipo: GUID_NULL</li>
<li>Tipo di formato: MEDIATYPE_File</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce pin di output</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Filtro CLSID</td>
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

Il filtro crea un pin di output per ogni file elencato nel file di origine. Il tipo di output è MEDIATYPE File e il blocco di formato per il tipo di output è una \_ stringa di caratteri wide che contiene il nome del file. Ogni pin si connette a un'istanza del filtro [Renderer del flusso di](file-stream-renderer-filter.md) file. Il filtro Renderer del flusso di file crea un pin di output, che espone [**l'interfaccia IStreamBuilder.**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) Il pin di output esegue il rendering del file specificato. Non vengono trasmessi dati multimediali tra il parser multi-file e il renderer del flusso di file.

Il CLSID del filtro non è definito in Uuids.h. Usare questa macro nel proprio file di intestazione:


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



