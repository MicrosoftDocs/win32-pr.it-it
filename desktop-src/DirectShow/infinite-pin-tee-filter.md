---
description: Filtro tee per pin infinito
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filtro tee Perni infiniti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3433a0c2f5fe55fa59c42ed6e02d34f6e2cf0e6d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909229"
---
# <a name="infinite-pin-tee-filter"></a>Filtro tee per pin infinito

Questo filtro recapita gli esempi recapitati al pin di input a un numero variabile di pin di output. Quando viene creata un'istanza del filtro, ha un pin di output. Ogni volta che un pin di output è connesso, il filtro crea un altro pin di output. Tutti i pin di output condividono lo stesso tipo di supporto del pin di input.

Una versione di questo filtro viene fornita anche come esempio sdk. Vedere [Esempio di filtro InfTee](inftee-filter-sample.md).



| Label | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipi di supporti pin di input                    | Qualsiasi tipo di supporto                                                                                                                                     |
| Interfacce pin di input                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipi di supporti pin di output                   | Qualsiasi tipo di supporto. Il tipo di output corrisponde sempre al tipo di input, per tutti i pin di output                                                                 |
| Interfacce pin di output                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID del filtro                             | CLSID \_ InfTee                                                                                                                                      |
| CLSID pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                                   |
| File eseguibile                               | qcap.dll                                                                                                                                           |
| [Merito](merit.md)                       | NON \_ \_ USARE \_                                                                                                                                |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filters](directshow-filters.md)
</dt> </dl>

 

 



