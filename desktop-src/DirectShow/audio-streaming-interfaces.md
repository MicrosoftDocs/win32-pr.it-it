---
description: Interfacce di streaming audio
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: Interfacce di streaming audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1087ab127258fcd4f587cdd029d4604c35524689b5f0877476e1137e2ed924eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824471"
---
# <a name="audio-streaming-interfaces"></a>Interfacce di streaming audio

> [!Note]  
> Queste API sono deprecate. Le applicazioni devono usare il [**filtro Grabber**](sample-grabber-filter.md) di esempio o implementare un filtro personalizzato per ottenere dati da un DirectShow di filtro.

 



| Interfaccia                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | Controlla i flussi multimediali audio. Questa interfaccia eredita [**dall'interfaccia IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) e viene usata per creare uno o più [**oggetti IAudioStreamSample.**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) Viene inoltre usato per impostare e recuperare il formato corrente dei dati del flusso.                                                                                                            |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | Recupera informazioni dagli oggetti dati [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) sottostanti.                                                                                                                                                                                                                                                                                                        |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | Contiene metodi che impostano e recuperano i dati di memoria sugli oggetti dati audio. Gli oggetti dati audio forniscono i dati sottostanti a cui accedono i campioni di flusso. Questa interfaccia consente di inizializzare i buffer di memoria e di impostare le quantità effettive di dati audio negli oggetti . Inoltre, il [**metodo IMemoryData::GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) può essere usato per recuperare i dati della memoria audio. |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | Fornisce metodi che consentono alle applicazioni di impostare e ottenere i dati audio sottostanti a cui i flussi audio fanno riferimento. Il formato dei dati audio è impostato nella [**struttura WAVEFORMATEX.**](/previous-versions/dd757713(v=vs.85))                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elenco di interfacce di streaming multimediale](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
