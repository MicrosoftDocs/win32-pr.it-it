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
# <a name="internal-script-command-renderer-filter"></a>Filtro renderer interno comando script

Riceve i comandi di script e li invia all'applicazione.

Questo filtro accetta i comandi script in uno dei due formati seguenti:

-   \_Testo MEDIATYPE: ogni esempio multimediale contiene una stringa di testo ANSI.
-   MEDIATYPE \_ ScriptCommand: ogni esempio di supporto contiene due stringhe Unicode con terminazione null, concatenate insieme. La prima stringa descrive il tipo di comando e la seconda stringa è il comando script.

    Quando il filtro riceve un esempio, invia una notifica degli eventi dell' [**\_ \_ evento OLE EC**](ec-ole-event.md) . Il primo parametro dell'evento è un **BSTR** con il tipo di comando o `Text` se il formato è MEDIATYPE \_ testo. Il secondo parametro dell'evento è un **BSTR** con il comando script. L'applicazione può recuperare l'evento e rispondere al comando script.

Per un esempio di come usare questo filtro, vedere [parser Sami (CC)](sami--cc--parser-filter.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td><ul>
<li>MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</li>
<li>MEDIATYPE_Text, MEDIASUBTYPE_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td>Non applicabile</td>
</tr>
<tr class="odd">
<td>Interfacce del PIN di output</td>
<td>Non applicabile</td>
</tr>
<tr class="even">
<td>CLSID filtro</td>
<td>{48025243-2D39-11CE-875D-00608CB78066}</td>
</tr>
<tr class="odd">
<td>CLSID della pagina delle proprietà</td>
<td>Nessuna pagina delle proprietà</td>
</tr>
<tr class="even">
<td>File eseguibile</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Merito</a></td>
<td>MERIT_PREFERRED + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



