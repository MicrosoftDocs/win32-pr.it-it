---
description: Filtro barra incrociata video analogico
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Filtro barra incrociata video analogico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17d8700131dbc658a5233d56f339c39eac7a3a0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909599"
---
# <a name="analog-video-crossbar-filter"></a>Filtro barra incrociata video analogico

Il filtro crossbar video analogico rappresenta una barra incrociata video in un dispositivo di acquisizione video che supporta Windows Driver Model (WDM).

Questo filtro è un filtro wrapper per le barre incrociate nei dispositivi di streaming WDM. Il nome descrittivo del filtro deriva dal dispositivo. Ogni pin di output rappresenta un percorso hardware per video di baseband analogico. Uno dei pin di input proviene da un siner TV [(TV Tuner Filter).](tv-tuner-filter.md) Altri pin di input supportano flussi audio o video. Il filtro supporta tutti i sottotipi multimediali e i formati supportati nelle connessioni downstream.

Non è possibile creare direttamente questo filtro con CoCreateInstance. [**L'interfaccia ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) aggiunge automaticamente questo filtro al grafo in base alle esigenze.

Per altre informazioni sui filtri wrapper e sui dispositivi di streaming WDM, vedere [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).



| Label | Valore |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream |
| Tipi di supporti pin di input                    | MEDIATYPE \_ AnalogAudio, MEDIATYPE \_ AnalogVideo                                                 |
| Interfacce pin di input                     | [**IKsPropertySet**](ikspropertyset.md)                                                       |
| Tipi di supporti pin di output                   | MEDIATYPE \_ AnalogAudio, MEDIATYPE \_ AnalogVideo                                                 |
| Interfacce pin di output                    | [**IKsPropertySet**](ikspropertyset.md)                                                       |
| Filtro CLSID                             | Non applicabile                                                                                 |
| CLSID della pagina delle proprietà                      | CLSID \_ CrossbarFilterPropertyPage                                                              |
| File eseguibile                               | ksxbar.ax                                                                                      |
| [Merito](merit.md)                       | Dipendente dal driver.                                                                              |
| [Categoria filtro](filter-categories.md) | AM \_ KSCATEGORY \_ CROSSBAR                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Uso delle barre incrociate](working-with-crossbars.md)
</dt> </dl>

 

 



