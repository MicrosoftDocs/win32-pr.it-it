---
description: Filtro writer di file
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Filtro writer di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9f21009d8135cb42ec93c4f5727398dcdf3094ed4e5da666c325c959dbffc16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651371"
---
# <a name="file-writer-filter"></a>Filtro writer di file

Il filtro Writer di file può essere usato per scrivere file su disco indipendentemente dal formato. Il filtro scrive semplicemente su disco tutto ciò che riceve sul pin di input, quindi deve essere connesso a monte a un multiplexer in grado di formattare correttamente il file. È possibile creare un nuovo file di output con Il writer di file o specificare un file esistente. Se il file esiste già, verrà completamente sovrascritto con i nuovi dati.

Il filtro del writer di file usa i timestamp del flusso di input come offset di file e fornisce l'accesso casuale al file. Supporta **IStream** per consentire la lettura e la scrittura dell'intestazione del file dopo l'arresto del grafo. Per migliorare le prestazioni, supporta anche scritture sovrapposte senza buffer e gestisce la negoziazione del buffer corrispondente.

> [!Note]  
> Per scrivere file ASF, usare il [filtro WM ASF Writer.](wm-asf-writer-filter.md)

 



| Etichetta | Valore |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce di filtro                        | [**IAMFilterMiscFlags,**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSinkFilter,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) [**IFileSinkFilter2,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2) **IPersistStream** |
| Tipi di supporti pin di input                    | Flusso \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                                                                                                              |
| Interfacce pin di input                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) **IStream**                                                                                |
| Tipi di supporti pin di output                   | Non applicabile                                                                                                                                                                                     |
| Interfacce pin di output                    | Non applicabile                                                                                                                                                                                     |
| Filtro CLSID                             | CLSID \_ FileWriter                                                                                                                                                                                  |
| CLSID della pagina delle proprietà                      | Nessuna pagina delle proprietà                                                                                                                                                                                   |
| File eseguibile                               | qcap.dll                                                                                                                                                                                           |
| [Merito](merit.md)                       | MERITO \_ NON \_ \_ USARE                                                                                                                                                                                |
| [Categoria filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



