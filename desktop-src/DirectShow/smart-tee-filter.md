---
description: Filtro Smart Tee
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Filtro Smart Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647e04ef2a24bde43c9d02b7986fd8a645a6b60c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482300"
---
# <a name="smart-tee-filter"></a>Filtro Smart Tee

Il filtro Smart Tee viene usato nei grafici di acquisizione video per suddividere il flusso video in un flusso di anteprima e in un flusso di acquisizione. Questa operazione viene eseguita senza ulteriori operazioni di copia dei dati. I pin di output supportano tutti i tipi di supporto supportati nella connessione downstream.

Il filtro Smart Tee è utile quando un filtro di acquisizione video non fornisce pin distinti per l'acquisizione e l'anteprima. Il filtro Smart Tee recapita i dati di anteprima solo se questa operazione non danneggia le prestazioni di acquisizione. Consente inoltre di rimuovere gli indicatori temporali dal flusso di anteprima. Il generatore del grafico di acquisizione inserisce automaticamente il filtro di Smart Tee quando necessario. Per altre informazioni, vedere [combinazione di acquisizione video e anteprima](combining-video-capture-and-preview.md).

Nella figura seguente viene illustrato un tipico grafico di acquisizione che utilizza il filtro Smart Tee.

![uso del filtro Smart Tee](images/smarttee.png)



|                                          |                                                                                                                |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| Tipi di supporti pin di input                    | MEDIATYPE \_ video, MEDIASUBTYPE \_ null                                                                           |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)         |
| Tipi di supporti pin di output                   | MEDIATYPE \_ video, MEDIASUBTYPE \_ null                                                                           |
| Interfacce del PIN di output                    | [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID filtro                             | \_SMARTTEE CLSID                                                                                                |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                              |
| File eseguibile                               | qcap.dll                                                                                                       |
| [Merito](merit.md)                       | il merito non viene \_ \_ \_ utilizzato                                                                                            |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                  |



 

## <a name="remarks"></a>Commenti

Il pin di acquisizione è il pin di output 0 e il pin di anteprima è il pin di output 1.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



