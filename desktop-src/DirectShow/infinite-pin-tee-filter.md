---
description: Filtro del Pin Tee infinito
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filtro del Pin Tee infinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e9a80baf047cdd5559fadaa0f13ea1352d4ed0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401268"
---
# <a name="infinite-pin-tee-filter"></a>Filtro del Pin Tee infinito

Questo filtro recapita gli esempi recapitati al pin di input a un numero variabile di pin di output. Quando viene creata un'istanza del filtro, è presente un pin di output. Ogni volta che viene connesso un pin di output, il filtro crea un altro pin di output. Tutti i pin di output condividono lo stesso tipo di supporto del PIN di input.

Una versione di questo filtro viene fornita anche come esempio SDK. Vedere l' [esempio di filtro InfTee](inftee-filter-sample.md).



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| Tipi di supporti pin di input                    | Qualsiasi tipo di supporto                                                                                                                                     |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Tipi di supporti pin di output                   | Qualsiasi tipo di supporto. Il tipo di output corrisponde sempre al tipo di input, per tutti i pin di output                                                                 |
| Interfacce del PIN di output                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID filtro                             | \_INFTEE CLSID                                                                                                                                      |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                                   |
| File eseguibile                               | qcap.dll                                                                                                                                           |
| [Merito](merit.md)                       | il merito non viene \_ \_ \_ utilizzato                                                                                                                                |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



