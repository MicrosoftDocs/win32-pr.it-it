---
description: Non tutte le applicazioni richiedono l'uso del riconoscimento, ma poiché la maggior parte delle applicazioni è stata progettata con il testo come tipo di dati principale, la possibilità di convertire l'input penna in testo è molto utile.
ms.assetid: 70d25839-6ddd-40db-8891-92da074d17b0
title: Riconoscimento input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c3f1431aca97f41b4de9aef64108f3e619ef7b6f9239f46fdde9f7bf4ff3da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718297"
---
# <a name="ink-recognition"></a>Riconoscimento input penna

Non tutte le applicazioni richiedono l'uso del riconoscimento, ma poiché la maggior parte delle applicazioni è stata progettata con il testo come tipo di dati principale, la possibilità di convertire l'input penna in testo è molto utile. È possibile usare le funzionalità di riconoscimento dell'API della piattaforma Tablet PC per eseguire query per ottenere informazioni sui motori di riconoscimento disponibili, ad esempio le lingue che riconoscono. È quindi possibile inviare una [**raccolta Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) da un [**oggetto Ink**](inkdisp-class.md) a un motore di riconoscimento e fare in modo che restituisci un [**oggetto RecognitionResult.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)

## <a name="recognizercontext-object"></a>Oggetto RecognizerContext

Un [**oggetto RecognizerContext**](inkrecognizercontext-class.md) è la creazione di un'istanza di un sistema di riconoscimento specificato. **L'oggetto RecognizerContext** consente di riconoscere una determinata raccolta di tratti in modo sincrono o asincrono. Quando si riconosce in modo asincrono, **l'oggetto RecognizerContext** restituisce [**l'oggetto RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) in un callback dell'evento all'applicazione.

## <a name="recognizers-and-recognizer-objects"></a>Riconoscitori e oggetti di riconoscimento

In un singolo Tablet PC possono essere disponibili uno o più riconoscitori. È possibile eseguire una query sulla raccolta del riconoscitore per determinare quale riconoscitore usare. Un sistema di riconoscimento fornisce informazioni specifiche sulle funzionalità, ad esempio la lingua che può riconoscere e il produttore.

Per determinare se è installato almeno un sistema di riconoscimento, creare un'istanza di un oggetto [**InkRecognizerContext,**](inkrecognizercontext-class.md) come illustrato negli esempi di codice C++ e C \# seguenti. Se non è presente un riconoscitore, questa chiamata a [**CoCreateInstance ha**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) esito negativo.


```C++
CComPtr<IInkRecognizerContext> g_pIInkRecoContext;
hr = CoCreateInstance(CLSID_InkRecognizerContext, 
      NULL, CLSCTX_INPROC_SERVER,
      IID_IInkRecognizerContext, 
(void **) &g_pIInkRecoContext);
if (FAILED(hr)) 
{
      ::MessageBox(NULL, TEXT("No recognizers installed.\nExiting."), 
      gc_szAppName, MB_ICONERROR);
      return -1;
}
```




```CSharp
try
{
  Recognizers recos = new Recognizers();//Check for recognizer.
  Recognizer defReco = recos.GetDefaultRecognizer();
  recoContext = defReco.CreateRecognizerContext();
}
catch
{
  MessageBox.Show("No recognizers installed.");
}
```



## <a name="recognitionresult-and-recognitionalternate-objects"></a>Oggetti RecognitionResult e RecognitionAlternate

I risultati del riconoscimento vengono restituiti in un [**oggetto RecognitionResult.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) I risultati contengono una stringa di risultati migliore nella [proprietà TopString,](/previous-versions/ms829602(v=msdn.10)) nonché una raccolta di risultati alternativi in una [**raccolta RecognitionAlternates.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) **L'oggetto RecognitionResult** può essere reso persistente con la raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) originale da cui è stato generato.

## <a name="recognizerguide-structure"></a>Struttura RecognizerGuide

La guida al riconoscimento può essere costituita da righe e colonne e offre al sistema di riconoscimento un contesto migliore in cui eseguire il riconoscimento. Ad esempio, è possibile disegnare linee orizzontali sullo schermo di un utente, quasi come un foglio di carta regolato, che mostrano dove deve verificarsi la grafia (questo tipo di guida è costituito solo da righe e nessuna colonna). Se un utente scrive sulle righe, invece di uno spazio arbitrario, l'accuratezza del riconoscimento migliora.

La figura seguente mostra una [**struttura RecognizerGuide**](inkrecognizerguide-class.md) con due righe per l'input.

![illustrazione che mostra la guida al riconoscimento a due righe](images/9791100b-8279-4dd0-823f-0a38a0308a74.jpg)

La figura seguente mostra una [**struttura RecognizerGuide**](inkrecognizerguide-class.md) con quattro colonne e tre righe.

![illustrazione che mostra la guida al riconoscitore tre per quattro](images/d1bbf2d3-9653-49d7-bf48-c1b26645074c.jpg)

Per altre informazioni sull'uso della [**struttura RecognizerGuide,**](inkrecognizerguide-class.md) vedere l'argomento **di riferimento RecognizerGuide.**

 

 
