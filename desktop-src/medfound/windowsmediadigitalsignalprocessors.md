---
description: Processori di segnale digitale
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: Processori di segnale digitale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f5c9aa0ee3c4cc2a8c7f725b3a8444f4852c8c5b52ee3713b533ec435f4a3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100943"
---
# <a name="digital-signal-processors"></a>Processori di segnale digitale

Questa sezione descrive gli oggetti DSP (Digital Signal Processor) forniti da Windows.

Microsoft usa il termine *processore di segnale* digitale per designare un set di oggetti COM che eseguono trasformazioni su dati audio e video non compressi. I DSP descritti in questo SDK trasformano audio e video in un'ampia gamma di formati non compressi.

I DSP possono essere usati da soli o in combinazione con codec audio e video. Ad eccezione del DSP di acquisizione vocale, ogni DSP elencato qui implementa due interfacce separate ma simili.



| Interfaccia                              | Descrizione                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Compatibile con Microsoft Media Foundation. |
| [**Oggetto IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Compatibile con DirectShow.                 |



 

È possibile configurare i DSP usando [**l'interfaccia IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per impostare le proprietà. Alcuni DSP dispongono di interfacce aggiuntive che impostano le proprietà. Per usare queste interfacce, chiamare il [**metodo QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) di qualsiasi altra interfaccia del DSP. L'argomento di riferimento per ogni provider di servizi di configurazione elenca le proprietà, le interfacce e altre funzionalità supportate.

In questa sezione vengono trattati gli argomenti seguenti.



| Dsp                                                      | Descrizione                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [Audio Resampler DSP](audioresampler.md)                | Converte la frequenza di campionamento di un flusso audio.       |
| [DSP trasformazione controllo colore](colorcontroltransform.md) | Regola le caratteristiche di colore di un flusso video. |
| [DSP convertitore di colori](colorconverter.md)                | Converte un flusso video tra formati di colore.       |
| [DSP (Frame Rate Converter)](framerateconverter.md)       | Modifica la frequenza dei fotogrammi di un flusso video.            |
| [DSP di Ridimensionamento video](videoresizer.md)                    | Ridimensiona un flusso video.                              |
| [Voice Capture DSP](voicecapturedmo.md)                 | Incapsula diversi DSP correlati all'acquisizione vocale.  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione di Media Foundation](media-foundation-programming-reference.md)
</dt> </dl>

 

 
