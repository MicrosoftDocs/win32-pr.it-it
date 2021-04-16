---
description: Interfacce di streaming audio
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: Interfacce di streaming audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68210beef0b05fcfc89ae5005c485fbc4b74d40f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522482"
---
# <a name="audio-streaming-interfaces"></a>Interfacce di streaming audio

> [!Note]  
> Queste API sono deprecate. Le applicazioni devono usare il filtro [**grabber di esempio**](sample-grabber-filter.md) o implementare un filtro personalizzato per ottenere i dati da un grafico filtro DirectShow.

 



| Interfaccia                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | Controlla i flussi multimediali audio. Questa interfaccia eredita dall'interfaccia [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) e viene usata per creare uno o più oggetti [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) . Viene inoltre utilizzato per impostare e recuperare il formato corrente dei dati del flusso.                                                                                                            |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | Recupera le informazioni dagli oggetti dati [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) sottostanti.                                                                                                                                                                                                                                                                                                        |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | Contiene metodi che impostano e recuperano i dati di memoria sugli oggetti dati audio. Gli oggetti dati audio forniscono i dati sottostanti ai quali viene eseguito il flusso degli esempi. Questa interfaccia fornisce un modo per inizializzare i buffer di memoria e impostare quantità effettive di dati audio negli oggetti. Inoltre, è possibile usare il metodo [**IMemoryData:: GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) per recuperare i dati di memoria audio. |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | Fornisce metodi che consentono alle applicazioni di impostare e ottenere i dati audio sottostanti a cui faranno riferimento i flussi audio. Il formato dei dati audio è impostato nella struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elenco di interfacce di streaming multimediali](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
