---
description: Filtro del writer di file
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Filtro del writer di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f438f13f8d63b2856efd147c57ba6f071af26ff8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225465"
---
# <a name="file-writer-filter"></a>Filtro del writer di file

Il filtro del writer di file può essere usato per scrivere file su disco indipendentemente dal formato. Il filtro scrive semplicemente nel disco tutto ciò che riceve sul pin di input, quindi deve essere collegato a un multiplexer in grado di formattare il file in modo corretto. È possibile creare un nuovo file di output con il writer di file o specificare un file esistente. Se il file esiste già, verrà completamente sovrascritto con i nuovi dati.

Il filtro del writer di file usa i timestamp del flusso di input come offset del file e fornisce l'accesso casuale al file. Supporta **IStream** per consentire la lettura e la scrittura dell'intestazione del file dopo l'arresto del grafo. Per migliorare le prestazioni, supporta anche le scritture sovrapposte senza buffer e gestisce la negoziazione del buffer corrispondente.

> [!Note]  
> Per scrivere file ASF, usare il filtro [WM ASF Writer](wm-asf-writer-filter.md) .

 



|                                          |                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream** |
| Tipi di supporti pin di input                    | \_Flusso MEDIATYPE, MEDIASUBTYPE \_ null                                                                                                                                                              |
| Interfacce pin di input                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**                                                                                |
| Tipi di supporti pin di output                   | Non applicabile                                                                                                                                                                                     |
| Interfacce del PIN di output                    | Non applicabile                                                                                                                                                                                     |
| CLSID filtro                             | CLSID \_ FileWriter                                                                                                                                                                                  |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                                                                                   |
| File eseguibile                               | qcap.dll                                                                                                                                                                                           |
| [Merito](merit.md)                       | il merito non viene \_ \_ \_ utilizzato                                                                                                                                                                                |
| [Categoria filtro](filter-categories.md) | \_LEGACYAMFILTERCATEGORY CLSID                                                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



