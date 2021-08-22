---
description: Filtro decodificatore riga 21
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Filtro decodificatore riga 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a265b2b547b2ef1a18b65b5588afb9ed7e5e0215446f5f9967244ca5dbd20332
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584461"
---
# <a name="line-21-decoder-filter"></a>Filtro decodificatore riga 21

Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

Questo filtro decodificatore Line 21 decodifica i dati della riga 21 e disegna il testo della didascalia sulle bitmap.

Il pin di input si connette a qualsiasi provider di dati della riga 21, in genere un decodificatore video DVD o il [filtro CC Decoder.](cc-decoder-filter.md) Il decodificatore CC fornisce i dati della riga 21 dall'interfaccia VBI di un segnale tv analogico. Il pin di output si connette a un segnaposto secondario nel Mixer [o](overlay-mixer-filter.md) a un altro renderer video, ad esempio vmr.

Questo filtro accetta i dati della riga 21 nel formato standard della coppia di byte o, per DVD, come pacchetto per l'intero gruppo di immagini (GOP). Per ogni GOP nel flusso video DVD, può essere presente un pacchetto di dati utente con le informazioni di intestazione e i dati della riga 21 specifici di GOP. Il formato delle coppie di byte è definito nello standard EIA/CEA-608-B; Per altre informazioni, fare riferimento a tale standard.

Sono disponibili due versioni di questo filtro:



| Filtra            | CLSID                 |
|-------------------|-----------------------|
| Decodificatore riga 21   | CLSID \_ Line21Decoder  |
| Decodificatore di riga 21 | CLSID \_ Line21Decoder2 |



 

Il filtro versione 1 viene usato nelle piattaforme Microsoft® Windows® 95/98/Me e Windows 2000. Il filtro versione 2 è disponibile in Microsoft Windows XP e versioni successive e viene usato ogni volta che il renderer di combinazione video si trova nel grafico.

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
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
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
Tipo di formato: FORMAT_VideoInfo<br/></td>
</tr>
<tr class="odd">
<td>Interfacce pin di output</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Filtro CLSID</td>
<td>Vedere la tabella precedente</td>
</tr>
<tr class="odd">
<td>CLSID della pagina delle proprietà</td>
<td>Nessuno</td>
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

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Sottotitoli codificati e teletext](closed-captions-and-teletext.md)
</dt> <dt>

[Configurazione del filtro DVD Graph](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




