---
description: Filtro traversa video analogico
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Filtro traversa video analogico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2eb086b85859a3e1e895cd322c68c56916ac19a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965641"
---
# <a name="analog-video-crossbar-filter"></a>Filtro traversa video analogico

Il filtro traversa video analogico rappresenta una traversa video in un dispositivo di acquisizione video che supporta il Windows Driver Model (WDM).

Questo filtro è un filtro wrapper per le barre multibarra nei dispositivi di streaming WDM. Il nome descrittivo del filtro viene ricavato dal dispositivo. Ogni pin di output rappresenta un percorso hardware per il video di Baseband analogico. Uno dei pin di input deriva da un sintonizzatore TV (il [filtro del sintonizzatore TV](tv-tuner-filter.md)). Altri pin di input supportano flussi video o audio. Il filtro supporta eventuali sottotipi di supporti e formati supportati nelle connessioni downstream.

Non è possibile creare direttamente questo filtro con CoCreateInstance. L'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) aggiunge automaticamente questo filtro al grafico in base alle esigenze.

Per ulteriori informazioni sui filtri wrapper e sui dispositivi di streaming WDM, vedere la pagina relativa al [modo in cui i dispositivi hardware partecipano al grafico dei filtri](how-hardware-devices-participate-in-the-filter-graph.md).



|                                          |                                                                                                |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream |
| Tipi di supporti pin di input                    | MEDIATYPE \_ AnalogAudio, MEDIATYPE \_ AnalogVideo                                                 |
| Interfacce pin di input                     | [**IKsPropertySet**](ikspropertyset.md)                                                       |
| Tipi di supporti pin di output                   | MEDIATYPE \_ AnalogAudio, MEDIATYPE \_ AnalogVideo                                                 |
| Interfacce del PIN di output                    | [**IKsPropertySet**](ikspropertyset.md)                                                       |
| CLSID filtro                             | Non applicabile                                                                                 |
| CLSID della pagina delle proprietà                      | \_CROSSBARFILTERPROPERTYPAGE CLSID                                                              |
| File eseguibile                               | ksxbar.ax                                                                                      |
| [Merito](merit.md)                       | Dipendente dal driver.                                                                              |
| [Categoria filtro](filter-categories.md) | \_KSCATEGORY \_ traversa                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Uso di maniglie](working-with-crossbars.md)
</dt> </dl>

 

 



