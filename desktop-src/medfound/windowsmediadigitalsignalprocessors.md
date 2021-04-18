---
description: Processori di segnale digitale
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: Processori di segnale digitale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0961554d9c9902e68f74c6b2b57662b23846614f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320514"
---
# <a name="digital-signal-processors"></a>Processori di segnale digitale

In questa sezione vengono descritti gli oggetti DSP (Digital Signal Processor) forniti da Windows.

Microsoft usa il termine *elaboratore di segnali digitali* per definire un set di oggetti com che eseguono trasformazioni su dati audio e video non compressi. Il DSP descritto in questo SDK trasforma audio e video in un'ampia gamma di formati non compressi.

Il DSP può essere usato autonomamente o in combinazione con codec audio e video. Ad eccezione del DSP di acquisizione vocale, ogni DSP elencato qui implementa due interfacce separate ma simili.



| Interfaccia                              | Descrizione                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Compatibile con Microsoft Media Foundation. |
| [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Compatibile con DirectShow.                 |



 

È possibile configurare DSP usando l'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per impostare le proprietà. Alcuni DSP hanno interfacce aggiuntive che impostano le proprietà. Per usare queste interfacce, chiamare il metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) di qualsiasi altra interfaccia del DSP. L'argomento di riferimento per ogni DSP elenca le proprietà, le interfacce e altre funzionalità supportate.

In questa sezione vengono trattati gli argomenti seguenti.



| DSP                                                      | Descrizione                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [DSP ricampionatore audio](audioresampler.md)                | Converte la frequenza di campionamento di un flusso audio.       |
| [Trasformazione controllo colori DSP](colorcontroltransform.md) | Regola le caratteristiche dei colori di un flusso video. |
| [Convertitore di colori DSP](colorconverter.md)                | Converte un flusso video tra i formati di colore.       |
| [Convertitore frequenza frame DSP](framerateconverter.md)       | Modifica la frequenza dei fotogrammi di un flusso video.            |
| [Ridimensionamento video DSP](videoresizer.md)                    | Ridimensiona un flusso video.                              |
| [DSP di acquisizione vocale](voicecapturedmo.md)                 | Incapsula diversi DSP correlati all'acquisizione vocale.  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione di Media Foundation](media-foundation-programming-reference.md)
</dt> </dl>

 

 
