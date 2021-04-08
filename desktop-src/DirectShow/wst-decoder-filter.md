---
description: Filtro decodificatore WST
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Filtro decodificatore WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f2d20873ff9a5e7c009c4a84f7a23c273d6590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880026"
---
# <a name="wst-decoder-filter"></a>Filtro decodificatore WST

Questo componente è stato rimosso da Windows Vista e dai sistemi operativi successivi. È disponibile per l'uso nei sistemi operativi Windows XP e Windows Server 2003.

> [!Note]  
> A partire da Windows Vista, DirectShow non fornisce un filtro per decodificare il televideo standard del mondo (WST).

 

Il decodificatore WST è un filtro in modalità kernel che accetta dati del televideo standard del mondo decodificati dal [codec WST](wst-codec-filter.md) e recapita le bitmap al pin 2 sul [mixer sovrapposto](overlay-mixer-filter.md) usando i tipi di carattere forniti da Microsoft. Al momento sono supportate solo le lingue europee occidentali; non sono attualmente disponibili tipi di carattere Unicode.

Questo filtro può essere aggiunto automaticamente al grafico chiamando [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), usando il pin di output del codec WST.



|                                          |                                                               |
|------------------------------------------|---------------------------------------------------------------|
| Interfacce di filtro                        | ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder) |
| Tipi di supporti pin di input                    | MEDIATYPE \_ VBI, MEDIASUBTYPE \_ Teletext                        |
| Interfacce pin di input                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| Tipi di supporti pin di output                   | Video di MEDIATYPE \_                                              |
| Interfacce del PIN di output                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| CLSID filtro                             | \_WSTDECODER CLSID                                             |
| CLSID della pagina delle proprietà                      | \_WSTDECODERPROPERTYPAGE CLSID                                 |
| File eseguibile                               | Wstdecod.DLL                                                  |
| [Merito](merit.md)                       | VALORE \_ normale                                                 |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Visualizzazione del televideo standard internazionale](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



