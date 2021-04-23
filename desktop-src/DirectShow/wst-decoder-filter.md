---
description: Filtro decodificatore WST
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Filtro decodificatore WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb6804f82e5d15aa324feb163261544969e3c45
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908479"
---
# <a name="wst-decoder-filter"></a>Filtro decodificatore WST

Questo componente è stato rimosso da Windows Vista e dai sistemi operativi successivi. È disponibile per l'uso nei sistemi operativi Windows XP e Windows Server 2003.

> [!Note]  
> A partire da Windows Vista, DirectShow non fornisce un filtro per decodificare WST (World Standard Teletext).

 

Il decodificatore WST è un filtro in modalità kernel che accetta dati teletext World Standard decodificati dal [codec WST](wst-codec-filter.md) e recapita le bitmap al Pin 2 nel [mixer](overlay-mixer-filter.md) di sovrapposizione usando i tipi di carattere forniti da Microsoft. Al momento sono supportate solo le lingue dell'Europa occidentale. Non sono attualmente disponibili tipi di carattere Unicode.

Questo filtro può essere aggiunto automaticamente al grafico chiamando [**ICaptureGraphBuilder2::RenderStream,**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)usando il pin di output del codec WST.



| Label | Valore |
|------------------------------------------|---------------------------------------------------------------|
| Interfacce di filtro                        | ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder) |
| Tipi di supporti pin di input                    | MEDIATYPE \_ VBI, MEDIASUBTYPE \_ TELETEXT                        |
| Interfacce pin di input                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Tipi di supporti pin di output                   | MEDIATYPE \_ Video                                              |
| Interfacce pin di output                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| CLSID del filtro                             | CLSID \_ WSTDecoder                                             |
| CLSID della pagina delle proprietà                      | CLSID \_ WstDecoderPropertyPage                                 |
| File eseguibile                               | Wstdecod.DLL                                                  |
| [Merito](merit.md)                       | MERITO \_ NORMALE                                                 |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Visualizzazione del teletesto standard del mondo](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



