---
title: Per recuperare esempi di supporti con il lettore sincrono
description: Per recuperare esempi di supporti con il lettore sincrono
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- Advanced Systems Format (ASF), recupero di esempi di supporti
- ASF (Advanced Systems Format), recupero di esempi di supporti
- Advanced Systems Format (ASF), lettori sincroni
- ASF (Advanced Systems Format), lettori sincroni
- lettori sincroni, recupero di esempi di supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1ec4fc7e8a894de304ea828cef9d8e019f4cdedfd2fbd851a427382ba741a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807431"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a>Per recuperare esempi di supporti con il lettore sincrono

È necessario richiedere ogni esempio uno alla volta dal lettore sincrono. In questo modo si ha maggiore controllo sui campioni ricevuti e su quando vengono ricevuti.

Usare il [**metodo IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) per recuperare un esempio. È necessario passare principalmente puntatori a variabili che verranno riempite con informazioni sull'esempio recuperato come parametri. L'unico parametro di input è *wStreamNum*. Se si passa un numero di flusso, **GetNextSample** recupererà l'esempio successivo con il numero di flusso specificato. Se si passa zero per *wStreamNum,* viene recuperato l'esempio successivo che si verifica in ordine cronologico nel file.

Per impostazione predefinita, il lettore sincrono recupera tutti gli esempi dagli output in un file in ordine cronologico. Se si chiama **GetNextSample** e non sono disponibili altri esempi da ottenere, restituirà NS E NO MORE SAMPLES, che è un codice \_ di errore non \_ \_ \_ riuscito. Quando si codifica pertanto, è possibile eseguire semplicemente un ciclo di esempi fino a quando il metodo non ha esito negativo.

> [!Note]  
> Per assicurarsi che il lettore sincrono consegnerà le durate di campionamento corrette per i flussi video, è prima necessario configurare l'output del flusso. Chiamare il [**metodo IWMSyncReader::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) per impostare g \_ wszVideoSampleDurations su **TRUE.**

 

Codice di esempio

Il codice di esempio seguente illustra come usare **GetNextSample** per recuperare tutti gli esempi in un file.


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

 

 




