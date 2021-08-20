---
description: Filtro decodificatore WST
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Filtro decodificatore WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d61da0540c683e8c4646074715b0518717b4e1958beea5b8ca2ae41fb4629790
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290771"
---
# <a name="wst-decoder-filter"></a>Filtro decodificatore WST

Questo componente è stato rimosso da Windows Vista e dai sistemi operativi successivi. È disponibile per l'uso nei sistemi operativi Windows XP e Windows Server 2003.

> [!Note]  
> A partire da Windows Vista, DirectShow non fornisce un filtro per decodificare il teletesto standard (WST).

 

Il decodificatore WST è un filtro in modalità kernel che accetta dati teletext World Standard decodificati dal [codec WST](wst-codec-filter.md) e recapita le bitmap al Pin 2 nel [Mixer](overlay-mixer-filter.md) di sovrapposizione usando i tipi di carattere forniti da Microsoft. Al momento sono supportate solo le lingue dell'Europa occidentale. Non sono attualmente disponibili tipi di carattere Unicode.

Questo filtro può essere aggiunto automaticamente al grafico chiamando [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)usando il pin di output del codec WST.



| Etichetta | Valore |
|------------------------------------------|---------------------------------------------------------------|
| Interfacce di filtro                        | ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder) |
| Tipi di supporti pin di input                    | MEDIATYPE \_ VBI, MEDIASUBTYPE \_ TELETEXT                        |
| Interfacce pin di input                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Tipi di supporti pin di output                   | MEDIATYPE \_ Video                                              |
| Interfacce pin di output                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Filtro CLSID                             | CLSID \_ WSTDecoder                                             |
| CLSID della pagina delle proprietà                      | CLSID \_ WstDecoderPropertyPage                                 |
| File eseguibile                               | Wstdecod.DLL                                                  |
| [Merito](merit.md)                       | MERITO \_ NORMALE                                                 |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Visualizzazione del teletesto standard del mondo](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



