---
title: Esempio Echo
description: Esempio Echo
ms.assetid: f28af52f-e948-464c-9600-aa516ab984f4
keywords:
- Plug-in di Windows Media Player, panoramica dell'esempio Echo
- plug-in, Panoramica di esempio Echo
- plug-in di elaborazione dei segnali digitali, panoramica dell'esempio Echo
- Plug-in DSP, panoramica dell'esempio Echo
- Guida per programmatori, plug-in DSP
- esempi, plug-in DSP
- Esempio di plug-in Echo DSP, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498f2dfe6a59257b8a16dc31a5b4cb751d649cd6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955559"
---
# <a name="the-echo-sample"></a>Esempio Echo

La procedura guidata plug-in di Windows Media Player può creare un progetto di plug-in DSP per Microsoft Visual C++. Il codice predefinito generato dalla procedura guidata consente all'utente di fornire un fattore di scala compreso tra 0 e 1, usato dal programma come moltiplicatore per gli esempi audio. Si tratta di un'implementazione molto semplice che è possibile studiare per comprendere il modo in cui Windows Media Player interagisce con i plug-in DSP. Le informazioni contenute nella sezione informazioni [sui plug-in DSP](about-dsp-plug-ins.md) consentono di comprendere l'implementazione predefinita.

L'esempio descritto in questa sezione è un po' più complesso. Questo esempio consente all'utente di specificare un intervallo di tempo, in millisecondi e un livello di effetto. Il codice usa questi valori per generare un effetto eco durante la riproduzione di file che contengono audio PCM (Pulse Code Modulation). Molti dei tipi di file che Windows Media Player esegue il rendering utilizzano audio PCM.

Questa guida è suddivisa nelle sezioni seguenti:



| Sezione                                                                                | Descrizione                                                                                                         |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Panoramica dell'esempio Echo](echo-sample-overview.md)                                       | Vengono descritti i requisiti e le specifiche generali per l'esempio. Viene descritto il funzionamento del plug-in.              |
| [Proprietà di esempio Echo](echo-sample-properties.md)                                   | Viene descritto come modificare la proprietà del codice della procedura guidata e aggiungere metodi per la nuova proprietà richiesta per l'esempio Echo. |
| [Modifica della pagina delle proprietà di esempio Echo](modifying-the-echo-sample-property-page.md) | Viene illustrato come modificare l'implementazione della pagina delle proprietà esistente per utilizzare l'esempio Echo.                         |
| [Uso delle risorse di streaming](working-with-streaming-resources.md)               | Viene illustrata l'aggiunta di codice per allocare e liberare un buffer necessario per l'esempio Echo.                                |
| [Implementazione di CEcho::D oProcessOutput](implementing-cecho--doprocessoutput.md)         | Viene descritto come implementare il codice che crea l'effetto Echo.                                                   |
| [Uso del plug-in DSP di esempio Echo](using-the-echo-sample-dsp-plug-in.md)             | Viene descritto come utilizzare l'esempio completato.                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla programmazione di plug-in DSP**](dsp-plug-ins-programming-guide.md)
</dt> </dl>

 

 




