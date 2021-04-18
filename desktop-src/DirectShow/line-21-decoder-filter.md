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
# <a name="line-21-decoder-filter"></a>Filtro decodificatore riga 21

Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

Questo filtro decodificatore riga 21 decodifica i dati della riga 21 e disegna il testo della didascalia sulle bitmap.

Il pin di input si connette a un provider di dati della riga 21, in genere un decodificatore video DVD o il filtro [decodificatore CC](cc-decoder-filter.md) . Il decodificatore CC fornisce i dati della riga 21 dal VBI di un segnale televisivo analogo. Il pin di output si connette a un pin secondario sul [mixer della sovrimpressione](overlay-mixer-filter.md) o a un altro renderer video, ad esempio VMR.

Questo filtro accetta i dati della riga 21 nel formato standard della coppia di byte oppure, per DVD, come pacchetto per l'intero Group of Pictures (GOP). Per ogni GOP nel flusso video DVD, può essere presente un pacchetto di dati utente con le informazioni di intestazione e i dati della riga 21 specifici del GOP. Il formato delle coppie di byte è definito nello standard EIA/CEA-608-B; Per ulteriori informazioni, fare riferimento a tale standard.

Sono disponibili due versioni di questo filtro:



| Filtra            | CLSID                 |
|-------------------|-----------------------|
| Decodificatore riga 21   | \_LINE21DECODER CLSID  |
| Decodificatore riga 21 2 | \_LINE21DECODER2 CLSID |



 

Il filtro versione 1 viene usato nelle piattaforme Microsoft® Windows® 95/98/me e Windows 2000. Il filtro versione 2 è disponibile in Microsoft Windows XP e versioni successive e viene usato ogni volta che il renderer di missaggio video si trova nel grafico.

Le informazioni nella tabella seguente si applicano a entrambe le versioni del filtro:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td><a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td>Tipo principale: MEDIATYPE_AUXLine21DataSubtype:<br/>
<ul>
<li>MEDIASUBTYPE_Line21_BytePair (riga standard 21)</li>
<li>MEDIASUBTYPE_Line21_GOPPacket (riga DVD 21)</li>
</ul>
Tipo di formato: FORMAT_VideoInfo o GUID_NULL<br/></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td>Tipo principale: MEDIATYPE_VideoSubtype:<br/>
<ul>
<li>MEDIASUBTYPE_RGB8</li>
<li>MEDIASUBTYPE_RGB555</li>
<li>MEDIASUBTYPE_RGB565</li>
<li>MEDIASUBTYPE_RGB24</li>
<li>MEDIASUBTYPE_RGB32</li>
</ul>
Tipo formato: FORMAT_VideoInfo<br/></td>
</tr>
<tr class="odd">
<td>Interfacce del PIN di output</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID filtro</td>
<td>Vedere la tabella precedente</td>
</tr>
<tr class="odd">
<td>CLSID della pagina delle proprietà</td>
<td>nessuno</td>
</tr>
<tr class="even">
<td>File eseguibile</td>
<td>qdvd.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Merito</a></td>
<td>Decodificatore riga 21: MERIT_NORMALLine 21 decodificatore 2: MERIT_NORMAL + 2<br/></td>
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
</dt> <dt>

[Didascalie e televideo chiusi](closed-captions-and-teletext.md)
</dt> <dt>

[Configurazione del grafico del filtro DVD](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




