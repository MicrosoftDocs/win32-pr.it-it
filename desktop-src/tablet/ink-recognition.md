---
description: Non tutte le applicazioni richiedono l'uso del riconoscimento, ma poiché la maggior parte delle applicazioni è stata progettata con testo come tipo di dati primario, la possibilità di convertire input penna in testo è molto utile.
ms.assetid: 70d25839-6ddd-40db-8891-92da074d17b0
title: Riconoscimento input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca4ec6f897c797d86df96c5d9c2cfd5d80f16c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553595"
---
# <a name="ink-recognition"></a>Riconoscimento input penna

Non tutte le applicazioni richiedono l'uso del riconoscimento, ma poiché la maggior parte delle applicazioni è stata progettata con testo come tipo di dati primario, la possibilità di convertire input penna in testo è molto utile. È possibile utilizzare le funzionalità di riconoscimento dell'API della piattaforma Tablet PC per eseguire una query per ottenere informazioni sui motori di riconoscimento disponibili, ad esempio le lingue riconosciute. È quindi possibile inviare una raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) da un oggetto [**Ink**](inkdisp-class.md) a un motore di riconoscimento e fare in modo che restituisca un oggetto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) .

## <a name="recognizercontext-object"></a>RecognizerContext (oggetto)

Un oggetto [**RecognizerContext**](inkrecognizercontext-class.md) è la creazione di un'istanza di un determinato riconoscimento. L'oggetto **RecognizerContext** consente di riconoscere un determinato insieme di tratti in modo sincrono o asincrono. Quando si riconosce in modo asincrono, l'oggetto **RecognizerContext** restituisce l'oggetto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) in un callback di evento all'applicazione.

## <a name="recognizers-and-recognizer-objects"></a>Riconoscitori e oggetti di riconoscimento

Un singolo Tablet PC può avere uno o più sistemi di riconoscimento disponibili. È possibile eseguire una query sulla raccolta del riconoscitore per determinare il riconoscimento da usare. Un riconoscitore fornisce informazioni specifiche sulle funzionalità, ad esempio il linguaggio che può riconoscere e il produttore.

Per determinare se è installato almeno un riconoscimento, creare un'istanza di un oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) come illustrato negli esempi di codice C++ e C seguenti \# . Se non è presente un riconoscitore, la chiamata a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ha esito negativo.


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

I risultati del riconoscimento vengono restituiti in un oggetto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) . I risultati contengono una stringa di risultato migliore nella proprietà di [tostringa](/previous-versions/ms829602(v=msdn.10)) , oltre a una raccolta di risultati alternativi in una raccolta [**RecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) . L'oggetto **RecognitionResult** può essere reso permanente con la raccolta di [**tratti**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) originale dalla quale è stato generato.

## <a name="recognizerguide-structure"></a>Struttura RecognizerGuide

La guida per il riconoscimento può essere costituita da righe e colonne e fornisce al riconoscimento un contesto migliore in cui eseguire il riconoscimento. Ad esempio, è possibile creare linee orizzontali sullo schermo di un utente, quasi come una parte di carta regolata, che mostra dove deve essere eseguita la grafia (questo tipo di guida è costituito solo da righe e senza colonne). Se un utente scrive sulle righe, anziché uno spazio arbitrario, l'accuratezza del riconoscimento migliora.

Nella figura seguente viene illustrata una struttura [**RecognizerGuide**](inkrecognizerguide-class.md) con due righe per l'input.

![illustrazione che mostra la guida per il riconoscimento a due righe](images/9791100b-8279-4dd0-823f-0a38a0308a74.jpg)

Nella figura seguente viene illustrata una struttura [**RecognizerGuide**](inkrecognizerguide-class.md) con quattro colonne e tre righe.

![illustrazione che mostra la guida per i riconoscitori tre per quattro](images/d1bbf2d3-9653-49d7-bf48-c1b26645074c.jpg)

Per ulteriori informazioni sull'utilizzo della struttura [**RecognizerGuide**](inkrecognizerguide-class.md) , vedere l'argomento di riferimento **RecognizerGuide** .

 

 
