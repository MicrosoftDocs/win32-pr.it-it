---
title: Variabili per archiviare le proprietà
description: Variabili per archiviare le proprietà
ms.assetid: a90a6e21-00fb-46f8-96c8-654d8f205905
keywords:
- Plug-in di Windows Media Player, proprietà di esempio Echo
- plug-in, proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, proprietà di esempio Echo
- Plug-in DSP, proprietà di esempio Echo
- Esempio di plug-in Echo DSP, proprietà
- Esempio di plug-in Echo DSP, variabili per l'archiviazione delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d252962116ba9c72464273f9c4ea1688b151898
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221595"
---
# <a name="variables-to-store-properties"></a>Variabili per archiviare le proprietà

Per prima cosa, è necessaria una variabile per archiviare l'ora di ritardo. L'esempio predefinito creato dalla procedura guidata per il plug-in di Windows Media Player fornisce una variabile denominata m \_ fScaleFactor per archiviare il moltiplicatore di scalabilità usato per l'elaborazione. Questo esempio non richiede più questa variabile, quindi è possibile modificarne il nome e il tipo per archiviare il valore di tempo di ritardo.

1.  Sostituire ogni istanza di m \_ fScaleFactor in Echo. h e Echo. cpp con m \_ dwDelayTime.
2.  Modificare il tipo di dati per m \_ fScaleFactor (ora m \_ dwDelayTime) da Double a DWORD in Echo. h.
3.  Nel costruttore per CEcho modificare il valore di tempo di ritardo predefinito in 1000.
    ```C++
    m_dwDelayTime = 1000;   // Default to a delay time of 1000 ms.
    
    ```

    

Dichiarare quindi due nuove variabili membro per archiviare la percentuale del segnale di effetto e la percentuale del segnale di origine da combinare nel buffer di output finale. Il termine "Wet" si riferisce all'effetto e il termine "Dry" si riferisce al segnale di origine. Aggiungere le seguenti dichiarazioni a Echo. h:


```C++
double  m_fWetMix;    // percentage of effect
double  m_fDryMix;    // percentage of dry signal

```



Questi valori vengono archiviati come rappresentazioni decimali delle percentuali in modo che possano essere facilmente usati come fattori di scala. Ad esempio, una combinazione di effetto 50% e segnale di origine 50% verrebbe rappresentata come valore 0,50 per ogni variabile. La somma dei valori per m \_ fWetMix e m \_ fDryMix non deve essere maggiore di 1,0 (100%). Questi valori saranno infine accessibili come proprietà.

Aggiungere il codice seguente al costruttore CEcho per impostare i valori predefiniti su 50 percent each:


```C++
m_fWetMix = 0.50;  // default to 50 percent wet
m_fDryMix = 0.50;  // default to 50 percent dry

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Proprietà di esempio Echo**](echo-sample-properties.md)
</dt> </dl>

 

 




