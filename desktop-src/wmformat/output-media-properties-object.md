---
title: Oggetto proprietà supporti di output
description: Oggetto proprietà supporti di output
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- Windows Media Format SDK, oggetti proprietà supporti di output
- ASF (Advanced Systems Format), oggetti proprietà dei supporti di output
- ASF (Advanced Systems Format), oggetti proprietà dei supporti di output
- oggetti, oggetti proprietà dei supporti di output
- oggetti proprietà supporti di output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61490464381a0b4e58be7994dfaeb0dfec2baa76
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046440"
---
# <a name="output-media-properties-object"></a>Oggetto proprietà supporti di output

Un oggetto proprietà del supporto di output viene usato per recuperare e impostare una proprietà di output. Gli oggetti proprietà del supporto di output vengono creati per i formati di output supportati dei flussi in un file caricato in un oggetto Reader. Per i flussi compressi, le proprietà di output sono determinate dai possibili output del codec di decompressione.

Un oggetto proprietà del supporto di output viene creato da [**IWMReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) questo metodo crea un oggetto proprietà del supporto di output che contiene le proprietà del formato di output predefinito. Altri formati possono essere supportati per un output. Per ottenere formati di output aggiuntivi, è possibile chiamare [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) per ottenere il numero di formati di output supportati e quindi eseguirne il ciclo usando le chiamate a [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat). **GetOutputFormat** crea un oggetto proprietà del supporto di output popolato con i dati per il formato di output selezionato.

Gli oggetti proprietà del supporto di output possono anche essere creati con il lettore sincrono. Tutti i nomi dei metodi sono identici a quelli del lettore e sono tutti esposti dall'interfaccia [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .

**GetOutputProps** e **GetOutputFormat** impostano entrambi un puntatore a un'interfaccia [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) . Le altre interfacce dell'oggetto proprietà del supporto di output possono essere ottenute chiamando il metodo **QueryInterface** .

Le interfacce seguenti sono supportate da ogni oggetto proprietà del supporto di output.



| Interfaccia                                          | Descrizione                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | Usato come interfaccia di base per le altre interfacce di proprietà del supporto (input, output e video).             |
| [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | Recupera le proprietà di un output.                                                                     |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | Gestisce le proprietà di un flusso video. Si tratta di un'interfaccia facoltativa, disponibile solo per i flussi video. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Oggetti**](objects.md)
</dt> <dt>

[**Oggetto Lettore**](reader-object.md)
</dt> </dl>

 

 




