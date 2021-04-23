---
description: Filtro writer file
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Filtro writer file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991536d505ee1bdfcaaaca5ce8660c4480decf6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909689"
---
# <a name="file-writer-filter"></a>Filtro writer file

Il filtro Writer file può essere usato per scrivere file su disco indipendentemente dal formato. Il filtro scrive semplicemente su disco tutto ciò che riceve sul pin di input, quindi deve essere connesso upstream a un multiplexer in grado di formattare correttamente il file. È possibile creare un nuovo file di output con il writer di file o specificare un file esistente. Se il file esiste già, verrà sovrascritto completamente con i nuovi dati.

Il filtro del writer di file usa i timestamp del flusso di input come offset di file e fornisce l'accesso casuale al file. Supporta **IStream** per consentire la lettura e la scrittura dell'intestazione del file dopo l'arresto del grafo. Per migliorare le prestazioni, supporta anche scritture sovrapposte senza buffer e gestisce la negoziazione del buffer corrispondente.

> [!Note]  
> Per scrivere file ASF, usare il [filtro WM ASF Writer.](wm-asf-writer-filter.md)

 



| Label | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMFilterMiscFlags,**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSinkFilter,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) [**IFileSinkFilter2,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2) **IPersistStream** |
| Tipi di supporti pin di input                    | Flusso \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                                                                                                              |
| Interfacce pin di input                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**                                                                                |
| Tipi di supporti pin di output                   | Non applicabile                                                                                                                                                                                     |
| Interfacce pin di output                    | Non applicabile                                                                                                                                                                                     |
| CLSID del filtro                             | CLSID \_ FileWriter                                                                                                                                                                                  |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                                                                                   |
| File eseguibile                               | qcap.dll                                                                                                                                                                                           |
| [Merito](merit.md)                       | MERITO \_ NON \_ \_ USARE                                                                                                                                                                                |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



