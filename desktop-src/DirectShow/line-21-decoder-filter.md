---
description: Filtro decodificatore riga 21
ms.assetid: 48fa5484-1f8c-4133-b2e1-888cb1834402
title: Filtro decodificatore riga 21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9951cd8e6093131d45597d1a89c32c36222eb20a
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986464"
---
# <a name="line-21-decoder-filter"></a>Filtro decodificatore riga 21

Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

Questo filtro del decodificatore Line 21 decodifica i dati della riga 21 e disegna il testo della didascalia sulle bitmap.

Il pin di input si connette a qualsiasi provider di dati di riga 21, in genere un decodificatore video DVD o il [filtro CC Decoder.](cc-decoder-filter.md) Il decodificatore CC fornisce i dati della riga 21 provenienti dall'interfaccia vbi di un segnale tv analogico. Il pin di output si connette a un pin secondario nel Mixer overlay [o](overlay-mixer-filter.md) a un altro renderer video, ad esempio vmr.

Questo filtro accetta i dati della riga 21 nel formato standard della coppia di byte o, per DVD, come pacchetto per l'intero gruppo di immagini (GOP). Per ogni GOP nel flusso video DVD, può essere presente un pacchetto di dati utente con le informazioni di intestazione e i dati della riga 21 specifici di GOP. Il formato delle coppie di byte è definito nello standard EIA/CEA-608-B; Per altre informazioni, fare riferimento a tale standard.

Sono disponibili due versioni di questo filtro:



| Filtra            | CLSID                 |
|-------------------|-----------------------|
| Decodificatore riga 21   | CLSID \_ Line21Decoder  |
| Decodificatore riga 21 | CLSID \_ Line21Decoder2 |



 

Il filtro versione 1 viene usato nelle piattaforme Microsoft® Windows® 95/98/Me Windows 2000. Il filtro versione 2 è disponibile in Microsoft Windows XP e versioni successive e viene usato ogni volta che il renderer di combinazione di video è presente nel grafico.

Le informazioni nella tabella seguente si applicano a entrambe le versioni del filtro:




| Etichetta | Valore |
|--------|-------|
| Interfacce di filtro | <a href="/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder"><strong>IAMLine21Decoder</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a> | 
| Tipi di supporti pin di input | Tipo principale: MEDIATYPE_AUXLine21DataSubtype:<br /><ul><li>MEDIASUBTYPE_Line21_BytePair (riga standard 21)</li><li>MEDIASUBTYPE_Line21_GOPPacket (dvd riga 21)</li></ul>Tipo di formato: FORMAT_VideoInfo o GUID_NULL<br /> | 
| Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipi di supporti pin di output | Tipo principale: MEDIATYPE_VideoSubtype:<br /><ul><li>MEDIASUBTYPE_RGB8</li><li>MEDIASUBTYPE_RGB555</li><li>MEDIASUBTYPE_RGB565</li><li>MEDIASUBTYPE_RGB24</li><li>MEDIASUBTYPE_RGB32</li></ul>Tipo di formato: FORMAT_VideoInfo<br /> | 
| Interfacce pin di output | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| CLSID del filtro | Vedere la tabella precedente | 
| CLSID pagina delle proprietà | Nessuno | 
| File eseguibile | qdvd.dll | 
| <a href="merit.md">Merito</a> | Decodificatore riga 21: MERIT_NORMALLine 21 Decoder 2: MERIT_NORMAL + 2<br /> | 
| <a href="filter-categories.md">Categoria filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Sottotitoli codificati e teletesto](closed-captions-and-teletext.md)
</dt> <dt>

[Configurazione dell'Graph DVD](dvd-filter-graph-configuration.md)
</dt> </dl>

 

 




