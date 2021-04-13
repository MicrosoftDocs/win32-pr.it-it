---
title: Per recuperare esempi di supporti con il lettore sincrono
description: Per recuperare esempi di supporti con il lettore sincrono
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- Formato di sistemi avanzati (ASF), recupero di esempi di supporti
- ASF (Advanced Systems Format), recupero di esempi di supporti
- ASF (Advanced Systems Format), lettori sincroni
- ASF (formato avanzato dei sistemi), lettori sincroni
- lettori sincroni, recupero di esempi di supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd341ea9616b18a5e65cfa8c1134e0f1be44b5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398579"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a>Per recuperare esempi di supporti con il lettore sincrono

È necessario richiedere ogni campione uno alla volta dal lettore sincrono. In questo modo si ottiene un maggiore controllo sugli esempi ricevuti e quando vengono ricevuti.

Usare il metodo [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) per recuperare un esempio. È necessario passare per lo più i puntatori alle variabili che verranno compilate con informazioni sull'esempio recuperato come parametri. L'unico parametro di input è *wStreamNum*. Se si passa un numero di flusso, **GetNextSample** recupererà l'esempio successivo con il numero di flusso specificato. Se si passa zero per *wStreamNum*, viene recuperato il seguente esempio che si verifica in ordine cronologico nel file.

Per impostazione predefinita, il lettore sincrono recupera tutti gli esempi dagli output in un file in ordine cronologico. Se si chiama **GetNextSample** e non sono disponibili altri esempi da ottenere, viene restituito NS \_ e \_ nessun \_ altro \_ campione, ovvero un codice di errore non riuscito. Quando si esegue la codifica, è possibile semplicemente scorrere gli esempi fino a quando il metodo non ha esito negativo.

> [!Note]  
> Per assicurarsi che il lettore sincrono fornisca durate di esempio corrette per i flussi video, è necessario innanzitutto configurare l'output del flusso. Chiamare il metodo [**IWMSyncReader:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) per impostare l' \_ impostazione g wszVideoSampleDurations su **true**.

 

Codice di esempio

Nell'esempio di codice seguente viene illustrato come utilizzare **GetNextSample** per recuperare tutti gli esempi in un file.


```C++
// Loop through all the samples in the file.
do
{
   // Get the next sample.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lettura di file con il lettore sincrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




