---
description: Filtro tee Perni infiniti
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filtro tee Perni infiniti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28edb67da9d6aae01786cece43b45dfcd33d571b82bdbab21ecf82a2473ff0d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818786"
---
# <a name="infinite-pin-tee-filter"></a>Filtro tee Perni infiniti

Questo filtro recapita gli esempi recapitati al pin di input a un numero variabile di pin di output. Quando viene creata un'istanza del filtro, ha un pin di output. Ogni volta che un pin di output è connesso, il filtro crea un altro pin di output. Tutti i pin di output condividono lo stesso tipo di supporto del pin di input.

Una versione di questo filtro viene fornita anche come esempio sdk. Vedere [Esempio di filtro InfTee](inftee-filter-sample.md).



| Etichetta | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipi di supporti pin di input                    | Qualsiasi tipo di supporto                                                                                                                                     |
| Interfacce pin di input                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipi di supporti pin di output                   | Qualsiasi tipo di supporto. Il tipo di output corrisponde sempre al tipo di input, per tutti i pin di output                                                                 |
| Interfacce pin di output                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtro CLSID                             | CLSID \_ InfTee                                                                                                                                      |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                                   |
| File eseguibile                               | qcap.dll                                                                                                                                           |
| [Merito](merit.md)                       | MERITO \_ NON \_ \_ USARE                                                                                                                                |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



