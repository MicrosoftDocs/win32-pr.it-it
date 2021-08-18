---
title: Esempio echo
description: Esempio echo
ms.assetid: f28af52f-e948-464c-9600-aa516ab984f4
keywords:
- Windows Media Player plug-in, Panoramica dell'esempio Echo
- plug-in, panoramica dell'esempio Echo
- plug-in di elaborazione del segnale digitale, panoramica dell'esempio Echo
- Plug-in DSP, panoramica dell'esempio Echo
- guida alla programmazione, plug-in DSP
- esempi, plug-in DSP
- Esempio di plug-in Echo DSP, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103054e82157d83085713937759de8aa9ed250a5491146ebe0c71559ab1ca338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762791"
---
# <a name="the-echo-sample"></a>Esempio echo

La Windows Media Player guidata plug-in può creare un progetto di plug-in DSP per Microsoft Visual C++. Il codice predefinito generato dalla procedura guidata consente all'utente di specificare un fattore di scala compreso tra 0 e 1, usato dal programma come moltiplicatore per i campioni audio. Si tratta di un'implementazione molto semplice che è possibile studiare per comprendere Windows Media Player interagisce con i plug-in DSP. Le informazioni contenute nella sezione [Informazioni sui plug-in DSP](about-dsp-plug-ins.md) consentono di comprendere l'implementazione predefinita.

L'esempio descritto in questa sezione è un po' più complesso. Questo esempio consente all'utente di specificare un tempo di ritardo, in millisecondi, e un livello di effetto. Il codice usa questi valori per generare un effetto echo durante la riproduzione di file che contengono audio PCM (Pulse Code Modulation). Molti dei tipi di file di cui Windows Media Player rendering usano l'audio PCM.

Questa guida è suddivisa nelle sezioni seguenti:



| Sezione                                                                                | Descrizione                                                                                                         |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Panoramica dell'esempio Echo](echo-sample-overview.md)                                       | Vengono descritti i requisiti generali e le specifiche per l'esempio. Viene descritto il funzionamento del plug-in.              |
| [Proprietà dell'esempio Echo](echo-sample-properties.md)                                   | Viene descritto come modificare la proprietà del codice della procedura guidata e aggiungere metodi per la nuova proprietà necessaria per l'esempio Echo. |
| [Modifica della pagina delle proprietà Echo Sample](modifying-the-echo-sample-property-page.md) | Illustra come modificare l'implementazione della pagina delle proprietà esistente per usare l'esempio Echo.                         |
| [Uso delle risorse di streaming](working-with-streaming-resources.md)               | Illustra l'aggiunta di codice per allocare e liberare un buffer necessario per l'esempio Echo.                                |
| [Implementazione di CEcho::D oProcessOutput](implementing-cecho--doprocessoutput.md)         | Viene descritto come implementare il codice che crea l'effetto echo.                                                   |
| [Uso del plug-in Echo Sample DSP](using-the-echo-sample-dsp-plug-in.md)             | Viene descritto come usare l'esempio completato.                                                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida alla programmazione dei plug-in DSP**](dsp-plug-ins-programming-guide.md)
</dt> </dl>

 

 




