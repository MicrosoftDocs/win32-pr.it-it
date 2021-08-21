---
title: Oggetto Proprietà supporti di output
description: Oggetto Proprietà supporti di output
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- Windows Media Format SDK,output media properties objects
- Advanced Systems Format (ASF), oggetti proprietà multimediali di output
- ASF (Advanced Systems Format),output media properties objects
- oggetti, output di oggetti proprietà multimediali
- oggetti proprietà supporti di output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6848270147a1a191faf93830f062cf7768a19ccd38a77598d15617197a1967a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084634"
---
# <a name="output-media-properties-object"></a>Oggetto Proprietà supporti di output

Un oggetto proprietà multimediali di output viene usato per recuperare e impostare una proprietà di output. Gli oggetti delle proprietà multimediali di output vengono creati per i formati di output supportati dei flussi in un file caricato in un oggetto lettore. Per i flussi compressi, le proprietà di output sono determinate dai possibili output del codec di decompressione.

Un oggetto proprietà multimediali di output viene creato da [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) Questo metodo crea un oggetto proprietà multimediali di output che contiene le proprietà del formato di output predefinito. Per un output possono essere supportati altri formati. Per ottenere formati di output aggiuntivi, è possibile chiamare [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) per ottenere il numero di formati di output supportati e quindi eseguire il ciclo tramite chiamate a [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat). **GetOutputFormat crea** un oggetto proprietà multimediali di output popolato con i dati per il formato di output selezionato.

Gli oggetti proprietà multimediali di output possono essere creati anche con il lettore sincrono. Tutti i nomi dei metodi sono identici a quelli nel lettore e sono tutti esposti [**dall'interfaccia IWMSyncReader.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)

**GetOutputProps e** **GetOutputFormat** impostano entrambi un puntatore a [**un'interfaccia IWMOutputMediaProps.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) Le altre interfacce dell'oggetto proprietà multimediali di output possono essere ottenute chiamando il **metodo QueryInterface.**

Le interfacce seguenti sono supportate da ogni oggetto proprietà del supporto di output.



| Interfaccia                                          | Descrizione                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | Usato come interfaccia di base per le altre interfacce di proprietà multimediali (input, output e video).             |
| [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | Recupera le proprietà di un output.                                                                     |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | Gestisce le proprietà di un flusso video. Si tratta di un'interfaccia facoltativa, disponibile solo per i flussi video. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Oggetto Lettore**](reader-object.md)
</dt> </dl>

 

 




