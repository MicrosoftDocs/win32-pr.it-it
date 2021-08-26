---
description: Filtro Smart Tee
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Filtro Smart Tee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50a8e829d78658b867d3884240250c10d10a65c7cd309f109fe29b023c726518
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964997"
---
# <a name="smart-tee-filter"></a>Filtro Smart Tee

Il filtro Smart Tee viene usato nei grafici di acquisizione video per suddividere il flusso video in un flusso di anteprima e un flusso di acquisizione. Questa operazione viene eseguita senza alcuna copia aggiuntiva dei dati. I pin di output supportano tutti i tipi di supporti supportati nella connessione downstream.

Il filtro Smart Tee è utile quando un filtro di acquisizione video non fornisce pin separati per l'acquisizione e l'anteprima. Il filtro Smart Tee fornisce i dati di anteprima solo se questa operazione non influisce sulle prestazioni di acquisizione. Rimuove anche i timestamp dal flusso di anteprima. Il generatore di grafi di acquisizione inserisce automaticamente il filtro Smart Tee quando necessario. Per altre informazioni, vedere [Combinazione di acquisizione video e anteprima.](combining-video-capture-and-preview.md)

La figura seguente mostra un tipico grafico di acquisizione che usa il filtro Smart Tee.

![uso del filtro Smart Tee](images/smarttee.png)



| Etichetta | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**Filtro IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| Tipi di supporti pin di input                    | VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                           |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)         |
| Tipi di supporti pin di output                   | VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                           |
| Interfacce pin di output                    | [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID del filtro                             | CLSID \_ SmartTee                                                                                                |
| CLSID pagina delle proprietà                      | Nessuna pagina delle proprietà.                                                                                              |
| File eseguibile                               | qcap.dll                                                                                                       |
| [Merito](merit.md)                       | NON \_ \_ USARE \_                                                                                            |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                  |



 

## <a name="remarks"></a>Commenti

Il pin di acquisizione è il pin di output 0 e il pin di anteprima è il pin di output 1.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



